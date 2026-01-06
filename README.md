"# ahmed-web" 
<!DOCTYPE html>
<html lang="en">
<head>
    <base target="_self">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Greenwood Academy | Excellence in Education</title>
    <meta name="description" content="Greenwood Academy - A premier educational institution providing quality education from kindergarten to high school. Modern facilities, experienced faculty, and holistic development.">
    <meta name="keywords" content="school, education, academy, learning, students, teachers, curriculum">
    <meta name="author" content="Greenwood Academy">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: "#1e40af",
                        secondary: "#0ea5e9",
                        accent: "#f59e0b",
                        dark: "#1e293b",
                        light: "#f8fafc"
                    },
                    fontFamily: {
                        'sans': ['Inter', 'system-ui', 'sans-serif'],
                        'display': ['Poppins', 'system-ui', 'sans-serif']
                    },
                    animation: {
                        'fade-in': 'fadeIn 0.5s ease-in-out',
                        'slide-up': 'slideUp 0.5s ease-out'
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' }
                        },
                        slideUp: {
                            '0%': { transform: 'translateY(20px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' }
                        }
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Poppins:wght@400;500;600;700&display=swap');
        
        .hero-gradient {
            background: linear-gradient(135deg, #1e40af 0%, #0ea5e9 100%);
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: #f59e0b;
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
    </style>
</head>
<body class="font-sans text-gray-800 bg-light">
    <!-- Cookie Consent Banner -->
    <div id="cookieConsent" class="fixed bottom-0 left-0 right-0 bg-dark text-white p-4 z-50 hidden">
        <div class="container mx-auto flex flex-col md:flex-row items-center justify-between">
            <p class="mb-4 md:mb-0">We use cookies to enhance your experience. By continuing to visit this site you agree to our use of cookies.</p>
            <div class="flex space-x-4">
                <button onclick="acceptCookies()" class="bg-accent text-white px-6 py-2 rounded-lg hover:bg-yellow-600 transition">Accept</button>
                <button onclick="declineCookies()" class="bg-gray-600 text-white px-6 py-2 rounded-lg hover:bg-gray-700 transition">Decline</button>
            </div>
        </div>
    </div>

    <!-- Header & Navigation -->
    <header class="sticky top-0 z-40 bg-white shadow-md">
        <div class="container mx-auto px-4">
            <div class="flex items-center justify-between py-4">
                <!-- Logo -->
                <div class="flex items-center space-x-3">
                    <div class="w-12 h-12 bg-primary rounded-full flex items-center justify-center">
                        <i class="fas fa-graduation-cap text-white text-2xl"></i>
                    </div>
                    <div>
                        <h1 class="text-2xl font-bold text-primary">Greenwood Academy</h1>
                        <p class="text-sm text-gray-600">Excellence in Education</p>
                    </div>
                </div>

                <!-- Desktop Navigation -->
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="nav-link text-gray-700 hover:text-primary font-medium">Home</a>
                    <a href="#about" class="nav-link text-gray-700 hover:text-primary font-medium">About Us</a>
                    <a href="#academics" class="nav-link text-gray-700 hover:text-primary font-medium">Academics</a>
                    <a href="#admissions" class="nav-link text-gray-700 hover:text-primary font-medium">Admissions</a>
                    <a href="#facilities" class="nav-link text-gray-700 hover:text-primary font-medium">Facilities</a>
                    <a href="#contact" class="nav-link text-gray-700 hover:text-primary font-medium">Contact</a>
                    <button onclick="showLoginModal()" class="bg-primary text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition">Portal Login</button>
                </nav>

                <!-- Mobile Menu Button -->
                <button id="mobileMenuButton" class="md:hidden text-gray-700">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>

            <!-- Mobile Navigation -->
            <div id="mobileMenu" class="md:hidden hidden py-4 border-t">
                <div class="flex flex-col space-y-4">
                    <a href="#home" class="text-gray-700 hover:text-primary font-medium py-2">Home</a>
                    <a href="#about" class="text-gray-700 hover:text-primary font-medium py-2">About Us</a>
                    <a href="#academics" class="text-gray-700 hover:text-primary font-medium py-2">Academics</a>
                    <a href="#admissions" class="text-gray-700 hover:text-primary font-medium py-2">Admissions</a>
                    <a href="#facilities" class="text-gray-700 hover:text-primary font-medium py-2">Facilities</a>
                    <a href="#contact" class="text-gray-700 hover:text-primary font-medium py-2">Contact</a>
                    <button onclick="showLoginModal()" class="bg-primary text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition w-full">Portal Login</button>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero-gradient text-white">
        <div class="container mx-auto px-4 py-20">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="animate-fade-in">
                    <h2 class="text-4xl md:text-5xl font-bold mb-6 font-display">Shaping Future Leaders Through Quality Education</h2>
                    <p class="text-xl mb-8 opacity-90">At Greenwood Academy, we nurture young minds with a perfect blend of academic excellence, character building, and holistic development.</p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-6">
                        <button onclick="scrollToSection('admissions')" class="bg-accent text-white px-8 py-3 rounded-lg text-lg font-semibold hover:bg-yellow-600 transition transform hover:scale-105">Apply Now</button>
                        <button onclick="scrollToSection('about')" class="bg-white text-primary px-8 py-3 rounded-lg text-lg font-semibold hover:bg-gray-100 transition">Learn More</button>
                    </div>
                </div>
                <div class="animate-slide-up">
                    <img 
                        src="https://picsum.photos/600/400?random=1" 
                        alt="Students learning in modern classroom" 
                        class="rounded-2xl shadow-2xl"
                        loading="lazy"
                    />
                </div>
            </div>
        </div>
    </section>

    <!-- Quick Stats -->
    <section class="bg-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                <div class="text-center">
                    <div class="text-4xl font-bold text-primary mb-2">1500+</div>
                    <div class="text-gray-600">Students Enrolled</div>
                </div>
                <div class="text-center">
                    <div class="text-4xl font-bold text-primary mb-2">120+</div>
                    <div class="text-gray-600">Qualified Faculty</div>
                </div>
                <div class="text-center">
                    <div class="text-4xl font-bold text-primary mb-2">25+</div>
                    <div class="text-gray-600">Years Experience</div>
                </div>
                <div class="text-center">
                    <div class="text-4xl font-bold text-primary mb-2">98%</div>
                    <div class="text-gray-600">Graduation Rate</div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">About Greenwood Academy</h2>
                <p class="text-gray-600 max-w-3xl mx-auto">Established in 1998, we have been at the forefront of providing quality education that combines traditional values with modern teaching methodologies.</p>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <img 
                        src="https://picsum.photos/600/400?random=2" 
                        alt="School campus and facilities" 
                        class="rounded-2xl shadow-lg"
                        loading="lazy"
                    />
                </div>
                <div>
                    <h3 class="text-2xl font-bold text-dark mb-6">Our Mission & Vision</h3>
                    <p class="text-gray-700 mb-6">Our mission is to provide a nurturing environment that fosters intellectual growth, character development, and social responsibility. We believe in empowering students to become lifelong learners and responsible global citizens.</p>
                    
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <i class="fas fa-check-circle text-accent text-xl mt-1 mr-3"></i>
                            <div>
                                <h4 class="font-semibold text-dark">Holistic Development</h4>
                                <p class="text-gray-600">Focus on academic, physical, emotional, and social growth</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <i class="fas fa-check-circle text-accent text-xl mt-1 mr-3"></i>
                            <div>
                                <h4 class="font-semibold text-dark">Innovative Teaching</h4>
                                <p class="text-gray-600">Modern teaching methods with technology integration</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <i class="fas fa-check-circle text-accent text-xl mt-1 mr-3"></i>
                            <div>
                                <h4 class="font-semibold text-dark">Safe Environment</h4>
                                <p class="text-gray-600">Secure campus with 24/7 surveillance and safety protocols</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Academics Section -->
    <section id="academics" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">Academic Programs</h2>
                <p class="text-gray-600 max-w-3xl mx-auto">Comprehensive curriculum designed to meet the needs of every student from kindergarten through high school.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Elementary -->
                <div class="bg-white rounded-2xl shadow-lg p-8 card-hover">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-child text-primary text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-dark mb-4">Elementary School</h3>
                    <p class="text-gray-600 mb-6">Grades K-5: Building strong foundations in literacy, numeracy, and social skills through interactive learning.</p>
                    <ul class="space-y-2 mb-6">
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>Interactive Learning</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>Art & Music Programs</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>Physical Education</span>
                        </li>
                    </ul>
                </div>
                
                <!-- Middle School -->
                <div class="bg-white rounded-2xl shadow-lg p-8 card-hover">
                    <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-users text-primary text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-dark mb-4">Middle School</h3>
                    <p class="text-gray-600 mb-6">Grades 6-8: Developing critical thinking and problem-solving skills with specialized subject teachers.</p>
                    <ul class="space-y-2 mb-6">
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>STEM Programs</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>Foreign Languages</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>Leadership Development</span>
                        </li>
                    </ul>
                </div>
                
                <!-- High School -->
                <div class="bg-white rounded-2xl shadow-lg p-8 card-hover">
                    <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-graduation-cap text-primary text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-dark mb-4">High School</h3>
                    <p class="text-gray-600 mb-6">Grades 9-12: College preparatory curriculum with AP courses and career guidance.</p>
                    <ul class="space-y-2 mb-6">
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>AP Courses</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>College Counseling</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-check text-accent mr-2"></i>
                            <span>Career Preparation</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Facilities Section -->
    <section id="facilities" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">Our Facilities</h2>
                <p class="text-gray-600 max-w-3xl mx-auto">State-of-the-art infrastructure designed to support comprehensive learning and development.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-white rounded-2xl overflow-hidden shadow-lg card-hover">
                    <img 
                        src="https://picsum.photos/400/300?random=3" 
                        alt="Modern science laboratory" 
                        class="w-full h-48 object-cover"
                        loading="lazy"
                    />
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-dark mb-3">Science Labs</h3>
                        <p class="text-gray-600">Fully equipped physics, chemistry, and biology laboratories for hands-on learning.</p>
                    </div>
                </div>
                
                <div class="bg-white rounded-2xl overflow-hidden shadow-lg card-hover">
                    <img 
                        src="https://picsum.photos/400/300?random=4" 
                        alt="School library with books" 
                        class="w-full h-48 object-cover"
                        loading="lazy"
                    />
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-dark mb-3">Digital Library</h3>
                        <p class="text-gray-600">Extensive collection of books, e-books, and research materials with computer access.</p>
                    </div>
                </div>
                
                <div class="bg-white rounded-2xl overflow-hidden shadow-lg card-hover">
                    <img 
                        src="https://picsum.photos/400/300?random=5" 
                        alt="Sports ground and facilities" 
                        class="w-full h-48 object-cover"
                        loading="lazy"
                    />
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-dark mb-3">Sports Complex</h3>
                        <p class="text-gray-600">Basketball court, football field, swimming pool, and indoor sports facilities.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Admissions Section -->
    <section id="admissions" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <h2 class="text-3xl md:text-4xl font-bold text-dark mb-6">Admissions Open for 2024-25</h2>
                    <p class="text-gray-700 mb-8">Join our community of learners and achievers. Limited seats available for all grades. Early application is encouraged.</p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <div class="bg-primary text-white rounded-full w-10 h-10 flex items-center justify-center mr-4 flex-shrink-0">
                                <span class="font-bold">1</span>
                            </div>
                            <div>
                                <h4 class="font-semibold text-dark mb-2">Submit Application</h4>
                                <p class="text-gray-600">Complete the online application form with required documents</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-primary text-white rounded-full w-10 h-10 flex items-center justify-center mr-4 flex-shrink-0">
                                <span class="font-bold">2</span>
                            </div>
                            <div>
                                <h4 class="font-semibold text-dark mb-2">Assessment & Interview</h4>
                                <p class="text-gray-600">Student assessment and parent interview scheduled</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-primary text-white rounded-full w-10 h-10 flex items-center justify-center mr-4 flex-shrink-0">
                                <span class="font-bold">3</span>
                            </div>
                            <div>
                                <h4 class="font-semibold text-dark mb-2">Admission Decision</h4>
                                <p class="text-gray-600">Notification of admission status within 2 weeks</p>
                            </div>
                        </div>
                    </div>
                    
                    <button onclick="showAdmissionForm()" class="mt-8 bg-primary text-white px-8 py-3 rounded-lg text-lg font-semibold hover:bg-blue-700 transition">Start Application</button>
                </div>
                
                <div class="bg-gray-50 rounded-2xl p-8 shadow-lg">
                    <h3 class="text-2xl font-bold text-dark mb-6">Important Dates</h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-center justify-between border-b pb-4">
                            <div>
                                <h4 class="font-semibold text-dark">Application Deadline</h4>
                                <p class="text-gray-600">For 2024-25 Academic Year</p>
                            </div>
                            <div class="text-right">
                                <div class="font-bold text-primary">March 31, 2024</div>
                            </div>
                        </div>
                        
                        <div class="flex items-center justify-between border-b pb-4">
                            <div>
                                <h4 class="font-semibold text-dark">Entrance Tests</h4>
                                <p class="text-gray-600">Grades 6-12</p>
                            </div>
                            <div class="text-right">
                                <div class="font-bold text-primary">April 15, 2024</div>
                            </div>
                        </div>
                        
                        <div class="flex items-center justify-between border-b pb-4">
                            <div>
                                <h4 class="font-semibold text-dark">Academic Year Begins</h4>
                                <p class="text-gray-600">First day of school</p>
                            </div>
                            <div class="text-right">
                                <div class="font-bold text-primary">August 15, 2024</div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-8 p-4 bg-blue-50 rounded-lg">
                        <h4 class="font-semibold text-dark mb-2">Need Help?</h4>
                        <p class="text-gray-600 mb-4">Contact our admissions office for assistance</p>
                        <div class="flex items-center">
                            <i class="fas fa-phone text-primary mr-3"></i>
                            <span class="font-semibold">(555) 123-4567</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- News & Events -->
    <section class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">Latest News & Events</h2>
                <p class="text-gray-600 max-w-3xl mx-auto">Stay updated with the latest happenings at Greenwood Academy</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white rounded-2xl overflow-hidden shadow-lg card-hover">
                    <img 
                        src="https://picsum.photos/400/300?random=6" 
                        alt="Science fair exhibition" 
                        class="w-full h-48 object-cover"
                        loading="lazy"
                    />
                    <div class="p-6">
                        <div class="text-sm text-accent font-semibold mb-2">February 15, 2024</div>
                        <h3 class="text-xl font-bold text-dark mb-3">Annual Science Fair 2024</h3>
                        <p class="text-gray-600 mb-4">Students showcase innovative projects in our annual science exhibition. Open to public on Saturday.</p>
                        <a href="#" class="text-primary font-semibold hover:underline">Read More →</a>
                    </div>
                </div>
                
                <div class="bg-white rounded-2xl overflow-hidden shadow-lg card-hover">
                    <img 
                        src="https://picsum.photos/400/300?random=7" 
                        alt="Sports tournament" 
                        class="w-full h-48 object-cover"
                        loading="lazy"
                    />
                    <div class="p-6">
                        <div class="text-sm text-accent font-semibold mb-2">March 5, 2024</div>
                        <h3 class="text-xl font-bold text-dark mb-3">Inter-School Sports Tournament</h3>
                        <p class="text-gray-600 mb-4">Our basketball team wins regional championship. Congratulations to all participants!</p>
                        <a href="#" class="text-primary font-semibold hover:underline">Read More →</a>
                    </div>
                </div>
                
                <div class="bg-white rounded-2xl overflow-hidden shadow-lg card-hover">
                    <img 
                        src="https://picsum.photos/400/300?random=8" 
                        alt="Parent teacher meeting" 
                        class="w-full h-48 object-cover"
                        loading="lazy"
                    />
                    <div class="p-6">
                        <div class="text-sm text-accent font-semibold mb-2">March 20, 2024</div>
                        <h3 class="text-xl font-bold text-dark mb-3">Parent-Teacher Conference</h3>
                        <p class="text-gray-600 mb-4">Quarterly meetings scheduled for March 25-27. Book your slot through the parent portal.</p>
                        <a href="#" class="text-primary font-semibold hover:underline">Read More →</a>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <button onclick="window.location.href='#news'" class="bg-white text-primary border-2 border-primary px-8 py-3 rounded-lg font-semibold hover:bg-primary hover:text-white transition">View All News</button>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">Contact Us</h2>
                <p class="text-gray-600 max-w-3xl mx-auto">We'd love to hear from you. Reach out for inquiries, visits, or general information.</p>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <!-- Contact Information -->
                <div>
                    <div class="space-y-8">
                        <div class="flex items-start">
                            <div class="bg-primary text-white rounded-full w-12 h-12 flex items-center justify-center mr-4 flex-shrink-0">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-dark mb-2">Visit Our Campus</h3>
                                <p class="text-gray-600">123 Education Lane, Greenwood City, GC 12345</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-primary text-white rounded-full w-12 h-12 flex items-center justify-center mr-4 flex-shrink-0">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-dark mb-2">Call Us</h3>
                                <p class="text-gray-600">Main Office: (555) 123-4567</p>
                                <p class="text-gray-600">Admissions: (555) 123-4568</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-primary text-white rounded-full w-12 h-12 flex items-center justify-center mr-4 flex-shrink-0">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-dark mb-2">Email Us</h3>
                                <p class="text-gray-600">info@greenwoodacademy.edu</p>
                                <p class="text-gray-600">admissions@greenwoodacademy.edu</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-primary text-white rounded-full w-12 h-12 flex items-center justify-center mr-4 flex-shrink-0">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-dark mb-2">Office Hours</h3>
                                <p class="text-gray-600">Monday - Friday: 8:00 AM - 4:30 PM</p>
                                <p class="text-gray-600">Saturday: 9:00 AM - 12:00 PM</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-12">
                        <h3 class="text-xl font-bold text-dark mb-6">Follow Us</h3>
                        <div class="flex space-x-4">
                            <a href="#" class="w-12 h-12 bg-gray-100 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition">
                                <i class="fab fa-facebook-f"></i>
                            </a>
                            <a href="#" class="w-12 h-12 bg-gray-100 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition">
                                <i class="fab fa-twitter"></i>
                            </a>
                            <a href="#" class="w-12 h-12 bg-gray-100 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href="#" class="w-12 h-12 bg-gray-100 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition">
                                <i class="fab fa-youtube"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Contact Form -->
                <div class="bg-gray-50 rounded-2xl p-8 shadow-lg">
                    <h3 class="text-2xl font-bold text-dark mb-6">Send Us a Message</h3>
                    <form id="contactForm" onsubmit="submitContactForm(event)">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label class="block text-gray-700 mb-2" for="name">Full Name *</label>
                                <input type="text" id="name" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2" for="email">Email Address *</label>
                                <input type="email" id="email" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition">
                            </div>
                        </div>
                        
                        <div class="mb-6">
                            <label class="block text-gray-700 mb-2" for="phone">Phone Number</label>
                            <input type="tel" id="phone" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition">
                        </div>
                        
                        <div class="mb-6">
                            <label class="block text-gray-700 mb-2" for="subject">Subject *</label>
                            <select id="subject" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition">
                                <option value="">Select a subject</option>
                                <option value="admissions">Admissions Inquiry</option>
                                <option value="general">General Information</option>
                                <option value="visit">Schedule a Visit</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        
                        <div class="mb-6">
                            <label class="block text-gray-700 mb-2" for="message">Message *</label>
                            <textarea id="message" rows="5" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition"></textarea>
                        </div>
                        
                        <button type="submit" class="w-full bg-primary text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter -->
    <section class="py-16 bg-primary text-white">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-4">Stay Updated</h2>
            <p class="text-xl opacity-90 mb-8 max-w-2xl mx-auto">Subscribe to our newsletter for the latest news, events, and important announcements.</p>
            
            <form id="newsletterForm" onsubmit="subscribeNewsletter(event)" class="max-w-md mx-auto">
                <div class="flex flex-col sm:flex-row gap-4">
                    <input type="email" id="newsletterEmail" required placeholder="Your email address" class="flex-grow px-6 py-3 rounded-lg text-gray-800 outline-none">
                    <button type="submit" class="bg-accent text-white px-8 py-3 rounded-lg font-semibold hover:bg-yellow-600 transition">Subscribe</button>
                </div>
                <p class="text-sm opacity-80 mt-4">We respect your privacy. Unsubscribe at any time.</p>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white">
        <div class="container mx-auto px-4 py-12">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- School Info -->
                <div>
                    <div class="flex items-center space-x-3 mb-6">
                        <div class="w-10 h-10 bg-primary rounded-full flex items-center justify-center">
                            <i class="fas fa-graduation-cap text-white"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold">Greenwood Academy</h3>
                        </div>
                    </div>
                    <p class="text-gray-400 mb-6">Providing quality education since 1998. Nurturing young minds for a better tomorrow.</p>
                </div>
                
                <!-- Quick Links -->
                <div>
                    <h4 class="text-lg font-bold mb-6">Quick Links</h4>
                    <ul class="space-y-3">
                        <li><a href="#home" class="text-gray-400 hover:text-white transition">Home</a></li>
                        <li><a href="#about" class="text-gray-400 hover:text-white transition">About Us</a></li>
                        <li><a href="#academics" class="text-gray-400 hover:text-white transition">Academics</a></li>
                        <li><a href="#admissions" class="text-gray-400 hover:text-white transition">Admissions</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-white transition">Contact</a></li>
                    </ul>
                </div>
                
                <!-- Resources -->
                <div>
                    <h4 class="text-lg font-bold mb-6">Resources</h4>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Parent Portal</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Student Portal</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">School Calendar</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Lunch Menu</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Downloads</a></li>
                    </ul>
                </div>
                
                <!-- Contact Footer -->
                <div>
                    <h4 class="text-lg font-bold mb-6">Contact Info</h4>
                    <ul class="space-y-3">
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt text-accent mt-1 mr-3"></i>
                            <span class="text-gray-400">123 Education Lane, Greenwood City</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone text-accent mr-3"></i>
                            <span class="text-gray-400">(555) 123-4567</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope text-accent mr-3"></i>
                            <span class="text-gray-400">info@greenwoodacademy.edu</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 text-center">
                <p class="text-gray-400">© 2024 Greenwood Academy. All rights reserved.</p>
                <div class="mt-4 text-sm text-gray-500">
                    <a href="#" class="hover:text-white transition mx-4">Privacy Policy</a>
                    <a href="#" class="hover:text-white transition mx-4">Terms of Service</a>
                    <a href="#" class="hover:text-white transition mx-4">Accessibility</a>
                    <a href="#" class="hover:text-white transition mx-4">Sitemap</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Login Modal -->
    <div id="loginModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 hidden items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-md w-full p-8">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold text-dark">Portal Login</h3>
                <button onclick="hideLoginModal()" class="text-gray-500 hover:text-gray-700">
                    <i class="fas fa-times text-2xl"></i>
                </button>
            </div>
            
            <form id="loginForm" onsubmit="handleLogin(event)">
                <div class="mb-6">
                    <label class="block text-gray-700 mb-2" for="loginEmail">Email Address</label>
                    <input type="email" id="loginEmail" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition">
                </div>
                
                <div class="mb-6">
                    <label class="block text-gray-700 mb-2" for="loginPassword">Password</label>
                    <input type="password" id="loginPassword" required class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition">
                </div>
                
                <div class="flex items-center justify-between mb-6">
                    <div class="flex items-center">
                        <input type="checkbox" id="remember" class="mr-2">
                        <label for="remember" class="text-gray-700">Remember me</label>
                    </div>
                    <a href="#" class="text-primary hover:underline">Forgot password?</a>
                </div>
                
                <button type="submit" class="w-full bg-primary text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition mb-4">Login</button>
                
                <div class="text-center">
                    <p class="text-gray-600">Select portal type:</p>
                    <div class="flex justify-center space-x-4 mt-3">
                        <button type="button" onclick="setPortalType('parent')" class="px-4 py-2 bg-gray-100 rounded-lg hover:bg-gray-200 transition">Parent</button>
                        <button type="button" onclick="setPortalType('student')" class="px-4 py-2 bg-gray-100 rounded-lg hover:bg-gray-200 transition">Student</button>
                        <button type="button" onclick="setPortalType('staff')" class="px-4 py-2 bg-gray-100 rounded-lg hover:bg-gray-200 transition">Staff</button>
                    </div>
                </div>
            </form>
        </div>
    </div>

    <!-- Admission Form Modal -->
    <div id="admissionModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 hidden items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-2xl w-full p-8 max-h-[90vh] overflow-y-auto">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold text-dark">Admission Application</h3>
                <button onclick="hideAdmissionModal()" class="text-gray-500 hover:text-gray-700">
                    <i class="fas fa-times text-2xl"></i>
                </button>
            </div>
            
            <form id="admissionForm" onsubmit="submitAdmissionForm(event)">
                <div class="space-y-6">
                    <div>
                        <h4 class="text-lg font-semibold text-dark mb-4">Student Information</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-gray-700 mb-2">First Name *</label>
                                <input type="text" required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Last Name *</label>
                                <input type="text" required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Date of Birth *</label>
                                <input type="date" required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Grade Applying For *</label>
                                <select required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                                    <option value="">Select Grade</option>
                                    <option value="k">Kindergarten</option>
                                    <option value="1">Grade 1</option>
                                    <option value="2">Grade 2</option>
                                    <option value="3">Grade 3</option>
                                    <option value="4">Grade 4</option>
                                    <option value="5">Grade 5</option>
                                    <option value="6">Grade 6</option>
                                    <option value="7">Grade 7</option>
                                    <option value="8">Grade 8</option>
                                    <option value="9">Grade 9</option>
                                    <option value="10">Grade 10</option>
                                    <option value="11">Grade 11</option>
                                    <option value="12">Grade 12</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <h4 class="text-lg font-semibold text-dark mb-4">Parent/Guardian Information</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-gray-700 mb-2">Parent Name *</label>
                                <input type="text" required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Email *</label>
                                <input type="email" required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Phone *</label>
                                <input type="tel" required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Relationship *</label>
                                <select required class="w-full px-4 py-2 rounded-lg border border-gray-300">
                                    <option value="">Select</option>
                                    <option value="mother">Mother</option>
                                    <option value="father">Father</option>
                                    <option value="guardian">Guardian</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <h4 class="text-lg font-semibold text-dark mb-4">Previous School Information</h4>
                        <div class="space-y-4">
                            <div>
                                <label class="block text-gray-700 mb-2">Previous School Name</label>
                                <input type="text" class="w-full px-4 py-2 rounded-lg border border-gray-300">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Reason for Transfer</label>
                                <textarea rows="3" class="w-full px-4 py-2 rounded-lg border border-gray-300"></textarea>
                            </div>
                        </div>
                    </div>
                    
                    <div class="flex items-center">
                        <input type="checkbox" id="terms" required class="mr-2">
                        <label for="terms" class="text-gray-700">I agree to the terms and conditions *</label>
                    </div>
                    
                    <div class="flex justify-end space-x-4">
                        <button type="button" onclick="hideAdmissionModal()" class="px-6 py-2 border border-gray-300 rounded-lg hover:bg-gray-50 transition">Cancel</button>
                        <button type="submit" class="px-6 py-2 bg-primary text-white rounded-lg hover:bg-blue-700 transition">Submit Application</button>
                    </div>
                </div>
            </form>
        </div>
    </div>

    <!-- Success Message -->
    <div id="successMessage" class="fixed top-4 right-4 bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg z-50 hidden">
        <div class="flex items-center">
            <i class="fas fa-check-circle mr-3"></i>
            <span>Your message has been sent successfully!</span>
        </div>
    </div>

    <script>
        // Define data at the beginning
        const schoolData = {
            "name": "Greenwood Academy",
            "address": "123 Education Lane, Greenwood City, GC 12345",
            "phone": "(555) 123-4567",
            "email": "info@greenwoodacademy.edu",
            "established": 1998,
            "grades": ["Kindergarten", "Elementary (1-5)", "Middle School (6-8)", "High School (9-12)"],
            "facultyCount": 120,
            "studentCount": 1500
        };

        const academicPrograms = [
            { "id": 1, "name": "Elementary School", "grades": "K-5", "icon": "fa-child", "color": "blue" },
            { "id": 2, "name": "Middle School", "grades": "6-8", "icon": "fa-users", "color": "green" },
            { "id": 3, "name": "High School", "grades": "9-12", "icon": "fa-graduation-cap", "color": "purple" }
        ];

        const facilities = [
            { "id": 1, "name": "Science Labs", "description": "Fully equipped laboratories", "image": "https://picsum.photos/400/300?random=3" },
            { "id": 2, "name": "Digital Library", "description": "Extensive book collection", "image": "https://picsum.photos/400/300?random=4" },
            { "id": 3, "name": "Sports Complex", "description": "Multiple sports facilities", "image": "https://picsum.photos/400/300?random=5" }
        ];

        // Mobile menu toggle
        document.getElementById('mobileMenuButton').addEventListener('click', function() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
            const icon = this.querySelector('i');
            if (menu.classList.contains('hidden')) {
                icon.className = 'fas fa-bars text-2xl';
            } else {
                icon.className = 'fas fa-times text-2xl';
            }
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    // Close mobile menu if open
                    const mobileMenu = document.getElementById('mobileMenu');
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                        document.getElementById('mobileMenuButton').querySelector('i').className = 'fas fa-bars text-2xl';
                    }
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Scroll to section function
        function scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                window.scrollTo({
                    top: section.offsetTop - 80,
                    behavior: 'smooth'
                });
            }
        }

        // Modal functions
        function showLoginModal() {
            document.getElementById('loginModal').classList.remove('hidden');
            document.body.style.overflow = 'hidden';
        }

        function hideLoginModal() {
            document.getElementById('loginModal').classList.add('hidden');
            document.body.style.overflow = 'auto';
        }

        function showAdmissionForm() {
            document.getElementById('admissionModal').classList.remove('hidden');
            document.body.style.overflow = 'hidden';
        }

        function hideAdmissionModal() {
            document.getElementById('admissionModal').classList.add('hidden');
            document.body.style.overflow = 'auto';
        }

        // Portal type selection
        function setPortalType(type) {
            const buttons = document.querySelectorAll('#loginModal button[type="button"]');
            buttons.forEach(btn => {
                btn.classList.remove('bg-primary', 'text-white');
                btn.classList.add('bg-gray-100');
            });
            
            const activeBtn = event.target;
            activeBtn.classList.remove('bg-gray-100');
            activeBtn.classList.add('bg-primary', 'text-white');
            
            // Update form action based on portal type
            const form = document.getElementById('loginForm');
            form.action = `/login/${type}`;
        }

        // Form submission handlers
        function handleLogin(e) {
            e.preventDefault();
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            
            // In a real application, this would be an API call
            console.log('Login attempt:', { email, password });
            
            // Show success message
            showSuccessMessage('Login successful! Redirecting...');
            setTimeout(() => {
                hideLoginModal();
                // Redirect to portal dashboard
                window.location.href = '/dashboard';
            }, 1500);
        }

        function submitContactForm(e) {
            e.preventDefault();
            
            const formData = {
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                subject: document.getElementById('subject').value,
                message: document.getElementById('message').value
            };
            
            // In a real application, this would be an API call
            console.log('Contact form submitted:', formData);
            
            // Show success message
            showSuccessMessage('Thank you! Your message has been sent.');
            
            // Reset form
            document.getElementById('contactForm').reset();
            
            // Hide success message after 3 seconds
            setTimeout(() => {
                hideSuccessMessage();
            }, 3000);
        }

        function submitAdmissionForm(e) {
            e.preventDefault();
            
            // In a real application, this would be an API call
            console.log('Admission form submitted');
            
            // Show success message
            showSuccessMessage('Application submitted successfully! We will contact you soon.');
            
            // Hide modal after delay
            setTimeout(() => {
                hideAdmissionModal();
                hideSuccessMessage();
            }, 2000);
        }

        function subscribeNewsletter(e) {
            e.preventDefault();
            
            const email = document.getElementById('newsletterEmail').value;
            
            // In a real application, this would be an API call
            console.log('Newsletter subscription:', email);
            
            // Show success message
            showSuccessMessage('Thank you for subscribing to our newsletter!');
            
            // Reset form
            document.getElementById('newsletterForm').reset();
            
            // Hide success message after 3 seconds
            setTimeout(() => {
                hideSuccessMessage();
            }, 3000);
        }

        // Success message functions
        function showSuccessMessage(text) {
            const message = document.getElementById('successMessage');
            if (text) {
                message.querySelector('span').textContent = text;
            }
            message.classList.remove('hidden');
            setTimeout(() => {
                message.classList.add('hidden');
            }, 3000);
        }

        function hideSuccessMessage() {
            document.getElementById('successMessage').classList.add('hidden');
        }

        // Cookie consent functions
        function checkCookies() {
            if (!localStorage.getItem('cookiesAccepted')) {
                setTimeout(() => {
                    document.getElementById('cookieConsent').classList.remove('hidden');
                }, 1000);
            }
        }

        function acceptCookies() {
            localStorage.setItem('cookiesAccepted', 'true');
            document.getElementById('cookieConsent').classList.add('hidden');
        }

        function declineCookies() {
            localStorage.setItem('cookiesAccepted', 'false');
            document.getElementById('cookieConsent').classList.add('hidden');
        }

        // Close modals when clicking outside
        document.addEventListener('click', function(e) {
            const loginModal = document.getElementById('loginModal');
            const admissionModal = document.getElementById('admissionModal');
            
            if (e.target === loginModal) {
                hideLoginModal();
            }
            if (e.target === admissionModal) {
                hideAdmissionModal();
            }
        });

        // Close modals with Escape key
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                hideLoginModal();
                hideAdmissionModal();
            }
        });

        // Initialize on page load
        document.addEventListener('DOMContentLoaded', function() {
            checkCookies();
            
            // Add current year to footer
            const yearSpan = document.querySelector('footer p:first-of-type');
            if (yearSpan) {
                yearSpan.innerHTML = yearSpan.innerHTML.replace('2024', new Date().getFullYear());
            }
            
            // Lazy load images
            const images = document.querySelectorAll('img[loading="lazy"]');
            const imageObserver = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const img = entry.target;
                        img.src = img.dataset.src || img.src;
                        observer.unobserve(img);
                    }
                });
            });
            
            images.forEach(img => imageObserver.observe(img));
        });

        // Form validation helper
        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        }

        function validatePhone(phone) {
            const re = /^[\+]?[1-9][\d]{0,15}$/;
            return re.test(phone.replace(/[\s\-\(\)]/g, ''));
        }
    </script>
</body>
</html>
