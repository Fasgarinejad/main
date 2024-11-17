<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <title>Fatemeh Asgarinejad Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            height: 100vh;
            background-color: #ffffff;
        }

        .container {
            display: flex;
            width: 100%;
        }

        .column {
            padding: 20px;
            box-sizing: border-box;
        }

        .left-column {
            flex: 1;
            text-align: center;
        }

        .left-column img {
            max-width: 100%;
            height: auto;
        }

        .right-column {
            flex: 2;
            padding-left: 40px;
        }

        .right-column p {
            margin: 0;
            font-size: 16px;
            line-height: 1.5;
        }

        h3.section-heading {
            font-size: 18px;
            font-weight: bold;
            border-bottom: 2px solid #0073e6;
            padding-bottom: 5px;
            margin-bottom: 10px;
        }

        h4.university-heading {
            font-size: 18px;
            font-weight: bold;
        }

        ul {
            list-style-type: none;
            padding-left: 0;
        }

        li::before {
            content: "•";
            color: #0073e6;
            font-size: 20px;
            margin-right: 10px;
        }

        .violet-box {
            background-color: #f0fff0;
            color: black;
            padding: 8px 12px;
            border-radius: 5px;
            font-size: 16px;
            margin: 10px 0;
            text-align: left;
            max-width: 90%;
            word-wrap: break-word;
        }

        .links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .links a {
            color: #0073e6;
            text-decoration: none;
            margin: 0 10px;
            font-size: 24px;
        }

        .links a:hover {
            color: #0056b3;
        }
    </style>
</head>

<body>
    <div class="container">
        <!-- Left Column -->
        <div class="column left-column">
            <img src="IMG_0739.JPG" alt="Fatemeh Asgarinejad">
            <div class="links">
                <a href="https://www.linkedin.com/in/fatemeh-asgarinejad/" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
                <a href="https://github.com/Fasgarinejad" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
                <a href="mailto:fasgarinejad@ucsd.edu" title="Email"><i class="fas fa-envelope"></i></a>
                <a href="https://www.youtube.com/@fatemehasgarinejad" target="_blank" title="YouTube"><i class="fab fa-youtube"></i></a>
                <a href="https://scholar.google.com/citations?user=UjbstjkAAAAJ&hl=en" target="_blank" title="Google Scholar"><i class="fas fa-book"></i></a>
            </div>
            <img src="image2.png" alt="Second Image" style="max-width: 100%; height: auto; margin-top: 20px;">
        </div>

        <!-- Right Column -->
        <div class="column right-column">
            <p>
                Hi! 👋 I'm Fatemeh ("Faa-teh-meh") Asgarinejad, a fifth-year Ph.D. candidate at the Electrical and Computer Engineering department at the University of California, San Diego (joint with San Diego State University). I work on Hyperdimensional Computing Security and synergy of Hyperdimensional Computing and Machine Learning under the supervision of <a href="https://cseweb.ucsd.edu/~trosing/">Prof. Tajana Rosing</a> and <a href="https://aksanli.sdsu.edu/">Prof. Baris Aksanli</a>.
            </p>
            <div class="violet-box">
                I am currently on the academic job market for faculty positions with a focus on <strong>teaching</strong>.
            </div>
            <h3 class="section-heading">Teaching</h3>
            <h4 class="university-heading">University of California, San Diego</h4>
            <ul>
                <li><strong>Instructor:</strong> CSE 20: Discrete Mathematics (Summer 2024). Recommendation: <strong>92.3%</strong></li>
                <li><strong>Teaching Assistant:</strong>
                    <ul>
                        <li>CSE 101: Design and Analysis of Algorithms (Summer 2023)</li>
                        <li>CSE 20: Discrete Mathematics (Various Terms)</li>
                        <li>CSE 21: Mathematics for Algorithms and Systems Analysis</li>
                    </ul>
                </li>
            </ul>

            <h4 class="university-heading">Other Teaching Roles</h4>
            <ul>
                <li><strong>Halıcıoğlu Data Science Institute:</strong> Teaching Assistant for DSC 200 and DSC 40A</li>
                <li><strong>San Diego State University:</strong> Instructor for First Year Seminars</li>
                <li><strong>UCSD Extension:</strong> Teaching Assistant for Machine Learning Fundamentals</li>
            </ul>

            <h3 class="section-heading">Publications</h3>
            <ul>
                <li><strong>F. Asgarinejad</strong>, et al., “HDXpose: Harnessing Hyperdimensional Computing’s Explainability for Adversarial Attacks”, ICCAD, 2024.</li>
                <li><strong>F. Asgarinejad</strong>, et al., “VisionHD: Revisiting Hyperdimensional Computing for Image Classification”, ISLPED, 2024.</li>
                <!-- Add more publications as needed -->
            </ul>

            <h3 class="section-heading">Awards</h3>
            <ul>
                <li>DAC’61 Young Fellow Best Video Presentation Award, 2024</li>
                <li>UCSD travel grant, 2024</li>
                <!-- Add more awards as needed -->
            </ul>
        </div>
    </div>
</body>

</html>
