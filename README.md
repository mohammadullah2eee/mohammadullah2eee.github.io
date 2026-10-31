# Mohammad Ullah: Portfolio

Live website: https://mohammadullah2eee.github.io

A personal portfolio website built with HTML, CSS and JavaScript and hosted on GitHub Pages. All of the content lives in one place (the `DATA` block in `index.html`), so you update the website by editing text and uploading pictures.

---

## 1. What is in this repository

```
mohammadullah2eee.github.io/
├── index.html     The whole website. Your content is in the DATA block near the bottom
├── README.md      This guide
├── images/        All pictures (portrait, projects, internships, awards)
└── assets/
    └── cv.pdf     Your CV (the Download CV button)
```

To preview on your computer, open `index.html` in a browser.

---

## 2. The basic way to edit (use this for everything)

1. Open the repository: https://github.com/mohammadullah2eee/mohammadullah2eee.github.io
2. Click `index.html`, then click the pencil icon (Edit this file).
3. Scroll to `const DATA = {` (or press Ctrl+F in the editor and search for a word).
4. Make your change using the templates in section 4.
5. Click **Commit changes** (green button, top right), then **Commit changes** again.
6. Wait about one minute, open the website and press **Ctrl+Shift+R** (Cmd+Shift+R on a Mac).

### Rules that keep the page from breaking

- Keep every quotation mark `"`, comma `,` and bracket `[ ] { }` in place. One missing quote can blank the whole website.
- Each entry in a list needs a comma after it. The last one can have no comma.
- Do not type a plain `"` inside your text. Use an apostrophe (`’`) or rephrase.
- Do not paste straight from Word or a chat app. It can bring in curly quotes (“ ”) that break the code. Paste into Notepad first.
- Make one change at a time and check the website after each one.

---

## 3. Picture names (the website finds pictures by name)

Upload pictures to the `images` folder. Use lowercase names. Both `.jpg` and `.jpeg` work.

| Picture | File name |
|---|---|
| Portrait | `profile` |
| Project cards, in card order | `project-1`, `project-2`, `project-3` ... |
| Internship cards, in card order | `internship-1`, `internship-2` ... |
| Award or certificate photos | `award-1`, `award-2` ... (you choose the names) |

Example: `images/project-7.jpg`. Uploading a new file with the same name replaces the old one.

Picture sizes: portrait about 800 × 1000 pixels (tall); project pictures about 800 × 440 pixels; internship pictures 16:9 (about 1280 × 720). Keep each file under about 500 KB. A free tool for shrinking pictures is squoosh.app.

Windows tip: turn on View > File name extensions in File Explorer so you do not end up with `profile.jpg.jpg`.

---

## 4. How to add new items

All templates below go inside the `DATA` block of `index.html`.

### 4.1 Adding a new project

Find `projects: [`. Copy this entry and paste it after the last project. Make sure there is a comma between the entries.

```js
{t:"Project title",d:"Two short sentences about what it does.",tags:["Tag 1","Tag 2","Tag 3"],link:"https://github.com/mohammadullah2eee/repository-name"},
```

- `t` is the title and `d` is the description.
- `tags` are the small labels on the card.
- `link` opens when someone clicks **View Project**. Use the project's GitHub repository, a YouTube video, or leave `link:""` until it is ready.
- Picture: upload `images/project-7.jpg` (the number follows the card order).

For each project, create its own GitHub repository with a `README.md` (what it is and how it works), a `BUILD_GUIDE.md` (steps to build it) and an `images` folder. Remove Wi-Fi passwords and keys from any code before uploading.

### 4.2 Adding a new skill

Find `skills: [`.

To add a skill to an existing group, add its name inside that group's list:

```js
["code","Code & Software",["KLayout","Python","New skill here"]],
```

To add a new group:

```js
["icon-name","Group name",["Skill 1","Skill 2","Skill 3"]],
```

Available icon names: `code`, `cpu`, `zap`, `layers`, `flask`, `globe`, `users`, `award`, `gear`, `power`, `folder`, `briefcase`, `book`, `cap`, `user`, `pin`, `link`.

### 4.3 Adding new education

Find `education: [`. Put the newest entry first.

```js
["Degree or certificate","Institution · Subject · Result","Level · Year"],
```

Example: `["Master of Science","University name · Subject · CGPA 3.80","University · 2030"],`

### 4.4 Adding a new internship

Find `internships: [`. Copy this entry and paste it after the last one.

```js
{c:"Company name",r:"Your role or department",dt:"Month Year – Month Year",d:"What you worked on and learned. Keep it to three or four sentences.",tags:["Skill 1","Skill 2"]},
```

- Picture: `images/internship-3.jpg` for the third card and so on.
- Do not upload photos that show confidential designs, screens with company data or your ID card. Check that the company allows you to mention the internship publicly.

### 4.5 Adding new experience

Find `experience: [`. Put the newest entry first.

```js
["Role title","Organization · what you did and achieved.","Month Year – Month Year"],
```

Use `Present` for the end date of a current role.

### 4.6 Adding a new award or recognition (with an optional photo)

Find `awards: [`.

Without a photo:

```js
["Award title","Organizer · why you received it","Year"],
```

With a photo of the certificate or award, add a fourth item. It is the picture name without the ending:

```js
["Award title","Organizer · why you received it","Year","award-1"],
```

Then upload `images/award-1.jpg` (or `.jpeg`). The photo appears under the award and clicking it opens it in full size. Use a different name for each award (`award-2`, `award-3` ...). If the picture is missing, nothing is shown. The same fourth item also works for education and experience entries if you want to show a certificate.

### 4.7 Adding a publication

The **Publications** section sits between Experience and Contact. Until you add something, it shows a short "No publications yet" message.

Find `publications: [` near the end of the `DATA` block. Add an entry like this:

```js
{title:"Paper title",authors:"Mohammad Ullah, Co-author Name",venue:"Journal or conference name",year:"2027",type:"Journal article",link:"https://doi.org/your-link"},
```

- `type` can be `Journal article`, `Conference paper`, `Thesis`, `Preprint` and so on.
- `link` opens when someone clicks **View paper**. Use the DOI or publisher page. Leave `link:""` if there is none.
- If your thesis is not finished, wait before adding it. Only list work that is published or officially accepted.
- Remove the two slashes (`//`) in front of the example line if you want to start from it.

---

## 5. Other things those can be changed

| To change | Where in `DATA` |
|---|---|
| Name, short description, subtitle | `name`, `subtitle`, `lead` |
| About text (two paragraphs) | `about` |
| Quick facts row | `facts` |
| Interests list | `interests` |
| Email, GitHub, LinkedIn, YouTube | `email`, `github`, `linkedin`, `youtube` |
| Location | `location` |
| CV | Upload a new `assets/cv.pdf` (same name) |
| Portrait | Upload a new `images/profile.jpg` (same name) |

---

## 6. Uploading pictures and files on GitHub

1. Open the repository and click the folder (for example `images`).
2. Click **Add file**, then **Upload files**.
3. Drag the files in and wait for the upload to finish.
4. Scroll down and click **Commit changes**.

A file with the same name replaces the old one.

---

## 7. When something goes wrong

- **The page is blank or a section is missing:** you probably removed a quote, comma or bracket. Check the lines you changed last. You can also upload your last good `index.html` again (**Add file**, **Upload files**). A file with the same name replaces the broken one.
- **A picture does not show:** check that the name is lowercase and exact (not `Project 1.jpg`) and that it is inside `images`. Remember that Windows may hide a double extension such as `profile.jpg.jpg`.
- **A link opens a "404" page:** the GitHub repository does not exist yet or is spelled differently. Create it or fix the address.
- **You still see the old version:** wait a minute and press Ctrl+Shift+R. You can also open the **Actions** tab and look for a green tick.
- **Placeholders show on the page:** anything in `[square brackets]` is a placeholder. Replace it or delete that entry.

---

## 8. Contact form

The form opens the visitor's email app with the message already filled in. For a form that sends without an email app, create a free Formspree form and ask for help connecting it.

---

## 9. What to do in the future

Keep a short routine, so the portfolio always stays current.

**After each milestone** (a new project, internship, award, paper or role)
1. Add the entry using the templates in section 4.
2. Upload its pictures.
3. Update your CV file in `assets/cv.pdf`.
4. Post about it on LinkedIn and link to the portfolio.

**Every few months**
- Click every link on the website (project repositories, YouTube, LinkedIn, GitHub).
- Re-read the About text and the short description. Update them as your interests change.
- Remove placeholders and old entries that no longer help you.
- Check that the contact details are correct.

**Each project, as you finish it**
- Create a GitHub repository with a README and a build guide.
- Link it from the project card.
- Pin your best repositories on your GitHub profile.

**Good habits**
- Keep a copy of your latest working `index.html` on your computer.
- Never publish passwords, keys or confidential company files.
- Only claim what is true. Say "designed" or "simulated" unless something was fabricated or measured.
- Ask your supervisor before publishing thesis details.
- Add the portfolio link to your CV, your LinkedIn profile (Contact info and Featured) and your email signature.

---

## Author

Mohammad Ullah, Electrical and Electronic Engineering, RUET
