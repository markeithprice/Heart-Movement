<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Movement - Exercise Guide</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #111827;
            --sidebar-bg: #1f2937;
            --main-bg: #111827;
            --text-color: #e5e7eb;
            --text-muted: #9ca3af;
            --accent-color: #38bdf8;
            --border-color: #374151;
            --details-bg: #1f2937;
            --details-open-bg: #374151;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            overflow-x: hidden;
        }

        .main-layout {
            display: flex;
            min-height: 100vh;
        }

        #sidebar {
            width: 280px;
            background-color: var(--sidebar-bg);
            padding: 2rem 1rem;
            position: fixed;
            height: 100%;
            overflow-y: auto;
            border-right: 1px solid var(--border-color);
        }

        #sidebar h1 {
            font-size: 1.8rem;
            font-weight: 700;
            color: #fff;
            text-align: center;
            margin-bottom: 0.25rem;
            letter-spacing: -0.025em;
        }
        
        #sidebar .guide-subtitle {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--text-color);
            text-align: center;
            margin-bottom: 0.5rem;
        }

        #sidebar .byline {
            font-size: 0.875rem;
            font-weight: 400;
            color: var(--text-muted);
            text-align: center;
            margin-bottom: 2rem;
        }

        #sidebar .nav-link {
            display: block;
            padding: 0.75rem 1rem;
            border-radius: 0.5rem;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.2s, color 0.2s;
            margin-bottom: 0.5rem;
        }

        #sidebar .nav-link:hover {
            background-color: var(--border-color);
        }

        #sidebar .nav-link.active {
            background-color: var(--accent-color);
            color: var(--bg-color);
        }

        #main-content {
            margin-left: 280px;
            padding: 2rem 3rem;
            width: calc(100% - 280px);
        }

        #main-content h2 {
            font-size: 2.25rem;
            font-weight: 700;
            color: #fff;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid var(--border-color);
        }

        .exercise-section {
            display: none;
        }

        .exercise-section.active {
            display: block;
        }

        details {
            background-color: var(--details-bg);
            border-radius: 0.5rem;
            margin-bottom: 1rem;
            transition: background-color 0.2s ease-in-out;
        }

        details[open] {
            background-color: var(--details-open-bg);
        }

        summary {
            font-size: 1.125rem;
            font-weight: 600;
            padding: 1rem 1.5rem;
            cursor: pointer;
            outline: none;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        summary::-webkit-details-marker {
            display: none;
        }

        summary::after {
            content: '+';
            font-size: 1.5rem;
            transition: transform 0.2s ease-in-out;
        }

        details[open] summary::after {
            content: '−';
        }

        .details-content {
            padding: 0 1.5rem 1.5rem 1.5rem;
            line-height: 1.6;
            color: var(--text-muted);
        }
        
        .details-content p {
            margin-bottom: 1rem;
        }

        .details-content strong {
            color: #93c5fd;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .main-layout {
                flex-direction: column;
            }
            #sidebar {
                position: relative;
                width: 100%;
                height: auto;
                border-right: none;
                border-bottom: 1px solid var(--border-color);
            }
            #main-content {
                margin-left: 0;
                width: 100%;
                padding: 2rem 1.5rem;
            }
        }

    </style>
</head>
<body>

    <div class="main-layout">
        <!-- Sidebar -->
        <aside id="sidebar">
            <h1>Heart Movement</h1>
            <p class="guide-subtitle">Exercise Guide</p>
            <p class="byline">By Heart Motivation and Markeith Price</p>
            <nav id="category-nav">
                <a class="nav-link active" data-target="olympic-lifting">Olympic Lifting</a>
                <a class="nav-link" data-target="powerlifting">Powerlifting</a>
                <a class="nav-link" data-target="strongman">Strongman</a>
                <a class="nav-link" data-target="pilates">Pilates</a>
                <a class="nav-link" data-target="yoga">Yoga</a>
                <a class="nav-link" data-target="animal-flow">Animal Flow</a>
                <a class="nav-link" data-target="loaded-carries">Loaded Carries</a>
                <a class="nav-link" data-target="functional-training">Functional Training</a>
            </nav>
        </aside>

        <!-- Main Content -->
        <main id="main-content">
            <!-- Olympic Lifting Section -->
            <section id="olympic-lifting" class="exercise-section active">
                <h2>Olympic Lifting</h2>
                <!-- Details elements for Olympic Lifting -->
                <details>
                    <summary>Snatch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A single, explosive movement where a barbell is lifted from the floor to an overhead position. The lifter pulls the bar as high as possible and drops under it into a deep overhead squat, then stands up.</p>
                        <p><strong>Benefits:</strong> Develops total body power, speed, coordination, and mobility. Engages nearly every muscle group, particularly the posterior chain, shoulders, and core.</p>
                    </div>
                </details>
                <details>
                    <summary>Clean and Jerk</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A two-part lift. First, the 'clean' moves the barbell from the floor to a racked position on the shoulders. Second, the 'jerk' moves the bar from the shoulders to an overhead position.</p>
                        <p><strong>Benefits:</strong> Builds incredible strength and power. Excellent for developing leg drive, shoulder stability, and overall athletic performance.</p>
                    </div>
                </details>
                <details>
                    <summary>Power Snatch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A variation of the snatch where the barbell is caught in a partial or quarter-squat position, rather than a full deep squat. Requires more explosive pulling power.</p>
                        <p><strong>Benefits:</strong> Excellent for developing explosive power and speed without the same mobility demands as a full snatch. Great for athletes in sports requiring quick bursts of energy.</p>
                    </div>
                </details>
                <details>
                    <summary>Power Clean</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A variation of the clean where the barbell is caught on the shoulders in a quarter-squat position. It emphasizes explosive pulling strength.</p>
                        <p><strong>Benefits:</strong> Builds explosive power in the hips and legs, improves coordination, and strengthens the upper back and shoulders. Widely used in athletic training.</p>
                    </div>
                </details>
                <details>
                    <summary>Hang Snatch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A snatch variation where the lift starts with the barbell "hanging" from the hands, typically at mid-thigh or knee level, instead of from the floor.</p>
                        <p><strong>Benefits:</strong> Helps to isolate and strengthen the second pull of the snatch, improving power and technique for the full lift. Reduces stress on the lower back.</p>
                    </div>
                </details>
                <details>
                    <summary>Hang Clean</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A clean variation where the lift starts with the barbell "hanging" from the hands, usually above the knees.</p>
                        <p><strong>Benefits:</strong> Focuses on developing explosive hip extension and speed in the second pull of the clean. A great teaching tool for beginners.</p>
                    </div>
                </details>
                <details>
                    <summary>Snatch Balance</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An assistance exercise where the lifter starts with the barbell on their back, then quickly drops under it into an overhead squat, catching it in the snatch receiving position.</p>
                        <p><strong>Benefits:</strong> Builds speed, confidence, and stability in the receiving portion of the snatch. Improves overhead squat strength and mobility.</p>
                    </div>
                </details>
                <details>
                    <summary>Overhead Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A squat performed while holding a barbell locked out overhead with a wide grip.</p>
                        <p><strong>Benefits:</strong> Develops exceptional core strength, shoulder stability, and mobility in the hips, ankles, and thoracic spine. A cornerstone of the snatch.</p>
                    </div>
                </details>
                <details>
                    <summary>Jerk</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The second part of the clean and jerk. The lifter dips and drives the barbell from the shoulders overhead, often splitting the legs into a lunge to receive the bar.</p>
                        <p><strong>Benefits:</strong> Develops powerful leg drive, upper body pressing strength, and total-body coordination. Allows lifters to move maximal weights overhead.</p>
                    </div>
                </details>
                <details>
                    <summary>Push Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An overhead press that uses a dip and drive from the legs to help propel the barbell upward. The legs do not re-bend to catch the bar.</p>
                        <p><strong>Benefits:</strong> Builds overhead pressing strength and power. Teaches the coordination of using leg drive to assist the upper body.</p>
                    </div>
                </details>
                <details>
                    <summary>Snatch Pull</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The first portion of the snatch, where the lifter explosively pulls the barbell from the floor to as high as possible without dropping underneath it.</p>
                        <p><strong>Benefits:</strong> Strengthens the pulling muscles (back, traps, legs) and reinforces the correct bar path for the snatch. Allows for overloading the pull.</p>
                    </div>
                </details>
                <details>
                    <summary>Clean Pull</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The pulling portion of the clean. The lifter explosively pulls the barbell from the floor to the upper chest level without racking it on the shoulders.</p>
                        <p><strong>Benefits:</strong> Builds immense pulling strength and power from the floor. Reinforces the powerful triple extension (ankles, knees, hips) needed for the clean.</p>
                    </div>
                </details>
                <details>
                    <summary>Muscle Snatch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A snatch variation performed with a narrower grip and without re-bending the knees. The bar is pulled and pressed into the overhead position in one continuous motion.</p>
                        <p><strong>Benefits:</strong> Builds upper body strength and reinforces a high, close bar path. Excellent for warm-ups and technique work with lighter weights.</p>
                    </div>
                </details>
                <details>
                    <summary>Tall Snatch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Starting from a standing position with the bar on the back, the lifter quickly drops into an overhead squat without any initial dip or drive.</p>
                        <p><strong>Benefits:</strong> Improves the speed and accuracy of the third pull (the pull under the bar). Develops confidence and stability in the catch position.</p>
                    </div>
                </details>
                <details>
                    <summary>Tall Clean</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The lifter starts standing tall with the bar at arm's length, then pulls themselves under the bar into the front rack position without any initial dip.</p>
                        <p><strong>Benefits:</strong> Teaches an aggressive and fast pull-under for the clean, improving turnover speed and a solid receiving position.</p>
                    </div>
                </details>
            </section>

            <!-- Powerlifting Section -->
            <section id="powerlifting" class="exercise-section">
                <h2>Powerlifting</h2>
                <!-- Details elements for Powerlifting -->
                <details>
                    <summary>Barbell Back Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> With a barbell resting on the upper back, the lifter squats down until the hip crease is below the knee, then stands back up.</p>
                        <p><strong>Benefits:</strong> Considered the "king" of exercises for building lower body strength, muscle mass, and bone density. Strengthens the quads, glutes, hamstrings, and core.</p>
                    </div>
                </details>
                <details>
                    <summary>Barbell Bench Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on a bench, the lifter lowers a barbell to their chest, pauses, and then presses it back up to full arm extension.</p>
                        <p><strong>Benefits:</strong> The primary exercise for developing upper body pushing strength. Builds the chest, shoulders (deltoids), and triceps.</p>
                    </div>
                </details>
                <details>
                    <summary>Conventional Deadlift</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lifting a loaded barbell from the floor until standing fully erect with locked hips and knees. The grip is outside the knees, and the stance is about hip-width.</p>
                        <p><strong>Benefits:</strong> Builds raw, total-body strength, particularly in the posterior chain (glutes, hamstrings, entire back). Improves grip strength and core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Sumo Deadlift</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A deadlift variation with a very wide stance and a grip inside the knees. The torso remains more upright compared to the conventional deadlift.</p>
                        <p><strong>Benefits:</strong> Emphasizes the hips, glutes, and quads more than the conventional style. Can be a better option for lifters with certain body types or back issues.</p>
                    </div>
                </details>
                <details>
                    <summary>Front Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A squat performed with the barbell resting across the front of the shoulders (front rack position). This forces a more upright torso.</p>
                        <p><strong>Benefits:</strong> Heavily targets the quadriceps and upper back. Builds tremendous core strength and is a great assistance lift for the clean.</p>
                    </div>
                </details>
                <details>
                    <summary>Pause Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A standard squat with a deliberate pause (1-3 seconds) at the bottom of the movement before ascending.</p>
                        <p><strong>Benefits:</strong> Eliminates the stretch reflex, building raw strength out of the "hole". Improves stability, control, and positional awareness at the bottom of the squat.</p>
                    </div>
                </details>
                <details>
                    <summary>Box Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Squatting down until seated on a box set to a specific height, then exploding back up to a standing position.</p>
                        <p><strong>Benefits:</strong> Teaches a strong posterior chain engagement (hips and glutes). Builds explosive strength and allows for consistent depth.</p>
                    </div>
                </details>
                <details>
                    <summary>Incline Bench Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A bench press performed on a bench set at an incline (typically 30-45 degrees).</p>
                        <p><strong>Benefits:</strong> Emphasizes the upper portion of the pectoral muscles and the anterior deltoids (front of the shoulders).</p>
                    </div>
                </details>
                <details>
                    <summary>Decline Bench Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A bench press performed on a bench set at a decline.</p>
                        <p><strong>Benefits:</strong> Targets the lower portion of the pectoral muscles. Often allows lifters to move more weight than a flat or incline press.</p>
                    </div>
                </details>
                 <details>
                    <summary>Close Grip Bench Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A bench press performed with the hands closer together on the bar, typically shoulder-width or slightly inside.</p>
                        <p><strong>Benefits:</strong> Places a greater emphasis on the triceps and inner chest. A key accessory movement for building a stronger bench press lockout.</p>
                    </div>
                </details>
                <details>
                    <summary>Board Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A bench press variation where the lifter lowers the bar to a wooden board (or several) placed on their chest, reducing the range of motion.</p>
                        <p><strong>Benefits:</strong> Allows for overloading specific portions of the lift, particularly the lockout. Helps to strengthen sticking points in the bench press.</p>
                    </div>
                </details>
                <details>
                    <summary>Romanian Deadlift</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A deadlift variation focusing on the hip hinge. The lifter starts from a standing position, lowering the bar by pushing the hips back while maintaining a slight bend in the knees.</p>
                        <p><strong>Benefits:</strong> Excellent for developing the hamstrings and glutes. Improves hip mobility and strengthens the lower back.</p>
                    </div>
                </details>
                <details>
                    <summary>Stiff-Legged Deadlift</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Similar to the Romanian Deadlift but often performed from the floor with minimal knee bend (but not locked knees), placing a greater stretch on the hamstrings.</p>
                        <p><strong>Benefits:</strong> Provides an intense stretch and strengthens the hamstrings, glutes, and lower back.</p>
                    </div>
                </details>
                <details>
                    <summary>Deficit Deadlift</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A deadlift performed while standing on a low platform or plate, which increases the range of motion.</p>
                        <p><strong>Benefits:</strong> Builds tremendous strength off the floor by making the initial pull harder. Increases leg drive and overall pulling power.</p>
                    </div>
                </details>
                <details>
                    <summary>Rack Pulls</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A deadlift performed with a limited range of motion, starting with the bar elevated on the safety pins of a power rack (usually at or below the knee).</p>
                        <p><strong>Benefits:</strong> Allows the lifter to handle supramaximal weights to overload the upper back, traps, and grip. Strengthens the top portion of the deadlift.</p>
                    </div>
                </details>
                <details>
                    <summary>Good Mornings</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> With a barbell on the back, the lifter performs a hip hinge, bending forward with a straight back and then returning to an upright position.</p>
                        <p><strong>Benefits:</strong> A powerful accessory exercise for strengthening the entire posterior chain: hamstrings, glutes, and spinal erectors.</p>
                    </div>
                </details>
                <details>
                    <summary>Glute-Ham Raise</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Performed on a Glute-Ham Developer (GHD) machine, the lifter kneels and lowers their torso towards the floor, then raises it back up using their hamstrings and glutes.</p>
                        <p><strong>Benefits:</strong> One of the best exercises for isolating and strengthening the hamstrings and glutes. Improves knee and hip stability.</p>
                    </div>
                </details>
            </section>

            <!-- Strongman Section -->
            <section id="strongman" class="exercise-section">
                <h2>Strongman</h2>
                <!-- Details elements for Strongman -->
                <details>
                    <summary>Atlas Stone Load</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The quintessential strongman event. A heavy, spherical stone is lifted from the ground, lapped, and then loaded onto a platform.</p>
                        <p><strong>Benefits:</strong> Develops raw, full-body strength, particularly in the posterior chain, back, and biceps. Builds immense core and grip strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Yoke Walk</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Carrying a heavy frame (yoke) across the shoulders for a set distance as quickly as possible.</p>
                        <p><strong>Benefits:</strong> Builds incredible core stability, leg strength, and mental toughness. Simulates carrying heavy, awkward loads.</p>
                    </div>
                </details>
                <details>
                    <summary>Farmer's Walk</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Walking for a set distance while carrying a heavy weight in each hand.</p>
                        <p><strong>Benefits:</strong> Develops phenomenal grip strength, upper back strength, and core stability. A fantastic full-body conditioning tool.</p>
                    </div>
                </details>
                <details>
                    <summary>Log Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lifting a specialized "log" bar from the floor to the chest, then pressing it overhead. The neutral grip is easier on the shoulders than a standard barbell.</p>
                        <p><strong>Benefits:</strong> Builds explosive overhead pressing power and full-body strength. The awkward nature of the log challenges stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Axle Bar Clean and Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A clean and press performed with a thick (axle) bar, which does not rotate. This makes the clean and the press significantly harder.</p>
                        <p><strong>Benefits:</strong> Builds tremendous grip and wrist strength. The lack of rotation requires more raw power to complete the lift.</p>
                    </div>
                </details>
                <details>
                    <summary>Tire Flip</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Flipping a very large, heavy tire end-over-end for a set distance.</p>
                        <p><strong>Benefits:</strong> A full-body power exercise that develops the posterior chain, chest, and arms. Excellent for conditioning and building explosive strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Sled Drag</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pulling a weighted sled, usually by walking backward while holding straps or a rope.</p>
                        <p><strong>Benefits:</strong> A fantastic, low-impact way to build leg strength (especially quads) and improve conditioning without heavy eccentric loading.</p>
                    </div>
                </details>
                <details>
                    <summary>Sled Push</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pushing a weighted sled across the floor for a set distance.</p>
                        <p><strong>Benefits:</strong> Builds leg drive, power, and cardiovascular endurance. A great tool for metabolic conditioning.</p>
                    </div>
                </details>
                <details>
                    <summary>Keg Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Carrying a keg, typically held in front of the body, for a set distance.</p>
                        <p><strong>Benefits:</strong> The shifting weight of the liquid inside the keg challenges core stability and grip in a unique way. Builds functional, real-world strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Sandbag Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Carrying a heavy sandbag, often bear-hugged to the chest or thrown over a shoulder, for a set distance.</p>
                        <p><strong>Benefits:</strong> The shifting, unstable nature of the sandbag builds immense core strength, grip, and mental fortitude.</p>
                    </div>
                </details>
                <details>
                    <summary>Car Deadlift</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A deadlift performed using a specialized frame that lifts the back end of a car. The lift is typically a partial range of motion.</p>
                        <p><strong>Benefits:</strong> A spectacular display of strength that builds the back, hips, and grip. Allows for lifting immense loads.</p>
                    </div>
                </details>
                <details>
                    <summary>Hercules Hold</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An isometric hold where the athlete stands between two hinged pillars and holds them up by gripping handles, preventing them from falling outwards.</p>
                        <p><strong>Benefits:</strong> The ultimate test of grip strength and endurance, also heavily taxing the shoulders and chest.</p>
                    </div>
                </details>
                <details>
                    <summary>Fingal's Fingers</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A series of progressively heavier, hinged poles ("fingers") are lifted from a horizontal position and pushed over to a vertical one.</p>
                        <p><strong>Benefits:</strong> Develops explosive power, coordination, and strength in the entire body, especially the hips, back, and shoulders.</p>
                    </div>
                </details>
                <details>
                    <summary>Duck Walk</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An athlete waddles for a set distance while carrying a heavy, awkwardly shaped weight between their legs, holding onto a handle at the top.</p>
                        <p><strong>Benefits:</strong> Builds grip strength, leg endurance, and core stability. A grueling test of conditioning.</p>
                    </div>
                </details>
                <details>
                    <summary>Conan's Wheel</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An athlete carries a heavy weight in the crooks of their elbows (Zercher style) that is attached to a pivoting arm, walking in a circle for maximum distance.</p>
                        <p><strong>Benefits:</strong> Builds incredible core strength, back strength, and pain tolerance. A brutal test of endurance.</p>
                    </div>
                </details>
            </section>
            
            <!-- Pilates Section -->
            <section id="pilates" class="exercise-section">
                <h2>Pilates</h2>
                <!-- Details elements for Pilates -->
                <details>
                    <summary>The Hundred</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back with legs extended or in a tabletop position, lift your head and shoulders and pump your arms up and down while taking five short breaths in and five short breaths out.</p>
                        <p><strong>Benefits:</strong> A classic warm-up that builds core strength and stability, improves circulation, and coordinates breath with movement.</p>
                    </div>
                </details>
                <details>
                    <summary>Roll Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back with arms extended overhead, slowly roll your spine up off the mat one vertebra at a time to a seated position, reaching for your toes. Then, slowly roll back down.</p>
                        <p><strong>Benefits:</strong> Increases spinal articulation and flexibility, strengthens the abdominal muscles, and stretches the hamstrings.</p>
                    </div>
                </details>
                <details>
                    <summary>Leg Circles</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back, extend one leg toward the ceiling and draw circles in the air with it, keeping the pelvis stable. Repeat in both directions, then switch legs.</p>
                        <p><strong>Benefits:</strong> Improves hip mobility and stability, strengthens the core, and challenges pelvic control.</p>
                    </div>
                </details>
                <details>
                    <summary>Rolling Like a Ball</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Sit balanced on your sit bones, hugging your knees to your chest and curving your spine into a "C" shape. Roll back to your shoulders and then roll back up to the starting position without letting your feet touch the floor.</p>
                        <p><strong>Benefits:</strong> Massages the spine, improves balance, and deeply engages the core muscles.</p>
                    </div>
                </details>
                <details>
                    <summary>Single Leg Stretch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back, hug one knee into your chest while the other leg extends out long. Quickly switch legs, coordinating the movement with your breath.</p>
                        <p><strong>Benefits:</strong> Builds abdominal endurance and coordination while stretching the hips.</p>
                    </div>
                </details>
                <details>
                    <summary>Double Leg Stretch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From a curled-up position, simultaneously extend your arms and legs away from your center, then circle your arms around to hug your knees back into your chest.</p>
                        <p><strong>Benefits:</strong> A challenging core exercise that builds deep abdominal strength and coordination.</p>
                    </div>
                </details>
                <details>
                    <summary>Criss-Cross</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back with hands behind your head, bring one knee in while rotating your opposite shoulder towards it, extending the other leg long. Alternate sides in a cycling motion.</p>
                        <p><strong>Benefits:</strong> Targets the oblique muscles, improves spinal rotation, and builds core strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Spine Stretch Forward</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Sit tall with legs extended and apart. Reach your arms forward and round your spine forward, as if stretching up and over a large ball.</p>
                        <p><strong>Benefits:</strong> Stretches the entire back of the body, including the spine and hamstrings, and strengthens the abdominals.</p>
                    </div>
                </details>
                <details>
                    <summary>Saw</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Sitting tall with legs wide and arms extended to the sides, twist from the waist and reach one hand towards the opposite foot, "sawing" off your pinky toe.</p>
                        <p><strong>Benefits:</strong> Increases spinal rotation and flexibility, stretches the hamstrings and hips, and energizes the body.</p>
                    </div>
                </details>
                <details>
                    <summary>Swan</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your stomach, press through your hands to lift your chest off the mat, creating an arch in your upper and mid-back.</p>
                        <p><strong>Benefits:</strong> Strengthens the back extensors, opens the chest and shoulders, and improves posture.</p>
                    </div>
                </details>
                <details>
                    <summary>Seal</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A playful rolling exercise similar to Rolling Like a Ball, but with the hands threaded through the legs to hold the ankles. Clap the feet together like a seal's flippers at the top.</p>
                        <p><strong>Benefits:</strong> Massages the spine, improves balance and coordination, and deeply works the core.</p>
                    </div>
                </details>
                <details>
                    <summary>Teaser</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The ultimate Pilates challenge. From lying down, simultaneously roll up your torso and lift your legs to create a "V" shape with your body, balancing on your sit bones.</p>
                        <p><strong>Benefits:</strong> Builds exceptional core strength, balance, and control.</p>
                    </div>
                </details>
                <details>
                    <summary>Corkscrew</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back, press your legs together and circle them in one direction, then the other, keeping your shoulders anchored to the mat.</p>
                        <p><strong>Benefits:</strong> Strengthens the obliques and lower abdominals while challenging pelvic stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Jackknife</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back, roll over to lift your hips and legs overhead (like a shoulder stand), then "jackknife" by lifting your legs straight to the ceiling.</p>
                        <p><strong>Benefits:</strong> A dynamic and advanced exercise that strengthens the core, shoulders, and back while improving spinal articulation.</p>
                    </div>
                </details>
                <details>
                    <summary>Side Kicks</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your side, lift the top leg to hip height and perform various movements like kicking forward and back, lifting and lowering, and making circles.</p>
                        <p><strong>Benefits:</strong> Strengthens the hips, glutes (especially the gluteus medius), and outer thighs while challenging core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Swimming</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your stomach with arms and legs extended, lift everything off the floor and flutter your opposite arm and leg up and down, as if swimming.</p>
                        <p><strong>Benefits:</strong> Strengthens the entire posterior chain (back, glutes, hamstrings) and improves coordination.</p>
                    </div>
                </details>
                <details>
                    <summary>Leg Pull Front</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From a plank position, lift one leg off the floor without changing the shape of your torso, then lower it with control. Alternate legs.</p>
                        <p><strong>Benefits:</strong> Builds total-body strength, focusing on the core, shoulders, and glutes.</p>
                    </div>
                </details>
                <details>
                    <summary>Leg Pull Back</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From a reverse plank position (facing up), lift one leg towards the ceiling without letting your hips drop. Alternate legs.</p>
                        <p><strong>Benefits:</strong> Strengthens the posterior chain, including the glutes, hamstrings, and back, as well as the shoulders and triceps.</p>
                    </div>
                </details>
                <details>
                    <summary>Control Balance</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An advanced exercise involving balancing on one shoulder while one leg reaches to the ceiling and the other reaches back towards the floor, holding the ankle with the hand.</p>
                        <p><strong>Benefits:</strong> The pinnacle of Pilates control, this move challenges strength, flexibility, and balance to the extreme.</p>
                    </div>
                </details>
            </section>

            <!-- Yoga Section -->
            <section id="yoga" class="exercise-section">
                <h2>Yoga</h2>
                <!-- Details elements for Yoga -->
                <details>
                    <summary>Downward-Facing Dog</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From hands and knees, lift your hips up and back to form an inverted "V" shape with your body. Press firmly through your hands and feet.</p>
                        <p><strong>Benefits:</strong> A full-body stretch that energizes and rejuvenates. It strengthens the arms and legs, stretches the shoulders, hamstrings, and calves, and calms the mind.</p>
                    </div>
                </details>
                <details>
                    <summary>Mountain Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Stand tall with feet together or hip-width apart, distributing weight evenly. Engage your leg muscles, lengthen your spine, and relax your shoulders down and back.</p>
                        <p><strong>Benefits:</strong> The foundation for all standing poses. It improves posture, firms the muscles of the legs and abdomen, and promotes a sense of grounding and balance.</p>
                    </div>
                </details>
                <details>
                    <summary>Warrior I</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From a lunge position with the front knee bent, ground the back foot at a 45-degree angle and lift your arms and torso overhead. Square your hips to the front.</p>
                        <p><strong>Benefits:</strong> Builds strength in the legs, back, and arms. Stretches the chest, shoulders, and hip flexors. Develops focus and stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Warrior II</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A standing pose with feet wide apart, front knee bent, and back leg straight. The torso is open to the side, with arms extended parallel to the floor.</p>
                        <p><strong>Benefits:</strong> Strengthens the legs and ankles, opens the hips and chest, and builds stamina and concentration.</p>
                    </div>
                </details>
                <details>
                    <summary>Triangle Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> With legs wide, hinge at the front hip to bring your torso over the front leg, resting your hand on your shin or the floor. Extend the top arm to the ceiling.</p>
                        <p><strong>Benefits:</strong> Stretches the hamstrings, hips, and spine. Strengthens the legs and core, and improves balance.</p>
                    </div>
                </details>
                <details>
                    <summary>Tree Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A balancing pose where you stand on one leg and place the sole of the other foot on your inner thigh or calf (avoiding the knee). Hands are typically in a prayer position.</p>
                        <p><strong>Benefits:</strong> Improves balance, focus, and concentration. Strengthens the ankles and legs.</p>
                    </div>
                </details>
                <details>
                    <summary>Cat-Cow Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> On hands and knees, inhale to drop the belly and look up (Cow), then exhale to round the spine and tuck the chin (Cat). Flow between the two poses.</p>
                        <p><strong>Benefits:</strong> A gentle warm-up that increases spinal flexibility and awareness. Relieves tension in the back and neck.</p>
                    </div>
                </details>
                <details>
                    <summary>Cobra Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your stomach, lift your head and chest off the floor, keeping your hips grounded. Use your back muscles to lift, with minimal pressure on the hands.</p>
                        <p><strong>Benefits:</strong> Strengthens the spine, opens the chest and shoulders, and improves posture. A gentler alternative to Upward-Facing Dog.</p>
                    </div>
                </details>
                <details>
                    <summary>Child's Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A resting posture. Kneel on the floor, sit back on your heels, and fold your torso forward, resting your forehead on the mat.</p>
                        <p><strong>Benefits:</strong> Gently stretches the hips, thighs, and ankles. Calms the mind, relieves stress, and reduces fatigue.</p>
                    </div>
                </details>
                <details>
                    <summary>Bridge Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back with knees bent, press through your feet to lift your hips off the floor. Clasp your hands underneath your back if possible.</p>
                        <p><strong>Benefits:</strong> Strengthens the glutes, hamstrings, and back. Stretches the chest, neck, and spine.</p>
                    </div>
                </details>
                <details>
                    <summary>Pigeon Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A deep hip-opening pose. Bring one shin forward, parallel to the front of the mat, and extend the other leg straight back. Fold forward over the front leg.</p>
                        <p><strong>Benefits:</strong> Provides an intense stretch for the hip rotators and flexors. Can help relieve sciatic pain and tension.</p>
                    </div>
                </details>
                <details>
                    <summary>Crow Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An arm balance where you squat down, place your hands on the floor, and rest your knees on your upper arms. Lean forward to lift your feet off the floor.</p>
                        <p><strong>Benefits:</strong> Builds arm, shoulder, and core strength. Improves balance and confidence.</p>
                    </div>
                </details>
                <details>
                    <summary>Headstand</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An advanced inversion where you balance on your head and forearms, with your legs extended towards the ceiling.</p>
                        <p><strong>Benefits:</strong> Strengthens the entire body, improves circulation, calms the nervous system, and builds focus and confidence.</p>
                    </div>
                </details>
                <details>
                    <summary>Shoulder Stand</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An inversion where you balance on your shoulders, supporting your back with your hands, with your legs extended towards the ceiling.</p>
                        <p><strong>Benefits:</strong> Often called the "queen" of all poses, it calms the mind, stimulates the thyroid gland, and stretches the neck and shoulders.</p>
                    </div>
                </details>
                <details>
                    <summary>Plank Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The top of a push-up position, holding a straight line from your head to your heels. Can be done on hands or forearms.</p>
                        <p><strong>Benefits:</strong> Builds strength in the core, arms, wrists, and shoulders. A foundational pose for many other movements.</p>
                    </div>
                </details>
                <details>
                    <summary>Chair Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Stand with feet together, bend your knees, and sink your hips as if sitting in a chair. Raise your arms overhead.</p>
                        <p><strong>Benefits:</strong> Strengthens the legs, back, and shoulders. Builds heat and stamina.</p>
                    </div>
                </details>
                <details>
                    <summary>Sun Salutation A</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A flowing sequence of poses, typically including Mountain, Upward Salute, Forward Fold, Half Lift, Plank, Chaturanga, Upward-Facing Dog, and Downward-Facing Dog.</p>
                        <p><strong>Benefits:</strong> A full-body warm-up that links breath to movement, builds heat, and improves flexibility and strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Sun Salutation B</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A more complex version of Sun Salutation A that incorporates Chair Pose and Warrior I into the sequence.</p>
                        <p><strong>Benefits:</strong> Builds more heat and stamina than Sun Salutation A, further challenging strength and endurance.</p>
                    </div>
                </details>
                <details>
                    <summary>Half Moon Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A challenging balancing pose. From Triangle Pose, shift your weight onto your front foot, bringing your hand to the floor and lifting your back leg parallel to the ground.</p>
                        <p><strong>Benefits:</strong> Improves balance and proprioception. Strengthens the ankles, legs, and core, while opening the hips and chest.</p>
                    </div>
                </details>
                <details>
                    <summary>Eagle Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A standing balance pose that involves wrapping one leg around the other and one arm under the other.</p>
                        <p><strong>Benefits:</strong> Improves balance and focus. Stretches the shoulders and upper back, and strengthens the legs and ankles.</p>
                    </div>
                </details>
                <details>
                    <summary>Camel Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Kneeling on your shins, place your hands on your lower back and arch your spine, reaching back to hold your heels if accessible.</p>
                        <p><strong>Benefits:</strong> A deep backbend that opens the entire front of the body, including the chest, abdomen, and hip flexors. Strengthens the back muscles.</p>
                    </div>
                </details>
                <details>
                    <summary>Fish Pose</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back, prop yourself up on your forearms and arch your back, allowing the crown of your head to rest gently on the floor.</p>
                        <p><strong>Benefits:</strong> A counter-pose to shoulder stand that stretches the front of the neck and chest.</p>
                    </div>
                </details>
                <details>
                    <summary>Seated Forward Bend</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Sit with legs extended in front of you. Hinge at your hips and fold your torso over your legs, holding onto your feet or shins.</p>
                        <p><strong>Benefits:</strong> Provides a deep stretch for the entire back of the body, especially the hamstrings and lower back. Calms the nervous system.</p>
                    </div>
                </details>
                <details>
                    <summary>Garland Pose (Malasana)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A deep squat with feet slightly wider than hips and turned out. The torso stays lifted, often with elbows pressing against the inner knees.</p>
                        <p><strong>Benefits:</strong> Excellent for hip and ankle mobility. Stretches the groin and lower back, and aids in digestion.</p>
                    </div>
                </details>
            </section>

            <!-- Animal Flow Section -->
            <section id="animal-flow" class="exercise-section">
                <h2>Animal Flow</h2>
                <!-- Details elements for Animal Flow -->
                <details>
                    <summary>Ape</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A foundational position starting in a deep squat. Variations include Ape Reach (reaching one arm up and rotating) and Traveling Ape (moving side to side).</p>
                        <p><strong>Benefits:</strong> Opens up the hips, ankles, and thoracic spine. Builds lower body strength and mobility.</p>
                    </div>
                </details>
                <details>
                    <summary>Beast</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A quadrupedal position (on hands and feet) with knees hovering just off the floor. This is the starting point for many other movements.</p>
                        <p><strong>Benefits:</strong> Builds total-body tension and stability, especially in the core and shoulders.</p>
                    </div>
                </details>
                <details>
                    <summary>Crab</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A ground-based position where you sit with knees bent, feet flat on the floor, and hands on the floor behind you, fingers pointing towards your feet.</p>
                        <p><strong>Benefits:</strong> A base position for movements like the Crab Reach. Opens the chest and shoulders.</p>
                    </div>
                </details>
                <details>
                    <summary>Scorpion Reach</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From Beast or Downward Dog, lift one leg and bend the knee, opening the hip and "reaching" the foot towards the opposite side, like a scorpion's tail.</p>
                        <p><strong>Benefits:</strong> Improves hip mobility and thoracic spine rotation. A dynamic stretch for the whole body.</p>
                    </div>
                </details>
                <details>
                    <summary>Side Kickthrough</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From Beast, lift one hand and the opposite foot, then pivot on the grounded foot while "kicking" the free leg through to the side.</p>
                        <p><strong>Benefits:</strong> Develops rotational power, coordination, and core strength. A signature, fluid movement in Animal Flow.</p>
                    </div>
                </details>
                <details>
                    <summary>Front Kickthrough</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A more advanced kickthrough where you kick the leg straight out in front of the body instead of to the side.</p>
                        <p><strong>Benefits:</strong> Requires greater core control, hip mobility, and dynamic strength than the side kickthrough.</p>
                    </div>
                </details>
                <details>
                    <summary>Underswitch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A transitional movement used to flow between Beast and Crab positions. It involves lifting opposite limbs and sweeping the body underneath itself.</p>
                        <p><strong>Benefits:</strong> The cornerstone of creating fluid flows. Improves coordination, body awareness, and core control.</p>
                    </div>
                </details>
                <details>
                    <summary>Wave Unload</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From Loaded Beast, initiate a wave-like motion through the spine to move forward into a plank-like position.</p>
                        <p><strong>Benefits:</strong> Promotes spinal articulation and mobility. Teaches how to generate force from the ground up.</p>
                    </div>
                </details>
                <details>
                    <summary>Traveling Beast (Forward/Backward)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Moving forward or backward in the Beast position by stepping with the opposite hand and foot simultaneously.</p>
                        <p><strong>Benefits:</strong> Builds coordination, core stability, and endurance. A fundamental crawling pattern.</p>
                    </div>
                </details>
                <details>
                    <summary>Traveling Ape (Forward/Backward)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Moving forward or sideways from the Ape (deep squat) position by placing the hands on the floor and lightly hopping the feet to meet them.</p>
                        <p><strong>Benefits:</strong> Develops explosive power, wrist strength, and coordination.</p>
                    </div>
                </details>
                <details>
                    <summary>Crab Reach</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From the Crab position, lift your hips high and reach one arm up and over your head, creating a full-body arch.</p>
                        <p><strong>Benefits:</strong> A fantastic movement for opening the entire front of the body, improving thoracic mobility, and activating the glutes.</p>
                    </div>
                </details>
                <details>
                    <summary>Loaded Beast</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From the Beast position, shift your hips back towards your heels while keeping your knees off the floor, "loading" the body like a spring.</p>
                        <p><strong>Benefits:</strong> Deeply stretches the lats, wrists, and ankles. Prepares the body for explosive movements.</p>
                    </div>
                </details>
                <details>
                    <summary>Full Scorpion</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An advanced movement that transitions from a Scorpion Reach into a full backbend, with the reaching foot touching the floor.</p>
                        <p><strong>Benefits:</strong> Requires and builds significant mobility in the hips and spine, as well as shoulder stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Levitating</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An advanced transition, often from a kickthrough, where the body hovers horizontally off the ground, supported by the hands.</p>
                        <p><strong>Benefits:</strong> Develops exceptional core strength, balance, and body control.</p>
                    </div>
                </details>
                <details>
                    <summary>Beast Reach</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From Beast, reach one arm forward while maintaining stability, creating a long line from fingertips to opposite heel.</p>
                        <p><strong>Benefits:</strong> Challenges core stability and anti-rotation, similar to a bird-dog but more demanding.</p>
                    </div>
                </details>
                <details>
                    <summary>Crab to Beast Transition</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The Underswitch is the primary way to perform this transition, allowing for a seamless flow between the two foundational positions.</p>
                        <p><strong>Benefits:</strong> Connects different movement patterns, enhancing the creativity and complexity of a flow.</p>
                    </div>
                </details>
            </section>

            <!-- Loaded Carries Section -->
            <section id="loaded-carries" class="exercise-section">
                <h2>Loaded Carries</h2>
                <!-- Details elements for Loaded Carries -->
                <details>
                    <summary>Suitcase Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A single-sided Farmer's Walk. Carry a heavy weight (dumbbell or kettlebell) in one hand, like carrying a suitcase.</p>
                        <p><strong>Benefits:</strong> Builds tremendous anti-lateral flexion core strength (resisting side-bending). Strengthens the obliques, grip, and upper back.</p>
                    </div>
                </details>
                <details>
                    <summary>Waiter's Walk</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Carry a weight (usually a kettlebell) in one hand, locked out overhead with a straight arm, as if you were a waiter carrying a tray.</p>
                        <p><strong>Benefits:</strong> Develops shoulder stability and strength. Challenges the core to maintain an upright, stable posture.</p>
                    </div>
                </details>
                <details>
                    <summary>Cross-Body Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A combination carry, holding one weight in the rack or overhead position and another weight in the opposite hand in the suitcase position.</p>
                        <p><strong>Benefits:</strong> Creates a complex stability challenge for the core, forcing it to resist multiple forces (flexion, rotation, lateral flexion) at once.</p>
                    </div>
                </details>
                <details>
                    <summary>Rack Carry (Single and Double)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Carry one or two kettlebells in the front rack position (resting on the forearms, close to the chest).</p>
                        <p><strong>Benefits:</strong> Builds anterior core strength (resisting extension), upper back strength, and improves posture by forcing an upright torso.</p>
                    </div>
                </details>
                <details>
                    <summary>Zercher Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Carry a barbell, sandbag, or other object in the crooks of your elbows.</p>
                        <p><strong>Benefits:</strong> Builds immense upper back and core strength. A very challenging and uncomfortable carry that builds mental toughness.</p>
                    </div>
                </details>
                <details>
                    <summary>Bear Hug Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Hug a heavy, awkward object (like a sandbag or stone) to your chest and walk for distance.</p>
                        <p><strong>Benefits:</strong> Develops crushing grip and upper body strength. The object's position heavily taxes the core and back muscles.</p>
                    </div>
                </details>
                <details>
                    <summary>Overhead Carry (Single and Double)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Walk for distance while holding one or two weights locked out directly overhead.</p>
                        <p><strong>Benefits:</strong> The ultimate test of shoulder and core stability. Improves posture and builds a rock-solid midsection.</p>
                    </div>
                </details>
                <details>
                    <summary>Bottoms-Up Kettlebell Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Hold a kettlebell upside down by the handle and walk, keeping it stable.</p>
                        <p><strong>Benefits:</strong> An incredible exercise for developing grip strength, rotator cuff stability, and shoulder health.</p>
                    </div>
                </details>
                <details>
                    <summary>Hex Bar Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A variation of the Farmer's Walk using a loaded hex (trap) bar. The neutral grips and centered weight distribution allow for very heavy loads.</p>
                        <p><strong>Benefits:</strong> Allows you to overload the Farmer's Walk pattern, building massive grip, trap, and back strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Plate Pinch Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pinch two or more weight plates together (smooth side out) with your fingertips and walk for distance.</p>
                        <p><strong>Benefits:</strong> Specifically targets and develops pinch grip strength, a crucial and often-neglected aspect of hand strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Sandbag Shoulder Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Hoist a heavy sandbag onto one shoulder and walk for distance, then switch shoulders.</p>
                        <p><strong>Benefits:</strong> A functional, real-world strength builder. The unilateral load creates a significant challenge for core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Uneven (Offset) Farmer's Walk</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Perform a Farmer's Walk with a significantly heavier weight in one hand than the other.</p>
                        <p><strong>Benefits:</strong> Creates a unique stability challenge, forcing the core to work harder to compensate for the imbalanced load.</p>
                    </div>
                </details>
                <details>
                    <summary>Husafell Stone Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Carry a large, shield-shaped stone (or a heavy sandbag held vertically) hugged to the chest for maximum distance.</p>
                        <p><strong>Benefits:</strong> A classic strongman test of strength, endurance, and pain tolerance. Builds the back, arms, and core.</p>
                    </div>
                </details>
                <details>
                    <summary>Goblet Carry</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Hold a single dumbbell or kettlebell vertically against your chest with both hands (like a goblet squat) and walk.</p>
                        <p><strong>Benefits:</strong> Reinforces an upright posture and builds anterior core and upper back strength.</p>
                    </div>
                </details>
            </section>

            <!-- Functional Training Section -->
            <section id="functional-training" class="exercise-section">
                <h2>Functional Training</h2>
                <!-- Details elements for Functional Training -->
                 <details>
                    <summary>Kettlebell Swing</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A powerful hip-hinge movement where a kettlebell is swung from between the legs up to chest height, driven by an explosive hip thrust.</p>
                        <p><strong>Benefits:</strong> Develops explosive power in the posterior chain (glutes and hamstrings), builds cardiovascular endurance, and improves grip strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Goblet Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A squat performed while holding a single kettlebell or dumbbell at chest height.</p>
                        <p><strong>Benefits:</strong> An excellent teaching tool for the squat pattern. The anterior load forces an upright torso and engages the core.</p>
                    </div>
                </details>
                <details>
                    <summary>Turkish Get-Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A complex, multi-stage movement that involves moving from a lying position on the floor to a standing position, all while holding a weight overhead.</p>
                        <p><strong>Benefits:</strong> A true full-body exercise that builds strength, stability, mobility, and coordination. Excellent for shoulder health and core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Pull-Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Hanging from a bar with an overhand grip, pull your body up until your chin is over the bar.</p>
                        <p><strong>Benefits:</strong> The ultimate test of upper body pulling strength. Builds the lats, biceps, and upper back.</p>
                    </div>
                </details>
                <details>
                    <summary>Chin-Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Similar to a pull-up, but performed with an underhand (supinated) grip.</p>
                        <p><strong>Benefits:</strong> Also builds the back, but places a greater emphasis on the biceps compared to the pull-up.</p>
                    </div>
                </details>
                <details>
                    <summary>Push-Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> In a plank position, lower your body until your chest touches the floor, then press back up to the starting position, maintaining a straight line from head to heels.</p>
                        <p><strong>Benefits:</strong> A fundamental bodyweight exercise for building upper body pushing strength (chest, shoulders, triceps) and core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Dip</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Supporting your body on parallel bars, lower yourself until your shoulders are below your elbows, then press back up.</p>
                        <p><strong>Benefits:</strong> A powerful exercise for building the chest, shoulders, and triceps.</p>
                    </div>
                </details>
                <details>
                    <summary>Lunge (Forward, Reverse, Lateral)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Step forward, backward, or to the side and lower your hips until both knees are bent at a 90-degree angle.</p>
                        <p><strong>Benefits:</strong> A unilateral exercise that builds leg strength, balance, and hip mobility. Each direction targets the muscles slightly differently.</p>
                    </div>
                </details>
                <details>
                    <summary>Step-Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Step onto a box or bench with one foot, drive up to a standing position on top of the box, and then step back down with control.</p>
                        <p><strong>Benefits:</strong> Builds single-leg strength, balance, and explosive power. Mimics climbing stairs and other daily activities.</p>
                    </div>
                </details>
                <details>
                    <summary>Box Jump</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A plyometric exercise where you jump from the floor onto an elevated box, landing softly and with control.</p>
                        <p><strong>Benefits:</strong> Develops explosive power and speed in the lower body.</p>
                    </div>
                </details>
                <details>
                    <summary>Burpee</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A full-body exercise that combines a squat, a push-up, and a jump. From standing, drop into a squat, kick your feet back to a push-up, perform a push-up, return to the squat, and jump up explosively.</p>
                        <p><strong>Benefits:</strong> A highly effective conditioning tool that builds strength, endurance, and agility.</p>
                    </div>
                </details>
                <details>
                    <summary>Wall Ball</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Holding a medicine ball at your chest, perform a full squat, and then explosively stand up, using the momentum to throw the ball to a target on a wall.</p>
                        <p><strong>Benefits:</strong> A full-body metabolic conditioning exercise that builds leg and shoulder endurance, and coordination.</p>
                    </div>
                </details>
                <details>
                    <summary>Battle Ropes (Waves, Slams)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Gripping two heavy ropes, create various wave patterns or slam them into the ground.</p>
                        <p><strong>Benefits:</strong> A high-intensity, low-impact conditioning tool that builds upper body endurance, core strength, and grip.</p>
                    </div>
                </details>
                <details>
                    <summary>Rowing (Machine)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Using a rowing machine (ergometer) to simulate the motion of rowing a boat.</p>
                        <p><strong>Benefits:</strong> A fantastic full-body, low-impact cardiovascular exercise that builds the legs, back, and arms.</p>
                    </div>
                </details>
                <details>
                    <summary>Bear Crawl</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A crawling pattern on hands and feet with knees bent and off the ground. Move by stepping with the opposite hand and foot.</p>
                        <p><strong>Benefits:</strong> Builds total-body strength, coordination, and core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Inchworm</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From a standing position, walk your hands out to a plank position, then walk your feet in to meet your hands. Repeat.</p>
                        <p><strong>Benefits:</strong> A dynamic warm-up that improves hamstring flexibility, core strength, and shoulder stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Plank (and variations)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Holding the top of a push-up position, either on hands or forearms, for time. Variations include lifting a limb or adding movement.</p>
                        <p><strong>Benefits:</strong> Builds isometric core strength and stability in the entire torso.</p>
                    </div>
                </details>
                <details>
                    <summary>Side Plank (and variations)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Supporting your body on one hand or forearm and the side of your foot, holding a straight line.</p>
                        <p><strong>Benefits:</strong> Specifically targets the obliques and other lateral core stabilizers like the gluteus medius.</p>
                    </div>
                </details>
                <details>
                    <summary>Bird-Dog</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> From a hands-and-knees position, extend one arm forward and the opposite leg backward, keeping your torso stable. Alternate sides.</p>
                        <p><strong>Benefits:</strong> Improves core stability, proprioception, and control. Excellent for building a stable spine.</p>
                    </div>
                </details>
                <details>
                    <summary>Dead Bug</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back, slowly lower one arm and the opposite leg towards the floor, keeping your lower back pressed into the mat. Alternate sides.</p>
                        <p><strong>Benefits:</strong> Teaches core control and how to brace the abdominals while moving the limbs, without arching the lower back.</p>
                    </div>
                </details>
                <details>
                    <summary>Hanging Leg Raise</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Hanging from a bar, raise your legs up towards your chest or higher, with either bent or straight knees.</p>
                        <p><strong>Benefits:</strong> A challenging exercise that builds the lower abdominals and hip flexors.</p>
                    </div>
                </details>
                <details>
                    <summary>Windmill (Kettlebell)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> With a kettlebell held overhead, hinge at the hip and lower your free hand towards the floor, keeping your eyes on the kettlebell.</p>
                        <p><strong>Benefits:</strong> Builds shoulder stability, hamstring flexibility, and oblique strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Renegade Row</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> In a plank position with hands on two dumbbells, perform a row with one arm, then the other, keeping the hips stable.</p>
                        <p><strong>Benefits:</strong> A compound exercise that builds back strength and incredible anti-rotational core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Bulgarian Split Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A single-leg squat with the rear foot elevated on a bench or box.</p>
                        <p><strong>Benefits:</strong> An excellent exercise for building strength and muscle in the quads and glutes while also improving balance and hip mobility.</p>
                    </div>
                </details>
                <details>
                    <summary>Single-Leg Romanian Deadlift</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A hip-hinge movement performed on one leg, holding a weight in the opposite hand.</p>
                        <p><strong>Benefits:</strong> Builds strength in the hamstrings and glutes while significantly challenging balance and stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Pistol Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A single-leg squat performed all the way down until the hamstring rests on the calf, with the non-working leg extended forward.</p>
                        <p><strong>Benefits:</strong> The ultimate test of single-leg strength, balance, and mobility.</p>
                    </div>
                </details>
                <details>
                    <summary>Rope Climb</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Climbing a rope using various techniques involving the hands and feet.</p>
                        <p><strong>Benefits:</strong> Develops incredible grip strength and upper body pulling power.</p>
                    </div>
                </details>
                <details>
                    <summary>Sledgehammer Swings (on tire)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Swinging a sledgehammer in a large arc to strike a large tire.</p>
                        <p><strong>Benefits:</strong> Builds rotational power, core strength, and conditioning. A great, aggressive workout.</p>
                    </div>
                </details>
                <details>
                    <summary>Dumbbell Pullover</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on a bench, hold a single dumbbell with both hands over your chest. Lower the dumbbell in an arc behind your head, feeling a stretch in your lats and chest, then pull it back to the starting position.</p>
                        <p><strong>Benefits:</strong> A unique exercise that works opposing muscle groups (chest and back) simultaneously. Improves shoulder mobility and strengthens the lats, serratus anterior, and chest.</p>
                    </div>
                </details>
                <details>
                    <summary>Barbell Pullover</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Similar to the dumbbell version, but performed with a barbell held with a shoulder-width grip. This variation allows for heavier loads.</p>
                        <p><strong>Benefits:</strong> Builds strength and size in the lats and chest. The fixed hand position can provide a different stimulus than the dumbbell version.</p>
                    </div>
                </details>
                <details>
                    <summary>Straight-Arm Cable Pullover</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Standing facing a high cable pulley with a straight bar or rope attachment, pull the weight down in a wide arc with straight arms until your hands reach your thighs.</p>
                        <p><strong>Benefits:</strong> Provides constant tension on the lats throughout the entire range of motion, making it excellent for muscle isolation and hypertrophy.</p>
                    </div>
                </details>
                <details>
                    <summary>Stability Ball Hamstring Curl</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your back with your heels on a stability ball, lift your hips into a bridge and then curl the ball towards you by bending your knees.</p>
                        <p><strong>Benefits:</strong> Isolates and strengthens the hamstrings while also challenging core and hip stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Pallof Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Standing perpendicular to a cable machine or band, hold the handle at your chest and press it straight out, resisting the rotational pull.</p>
                        <p><strong>Benefits:</strong> An excellent anti-rotation exercise that builds core stability and strength in the transverse plane.</p>
                    </div>
                </details>
                <details>
                    <summary>Cable Woodchop (High to Low, Low to High)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pulling a cable handle diagonally across your body, either from a high to low position or a low to high position.</p>
                        <p><strong>Benefits:</strong> Develops rotational strength and power in the core, mimicking many athletic movements.</p>
                    </div>
                </details>
                <details>
                    <summary>Face Pull</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Using a rope attachment on a cable machine, pull the handles towards your face, externally rotating your shoulders at the end of the movement.</p>
                        <p><strong>Benefits:</strong> Excellent for improving posture and shoulder health by strengthening the rear deltoids and external rotators.</p>
                    </div>
                </details>
                <details>
                    <summary>Dumbbell Thruster</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A compound movement combining a front squat with an overhead press, performed with dumbbells.</p>
                        <p><strong>Benefits:</strong> A full-body metabolic conditioning exercise that builds strength, power, and cardiovascular endurance.</p>
                    </div>
                </details>
                <details>
                    <summary>Kettlebell Halo</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Circle a kettlebell around your head, keeping it close to your body.</p>
                        <p><strong>Benefits:</strong> Improves shoulder mobility and stability, and warms up the entire shoulder girdle.</p>
                    </div>
                </details>
                <details>
                    <summary>TRX Row</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Using a suspension trainer, lean back to create tension and then pull your chest towards the handles.</p>
                        <p><strong>Benefits:</strong> A scalable back-strengthening exercise that also challenges core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>TRX Atomic Push-Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> With your feet in the TRX straps, perform a push-up, followed by a knee tuck, bringing your knees to your chest.</p>
                        <p><strong>Benefits:</strong> A highly challenging exercise that combines upper body strength with intense core work.</p>
                    </div>
                </details>
                <details>
                    <summary>Agility Ladder Drills</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Performing various fast-feet drills through a ladder laid on the ground.</p>
                        <p><strong>Benefits:</strong> Improves footwork, coordination, speed, and agility.</p>
                    </div>
                </details>
                <details>
                    <summary>Cone Drills (various patterns)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Sprinting, shuffling, and changing direction around a series of cones.</p>
                        <p><strong>Benefits:</strong> Develops agility, acceleration, deceleration, and the ability to change direction quickly.</p>
                    </div>
                </details>
                <details>
                    <summary>Broad Jump</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A standing long jump for maximum distance.</p>
                        <p><strong>Benefits:</strong> A simple and effective way to measure and develop horizontal explosive power.</p>
                    </div>
                </details>
                <details>
                    <summary>Vertical Jump</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Jumping as high as possible from a standing position.</p>
                        <p><strong>Benefits:</strong> A classic test and builder of vertical explosive power.</p>
                    </div>
                </details>
                <details>
                    <summary>Box Drill</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An agility drill where you sprint, shuffle, and backpedal between four cones arranged in a square.</p>
                        <p><strong>Benefits:</strong> Improves multi-directional speed and agility.</p>
                    </div>
                </details>
                <details>
                    <summary>Pro Agility (5-10-5) Drill</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A common agility test where you start in the middle of three cones, sprint 5 yards to one side, 10 yards to the other, and then 5 yards back to the start.</p>
                        <p><strong>Benefits:</strong> Measures lateral speed and the ability to change direction quickly.</p>
                    </div>
                </details>
                <details>
                    <summary>Single-Arm Dumbbell Snatch</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An explosive movement where a dumbbell is lifted from the floor to an overhead position in a single motion.</p>
                        <p><strong>Benefits:</strong> A full-body power exercise that is more accessible than the barbell snatch. Builds unilateral strength and coordination.</p>
                    </div>
                </details>
                <details>
                    <summary>Single-Arm Dumbbell Clean and Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lift a dumbbell from the floor to the shoulder, then press it overhead.</p>
                        <p><strong>Benefits:</strong> Builds functional, unilateral strength and power.</p>
                    </div>
                </details>
                <details>
                    <summary>Kettlebell Clean</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An explosive hip hinge used to "tame the arc" of the kettlebell and bring it smoothly into the front rack position.</p>
                        <p><strong>Benefits:</strong> A foundational kettlebell lift that builds power and serves as the starting point for presses and jerks.</p>
                    </div>
                </details>
                <details>
                    <summary>Kettlebell High Pull</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An explosive swing where the kettlebell is pulled up towards the chin, leading with the elbow.</p>
                        <p><strong>Benefits:</strong> Builds explosive power in the hips and strengthens the upper back and shoulders.</p>
                    </div>
                </details>
                <details>
                    <summary>Band Pull-Apart</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Holding a resistance band with both hands, pull it apart across your chest by squeezing your shoulder blades together.</p>
                        <p><strong>Benefits:</strong> An excellent exercise for strengthening the upper back muscles (rhomboids, rear delts) and improving posture.</p>
                    </div>
                </details>
                <details>
                    <summary>Clamshell</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying on your side with knees bent, lift your top knee towards the ceiling without rocking your pelvis, like a clam opening its shell.</p>
                        <p><strong>Benefits:</strong> Isolates and strengthens the gluteus medius, a key muscle for hip stability and injury prevention.</p>
                    </div>
                </details>
                <details>
                    <summary>Hip Thrust</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> With your upper back on a bench and a barbell across your hips, drive your hips up until your torso is parallel to the floor. Squeeze the glutes hard at the top.</p>
                        <p><strong>Benefits:</strong> The premier exercise for building strength and size in the gluteus maximus.</p>
                    </div>
                </details>
                <details>
                    <summary>Calf Raise</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pushing through the balls of your feet to raise your heels as high as possible.</p>
                        <p><strong>Benefits:</strong> Strengthens the calf muscles (gastrocnemius and soleus), which is important for running, jumping, and ankle stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Inverted Row</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying under a fixed bar (like in a squat rack), pull your chest up to the bar.</p>
                        <p><strong>Benefits:</strong> A great horizontal pulling exercise for building back strength. A good precursor to the pull-up.</p>
                    </div>
                </details>
                <details>
                    <summary>Wall Sit</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> An isometric exercise where you hold a squat position with your back against a wall.</p>
                        <p><strong>Benefits:</strong> Builds isometric strength and endurance in the quadriceps.</p>
                    </div>
                </details>
                <details>
                    <summary>Jump Rope</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Skipping rope.</p>
                        <p><strong>Benefits:</strong> A classic, highly effective tool for improving cardiovascular fitness, coordination, and footwork.</p>
                    </div>
                </details>
                <details>
                    <summary>Elliptical Trainer</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A stationary exercise machine used to simulate stair climbing, walking, or running without causing excessive pressure to the joints.</p>
                        <p><strong>Benefits:</strong> Provides a low-impact cardiovascular workout that can be adjusted for various intensity levels.</p>
                    </div>
                </details>
                <details>
                    <summary>Stair Climber</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A machine that simulates climbing stairs.</p>
                        <p><strong>Benefits:</strong> An intense cardiovascular workout that heavily targets the glutes, quads, and calves.</p>
                    </div>
                </details>
                <details>
                    <summary>Assault Bike Sprints</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Performing all-out sprints on an air bike, which uses a fan for resistance.</p>
                        <p><strong>Benefits:</strong> One of the most challenging metabolic conditioning tools available. Builds incredible cardiovascular capacity and mental toughness.</p>
                    </div>
                </details>
                <details>
                    <summary>Prowler Push</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pushing a weighted sled (often called a Prowler) across the floor.</p>
                        <p><strong>Benefits:</strong> Builds leg drive, power, and conditioning with minimal eccentric stress, allowing for quick recovery.</p>
                    </div>
                </details>
                <details>
                    <summary>Tire Drag</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Dragging a tire behind you, usually with a harness or rope.</p>
                        <p><strong>Benefits:</strong> A low-cost, effective way to build posterior chain strength and improve conditioning.</p>
                    </div>
                </details>
                <details>
                    <summary>Resistance Band Sprints</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Sprinting against the resistance of a large band being held by a partner or anchor.</p>
                        <p><strong>Benefits:</strong> Improves acceleration mechanics and explosive power by forcing you to drive hard against resistance.</p>
                    </div>
                </details>
                <details>
                    <summary>Lateral Bound</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A plyometric exercise where you jump from side to side off one foot, landing on the other.</p>
                        <p><strong>Benefits:</strong> Develops lateral power, agility, and the ability to absorb and redirect force.</p>
                    </div>
                </details>
                <details>
                    <summary>Box Shuffle</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Shuffling laterally up onto and down from a low box.</p>
                        <p><strong>Benefits:</strong> Improves lateral quickness, coordination, and cardiovascular fitness.</p>
                    </div>
                </details>
                <details>
                    <summary>Dot Drill</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Jumping between a pattern of dots on the floor as quickly as possible.</p>
                        <p><strong>Benefits:</strong> A classic drill for improving foot speed, agility, and coordination.</p>
                    </div>
                </details>
                <details>
                    <summary>Hurdle Hops</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Jumping over a series of low hurdles.</p>
                        <p><strong>Benefits:</strong> A plyometric exercise that improves reactive strength, vertical power, and coordination.</p>
                    </div>
                </details>
                <details>
                    <summary>Sled Pull (with rope)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pulling a sled towards you hand-over-hand using a long, thick rope.</p>
                        <p><strong>Benefits:</strong> Builds tremendous grip, back, and bicep strength and endurance.</p>
                    </div>
                </details>
                <details>
                    <summary>Heavy Bag Punching/Kicking</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Performing boxing or martial arts strikes on a heavy bag.</p>
                        <p><strong>Benefits:</strong> An incredible conditioning workout that develops power, coordination, and core strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Crawling Patterns (e.g., Spiderman Crawl)</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Various forms of crawling that challenge the body in different ways, like the Spiderman crawl where you bring your knee to your elbow.</p>
                        <p><strong>Benefits:</strong> Improves mobility, stability, and coordination. A great way to warm up and connect the body.</p>
                    </div>
                </details>
                <details>
                    <summary>GHD Sit-Up</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A sit-up performed on a Glute-Ham Developer, allowing for a greater range of motion where the torso goes past parallel to the floor.</p>
                        <p><strong>Benefits:</strong> A powerful exercise for strengthening the abs and hip flexors through a large range of motion.</p>
                    </div>
                </details>
                <details>
                    <summary>Back Extension</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Performed on a 45-degree back extension or GHD machine, this involves hinging at the hips to lower and raise the torso.</p>
                        <p><strong>Benefits:</strong> Strengthens the lower back (spinal erectors), glutes, and hamstrings.</p>
                    </div>
                </details>
                <details>
                    <summary>Reverse Hyperextension</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lying face down on a machine or box, the lifter raises their legs behind them by extending the hips.</p>
                        <p><strong>Benefits:</strong> Strengthens the posterior chain with less spinal compression than other exercises. Excellent for lower back health.</p>
                    </div>
                </details>
                <details>
                    <summary>Landmine Press</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Pressing the end of a barbell anchored in a landmine unit from shoulder height up and away from the body.</p>
                        <p><strong>Benefits:</strong> A shoulder-friendly pressing variation that builds upper body strength and core stability.</p>
                    </div>
                </details>
                <details>
                    <summary>Landmine Squat</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A squat performed while holding the end of a landmine-anchored barbell at chest height.</p>
                        <p><strong>Benefits:</strong> The arcing motion of the bar makes it a very accessible and natural-feeling squat variation, great for beginners.</p>
                    </div>
                </details>
                <details>
                    <summary>Landmine Row</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A row performed by pulling the end of a landmine-anchored barbell towards the chest.</p>
                        <p><strong>Benefits:</strong> Allows for a strong contraction in the back muscles and is easy to set up.</p>
                    </div>
                </details>
                <details>
                    <summary>Barbell Rollout</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Kneeling on the floor, roll a loaded barbell away from you, extending your torso, and then pull it back in.</p>
                        <p><strong>Benefits:</strong> A highly challenging core exercise that builds anti-extension strength.</p>
                    </div>
                </details>
                <details>
                    <summary>Ab Wheel Rollout</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> The classic version of the rollout performed with a dedicated ab wheel.</p>
                        <p><strong>Benefits:</strong> Builds a rock-solid core by resisting spinal extension. One of the most effective abdominal exercises.</p>
                    </div>
                </details>
                <details>
                    <summary>Hanging Windshield Wipers</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Hanging from a bar, raise your legs and then rotate them from side to side like a car's windshield wipers.</p>
                        <p><strong>Benefits:</strong> An advanced core exercise that builds incredible strength in the abs and obliques.</p>
                    </div>
                </details>
                <details>
                    <summary>Dragon Flag</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Made famous by Bruce Lee. Lying on a bench and holding on behind your head, lift your entire body into a straight line and then lower it with control, keeping the body rigid.</p>
                        <p><strong>Benefits:</strong> The ultimate test of total-body core strength, particularly eccentric control of the abdominals.</p>
                    </div>
                </details>
                <details>
                    <summary>Medicine Ball Slam</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lift a medicine ball overhead, rising onto your toes, then use your entire body to slam the ball into the ground in front of you as hard as possible.</p>
                        <p><strong>Benefits:</strong> Develops explosive power, core strength, and cardiovascular endurance. A great outlet for stress and aggression.</p>
                    </div>
                </details>
                <details>
                    <summary>Medicine Ball Rotational Toss</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Stand perpendicular to a solid wall. Hold the medicine ball at your hip, rotate your torso away from the wall, then explosively rotate back and throw the ball against the wall.</p>
                        <p><strong>Benefits:</strong> Builds rotational power through the core and hips, which is crucial for many sports like baseball, golf, and tennis.</p>
                    </div>
                </details>
                <details>
                    <summary>Medicine Ball Overhead Throw for Distance</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Facing an open field, hold a medicine ball at your chest, squat down, and then explosively jump up and forward, throwing the ball overhead for maximum distance.</p>
                        <p><strong>Benefits:</strong> Develops total-body explosive power, mimicking movements like the triple extension in Olympic lifting.</p>
                    </div>
                </details>
                <details>
                    <summary>Medicine Ball Lateral Slam</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Lift a medicine ball up and over one shoulder, then slam it down on the ground just outside the opposite foot. Alternate sides.</p>
                        <p><strong>Benefits:</strong> Targets the obliques and develops power in the transverse (rotational) plane of motion.</p>
                    </div>
                </details>
                <details>
                    <summary>Medicine Ball Chest Pass</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Stand facing a wall or a partner. Hold a medicine ball at your chest and explosively press it forward, extending your arms fully.</p>
                        <p><strong>Benefits:</strong> Develops explosive pushing power in the chest, shoulders, and triceps. A great plyometric exercise for upper body power.</p>
                    </div>
                </details>
                <details>
                    <summary>Medicine Ball Scoop Toss</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> Stand facing a wall. Hold a medicine ball with both hands between your legs. Hinge at the hips, then explosively extend your hips and knees, scooping the ball up and forward against the wall.</p>
                        <p><strong>Benefits:</strong> Builds explosive power in the posterior chain (glutes and hamstrings), similar to a kettlebell swing.</p>
                    </div>
                </details>
                <details>
                    <summary>Medicine Ball Rainbow Slam</summary>
                    <div class="details-content">
                        <p><strong>Explanation:</strong> A variation of the lateral slam where you trace a large "rainbow" arc with the ball from one side of your body, up over your head, and down to slam on the other side.</p>
                        <p><strong>Benefits:</strong> A dynamic, full-body movement that challenges coordination and develops rotational and anti-rotational core strength.</p>
                    </div>
                </details>
            </section>
        </main>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const sections = document.querySelectorAll('.exercise-section');

            navLinks.forEach(link => {
                link.addEventListener('click', function() {
                    // Deactivate all links and sections
                    navLinks.forEach(l => l.classList.remove('active'));
                    sections.forEach(s => s.classList.remove('active'));

                    // Activate the clicked link
                    this.classList.add('active');

                    // Activate the target section
                    const targetId = this.getAttribute('data-target');
                    const targetSection = document.getElementById(targetId);
                    if (targetSection) {
                        targetSection.classList.add('active');
                    }
                });
            });
        });
    </script>

</body>
</html>
