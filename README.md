projects = [
    {
        "sr_no": 1,
        "name": "QUIZ-COMPETITION",
        "description": "Python Quiz Competition app with MCQs, coding challenges, debugging & logical problems.",
        "code_link": "https://github.com/v595/QUIZ-COMPETITION",
        "demo_link": "https://quiz-competition-f83r.onrender.com/"
    },
    {
        "sr_no": 2,
        "name": "EXPENSES-TRACKER",
        "description": "Personal finance management app to track income, expenses, budgets and spending habits.",
        "code_link": "https://github.com/v595/expenses_tracker",
        "demo_link": "https://expenses-tracker-bysn.onrender.com/"
    },
    {
        "sr_no": 3,
        "name": "HOTEL-MANAGEMENT-SYSTEM",
        "description": "Hotel management system for bookings, rooms, and customer records.",
        "code_link": "https://github.com/v595/hotel-management-system",
        "demo_link": ""
    }
]

# Create README content
markdown = """# All Project List with Code – v595

**GitHub Profile:** https://github.com/v595

## Projects

| Sr No | Project Name | Description | Code Link | Demo Link |
|------|--------------|-------------|-----------|-----------|
"""

# Add project rows
for project in projects:
    demo = (
        f"[View Demo]({project['demo_link']})"
        if project["demo_link"]
        else "Not Available"
    )

    markdown += (
        f"| {project['sr_no']} "
        f"| {project['name']} "
        f"| {project['description']} "
        f"| [View Code]({project['code_link']}) "
        f"| {demo} |\n"
    )

# Footer
markdown += """

---

**Made by:** Vishal Chauhan (v595)  
**GitHub:** https://github.com/v595
"""

# Save README.md
with open("README.md", "w", encoding="utf-8") as file:
    file.write(markdown)

print("README.md generated successfully!")
