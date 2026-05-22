projects = [
    {
        "sr_no": 1,
        "name": "QUIZ-COMPETITION",
        "description": "A Python Quiz Competition app with MCQs, coding challenges, debugging & logical problems.",
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
        "description": "A hotel management system project for managing hotel operations, bookings, rooms, and customer records.",
        "code_link": "https://github.com/v595/hotel-management-system",
        "demo_link": "—"
    }
]

# Generate Markdown Content
markdown = "# All Project List with Code – v595\n\n"
markdown += "**GitHub Profile:** https://github.com/v595\n\n"
markdown += "## Projects\n\n"
markdown += "| Sr No | Project Name | Description | Code Link | Demo Link |\n"
markdown += "|-------|--------------|-------------|-----------|-----------|\n"

for project in projects:
    markdown += (
        f"| {project['sr_no']} | **{project['name']}** | "
        f"{project['description']} | "
        f"[View Code]({project['code_link']}) | "
        f"{project['demo_link']} |\n"
    )

markdown += "\n---\n\n"
markdown += "**Made by:** Vishal Chauhan (v595)  \n"
markdown += "**GitHub:** https://github.com/v595\n"
markdown += "\n# all-projects"

# Save to README.md
with open("README.md", "w", encoding="utf-8") as file:
    file.write(markdown)

print("README.md generated successfully!")
