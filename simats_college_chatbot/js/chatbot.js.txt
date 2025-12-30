function getResponse(text) {
  text = text.toLowerCase();

  // greetings
  if (text.includes("hi") || text.includes("hello") || text.includes("hey")) {
    return "Hello!\nHow can I help you today regarding SIMATS Engineering?";

  // college about
  } else if (text.includes("simats") || text.includes("simats engineering") || text.includes("about college")) {
    return (
      "About SIMATS Engineering:\n" +
      "• Engineering institution under Saveetha Institute of Medical and Technical Sciences.\n" +
      "• Offers UG and PG programmes in multiple engineering departments.\n" +
      "• Focus on academics, research and placements."
    );

  // departments + branches list
  } else if (text.includes("department") || text.includes("departments") || text.includes("courses")) {
    return (
      "Departments and branches:\n" +
      "• CSE – CSE (Core)\n" +
      "• CSE‑AI – CSE with Artificial Intelligence & Machine Learning\n" +
      "• CSE‑DS – CSE with Data Science\n" +
      "• IT – Information Technology\n" +
      "• ECE – Electronics and Communication Engineering\n" +
      "• EEE – Electrical and Electronics Engineering\n" +
      "• MECH – Mechanical Engineering\n" +
      "• CIVIL – Civil Engineering"
    );

  // CSE detail / branches
  } else if (text.includes("cse") && text.includes("branch")) {
    return (
      "CSE related branches:\n" +
      "• CSE – Computer Science and Engineering (Core)\n" +
      "• CSE‑AI – CSE with Artificial Intelligence & Machine Learning\n" +
      "• CSE‑DS – CSE with Data Science"
    );

  // other specific departments
  } else if (text.includes("ece")) {
    return (
      "ECE department:\n" +
      "• Communication systems.\n" +
      "• VLSI and embedded systems.\n" +
      "• Signal processing and electronics design."
    );
  } else if (text.includes("eee")) {
    return (
      "EEE department:\n" +
      "• Power systems and electrical machines.\n" +
      "• Control systems.\n" +
      "• Renewable energy topics."
    );
  } else if (text.includes("mechanical")) {
    return (
      "Mechanical Engineering department:\n" +
      "• Design and manufacturing.\n" +
      "• Thermal engineering.\n" +
      "• Industrial engineering."
    );
  } else if (text.includes("civil")) {
    return (
      "Civil Engineering department:\n" +
      "• Structural engineering.\n" +
      "• Environmental engineering.\n" +
      "• Transportation and construction engineering."
    );

  // admissions
  } else if (text.includes("admission") || text.includes("apply") || text.includes("eligibility") || text.includes("entrance")) {
    return (
      "Admissions information:\n" +
      "• 10+2 with Physics, Chemistry and Mathematics.\n" +
      "• Need to meet the prescribed cut‑off marks.\n" +
      "• Seats filled through counselling and management quota."
    );

  // FEES STRUCTURE – per department
  } else if (text.includes("fee") || text.includes("fees") || text.includes("tuition") || text.includes("payment")) {

    if (text.includes("cse") && !text.includes("ai") && !text.includes("data")) {
      return "FEES STRUCTURE:\n• CSE: ₹1,90,000 per year (approx).";
    } else if (text.includes("cse-ai") || text.includes("cse ai") || text.includes("cse with ai") || text.includes("csa-ai")) {
      return "FEES STRUCTURE:\n• CSE‑AI: ₹2,00,000 per year (approx).";
    } else if (text.includes("data science") || text.includes("cse ds") || text.includes("csd")) {
      return "FEES STRUCTURE:\n• CSE‑DS (Data Science): ₹2,00,000 per year (approx).";
    } else if (text.includes("it") && !text.includes("kit")) {
      return "FEES STRUCTURE:\n• IT: ₹1,70,000 per year (approx).";
    } else if (text.includes("ece")) {
      return "FEES STRUCTURE:\n• ECE: ₹1,60,000 per year (approx).";
    } else if (text.includes("eee")) {
      return "FEES STRUCTURE:\n• EEE: ₹1,40,000 per year (approx).";
    } else if (text.includes("mechanical")) {
      return "FEES STRUCTURE:\n• Mechanical: ₹1,30,000 per year (approx).";
    } else if (text.includes("civil")) {
      return "FEES STRUCTURE:\n• Civil: ₹1,30,000 per year (approx).";
    } else {
      return (
        "FEES STRUCTURE (approx per year):\n" +
        "• CSE: ₹1,90,000\n" +
        "• CSE‑AI: ₹2,00,000\n" +
        "• CSE‑DS (Data Science): ₹2,00,000\n" +
        "• IT: ₹1,70,000\n" +
        "• ECE: ₹1,60,000\n" +
        "• EEE: ₹1,40,000\n" +
        "• Mechanical: ₹1,30,000\n" +
        "• Civil: ₹1,30,000"
      );
    }

  // HOSTEL – boys & girls
  } else if (text.includes("hostel")) {

    if (text.includes("boys") || text.includes("boy")) {
      return (
"BOYS HOSTEL – ROOM TYPES & FEES (approx per year with mess):\n" +
"Krishna (AC):\n" +
"• 2 in 1 AC  : ₹2,10,000\n" +
"• 4 in 1 AC  : ₹1,70,000\n" +
"\nKaveri (AC):\n" +
"• 2 in 1 AC  : ₹2,00,000\n" +
"• 4 in 1 AC  : ₹1,60,000\n" +
"\nPalar (Non‑AC):\n" +
"• 4 in 1 Non‑AC  : ₹1,20,000\n" +
"• 8 in 1 Non‑AC  : ₹1,00,000\n" +
"• 12 in 1 Non‑AC : ₹85,000"
      );
    } else if (text.includes("girls") || text.includes("girl")) {
      return (
"GIRLS HOSTEL – ROOM TYPES & FEES (approx per year with mess):\n" +
"Vaigai:\n" +
"• 2 in 1 AC      : ₹1,90,000\n" +
"• 4 in 1 AC      : ₹1,55,000\n" +
"• 4 in 1 Non‑AC  : ₹1,25,000\n" +
"\nSanthi:\n" +
"• 2 in 1 AC      : ₹1,85,000\n" +
"• 4 in 1 AC      : ₹1,50,000\n" +
"• 4 in 1 Non‑AC  : ₹1,20,000"
      );
    } else {
      return (
        "Hostel summary:\n" +
        "• Boys – Krishna (AC), Kaveri (AC), Palar (Non‑AC, larger sharing).\n" +
        "• Girls – Vaigai and Santhi with AC and Non‑AC options.\n" +
        "Type 'boys hostel' or 'girls hostel' to see room‑wise fee details."
      );
    }

  // FACILITIES
  } else if (text.includes("facility") || text.includes("facilities") || text.includes("campus life")) {
    return (
      "Campus facilities:\n" +
      "• Library – Textbooks, reference books, journals and digital library.\n" +
      "• Sports – Cricket, football, volleyball, basketball, indoor games and gym.\n" +
      "• Cultural events – Symposiums, culturals, fests, clubs for music, dance and drama.\n" +
      "• Basic amenities – Labs, computer centres, Wi‑Fi campus, canteen, transport and medical facility."
    );

  // PLACEMENTS
  } else if (text.includes("placement") || text.includes("placements") || text.includes("companies")) {
    return (
      "Placements overview:\n" +
      "Sample student offers:\n" +
      "• A. Karthik (CSE)     – ₹7.5 LPA – Infosys.\n" +
      "• B. Priya (CSE‑AI)    – ₹8.2 LPA – TCS Digital.\n" +
      "• C. Rahul (IT)        – ₹6.8 LPA – Wipro.\n" +
      "• D. Sneha (ECE)       – ₹6.5 LPA – Accenture.\n" +
      "• E. Arjun (Mechanical)– ₹5.2 LPA – Hyundai.\n\n" +
      "Major companies visiting / tie‑ups:\n" +
      "• TCS, Infosys, Wipro, HCL, Cognizant, Accenture, Capgemini, IBM,\n" +
      "• Tech Mahindra, L&T Technology Services, Amazon, Zoho, Oracle,\n" +
      "• Deloitte, EY, KPMG, Hexaware, Mindtree, Virtusa,\n" +
      "• Hyundai, Renault‑Nissan, Tata Elxsi, Bosch, Siemens, TVS Motors."
    );

  // timetable / exam
  } else if (text.includes("timetable") || text.includes("schedule") || text.includes("class") || text.includes("exam")) {
    return (
      "Timetable information:\n" +
      "• Class timetable is fixed at the start of the semester.\n" +
      "• Internal and semester exam schedules are announced by the department.\n" +
      "• Students are informed through notice boards or student portals."
    );

  // contact
  } else if (text.includes("contact") || text.includes("phone") || text.includes("email")) {
    return (
      "Contact information:\n" +
      "• College office handles admission and fee related queries.\n" +
      "• Department offices handle timetable and academic doubts.\n" +
      "• Official phone numbers and emails are shared through brochures and notices."
    );

  // goodbye
  } else if (text.includes("bye") || text.includes("exit") || text.includes("thank you")) {
    return "Thank you for using the SIMATS Engineering chatbot.\nAll the best for your studies!";

  // default
  } else {
    return (
      "I can help with:\n" +
      "• Departments and branches.\n" +
      "• FEES STRUCTURE for each department.\n" +
      "• Boys and girls hostel room types and fees.\n" +
      "• Campus facilities.\n" +
      "• Placements and companies.\n" +
      "• Admissions and timetable basics.\n" +
      "Please ask about any of these."
    );
  }
}

function appendMessage(sender, message) {
  const chat = document.getElementById("chat");
  const outer = document.createElement("div");
  outer.classList.add("msg");
  if (sender === "Bot") {
    outer.classList.add("bot");
  } else {
    outer.classList.add("user");
  }

  const bubble = document.createElement("div");
  bubble.classList.add("bubble");
  bubble.textContent = message;

  outer.appendChild(bubble);
  chat.appendChild(outer);
  chat.scrollTop = chat.scrollHeight;
}

function sendMessage() {
  const input = document.getElementById("userInput");
  const userText = input.value.trim();
  if (userText === "") return;

  appendMessage("You", userText);
  const botReply = getResponse(userText);
  appendMessage("Bot", botReply);

  input.value = "";
  input.focus();
}

document.getElementById("userInput").addEventListener("keydown", function (e) {
  if (e.key === "Enter") {
    sendMessage();
  }
});
