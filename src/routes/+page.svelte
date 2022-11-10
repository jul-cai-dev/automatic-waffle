<script lang="ts">
    import Job from "$lib/Job.svelte";
    import Particles from "$lib/Particles.svelte";

    let hlbSkills = {
        "primary" : ["Blockchain", "Angular", "Angular Material", "Web3", "Solidity", "AWS", "Lambda", "Go", "NodeJS"],
        "secondary" : ["Mathematics", "Typescript", "Sass", "React", "Redux", "Bootstrap", "GitHub Actions", "Semantic Release", "Cognito", "EC2"]
    }

    let kelennFTSkills = {
        "primary" : ["Real-Time Computing", "Distributed Systems", "C++", "C#", "WPF", "ASP.NET Core", "Angular", "Angular Material"],
        "secondary" : ["AVX-2/AVX-512", "ASP.NET MVC", "WinForms", "Typescript", "Sass", "Go", "Python", "PostgreSQL"]
    }

    let kelennInternSkills = {
        "primary" : ["C#", "WinForms", "ASP.NET MVC 5", "AngularJS", "Angular Material"],
        "secondary" : ["Python", "PostgreSQL"]
    }

    let TTEntrepreneursSkills = {
        "primary" : ["AngularJS", "jQuery", "Bootstrap", "Python", "Django"],
        "secondary" : ["Python", "Jade", "MongoDB", "Neo4j", "PostgreSQL"]
    }

    let openEMASkills = {
        "primary" : ["Perl", "CGI Scripting"],
        "secondary" : ["Webmin", "System Administration"]
    }
</script>

<style>
    .wavey {
        background-color: #374151;
        animation: wave 20s infinite linear;
    }

    .foamey {
        background-color: #1E293B;
        animation: wave2 20s infinite linear;
    }

    .wavey-sm {
        background-color: #374151;
        animation: wave-sm 20s infinite linear;
    }

    .foamey-sm {
        background-color: #1E293B;
        animation: wave2-sm 20s infinite linear;
    }
</style>

<div class="flex flex-col relative bg-gray-900">
    <div class="absolute h-full w-full z-10 invisible md:visible foamey"></div>
    <div class="absolute h-full w-full z-20 invisible md:visible wavey">
        <div class=" w-full h-full min-h-full z-30">
            <Particles />
        </div>
    </div>
    <div class="absolute h-full w-full z-10 visible md:invisible foamey-sm"></div>
    <div class="absolute h-full w-full z-20 visible md:invisible wavey-sm">
        <div class=" w-full h-full min-h-full z-30">
            <Particles id={1} limit="{30}" />
        </div>
    </div>
    <div class="flex flex-col relative items-center space-y-4 bg-gray-900 pb-12 mt-4">
        <img class="w-48 h-48 border-gray border-2 rounded-full z-30" src="images/mugshot.jpg" alt="Mugshot" />
        <div class="z-30">
            <h1 class="text-slate-100 text-3xl text-center">Julian CAILLE</h1>
            <h2 class="text-slate-300 text-center">Software Engineer</h2>
            <div class="flex flex-row items-center justify-center space-x-1">
                <img class="h-4 border-[1px]" src="images/fr.svg" alt="French Flag" />
                <h3 class="text-slate-300 text-center text-xs">CET</h3>
            </div>
        </div>
        <div class="z-30">
            <div class="flex flex-row bg-green-100 text-green-800 text-sm font-medium pl-2 rounded dark:bg-green-200 dark:text-green-900">
                <div>
                    <span class="absolute animate-ping inline-flex mt-1 h-3 w-3 rounded-full bg-green-400 opacity-75"></span>
                    <span class="relative inline-flex rounded-full mt-1 h-3 w-3 bg-green-500"></span>
                </div>
                <span class="pl-1.5 text-center pr-2.5">Looking for a remote job</span>
            </div>
        </div>
        <a class="flex flex-row z-30" href="mailto:jul.cai.dev@gmail.com">
            <img class="h-4 mt-1.5 mr-1" src="images/envelope-icon.png" alt="Email Icon" />
            <span class="text-slate-100 underline">Contact me</span>
        </a>
    </div>
</div>

<div class="flex min-h-screen justify-center items-start bg-gray-900 box-border sm:p-4 p-2">
    <div class="max-w-5xl w-full space-y-20">
        <div class="flex flex-col space-y-8">
            <h2 class="text-slate-100 text-2xl">About me</h2>
            <p class="text-slate-300">I am a french software engineer with 6 years of professional experience. I have worked in multiple different fields, such as Industrial Printing, Mail Routing, Data Analysis, and more recently, Blockchain technologies. I like taking on new challenges and working on projects with a rich tech stack. I am currently available and looking for a full-time remote job.</p>
        </div>
        <div class="flex flex-col space-y-4">
            <h2 class="text-slate-100 text-2xl mb-4">Experience</h2>
            <div class="border-box p-4">
                <Job skills={hlbSkills}>
                    <span slot="Company Name">Humble Luck Ball</span>
                    <span slot="Position">Chief Technical Officer</span>
                    <span slot="Duration">Mar 2021 - Sep 2022</span>
                    <span slot="Description">I designed and implemented a new blockchain protocol called Proof-Of-Entry in the form of modular Smart Contracts. I developed multiple dAPPs and serverless services around the protocol. Successfully deployed a testnet platform for end-users to use the protocol.</span>
                </Job>
            </div>
            <div class="flex justify-center">
                <div class="w-2 h-24 rounded-sm bg-slate-100"></div>
            </div>
            <div class="border-box p-4">
                <Job skills={kelennFTSkills}>
                    <span slot="Company Name">Kelenn Technology</span>
                    <span slot="Position">Lead Software Engineer</span>
                    <span slot="Duration">Mar 2017 - Mar 2021</span>
                    <span slot="Description">I was in charge of a small team of 5 developers while designing and implementing software for industrial printers, physical mail routing, industrial site supervision and various new technologies. I worked on distributed systems and low latency solutions, as well as desktop GUIs and web apps. I also trained and supervized 8 interns/trainees in software engineering.</span>
                </Job>
            </div>
            <div class="flex justify-center">
                <div class="w-2 h-24 rounded-sm bg-slate-100"></div>
            </div>
            <div class="border-box p-4">
                <Job skills={kelennInternSkills}>
                    <span slot="Company Name">Kelenn Technology</span>
                    <span slot="Position">Part-Time Software Engineer Intern</span>
                    <span slot="Duration">Sep 2016 - Mar 2017</span>
                    <span slot="Description">I debugged/fixed a production release and shipped new releases of a mail routing software used by the french national printing-house (Imprimerie Nationale). I designed and developed a web-app and a set of services to supervize the mailing site of a major french bank company (Société Générale).</span>
                </Job>
            </div>
            <div class="flex justify-center">
                <div class="w-2 h-24 rounded-sm bg-slate-100"></div>
            </div>
            <div class="border-box p-4">
                <Job skills={TTEntrepreneursSkills}>
                    <span slot="Company Name">33 Entrepreneurs</span>
                    <span slot="Position">Data Analyst/Developer Intern</span>
                    <span slot="Duration">Apr 2015 - Aug 2015</span>
                    <span slot="Description">I worked on a prototype for a startup analysis platform. I coded web scraping and data analysis services, designed databases and developed a web application for the platform. Finished with a minimum viable product, usable by data analysts at the company.</span>
                </Job>
            </div>
            <div class="flex justify-center">
                <div class="w-2 h-24 rounded-sm bg-slate-100"></div>
            </div>
            <div class="border-box p-4">
                <Job skills={openEMASkills}>
                    <span slot="Company Name">OpenEMA</span>
                    <span slot="Position">Software Developer Intern</span>
                    <span slot="Duration">Jul 2013 - Dec 2013</span>
                    <span slot="Description">I developed a customized N.A.S administration panel based on Webmin. I coded pluggable modules to configure services through CGI scripts for Slitaz GNU/Linux.</span>
                </Job>
            </div>
        </div>
        <div class="flex flex-col space-y-4">
            <h2 class="text-slate-100 text-2xl mb-4">Education</h2>
            <div class="flex flex-wrap justify-between">
                <div class="flex flex-row space-x-2 mt-4 items-center sm:items-start">
                    <img class="h-16 px-2 lg:px-0" src="images/epitech-sm-logo.png" alt="Epitech Logo" />
                    <div>
                        <div class="flex flex-row justify-between">
                            <h3 class="text-slate-100 text-xl">Epitech</h3>
                            <h3 class="text-slate-300">2012 - 2017</h3>
                        </div>
                        <h4 class="text-slate-300">Master - Expert in Information Technology</h4>
                    </div>
                </div>
                <div class="flex flex-row space-x-2 mt-4 items-center sm:items-start">
                    <img class="h-16" src="images/BJTU-sm-logo.png" alt="BJTU Logo" />
                    <div>
                        <div class="flex flex-row justify-between">
                            <h3 class="text-slate-100 text-xl">BJTU</h3>
                            <h3 class="text-slate-300">2015 - 2016</h3>
                        </div>
                        <h4 class="text-slate-300">Master in Software Engineering (Intl Year)</h4>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex flex-col space-y-4">
            <h2 class="text-slate-100 text-2xl mb-4">Hobbies</h2>
            <div class="flex flex-wrap mt-4 justify-between items-center sm:items-start">
                <div class="flex flex-row">
                    <img class="h-16" src="images/blender_community_badge_white.png" alt="Blender Community Badge" />
                    <h3 class="text-slate-100 text-xl pt-3.5">3D Modeling</h3>
                </div>
                <div class="flex flex-row">
                    <img class="h-16" src="images/infosec.png" alt="Information Security Icon" />
                    <h3 class="text-slate-100 text-xl pt-3.5 pl-1">Infosec</h3>
                </div>
                <div class="flex flex-row">
                    <img class="h-16" src="images/forest.png" alt="Forest Icon" />
                    <h3 class="text-slate-100 text-xl pt-3.5 pl-1">Hiking</h3>
                </div>
            </div>
        </div>
        <div class="flex flex-row justify-center" style="margin-top: 59px;">
            <span class="text-slate-300 text-sm">2022 Julian CAILLE</span>
        </div>
    </div>
</div>