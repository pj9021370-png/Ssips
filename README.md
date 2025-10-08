<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SS International Public School</title>
<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background-color: white;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

/* Sections */
section {
    flex: 1;
    padding: 40px 20px;
    display: none;
}

section.active {
    display: block;
}

/* Home Boxes */
.home-boxes {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}

.home-boxes div {
    flex: 1 1 150px;
    min-width: 120px;
    max-width: 180px;
    height: 120px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-weight: bold;
    font-size: 16px;
    border-radius: 12px;
    cursor: pointer;
    transition: transform 0.3s;
    text-align: center;
}

.home-boxes div:hover {
    transform: scale(1.05);
}

/* Box Colors */
.box-learning { background-color: #4CAF50; }
.box-message { background-color: #2196F3; }
.box-attendance { background-color: #FF9800; }
.box-gallery { background-color: #FF5722; }
.box-ask-ai { background-color: #9C27B0; }
</style>
</head>
<body>

<!-- Sirf Sections -->
<section id="home" class="active">
    <div class="home-boxes">
        <div class="box-learning" onclick="showSection('home')">Learning</div>
        <div class="box-message" onclick="window.location.href='http://localhost:8080/home.html'">Message</div>
        <div class="box-attendance" onclick="window.location.href='http://localhost:8080/n.html'">Attendance</div>
        <div class="box-gallery" onclick="window.location.href='http://localhost:8080/profile.html'">Gallery</div>
        <div class="box-ask-ai" onclick="window.location.href='http://localhost:8080/m.html'">Ask with AI</div>
    </div>
</section>

<section id="message">
    <h2>Message</h2>
    <p>Yahan tumhare messages show honge.</p>
</section>

<section id="profile">
    <h2>Profile</h2>
    <p>Yahan profile information milegi.</p>
</section>

<script>
function showSection(id) {
    document.querySelectorAll('section').forEach(sec => sec.classList.remove('active'));
    document.getElementById(id).classList.add('active');
}
</script>

</body>
</html>
