import telebot
import random


bot = telebot.TeleBot("8347705789:AAHG5hbkj5jSvgLhDPAHUj8vDMoH00zol0o")

@bot.message_handler(commands=['start'])
def send_welcome(message):
    bot.reply_to(message, "Добро пожаловать на базу ТВ менов и в целом на базу альянса! Вот наш ТГК https://t.me/+595K8pUYRwI0ZjQy")

@bot.message_handler(commands=['hello'])
def send_hello(message):
    bot.reply_to(message, "Привет!")

@bot.message_handler(commands=['Pls_Helpme'])
def send_random_answer(message):
     Pls_Helpme = {
        "Чем могу помочь?",
        "С чем нужна помощь?"
    }
bot.send_message(message_thread_id=['Вот, пожалуйста :3'])

@bot.message_handler(commands=['bye'])
def send_bye(message):
    bot.reply_to(message, "Пока! Удачи!")

@bot.message_handler(func=lambda message: True)
def echo_all(message):
    bot.reply_to(message, message.text)

bot.polling()
