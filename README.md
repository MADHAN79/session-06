# Session-06 Task :

JSON FORMAT :

```
{
  "name": "John Doe",
  "contact": {
    "email": "johndoe@example.com",
    "phone": "+1234567890",
    "address": "123 Developer St, Tech City, USA",
    "linkedIn": "https://linkedin.com/in/johndoe",
    "github": "https://github.com/johndoe"
  },
  "summary": "Full Stack MERN Developer with 5+ years of experience in building scalable web applications and APIs. Expertise in React, Node.js, Express, and MongoDB. Passionate about creating efficient solutions and working on innovative projects.",
  "skills": {
    "languages": ["JavaScript", "HTML", "CSS", "Python"],
    "frontend": ["React.js", "Redux", "Tailwind CSS", "Bootstrap"],
    "backend": ["Node.js", "Express.js", "REST APIs", "GraphQL"],
    "database": ["MongoDB", "MySQL"],
    "tools": ["Git", "Docker", "Webpack", "Babel", "Jest", "Postman"],
    "cloud": ["AWS", "Heroku", "Render", "Netlify"]
  },
  "experience": [
    {
      "company": "Tech Solutions",
      "position": "Senior Full Stack Developer",
      "duration": "March 2021 - Present",
      "responsibilities": [
        "Led the development of a highly scalable e-commerce platform using React and Node.js.",
        "Collaborated with cross-functional teams to design and implement RESTful APIs.",
        "Optimized application performance, reducing load times by 30%.",
        "Integrated third-party services such as payment gateways and SMS notifications."
      ],
      "technologies": ["React.js", "Node.js", "Express.js", "MongoDB", "AWS"]
    },
    {
      "company": "Innovative Web Solutions",
      "position": "Full Stack Developer",
      "duration": "January 2018 - February 2021",
      "responsibilities": [
        "Developed and maintained front-end applications using React and Redux.",
        "Implemented server-side logic with Node.js and Express, handling various RESTful API requests.",
        "Worked on improving application security and optimized performance for better user experience.",
        "Mentored junior developers and assisted with code reviews and project management."
      ],
      "technologies": ["React.js", "Node.js", "Express.js", "MongoDB", "Heroku"]
    }
  ],
  "projects": [
    {
      "name": "E-commerce Platform",
      "description": "Built a fully functional e-commerce platform with features such as user authentication, product management, and payment integration.",
      "technologies": ["React.js", "Node.js", "Express.js", "MongoDB", "Stripe"],
      "role": "Full Stack Developer",
      "github": "https://github.com/johndoe/ecommerce-platform"
    },
    {
      "name": "Task Management App",
      "description": "Developed a task management app to help teams track and manage their tasks efficiently.",
      "technologies": ["React.js", "Node.js", "Express.js", "MongoDB", "JWT"],
      "role": "Frontend & Backend Developer",
      "github": "https://github.com/johndoe/task-manager"
    },
    {
      "name": "Blog Website",
      "description": "Created a dynamic blogging platform with features such as user login, blog creation, and comments.",
      "technologies": ["React.js", "Node.js", "Express.js", "MongoDB", "JWT"],
      "role": "Full Stack Developer",
      "github": "https://github.com/johndoe/blog-website"
    },
    {
      "name": "Portfolio Website",
      "description": "Designed a personal portfolio website to showcase my work and projects.",
      "technologies": ["React.js", "HTML", "CSS", "Tailwind CSS"],
      "role": "Frontend Developer",
      "github": "https://github.com/johndoe/portfolio-website"
    },
    {
      "name": "Real-Time Chat Application",
      "description": "Built a real-time chat application using WebSocket for seamless communication between users.",
      "technologies": ["React.js", "Node.js", "Express.js", "Socket.IO"],
      "role": "Full Stack Developer",
      "github": "https://github.com/johndoe/chat-app"
    }
  ],
  "education": {
    "degree": "Bachelor of Science in Computer Science",
    "institution": "Tech University",
    "graduationYear": 2017
  },
  "certifications": [
    {
      "name": "AWS Certified Solutions Architect",
      "date": "July 2020"
    },
    {
      "name": "Full Stack Web Development Certificate",
      "institution": "Coursera",
      "date": "May 2019"
    }
  ]
}
```

# Iteration Methods :
Below are examples of how to iterate over this JSON structure using different loops.

## 1. for loop

const resume = /* the JSON object above */;
for (let i = 0; i < resume.projects.length; i++) {
  console.log("Project Name:", resume.projects[i].name);
}

## 2. for...in loop

for (let key in resume) {
  console.log("Key:", key);
  if (Array.isArray(resume[key])) {
    resume[key].forEach(item => console.log(item));
  }
}

## 3. for...of loop

for (let project of resume.projects) {
  console.log("Project Description:", project.description);
}

## 4. forEach method

resume.experience.forEach((job) => {
  console.log(`Company: ${job.company}, Position: ${job.position}`);
});
