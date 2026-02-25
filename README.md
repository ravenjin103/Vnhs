<!DOCTYPE html>
<html>
<head>
    <title>VNHS | Modern Portal</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        /* ================= BODY ================= */
        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
                        url("/storage/emulated/0/DCIM/Facebook/FB_IMG_1771162537799_3.jpg") no-repeat center center fixed;
            background-size: cover;
            color: #fff;
        }

        .overlay {
            padding: 20px;
            max-width: 1200px;
            margin: auto;
        }

        /* ================= ANIMATIONS ================= */
        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes zoomIn {
            from { opacity: 0; transform: scale(0.7); }
            to { opacity: 1; transform: scale(1); }
        }

        /* ================= HEADER ================= */
        .header {
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(to right, #005bea, #00c6fb);
            padding: 20px 30px;
            border-radius: 50px;
            gap: 15px;
            flex-wrap: wrap;
            box-shadow: 0 5px 20px rgba(0,0,0,0.4);
            animation: slideDown 1s ease;
        }

        .header h1 {
            font-size: 28px;
            margin: 0;
            text-align: center;
            color: #fff;
            text-shadow: 0 0 10px #00c6fb;
        }

        /* ================= MAIN IMAGE ================= */
        .main-img-container {
            text-align: center;
            margin: 30px 0;
            animation: zoomIn 1.2s ease;
        }

        .main-img-container img {
            width: 250px;
            border-radius: 50%;
            box-shadow: 0 10px 25px rgba(0,0,0,0.6);
            border: 5px solid #00c6fb;
        }

        /* ================= BUTTONS ================= */
        .buttons {
            text-align: center;
            margin-bottom: 40px;
        }

        .buttons button {
            padding: 12px 20px;
            margin: 8px;
            border: none;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            background: linear-gradient(45deg, #00c6fb, #005bea);
            color: white;
            font-size: 16px;
            transition: 0.3s;
            box-shadow: 0 5px 15px rgba(0,198,251,0.6);
            animation: fadeUp 0.8s ease forwards;
        }

        .buttons button:hover {
            background: linear-gradient(45deg, #3b82f6, #60a5fa);
            transform: scale(1.1);
            box-shadow: 0 0 25px #00c6fb, 0 0 40px #005bea;
        }

        /* ================= SECTIONS ================= */
        .section {
            display: none;
            background: rgba(0,0,0,0.6);
            padding: 25px;
            border-radius: 25px;
            margin-bottom: 40px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
            animation: fadeUp 0.8s ease;
        }

        .section.show {
            display: block;
        }

        .section h2 {
            color: #00c6fb;
            text-align: center;
            text-shadow: 0 0 10px #3b82f6;
            margin-bottom: 15px;
        }

        .section p, .section ul {
            font-size: 16px;
            line-height: 1.6;
        }

        /* ================= FACILITIES LIST ================= */
        .facilities p {
            margin: 12px 0;
            padding: 10px;
            border-left: 5px solid #00c6fb;
            background: rgba(255,255,255,0.1);
            border-radius: 8px;
        }

        /* ================= GALLERY ================= */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .gallery img {
            width: 100%;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.5);
            transition: transform 0.3s;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        /* ================= CONTACTS ================= */
        .contacts p {
            margin: 8px 0;
            font-size: 16px;
            background: rgba(255,255,255,0.1);
            padding: 10px;
            border-radius: 8px;
        }

        /* ================= SCHOOL HYMN ================= */
        .hymn video {
            width: 100%;
            max-width: 800px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.5);
            display: block;
            margin: auto;
        }

        /* ================= GLOW BUTTONS ================= */
        .section-button {
            margin-top: 15px;
            display: block;
            padding: 12px 20px;
            border: none;
            border-radius: 25px;
            font-weight: bold;
            background: linear-gradient(45deg, #00c6fb, #005bea);
            color: white;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,198,251,0.6);
            transition: 0.3s;
        }

        .section-button:hover {
            transform: scale(1.05);
            box-shadow: 0 0 25px #00c6fb, 0 0 40px #005bea;
        }
    </style>
</head>
<body>
<div class="overlay">

    <!-- HEADER -->
    <div class="header">
        <h1>VICTORIAS NATIONAL HIGH SCHOOL</h1>
    </div>

    <!-- MAIN IMAGE -->
    <div class="main-img-container">
        <img src="/storage/emulated/0/vnhs/vnhs.png" alt="VNHS Logo">
    </div>

    <!-- BUTTONS -->
    <div class="buttons">
        <button onclick="showSection('about')">🏫 About VNHS</button>
        <button onclick="showSection('facilities')">🏢 Facilities</button>
        <button onclick="showSection('achievements')">🏆 Achievements</button>
        <button onclick="showSection('gallery')">📸 Gallery</button>
        <button onclick="showSection('contacts')">📞 Contacts</button>
        <button onclick="showSection('hymn')">🎵 School Hymn</button>
    </div>

    <!-- ABOUT VNHS -->
    <div id="about" class="section">
        <h2>About VNHS</h2>
        <p>
            Victorias National High School (VNHS) is a leading public secondary school committed to
            providing quality, inclusive, and learner-centered education. The school develops academically competent,
            morally upright, and socially responsible students equipped with 21st-century skills. For over 75 years,
            VNHS has served as a pillar of excellence in Victorias City, producing graduates who excel in academics,
            leadership, sports, and community service.
        </p>
        <button class="section-button" onclick="alert('Welcome to VNHS!')">✨ Learn More</button>
    </div>

    <!-- FACILITIES -->
    <div id="facilities" class="section facilities">
        <h2>Our Facilities</h2>
        <p><b>PAGCOR – ICT Computer Rooms:</b> Technology-equipped learning space with computers and internet access for ICT classes.</p>
        <p><b>Science Laboratory:</b> A room with equipment and materials used for science experiments and practical activities.</p>
        <p><b>Library / LRC:</b> A quiet place with books, modules, and references for reading, studying, and research.</p>
        <p><b>Guidance Office:</b> Provides counseling, advice, and support for students’ academic and personal concerns.</p>
        <p><b>School Canteen:</b> Where students and staff can buy food, drinks, and snacks during break time.</p>
        <p><b>Classrooms:</b> Rooms where teachers conduct lessons and students attend daily classes.</p>
        <p><b>Sports Facilities / Covered Court & Football field:</b> Areas for PE classes, sports, and competitions.</p>
    </div>

    <!-- ACHIEVEMENTS -->
    <div id="achievements" class="section">
        <h2>School Achievements</h2>
        <p>🏆 Division Champion – Science Investigatory Project</p>
        <p>🏆 Regional Qualifier – Campus Journalism</p>
        <p>🏆 Provincial Champion – Football Tournament</p>
        <p>🏆 Outstanding Public Secondary School Award</p>
        <p>🏆 National Achievement Test Top Performing School</p>
    </div>

    <!-- GALLERY -->
    <div id="gallery" class="section">
        <h2>School Gallery</h2>
        <div class="gallery">
            <img src="/storage/emulated/0/vnhs/photo1.jpg" alt="VNHS Main Stage">
            <img src="/storage/emulated/0/vnhs/photo2.jpg" alt="VNHS Clinic">
            <img src="/storage/emulated/0/vnhs/photo3.jpg" alt="VNHS Pagcor">
            <img src="/storage/emulated/0/vnhs/photo4.jpg" alt="VNHS Covered Court">
            <img src="/storage/emulated/0/vnhs/photo5.jpg" alt="VNHS Canteen">
            <img src="/storage/emulated/0/vnhs/photo6.jpg" alt="VNHS Paaman">
        </div>
    </div>

    <!-- CONTACTS -->
    <div id="contacts" class="section contacts">
        <h2>Contact Us</h2>
        <p>📧 Email: 302695@deped.gov.ph</p>
        <p>📱 Phone: (676) 767 6767</p>
        <p>📍 Yap Quiña Street, Barangay V, Victorias City, Negros Occidental</p>
    </div>

    <!-- SCHOOL HYMN -->
    <div id="hymn" class="section hymn">
        <h2>Victorias Hymn</h2>
        <video src="/storage/emulated/0/vnhs/Victorias hymn.mp4" controls></video>
    </div>

</div>

<script>
    function showSection(id) {
        var sections = document.querySelectorAll(".section");
        sections.forEach(section => section.classList.remove("show"));
        document.getElementById(id).classList.add("show");
    }
</script>
</body>
</html>
