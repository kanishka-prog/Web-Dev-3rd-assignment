# Web-Dev-3rd-assignment
/* =========================================================
   ROOT VARIABLES (modern color system)
========================================================= */
:root {
  --primary: #0db0e6;
  --secondary: #0a7fd9;
  --text: #333;
  --bg: #f4f4f9;
  --white: #ffffff;
  --radius: 10px;
  --transition: 0.3s ease;
  --shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  --accent-green: rgb(3, 98, 43);
}

/* =========================================================
   GLOBAL RESET + BASE STYLES
========================================================= */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Poppins", Arial, sans-serif;
  background-color: var(--bg);
  color: var(--text);
  line-height: 1.7;
  scroll-behavior: smooth;
}

/* =========================================================
   HEADER
========================================================= */
header {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  color: var(--white);
  padding: 30px 0;
  text-align: center;
  box-shadow: var(--shadow);
}

header h1 {
  margin: 0;
  font-size: 2.5em;
  animation: fadeDown 1s ease-in-out;
}

/* Animation */
@keyframes fadeDown {
  from { opacity: 0; transform: translateY(-20px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* =========================================================
   NAVIGATION
========================================================= */
nav {
  margin-top: 10px;
}

nav ul {
  list-style: none;
}

nav li {
  display: inline-block;
  margin: 0 15px;
}

nav a {
  color: var(--accent-green);
  text-decoration: none;
  font-weight: bold;
  font-size: 1.1rem;
  position: relative;
  transition: var(--transition);
}

nav a::after {
  content: "";
  position: absolute;
  width: 0%;
  height: 2px;
  bottom: -5px;
  left: 0;
  background: var(--secondary);
  transition: var(--transition);
}

nav a:hover::after {
  width: 100%;
}

/* =========================================================
   MAIN CONTAINER
========================================================= */
main {
  max-width: 950px;
  margin: 40px auto;
  padding: 25px;
  background-color: var(--white);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  animation: fadeIn 0.8s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: scale(0.97); }
  to   { opacity: 1; transform: scale(1); }
}

/* =========================================================
   SECTION HEADINGS
========================================================= */
section h2 {
  border-left: 5px solid var(--primary);
  padding-left: 10px;
  margin-top: 40px;
  font-size: 1.8rem;
}

/* =========================================================
   ABOUT SECTION IMAGE
========================================================= */
#about img {
  display: block;
  margin: 20px auto;
  border-radius: 50%;
  width: 160px;
  height: 160px;
  object-fit: cover;
  box-shadow: var(--shadow);
  transition: var(--transition);
}

#about img:hover {
  transform: scale(1.1);
}

/* =========================================================
   PROJECT CARDS
========================================================= */
article {
  background-color: #fafafa;
  padding: 20px;
  margin-top: 20px;
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  transition: var(--transition);
}

article:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 25px rgba(0, 0, 0, 0.15);
}

/* =========================================================
   SKILLS TABLE
========================================================= */
table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

table th,
table td {
  border: 1px solid #ccc;
  padding: 12px;
  text-align: left;
}

table th {
  background-color: var(--secondary);
  color: var(--white);
}

table tr:hover {
  background: rgba(13, 176, 230, 0.1);
}

/* =========================================================
   CONTACT FORM
========================================================= */
form {
  background-color: #fafafa;
  padding: 20px;
  border-radius: var(--radius);
  box-shadow: var(--shadow);
}

label {
  font-weight: bold;
}

input,
textarea {
  width: 100%;
  padding: 12px;
  margin: 10px 0 20px;
  border: 2px solid #ddd;
  border-radius: var(--radius);
  transition: var(--transition);
}

input:focus,
textarea:focus {
  border-color: var(--primary);
  outline: none;
  box-shadow: 0 0 10px rgba(13, 176, 230, 0.3);
}

input[type="submit"] {
  background-color: var(--primary);
  color: white;
  border: none;
  cursor: pointer;
  font-size: 1.1em;
  padding: 12px;
  border-radius: var(--radius);
  transition: var(--transition);
}

input[type="submit"]:hover {
  background-color: var(--secondary);
  transform: translateY(-2px);
}

/* =========================================================
   FOOTER
========================================================= */
footer {
  text-align: center;
  background-color: var(--secondary);
  color: white;
  padding: 15px 0;
  margin-top: 40px;
  box-shadow: var(--shadow);
}

/* =========================================================
   RESPONSIVE DESIGN
========================================================= */
@media (max-width: 768px) {
  nav li {
    display: block;
    margin: 10px 0;
  }

  header h1 {
    font-size: 2rem;
  }

  main {
    margin: 20px;
    padding: 20px;
  }

  table th,
  table td {
    font-size: 0.9rem;
  }
}

