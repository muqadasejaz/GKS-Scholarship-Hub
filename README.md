# 🎓 GKS Scholarship Hub: Your Whole GKS-G Journey in One Place

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/94bed84b-6d86-4973-8fc1-f32ac3b4ec8c" />


---

## Overview

**GKS Scholarship Hub** is a free web app for international students applying to the **Global Korea Scholarship for Graduate Degrees (GKS-G)**, the Korean government's fully funded Master's and PhD scholarship.

Applying for GKS-G means jumping between the official guidelines, dozens of university websites, hundreds of department pages and scattered professor profiles, then writing and tracking emails by hand. The hub puts that whole journey in one place. It covers the guide and tracks, all 74 universities and their departments, verified professors and email templates, plus a tracker for every professor you contact.

It's built as a **single, fast, dependency-free web page**. It needs no sign-up, and each user's data stays in their own browser.

---

## Live Demo

 **[gks-scholarship-hub.vercel.app](https://gks-scholarship-hub.vercel.app)**

---

##  The Problem It Solves

| Problem applicants face | How the hub solves it |
|---|---|
| The GKS rules, tracks and quotas are spread across long PDF guidelines | A plain-language **GKS guide** that explains the Embassy and University tracks, the programs and a document checklist |
| Finding which universities and departments accept GKS scholars takes hours | **74 universities and 4,311 departments** from NIIED's official 2026 GKS-G files, searchable and filterable |
| Professor information is buried in Korean-language faculty pages | **3,000+ professors** collected from official university pages, with emails, labs, research areas and the source link |
| Hard to tell which professors match your research | **Research-keyword matching** that labels professors as a "fit" and ranks them first |
| Writing a good first email to a professor is stressful | **Ready-made email templates** that fill in your details and the professor's research automatically |
| Keeping track of who you emailed, who replied and when to follow up | An **outreach tracker** with status, replies and follow-up reminders |

---

## Features

- 🧭 **Guided five-step flow:** Track → University → Department → Professor → Email
- 📚 **GKS guide and tracks:** Embassy vs University track, program types and an application checklist
- 🏛️ **University explorer:** filter by Type A or Type B, program and field
- 🏢 **Department details:** degree levels, language of instruction, TOPIK requirements and intake months
- 👩‍🏫 **Verified professors:** names (Korean and English), positions, emails, labs, research areas and homepages, each linked to its official source page
- 🎯 **Research fit:** add your keywords (for example "computer vision, LLM") and matching professors rise to the top
- 🔎 **Global search:** find universities, departments and professors from one search bar
- ✉️ **Email templates:** first contact and follow-up drafts, filled with your profile and the professor's research
- 📋 **Outreach tracker:** shortlist professors, log emails, record replies and get follow-up reminders
- 🔒 **Private by default:** no account needed; everything is saved in your own browser
- 💾 **Backup and restore:** move your tracker to another device with one copy-paste
- 🌗 **Light and dark mode**, fully responsive on mobile

---

##  How It Works

 <img width="1600" height="960" alt="image" src="https://github.com/user-attachments/assets/3606d29c-0e57-4be7-9052-65bd1fc0f5d3" />

1. **Pick your track.** Learn the difference between the Embassy and University tracks and choose yours.
2. **Choose a university.** Browse the 74 GKS-G universities, filtered by type and program.
3. **Find a department.** Check degrees, language and TOPIK rules for each department.
4. **Match a professor.** Filter by university, research keywords and "email listed", then read each professor's official details.
5. **Email and track.** Draft a personal email from a template, send it, and track replies and follow-ups in one list.

---

##  Tools and Technologies

| Category | Details |
|---|---|
| Frontend | Vanilla **HTML, CSS and JavaScript** in a single file, with no framework and no dependencies |
| Graphics | Hand-made inline **SVG** illustrations and icons |
| Data pipeline | **Python** build script that cleans, normalizes and merges the data into the page |
| Data collection | Browser-based extraction from official university faculty pages, with source URLs and check dates kept |
| Name handling | Official English names where available, with Korean-to-English **romanization** as a fallback |
| Storage | Browser **localStorage**, plus JSON backup and restore |
| Hosting | **Vercel** (static deployment) |

---

##  Data and Coverage

| Data | Source | Coverage |
|---|---|---|
| Universities | NIIED 2026 GKS-G university list | 74 universities (Type A and Type B) |
| Departments | NIIED 2026 GKS-G department files | 4,311 departments |
| Professors | Official university faculty pages | 3,000+ professors across 179 departments and 22 universities, growing regularly |

Every professor list stores the **official page it came from** and the **date it was checked**, so users can verify the details themselves.

> **Note:** The 2027 GKS-G guidelines may change the rules. Always confirm deadlines and requirements on [Study in Korea](https://www.studyinkorea.go.kr) before applying.

---

## Project Structure

```
gks-scholarship-hub/
├── index.html            
├── README.md
├── LICENSE
```

The build workspace that produces `index.html` looks like this:

```
build/
├── app_template.html     
├── build.py              
├── data.json             
├── pg.json               
├── prof/ , prof2/        
├── en_names.py, snu_en.py
└── site/index.html       
```

---

##  Usage

### 1. Clone the Repository

```bash
git clone https://github.com/muqadasejaz/gks-scholarship-hub.git
cd gks-scholarship-hub
```

### 2. Run Locally

It's a static page, so just open `index.html` in your browser. To serve it locally instead:

```bash
python -m http.server 8000
# then open http://localhost:8000
```


### 3. Deploy on Vercel

1. Push the repository to GitHub.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Set the **Framework Preset** to **Other** and leave the build command empty.
4. Click **Deploy**. Every push to GitHub updates the live site automatically.

---

##  Privacy

- No sign-up, no tracking and no server-side database.
- Each user's profile, email drafts and tracker are stored **only in their own browser**.
- Users can export a backup at any time and restore it on another device.

---

##  Limitations

- Professor coverage is still growing: 22 of the 74 universities currently have professor data.
- Some faculty pages are Korean-only, so some English names are romanized and some research areas are in Korean.
- Saved data doesn't sync across devices automatically (use backup and restore).
- Some university websites block automated access, so those departments need to be added manually.

---

##  Roadmap

- [x] GKS guide, tracks and checklist
- [x] 74 universities and 4,311 departments
- [x] 3,000+ verified professors with source links
- [x] Email templates and outreach tracker
- [ ] Professor data for all 74 universities
- [ ] Optional accounts for cross-device sync
- [ ] Research-paper links for each professor
- [ ] Deadline reminders for each university

---

##  References

- [Study in Korea: Global Korea Scholarship](https://www.studyinkorea.go.kr)
- [NIIED (National Institute for International Education)](https://www.niied.go.kr)
- [Vercel documentation](https://vercel.com/docs)

---

##  Author

**Muqadas Ejaz**, AI/ML Engineer

📫 [muqadasejaz3@gmail.com](mailto:muqadasejaz3@gmail.com)
🌐 [LinkedIn](https://www.linkedin.com/in/muqadasejaz) · [GitHub](https://github.com/muqadasejaz) · [Portfolio](https://muqadasejaz.github.io/portfolio/)
📬 [Instagram](https://www.instagram.com/bymuqadasejaz) · [X](https://x.com/muqadas__ejaz)

---

##  License

This project is licensed under the [MIT License](LICENSE).

*GKS Scholarship Hub is an independent tool and is not affiliated with NIIED or Study in Korea.*

⭐ If this project helps you or someone applying for GKS, please give it a star!
