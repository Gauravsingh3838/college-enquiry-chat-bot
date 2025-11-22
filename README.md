# college-enquiry-chat-bot
def get_reply(message):
    msg = message.lower()

    if re.search(r"\b(hi|hello|hey|hii)\b", msg):
        return "Hi there! What would you like to know about the college? LIKE : FEE, COURSE, ADMISSION, FACILITY, LOCATION, CONTACT."

    if "course" in msg or "courses" in msg:
        return (
            "Here are the main courses available:\n"
            "- B.Tech (CSE, CSE Specializations, ECE, ME, CE)\n"
            "- BBA, MBA\n"
            "- M.Tech\n"
        )

    if "admission" in msg:
        return (
            "Admissions are done through the VITEEE entrance exam followed by counselling.\n"
            "You need to fill out the online form on the official website. Seat allotment is based on your VITEEE rank."
        )

    if "fee" in msg or "fees" in msg:
        return (
            "Here’s the approx fee structure:\n"
            "- B.Tech: around ₹2,00,000 CAT1 per year\n"
            "- B.Tech: around ₹3,00,000 CAT2 per year\n"
            "- B.Tech: around ₹4,00,000 CAT3 per year\n"
            "- B.Tech: around ₹4,50,000 CAT4 per year\n"
            "- B.Tech: around ₹5,00,000 CAT5 per year\n"
            "- BBA/BCA: around ₹1,00,000 per year\n"
        )

    if "facility" in msg or "facilities" in msg:
        return (
            "Facilities available on campus:\n"
            "- Library\n- Hostel\n- Transport\n- Wi-Fi\n- Sports complex"
        )

    if "location" in msg or "where" in msg:
        return "The college is situated near Bhopal, in Sehore district, Aastha village — pincode 466114."

    if "contact" in msg or "phone" in msg:
        return "You can reach us at +91-9876543210 or drop a mail at vitbhopal@gmail.com."

    return "I’m not sure I got that. Try asking about admissions, fees, courses, or facilities."


print("College Enquiry Chatbot (type 'exit' to quit)")
while True:
    user_text = input("You: ")
    if user_text.strip().lower() == 'exit':
        print("Chatbot: Alright, take care!")
        break
    print("Chatbot:", get_reply(user_text))
