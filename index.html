from telethon import TelegramClient, events
import logging

# إعدادات السجل
logging.basicConfig(level=logging.INFO)

api_id = '20964672'
api_hash = '142ad3118b3b176d2817a991edda3f40'  # تأكد من عدم نشره علنًا

# إنشاء عميل المستخدم
client = TelegramClient('user', api_id, api_hash)

# معرف المجموعة التي تريد إعادة توجيه الرسائل إليها
target_group_id = 1002209067308

# الكلمات التي سيتم البحث عنها
filter_keywords = {
    'يسوي', 'يحل', 'ابي', 'ابغا', 'ابغى', 'سيفي',
    'عرض', 'عروض', 'عذر', 'اعذار', 'برزنتيشن', 'ابغئ', 'حل', 'حلول',
    'cv', 'سيرة', 'سيره', 'ذاتية', 'سكليف', 'اختبار', 'كويز', 'كوز', 'فاينل',
    'يعرف', 'احتاج', 'أحتاج', 'مساعدة', 'مساعده', 'طبي', 'ذاتيه', 'محتاج', 'محتأج', 'يقدر', 'احد'
}

@client.on(events.NewMessage)
async def forward_messages(event):
    if event.is_group and event.raw_text:
        message_text = event.raw_text
        if any(keyword in message_text for keyword in filter_keywords):
            sender = await event.get_sender()
            sender_username = getattr(sender, 'username', 'غير معروف')
            sender_name = sender.first_name or 'غير معروف'
            chat_username = getattr(event.chat, 'username', 'غير معروف')

            # صياغة محتوى الرسالة مع تضمين اسم المستخدم للمجموعة
            message_content = (
                f"رسالة من المجموعة: @{chat_username}\n"
                f"المُرسل: {sender_name} (@{sender_username})\n\n"
                f"{message_text}"
            )
            try:
                # إرسال الرسالة المعدلة إلى المجموعة المستهدفة
                await client.send_message(target_group_id, message_content)
                logging.info(f"تم إعادة توجيه رسالة من @{sender_username} إلى المجموعة المستهدفة.")
            except Exception as e:
                logging.error(f"فشل في إعادة توجيه الرسالة: {e}")

# تشغيل العميل
if __name__ == '__main__':
    with client:
        print("Bot is running and listening for messages...")
        client.run_until_disconnected()
