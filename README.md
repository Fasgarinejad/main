<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Fatemeh Asgarinejad — Assistant Professor of Teaching, UCR</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #fff; color: #222; text-align: justify; }
    header { background-color: #ffffff; padding: 20px; display: flex; justify-content: space-between; align-items: center; }
    #name { font-size: 24px; font-weight: bold; }
    #title { font-size: 14px; color: #666; }
    .contact { text-align: justify; font-size: 14px; }
    .ucr-logo { height: 50px; margin-left: 15px; }

    .tabs { display: flex; justify-content: center; background-color: #003DA5; }
    .tabs button { background-color: #003DA5; color: white; border: none; padding: 14px 20px; cursor: pointer; font-size: 16px; font-weight: bold; }
    .tabs button:hover, .tabs button.active { background-color: #FFCC00; color: #003DA5; }
    .tab-content { display: none; max-width: 900px; margin: auto; padding: 2rem; }
    .tab-content.active { display: block; }

    /* About page layout */
    .about-container { display: flex; gap: 40px; align-items: flex-start; }
    .about-left { flex: 1; text-align: center; }
    .about-right { flex: 2; }
    .about-left img { max-width: 100%; height: auto; border-radius: 10px; }

    /* Links styling */
    .links { color: #0076C2; display: flex; justify-content: center; flex-wrap: wrap; margin-top: 20px; }
    .links a { color: #005A91; text-decoration: none; margin: 0 10px; font-size: 24px; }
    .links a:hover { color: #0056b3; }

    /* News box */
    .violet-box { background-color: #f0fff0; color: black; padding: 12px 16px; border-radius: 8px; font-size: 16px; margin: 20px 0; max-width: 100%; word-wrap: break-word; }

    /* University headings */
    .university-heading { font-size: 18px; margin-top: 15px; font-weight: bold; color: #333; }
    .university-heading.current { color: #003DA5; font-size: 1.2em; font-weight: bold; }
    .university-heading.ucsd { color: #00629B; }
    .university-heading.sdsu { color: #CC0000; }

    /* Section headings */
    .section-heading { font-size: 18px; font-weight: bold; border-bottom: 2px solid #0073e6; padding-bottom: 5px; margin-bottom: 15px; margin-top: 25px; }

    /* Lists */
    ul { list-style-type: none; padding-left: 0; }
    li::before { content: "•"; color: #0073e6; font-size: 16px; margin-right: 8px; }
    li { margin-bottom: 8px; }

    /* Divider */
    .hr-with-icon { display: flex; align-items: center; text-align: center; margin: 20px 0; }
    .hr-with-icon::before, .hr-with-icon::after { content: ''; flex: 1; border-bottom: 2px solid #ccc; }
    .hr-with-icon i { margin: 0 10px; color: #333; }

    /* Legacy link pill */
    .v-box { background: linear-gradient(135deg, rgba(243, 229, 0, 0.5) 30%, rgba(0, 198, 215, 0.5) 80%); color: black; padding: 6px 10px; border-radius: 5px; text-decoration: none; display: inline-block; margin: 2px 0; }
    .v-box:hover { background: linear-gradient(135deg, rgba(243, 229, 0, 0.7) 30%, rgba(0, 198, 215, 0.7) 80%); }

    /* === New: Course Cards (cooler than simple pills) === */
    .course-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 16px; margin-top: 12px; }

    .course-card { position: relative; border-radius: 18px; padding: 18px; color: #0d1b2a; overflow: hidden; background: #ffffff; border: 1px solid rgba(0,0,0,0.08); box-shadow: 0 8px 20px rgba(0,0,0,0.06);
      transition: transform .2s ease, box-shadow .2s ease; }

    /* Animated gradient ring */
    .course-card::before { content: ""; position: absolute; inset: -2px; z-index: 0; border-radius: 20px; padding: 2px; background: conic-gradient(from 180deg, #003DA5, #00C6D7, #FFCC00, #003DA5); -webkit-mask: linear-gradient(#000 0 0) content-box, linear-gradient(#000 0 0); -webkit-mask-composite: xor; mask-composite: exclude; opacity: .7; animation: spin 6s linear infinite; }

    @keyframes spin { to { transform: rotate(1turn); } }

    .course-card .inner { position: relative; z-index: 1; background: #ffffff; border-radius: 14px; padding: 12px; }

    .course-header { display: flex; align-items: center; gap: 10px; }
    .course-icon { font-size: 24px; color: #003DA5; }
    .course-code { font-weight: 800; font-size: 18px; color: #003DA5; letter-spacing: .3px; }
    .course-title { font-size: 14px; color: #333; }

    .badge { position: absolute; right: 14px; top: 14px; background: #003DA5; color: #fff; font-size: 12px; padding: 4px 10px; border-radius: 999px; box-shadow: 0 2px 8px rgba(0,0,0,.15); }

    .meta { display: flex; gap: 8px; flex-wrap: wrap; margin-top: 10px; }
    .chip { font-size: 12px; padding: 4px 8px; border-radius: 999px; background: rgba(0,61,165,.08); color: #003DA5; border: 1px solid rgba(0,61,165,.15); }

    .actions { margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap; }
    .btn-link { text-decoration: none; font-weight: 600; font-size: 13px; padding: 8px 10px; border-radius: 10px; border: 1px solid rgba(0,0,0,.1); }
    .btn-link.primary { background: linear-gradient(135deg,#FFCC00,#00C6D7); color: #0d1b2a; border: none; }
    .btn-link.secondary { background: #f6f8ff; color: #003DA5; }

    .course-card:hover { transform: translateY(-2px); box-shadow: 0 12px 26px rgba(0,0,0,0.1); }

    @media (max-width: 768px) {
      .about-container { flex-direction: column; }
      .about-left, .about-right { flex: 1; }
    }

    a {
    color: #0076C2;
    text-decoration: none;
    }

    a:hover {
      color: #005A91;
      text-decoration: underline;
    }
  </style>
</head>
<body>
<header>
  <div style="display:flex; align-items:center;">
    <div>
      <div id="name">Fatemeh Asgarinejad</div>
      <div id="title">Assistant Professor of Teaching — Department of Electrical & Computer Engineering @ UC Riverside</div>
    </div>
  </div>
  
  <div style="display:flex; align-items:center;">
    <img src="ucr-logo.png" alt="UCR Logo" style="height: 60px; margin: 0 20px;">
  </div>
  
  <div class="contact">
    office: tbd<br>
    email: fatemeh.asgarinejad1@ucr.edu
  </div>
</header>

  <div class="tabs">
    <button class="active" data-tab="about">About</button>
    <button data-tab="teaching">Teaching</button>
    <button data-tab="awards">Awards</button>
    <button data-tab="publications">Research and Publications</button>
    <button data-tab="outreach">Outreach / Service</button>
    <button data-tab="talks">Talks</button>
  </div>

  <div id="about" class="tab-content active">
    <div class="about-container">
      <div class="about-left">
        <img src="IMG_0739.JPG" alt="Fatemeh Asgarinejad">
        <div class="links">
          <a href="https://www.linkedin.com/in/fatemeh-asgarinejad/" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
          <a href="https://github.com/Fasgarinejad" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
          <a href="mailto:fasga001@ucr.edu" title="Email"><i class="fas fa-envelope"></i></a>
          <a href="https://www.youtube.com/@fatemehasgarinejad" target="_blank" title="YouTube"><i class="fab fa-youtube"></i></a>
<a href="https://scholar.google.com/citations?user=UjbstjkAAAAJ&hl=en" target="_blank" title="Google Scholar"><img src="https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1/svg/google-scholar.svg" alt="Google Scholar" style="width: 24px; height: auto;"></a>        </div>
        <img src="image2.png" alt="Second Image" style="max-width: 100%; height: auto; margin-top: 20px;">
      </div>

      <div class="about-right">
      <p>Hi! 👋 I'm Fatemeh (“Faa-teh-meh”) Asgarinejad. Starting Fall 2025, I’ll be an Assistant Professor of Teaching in <a href="https://www.ee.ucr.edu/">Electrical and Computer Engineering Department</a> at <a href="https://www.ucr.edu/">University of California Riverside</a> :). My research explores the intersection of CS and ECE education—centering engaged, continuous learning—and uses machine learning, data science and mathematics to solve real-world problems.</p>

        <p>Previously, I received my Ph.D. from the <a href="https://ucsd.edu/">University of California San Diego</a>, where I had the privilege of being advised by Professors <a href="https://cseweb.ucsd.edu/~trosing/">Tajana Rosing</a> and <a href="https://aksanli.sdsu.edu/">Baris Aksanli</a> (joint with San Diego State University). During my Ph.D., I worked on Secure, Efficient and Private Computing at the Edge with Hyperdimensional Computing, and explored its synergy with Machine Learning. I am honored to have received the <a href="https://senate.ucsd.edu/grants-awards/senate-awards/distinguished-teaching-award">2025 Barbara J. and Paul D. Saltman Excellent Teaching Award from UC San Diego</a>, as well as the <a href="https://cse.ucsd.edu/graduate/cse-department-awards">2025 Excellence in Teaching Award from the UCSD Computer Science and Engineering Department</a>.</p>

        <p><strong>Collaborations</strong>: If you are interested in collaborating with me, please contact me at <a href="mailto:fasga001@ucr.edu">fatemeh.asgarinejad1@ucr.edu</a></p>

        <div class="violet-box">
          <strong>News</strong>:<br>
          <span style="color:#C69214;">July 2025:</span> My recent work in HD Computing was recognized as one of the two top achievements in the Cocosys Spring Quarter Review.<br>
          <span style="color:#C69214;">May 2025:</span> I won the UCSD CSE Department Award for Excellence in Teaching<br>
          <span style="color:#C69214;">May 2025:</span> Defended my PhD!<br>
          <span style="color:#C69214;">May 2025:</span> Poster accepted in Mathematics Association of America MathFest.<br>
          <span style="color:#C69214;">April 2025:</span> I won the <strong>UCSD 2025 Barbara J. and Paul D. Saltman Excellent Teaching Award</strong>!
        </div>
      </div>
    </div>
  </div>

  <div id="teaching" class="tab-content">
    <!-- University of California, Riverside -->
    <h4 class="university-heading current">University of California, Riverside</h4>
    <ul>
      <strong>Instructor</strong>, Electrical and Computer Engineering
      <ul>
        <li><strong style="color: #00629B;">EE 5</strong>: Circuits and Electronics (Fall 2025)</li>
        <li><strong style="color: #FDB515;">EE 16</strong>: Data Analysis for Engineering Applications (Fall 2025)</li>
      </ul>
    </ul>

    <!-- New cool course cards for EE 05 and EE 101 -->
    <div class="course-grid" aria-label="UCR Fall 2025 Courses">
      <div class="course-card">
        <span class="badge">Fall 2025</span>
        <div class="inner">
          <div class="course-header">
            <i class="fa-solid fa-bolt course-icon" aria-hidden="true"></i>
            <div>
              <div class="course-code">EE 05</div>
              <div class="course-title">Circuits & Electronics</div>
            </div>
          </div>
          <!-- <div class="meta">
            <span class="chip">UCR</span>
            <span class="chip">Undergraduate</span>
            <span class="chip">Hands-on labs</span>
          </div> -->
          <div class="actions">
            <a class="btn-link secondary" href="#" aria-disabled="true">Syllabus (TBD)</a>
            <a class="btn-link secondary" href="#" aria-disabled="true">Course Site (TBD)</a>
          </div>
        </div>
      </div>

      <div class="course-card">
        <span class="badge">Fall 2025</span>
        <div class="inner">
          <div class="course-header">
            <i class="fa-solid fa-chart-line course-icon" aria-hidden="true"></i>
            <div>
              <div class="course-code">EE 16</div>
              <div class="course-title">Data Analysis for Engineering Applications</div>
            </div>
          </div>
          <!-- <div class="meta">
            <span class="chip">UCR</span>
            <span class="chip">Undergraduate</span>
            <span class="chip">Real-World-Application-focused</span>
          </div> -->
          <div class="actions">
            <a class="btn-link secondary" href="#" aria-disabled="true">Syllabus (TBD)</a>
            <a class="btn-link secondary" href="#" aria-disabled="true">Course Site (TBD)</a>
          </div>
        </div>
      </div>
    </div>

    <div class="hr-with-icon"><i class="fas fa-graduation-cap"></i></div>

    <!-- University of California, San Diego -->
    <h4 class="university-heading ucsd">University of California, San Diego</h4>
    <ul>
      <strong>Instructor</strong>, Computer Science and Engineering
      <ul>
        <li><a href="CSE20_Summer_2024.html" class="v-box"><strong>CSE 20:</strong> Discrete Mathematics (Summer 2024)</a><a href="https://drive.rle.com/file/d/1BRmIGQutY4DPvpvFwI-xlrVUsYrCOxp1/view?usp=sharing" target="_blank" style="margin-left: 10px;">[Course Syllabus]</a></li>
      </ul>
      <br>
      <strong>Teaching Assistant, Computer Science and Engineering</strong>
      <ul>
        <li><strong>CSE 101:</strong> Design and Analysis of Algorithms (Summer 2023)</li>
        <li><strong>CSE 20:</strong> Discrete Mathematics (Spring 2021, Spring 2022, Summer 2022, Spring 2023, Winter 2023, Winter 2025, Spring 2025)</li>
        <li><strong>CSE 21:</strong> Mathematics for Algorithms and Systems Analysis (Winter, Spring, and Fall 2024)</li>
      </ul>
      <br>
      <strong>Teaching Assistant, Halıcıoğlu Data Science Institute</strong>
      <ul>
        <li><strong>DSC 200:</strong> Data Science Programming (Fall 2023)</li>
        <li><strong>DSC 40A:</strong> Theoretical Foundations of Data Science (Summer 2023)</li>
      </ul>
    </ul>
    <br>

    <!-- San Diego State University -->
    <h4 class="university-heading sdsu">San Diego State University</h4>
    <ul>
      <li><strong>Instructor:</strong> First Year Seminars, four Classes (Fall 2021)</li>
    </ul>
    <br>

    <!-- UC San Diego Extended Studies -->
    <h4 class="university-heading ucsd">UC San Diego Extended Studies</h4>
    <ul>
      <li><strong>Instructor</strong> Fundamentals of Data Science (July 2025)</li>
    </ul>
    <br>

    <!-- UC San Diego Extension -->
    <h4 class="university-heading ucsd">UC San Diego Extension</h4>
    <ul>
      <li><strong>Teaching Assistant:</strong> DSE 220x - Machine Learning Fundamentals (Prof. Sanjoy Dasgupta, Three Semesters Sep 2019 - Aug 2020)</li>
    </ul>
    <br>

    <h4 class="university-heading ucsd">UC San Diego Teaching Certificates</h4>
    <ul>
      <li><strong>UC San Diego Student-Centered College Teaching & Course Design Certificate</strong></li>
      <li><strong>Leadership in Teaching: Graduate Peer Review of Instruction Program Certificate</strong></li>
      <li><strong>Transparency in Learning and Teaching (TILT) Community of Practice Certificate</strong></li>
    </ul>
  </div>

  <div id="publications" class="tab-content">
    <h3 class="section-heading">Publications</h3>
    <ul>
      <li><strong>F. Asgarinejad</strong>, F. Ponzina, O. Gungor, T. Rosing, B. Aksanli, "<a href="https://www.researchgate.net/profile/Onat-Gungor/publication/386284039_HDXpose_Harnessing_Hyperdimensional_Computing's_Explainability_for_Adversarial_Attacks/links/674bc8e63d17281c7deebe28/HDXpose-Harnessing-Hyperdimensional-Computings-Explainability-for-Adversarial-Attacks.pdf">HDXpose: Harnessing Hyperdimensional Computing's Explainability for Adversarial Attacks</a>", ICCAD, 2024. [<a href="https://drive.google.com/file/d/1aFNGfm4ebCrcbrD8ZCvJMOYANDoJ-V0b/view?usp=sharing">slides</a>]</li>
      <li><strong>F. Asgarinejad</strong>, F. Asgarinejad, J. Morris, T. Rosing, B. Aksanli, <a href="https://dl.acm.org/doi/abs/10.1145/3665314.3670852">VisionHD: Revisiting Hyperdimensional Computing for Improved Image Classification</a>, ISLPED, 2024.</li>
      <li>M. Gaddi, F. Ponzina, <strong>F. Asgarinejad</strong>, B. Aksanli, T. Rosing, "<a href="https://ieeexplore.ieee.org/abstract/document/10820450">HyperECG: ECG Signal Inference from Radar with Hyperdimensional Computing</a>", BIBE, 2024.</li>
      <li><strong>F. Asgarinejad</strong>, J. Morris, T. Rosing, B. Aksanli, <a href="https://ieeexplore.ieee.org/abstract/document/10473862">PIONEER: Towards Highly Efficient and Accurate Hyperdimensional Computing using Learned Projection</a>, ASP-DAC, 2024. [<a href="https://drive.google.com/file/d/1UA5_tglLJhhkm3kLhmsZYRfLL5nprNRq/view?usp=sharing">slides</a>]</li>
      <li><strong>F. Asgarinejad</strong>, A. Thomas, R. Hildebrant, Z Zhang, S. Ren. Rosing, B. Aksanli <a href="https://www.mdpi.com/2078-2489/15/8/490">Optimized Early Prediction of Business Processes with Hyperdimensional Computing</a>, MDPI Information, 2024.</li>
      <li><strong>F. Asgarinejad</strong>, X. Yu, D. Jiang, J. Morris, T. Rosing, B. Aksanli, <a href="https://www.mdpi.com/1424-8220/24/3/1014">Enhanced Noise-Resilient Pressure Mat System Based on Hyperdimensional Computing</a>, MDPI Sensors, 2024.</li>
      <li>R. Chandrasecaran, <strong>F. Asgarinejad</strong>, J. Morris, T. Rosing, <a href="https://ieeexplore.ieee.org/abstract/document/10196438">Multi-label classification with Hyperdimensional Representations</a> IEEE ACCESS, 2023.</li>
      <li>X. Yu, M. Zhou, <strong>F. Asgarinejad</strong>, O. Gungor, B. Aksanli, T. Rosing, <a href="https://ieeexplore.ieee.org/abstract/document/10247820">Lightning Talk: Private and Secure Edge AI with Hyperdimensional Computing</a>, DAC, 2023.</li>
      <li>Z. Zhang, R. Hildebrant, <strong>F. Asgarinejad</strong>, N. Venkatasubramanian, S. Ren, <a href="https://ieeexplore.ieee.org/abstract/document/9610661">Improving Process Discovery Results by Filtering Out Outliers from Event Logs with Hidden Markov Models</a>, CBI, 2021.</li>
      <li>R. Garcia, <strong>F. Asgarinejad</strong>, B. Khaleghi, T. Rosing, M. Imani <a href="https://ieeexplore.ieee.org/abstract/document/9474239">TruLook: A Framework for Configurable GPU Approximation</a>, DATE, 2021.</li>
      <li><strong>F. Asgarinejad</strong>, A. Thomas, T. Rosing, <a href="https://ieeexplore.ieee.org/abstract/document/9175328">Detection of Epileptic Seizures from Surface EEG using Hyperdimensional Computing</a>, EMBC, 2020. [<a href="https://drive.google.com/file/d/1G-7ESC-DQj2xH6xuVQStgZYvNy5kauNS/view?usp=sharing">slides</a>], [<a href="https://www.youtube.com/watch?v=ch0Mm9_5cPw">presentation</a>]</li>
      <li>B. Khaleghi, S. Salamat, A. Thomas, <strong>F. Asgarinejad</strong>, Y. Kim, T. Rosing, <a href="https://dl.acm.org/doi/abs/10.1145/3370748.3406587">SHEARer Highly-Efficient Hyperdimensional Computing by Software-Hardware Enabled Multifold Approximation</a>, ISLPED, 2020.</li>
    </ul>

    <h3 class="section-heading">Mentorship</h3>
    <ul>
      <li>Jiaying Yang, B.Sc. student in Computer Science, UCSD, Project: Addressing Catastrophic Forgetting in Neural Networks using Hyperdimensional Computing (to be submitted in Fall 2025). Summer 2024-Summer 2025</li>
      <li>Matilda Gaddi, B.Sc. student in Data Science, UCSD, Project: ECG Signal Inference from Radar with Hyperdimensional Computing (published in IEEE BIBE 2024). Summer 2023-Winter 2025</li>
      <li>A.J. Olivares, B.Sc. student in Computer Science, UCSD, Project: Addressing Catastrophic Forgetting in Neural Networks using Hyperdimensional Computing. Summer 2024</li>
      <li>Amir Kiadi, B.Sc. student in Computer Science, UCSD, Project: Adversarial Attacks in Hypedimensional Computing (submitted to TCAD 2025). Fall 2025-Spring 2025</li>
      <li>Ava Emami, B.Sc. student in Computer Science, UCSD, Project: Defense mechanisms using HDC (to be submitted in Fall 2025). Spring 2025-Fall 2025</li>
      <li>Lilianne Montehermoso, High School student, PRISM Center Research Program, Project: Analyzing Adversarial Attacks in Machine Learning (submitted to journal of students research 2025). Summer 2024-Spring 2025</li>
    </ul>
  </div>

  <div id="talks" class="tab-content">
    <h3 class="section-heading">Invited Talks</h3>
    <ul>
      <li>SRC TECHCON, Research Scholar and Presenter, Sep 2025</li>
      <li>2025 Invited Seminar Series organized by IEEE Computer Society chapter of IEEE San Diego Section, Aug 2025</li>
      <li>Panelist, UCSD SRP Professional Development Forum - Graduate Student Panel (STEM), July 2025</li>
      <li>Panelist, UCSD Teaching and Learning Commons, Summer Teaching Community 2025, June 2025</li>
      <li>University of California Riverside, ECE, Logic Optimization and Multi-Level Minimization, Winter 2025</li>
      <li>Purdue University, CS, Induction and Recursion, Winter 2025</li>
      <li>California State University Long Beach, CECS, Towards Efficient Learning at the Edge by Hyperdimensional Computing, Winter 2025</li>
      <li>University of Texas Austin, CS, Clustering: K-Means, Winter 2025</li>
      <li>University of Texas A&M, CSE, Sorting Algorithms: Merge Sort, Winter 2025</li>
      <li>Chapman University, CS, Simple and Multiple Linear Regression, Winter 2025</li>
      <li>Northwestern University, Statistics and Data Science, Introduction to Hypothesis Testing and its Application in Real-Life and Data Science, Winter 2025</li>
      <li>Panelist, PRISM Center Annual Review, UC San Diego, "PRISM Center Summer Virtual High School Program", Nov 2024</li>
      <li>SRC TECHCON, "Harnessing Hyperdimensional Computing's Explainability for Adversarial Attacks", Sep 2024</li>
      <li>Colegio San Agustin-Bacolod University's 60th Founding Anniversary Research Conference, "Applying Machine Learning and Brain-Inspired Computing for Innovative Problem Solving", July 2023</li>
    </ul>

    <h3 class="section-heading">Conference Talks</h3>
    <ul>
      <li>ICCAD, 2024 [<a href="https://drive.google.com/file/d/1aoMJYb87zvwgYjKihUkDwLyLlLSKWa-a/view?usp=sharing">slides</a>]</li>
      <li>ASP-DAC, 2024 [<a href="https://drive.google.com/file/d/1UA5_tglLJhhkm3kLhmsZYRfLL5nprNRq/view?usp=sharing">slides</a>]</li>
      <li>EMBC, 2020 [<a href="https://drive.google.com/file/d/1G-7ESC-DQj2xH6xuVQStgZYvNy5kauNS/view?usp=sharing">slides</a>] | [<a href="https://www.youtube.com/watch?v=ch0Mm9_5cPw">presentation</a>]</li>
    </ul>
  </div>

  <div id="awards" class="tab-content">
    <ul>
      <li>UCSD CSE Department Award for Excellence in Teaching, 2025</li>
      <li><strong>UCSD 2025 Barbara J. and Paul D. Saltman Excellent Teaching Award</strong></li>
      <li>DAC'61 Young Fellow Best Video Presentation Award, 2024</li>
      <li>DAC Young Fellow at the 61st and 62nd Design Automation Conference in San Francisco, 2024, 2025</li>
      <li>SRC Research Scholar and awarded funding for conference participation, 2024, 2025</li>
      <li>UCSD travel grant, 2024</li>
      <li>Member of HKN (Eta Kappa Nu) Honor Society of UC San Diego since May 2022</li>
      <li>Ranked 20th (top 0.1%) in Iran's national university entrance exam for M.Sc. in Computer Science, 2017</li>
      <li>Ranked top 0.4% in Iran's national university entrance exam for M.Sc. in Computer Engineering, 2017</li>
      <!-- <li>Ranked top 0.9% and top 3.4% nationwide in Iran’s national university entrance exams for B.Sc. programs in Foreign Languages and Mathematics, respectively, 2012</li> -->

    </ul>
  </div>

  <div id="outreach" class="tab-content">
    <h3 class="section-heading">Belonging, Diversity and Equity</h3>
    <ul>
      <li>Research Mentor (at UC San Diego, <a href="https://seelab.ucsd.edu/index.html">SEElab</a> August 2023 - Summer 2025</li>
      <li><a href="https://ucsdwic.github.io/">Women In Computing Mentorship Program (at UC San Diego)</a>, Fall 2024 - Winter 2025</li>
      <li>Research Mentor (at UC San Diego, PRISM Center), <a href=https://cse.ucsd.edu/about/news/prisms-summer-outreach-program-introduces-high-school-students-world-scientific-research">Virtual High School Research Program for high school students</a>, Summer 2024</li>
      <li><a href="https://hkn.ucsd.edu/">HKN (Eta Kappa Nu) Honor Society of UC San Diego</a> Outreach Program for middle-school and High-school students</li>
      <li><a href=https://www.learn-python.ir/">Algorithmic Creativity and Python Programming Summer School Mentor (at Sharif University of Technology)</a>, under supervision of Prof. Ali Sharifi-Zarchi, Summer 2023 (in Persian)</li>
    </ul>

    <h3 class="section-heading">Professional Service</h3>
    <ul>
      <li>Panel Moderator at the UCSD 2025 Undergraduate Summer Research Conference</li>
      <li>Reviewer for ACM Computing Surveys</li>
      <li>Student Activities Chair for IEEE San Diego Section, summer 2025 - present</li>
    </ul>

  </div>

  <script>
    const buttons = document.querySelectorAll('.tabs button');
    const contents = document.querySelectorAll('.tab-content');

    buttons.forEach(button => {
      button.addEventListener('click', () => {
        buttons.forEach(b => b.classList.remove('active'));
        contents.forEach(c => c.classList.remove('active'));
        button.classList.add('active');
        document.getElementById(button.dataset.tab).classList.add('active');
      });
    });
  </script>
</body>
</html>
