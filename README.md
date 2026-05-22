projects = [
    {
        "sr_no": 1,
        "name": "QUIZ-COMPETITION",
        "code_link": "https://github.com/v595/QUIZ-COMPETITION",
        "demo_link": "https://quiz-competition-f83r.onrender.com/"
    },
    {
        "sr_no": 2,
        "name": "EXPENSES-TRACKER",
        "code_link": "https://github.com/v595/expenses_tracker",
        "demo_link": "https://expenses-tracker-bysn.onrender.com/"
    },
    {
        "sr_no": 3,
        "name": "HOTEL-MANAGEMENT-SYSTEM",
        "code_link": "https://github.com/v595/hotel-management-system",
        "demo_link": ""
    }
]

# GitHub icon
github_icon = "https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"

# Create README markdown
markdown = """
<h1 align="center">All Project List with Code</h1>

<p align="center">
<a href="https://github.com/v595">Visit My GitHub Profile</a>
</p>

<br>

<table>
<tr>
<th>Sr No</th>
<th>Name</th>
<th>Code Link</th>
<th>Demo Link</th>
</tr>
"""

# Add project rows
for project in projects:

    code_btn = f'''
    <a href="{project['code_link']}">
        <img src="{github_icon}" width="40">
    </a>
    '''

    if project["demo_link"]:
        demo_btn = f'''
        <a href="{project['demo_link']}">
            <img src="{github_icon}" width="40">
        </a>
        '''
    else:
        demo_btn = "Not Available"

    markdown += f"""
<tr>
<td>{project['sr_no']}</td>
<td>{project['name']}</td>
<td align="center">{code_btn}</td>
<td align="center">{demo_btn}</td>
</tr>
"""

# Footer
markdown += """
</table>

<br>

<h3 align="center">
Made by Vishal Chauhan (v595)
</h3>
"""

# Save README.md
with open("README.md", "w", encoding="utf-8") as file:
    file.write(markdown)

print("README.md generated successfully!")
