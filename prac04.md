# Week 4 - Development and deployment workflows

## Learning Activities
[Information architecture | LinkedIn Learning](https://www.linkedin.com/learning/mapping-the-modern-web-design-process)

[- How to Set Up a Local WordPress Environment (XAMPP Tutorial)](https://www.youtube.com/watch?v=suV93rTmTuA&t=312s)

[- Instantly Create A Local Development Environment - Beginner To Pro](https://www.youtube.com/watch?v=TXqSC2od4-8&t=54s)

[Easy Local WordPress Setup in 5 Minutes with Docker!](https://www.youtube.com/watch?v=gEceSAJI_3s&t=896s)

## Estimated Hours
8 hours

## Content Insights
I learned about the importance of planning the modern web design process, which is a crucial step before diving into any development. Mapping out the structure and user experience helps keep everything organised and focused. I explored different ways to set up a local development environment, especially for WordPress. While I initially tried using XAMPP, I ran into a lot of issues. Eventually, I learned about Docker and how it simplifies the setup process for local WordPress sites. I didn’t realise how much easier it would be to manage environments with Docker until I gave it a try.

## Career/Employability/Learning Insights

I successfully set up a local WordPress site using Docker, which was a huge win. While I struggled with XAMPP, Docker proved far more reliable and efficient. The tutorials I watched helped me understand the process of setting up local environments and gave me a clearer picture of why Docker is so widely used in development. This knowledge will be useful in future projects, especially when working with WordPress or any other platform that requires a local environment. Overall, this experience reinforced the importance of being open to trying new tools and techniques, even if things don’t go as planned the first time.


# Setting Up My Local Environment 

following through with one of the videos mentioned above - [Easy Local WordPress Setup in 5 Minutes with Docker!](https://www.youtube.com/watch?v=gEceSAJI_3s&t=896s)
the first step was ensuring that Docker was installed on my computer. Next, I created a docker-compose.yml file to define the services I needed for WordPress, including MySQL, phpMyAdmin, and WordPress itself. To securely store important details like the database name, user, password, and root password, I set up a .env file, which helped keep sensitive data organised.
Finally, I ran docker-compose to start all the containers.

When I first tried accessing localhost:8080 in my browser, the site wasn’t available, and I got an error saying, "Error establishing a database connection" I wasn’t sure what went wrong, so I started checking Docker logs and the configuration files. It turned out that the issue was related to a database connection problem.
After a bit of digging, I figured out that the issue was a simple typo in my .env file. It was such a small mistake in one of the database credentials, but it was enough to stop WordPress from connecting to MySQL. I fixed the typo, ran docker-compose up -d --build to rebuild the containers, and tried accessing the site again. It was a good reminder that even the smallest errors can cause a lot of frustration, but that’s also part of the process. I’ve learned to be patient and persistent, and now I feel more confident working with Docker.
