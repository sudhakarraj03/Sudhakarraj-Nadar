# Sudhakarraj-Nadar
personal
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dr. Sudhakarraj Nadar</title>
  <style>
    /* Reset & Basics */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      line-height: 1.6;
      background-color: #ffffff;
      color: #333;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* Navigation Bar */
    nav {
      background-color: #0d47a1;
      color: white;
      padding: 1rem 2rem;
      position: sticky;
      top: 0;
      z-index: 999;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    nav h1 {
      font-size: 1.25rem;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
    }

    nav ul li a {
      color: white;
      font-weight: 500;
    }

    nav ul li a:hover {
      border-bottom: 2px solid #fff;
    }

    /* Section Layout */
    section {
      max-width: 900px;
      margin: 4rem auto;
      padding: 0 2rem;
    }

    h2 {
      font-size: 1.5rem;
      color: #0d47a1;
      margin-bottom: 1rem;
      border-bottom: 1px solid #eee;
      padding-bottom: 0.5rem;
    }

    .section-content {
      background: #f9f9f9;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }

    ul {
      list-style: disc;
      padding-left: 1.5rem;
    }

    /* Responsive */
    @media (max-width: 768px) {
      nav {
        flex-direction: column;
        align-items: flex-start;
      }

      nav ul {
        flex-direction: column;
        gap: 1rem;
        margin-top: 1rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <nav>
    <h1>Dr. Sudhakarraj Nadar</h1>
    <ul>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#education">Education</a></li>
      <li><a href="#skills">Skills</a></li>
    </ul>
  </nav>

  <!-- Work Experience -->
  <section id="experience">
    <h2>Work Experience</h2>
    <div class="section-content">
      <ul>
        <li><strong>SIWS College (2020–Present)</strong> – In-charge of B.Com (B&I) & BMS. Taught Finance & Management subjects.</li>
        <li><strong>Rizvi College (2019–2020)</strong> – Academic and Exam Coordinator for BAF & BMS programs.</li>
        <li><strong>Guru Nanak College (2017–2019)</strong> – Lecturer in Commerce, guided M.Com projects.</li>
        <li><strong>Standard Chartered Bank (2016–2017)</strong> – Officer, RBI Liaisoning Team.</li>
        <li><strong>HDFC Bank (2016)</strong> – Trainee, Foreign Exchange Compliance.</li>
      </ul>
    </div>
  </section>

  <!-- Education -->
  <section id="education">
    <h2>Education</h2>
    <div class="section-content">
      <ul>
        <li><strong>Ph.D. in Commerce</strong> – Sabarmati University (2021)</li>
        <li><strong>UGC NET (Commerce)</strong> – Qualified in 2017</li>
        <li><strong>M.Com</strong> – Mumbai University (2015) – 67.75%</li>
        <li><strong>B.Com</strong> – SIES College, Mumbai (2013) – 76.28%</li>
        <li><strong>CA IPCC</strong> – Group I & II Cleared</li>
      </ul>
    </div>
  </section>

  <!-- Skills -->
  <section id="skills">
    <h2>Skills</h2>
    <div class="section-content">
      <ul>
        <li>Curriculum Design & Teaching</li>
        <li>Commerce & Financial Management</li>
        <li>Research & Academic Writing</li>
        <li>RBI Compliance & FEMA Regulations</li>
        <li>Committee & Event Management</li>
        <li>MS Office, Web Research</li>
        <li>Leadership & Communication</li>
      </ul>
    </div>
  </section>

</body>
</html>

<script>
// Smooth Scrolling
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener("click", function(e) {
    e.preventDefault();
    document.querySelector(this.getAttribute("href")).scrollIntoView({
      behavior: "smooth"
    });
  });
});

// Mobile Menu Toggle
document.getElementById("mobile-menu").addEventListener("click", function () {
  document.getElementById("navbar").classList.toggle("active");
});

// Contact Form Validation
document.getElementById("contactForm").addEventListener("submit", function (e) {
  e.preventDefault();
  
  const name = document.getElementById("name").value.trim();
  const email = document.getElementById("email").value.trim();
  const message = document.getElementById("message").value.trim();
  const feedback = document.getElementById("formMessage");

  // Basic Validation
  if (!name || !email || !message) {
    feedback.textContent = "Please fill out all fields.";
    feedback.style.color = "red";
    return;
  }

  // Email Format Check
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  if (!emailRegex.test(email)) {
    feedback.textContent = "Please enter a valid email address.";
    feedback.style.color = "red";
    return;
  }

  // Success (no backend here, just UI confirmation)
  feedback.textContent = "Message sent successfully!";
  feedback.style.color = "green";

  // Clear form
  this.reset();
});
</script>
