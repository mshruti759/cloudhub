# ☁️ Cloud Learning Hub

> **Learn Cloud. Build Skills. Deploy with Confidence.**

Cloud Learning Hub is a responsive educational website designed to help learners explore **Cloud Computing, AWS, Linux, DevOps, networking, deployment, and practical cloud projects** in an easy-to-understand way.

The website provides a modern learning interface with interactive sections, search functionality, dark/light mode, animated statistics, learning cards, projects, roadmap, FAQs, and a contact form.

---

## 📌 Project Overview

The **Cloud Learning Hub** is a front-end cloud-learning website created using:

* HTML5
* CSS3
* JavaScript
* Bootstrap
* Google Fonts
* AWS/Cloud-themed design

The JavaScript adds interactive functionality such as **dark/light mode, search, scroll animations, animated counters, active navigation highlighting, and a back-to-top button**.

---

## ✨ Features

### 🌐 Responsive Design

The website is designed to work on:

* 💻 Desktop
* 💻 Laptop
* 📱 Tablet
* 📱 Mobile

The CSS includes responsive breakpoints for different screen sizes.

### 🌙 Dark & Light Mode

Users can switch between light and dark themes.

The selected theme is stored using browser `localStorage`, so the theme preference can remain saved when the user returns to the website.

### 🔎 Search Functionality

The website includes a search box that filters searchable cards dynamically based on the entered text.

### ✨ Scroll Animations

Sections and cards appear with a smooth fade-in animation when they enter the screen using `IntersectionObserver`.

### 📊 Animated Statistics

Statistics counters animate from zero to their target values when they become visible on the page.

### 🧭 Active Navigation

The navigation automatically highlights the section currently visible while scrolling.

### ⬆️ Back-to-Top Button

A back-to-top button appears after scrolling down and smoothly returns the user to the top of the page.

### 📩 Contact Form

The website contains a contact form. Currently, JavaScript prevents the default submission and displays a message indicating that the form should be connected to a backend or form service before deployment.

---

## 🎨 Design & Styling

The project uses a cloud/AWS-inspired visual design.

### Main Colors

| Color              | Purpose                                       |
| ------------------ | --------------------------------------------- |
| 🟧 AWS Orange      | Buttons, highlights and headings              |
| 🔵 Dark Blue       | Navigation, hero section and primary elements |
| 🟢 Teal            | Cloud/learning accents                        |
| 🟩 Green           | Status and blog elements                      |
| ⚪ White            | Main background                               |
| 🌑 Dark Blue/Black | Dark mode                                     |

The stylesheet defines reusable CSS variables for colors, surfaces, borders and shadows.

The design includes:

* Modern cards
* Rounded corners
* Responsive grids
* Hero section
* Terminal-style code block
* Learning cards
* Project cards
* Roadmap
* FAQ section
* Contact section
* Smooth animations
* Dark mode

---

## 🛠️ Technologies Used

### Frontend

* **HTML5** – Website structure
* **CSS3** – Styling and responsive design
* **JavaScript** – Interactive functionality
* **Bootstrap** – Responsive UI components
* **Google Fonts** – Poppins and Roboto

### Cloud / Deployment

* **Amazon EC2**
* **Amazon Linux**
* **NGINX**
* **SSH**
* **DNS**
* **HTTPS / SSL**

The deployment notes specify installing NGINX on an EC2 instance and placing the website files in the NGINX web root.

---

## 📂 Project Structure

```text
Cloud-Learning-Hub/
│
├── index.html
├── styles.css
├── app.js
├── DEPLOYMENT.md
│
└── screenshots/
    ├── home.png
    ├── learning.png
    ├── projects.png
    └── contact.png
```

### File Description

| File            | Description                           |
| --------------- | ------------------------------------- |
| `index.html`    | Main website page                     |
| `styles.css`    | Website styling and responsive design |
| `app.js`        | Interactive JavaScript functionality  |
| `DEPLOYMENT.md` | EC2 + NGINX deployment instructions   |
| `screenshots/`  | Project screenshots                   |

The deployment notes specifically identify `index.html`, `styles.css`, and `app.js` as the local website files.

---

## ☁️ Cloud Learning Topics

The website is designed around practical cloud-learning concepts such as:

* Cloud Computing
* AWS
* EC2
* Linux
* NGINX
* Networking
* Deployment
* DevOps
* Cloud Projects
* Server Management
* DNS
* HTTPS

---

## 🚀 Deployment on AWS EC2

The project can be deployed using an **Amazon EC2 instance with NGINX**.

### Step 1: Update the server

```bash
sudo yum update -y
```

### Step 2: Install NGINX

```bash
sudo yum install nginx -y
```

### Step 3: Start NGINX

```bash
sudo systemctl enable --now nginx
```

### Step 4: Check NGINX

```bash
sudo systemctl status nginx
```

These commands follow the deployment instructions supplied with the project.

---

## 📤 Upload Website Files to EC2

From your local computer, upload the website files using SCP:

```bash
 ssh -i .\Downloads\shruti.pem ec2-user@34.228.25.83
```

Then copy them into the NGINX web directory:

```bash
sudo cp /tmp/index.html /usr/share/nginx/html/
sudo cp /tmp/styles.css /usr/share/nginx/html/
sudo cp /tmp/app.js /usr/share/nginx/html/
```

These paths and commands are included in the project's deployment documentation.

---

## 🌍 Domain & HTTPS

For production deployment:

1. Add an **A record** pointing your domain to the EC2 public IP.
2. Open **port 80** in the EC2 Security Group.
3. Open **port 443** in the EC2 Security Group.
4. Install Certbot according to the Amazon Linux version.
5. Configure HTTPS.
6. Test the HTTPS connection.

The supplied deployment notes include the same domain and HTTPS checklist.

---

## 🔐 AWS Security Group

Recommended web access:

| Type  | Port | Purpose               |
| ----- | ---: | --------------------- |
| SSH   |   22 | Server administration |
| HTTP  |   80 | Website               |
| HTTPS |  443 | Secure website        |

> **Security Note:** For production environments, avoid allowing SSH access from `0.0.0.0/0` unless there is a specific reason. Restrict SSH access to trusted IP addresses whenever possible.

---

## 📸 Screenshots

Add your project screenshots inside the `screenshots` folder.

Example:

```markdown
## 🖥️ Project Screenshots

### Home Page

![Cloud Learning Hub Home]()



> Make sure the image filenames and folder names exactly match your GitHub repository.

---

## 🧪 JavaScript Functionality

The `app.js` file provides several client-side features:

```text
Theme Toggle
     ↓
Dark / Light Mode
     ↓
localStorage
```

```text
Search Box
     ↓
Read Search Query
     ↓
Filter Searchable Cards
```

```text
Scroll
     ↓
IntersectionObserver
     ↓
Fade-in Animation
```

```text
Statistics
     ↓
IntersectionObserver
     ↓
Animated Counter
```

---

## 📚 Deployment Documentation

Detailed deployment instructions are available in:

```text
DEPLOYMENT.md
```

The supplied deployment document covers local files, NGINX installation, SCP file transfer, NGINX web-root deployment, domain configuration, and HTTPS.

---

## 🔮 Future Improvements

Possible future improvements include:

* 🔐 User authentication
* 🗄️ Database integration
* 📊 Student progress tracking
* 🏆 Achievement badges
* 📜 Course certificates
* 🧑‍💻 Interactive cloud labs
* 📝 Online quizzes
* 📈 Learning progress dashboard
* 💬 Real backend-powered contact form
* ☁️ More AWS practical projects
* 🚀 CI/CD deployment using GitHub Actions

---

## 🎯 Learning Outcomes

By building and deploying this project, learners can practice:

* Creating a responsive website
* Writing HTML and CSS
* Using JavaScript DOM manipulation
* Implementing dark mode
* Implementing search functionality
* Creating scroll animations
* Working with AWS EC2
* Installing and configuring NGINX
* Uploading files using SCP
* Configuring DNS
* Understanding HTTPS deployment
* Hosting a website on AWS

---

## 👩‍💻 Author

**Shruti More**

Cloud Computing & AWS Learner

## 

---

##
