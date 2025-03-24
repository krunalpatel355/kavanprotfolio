# Kavan Gajjar's Portfolio

Welcome to the repository for **Kavan Gajjar's Portfolio**, a showcase of 3D modeling, animation, and motion design expertise. This project is built using **Flask** and features a responsive design with **Bootstrap**.

<!-- ![Portfolio Screenshot](generated-icon.png) -->

## Table of Contents
awf
- [About](#about)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Deployment to AWS EC2](#deployment-to-aws-ec2)
- [License](#license)

## About

This portfolio highlights the creative journey and technical skills of Kavan Gajjar, a 3D artist and animator. It includes sections for projects, skills, resume, and more.

## Features

- **Dynamic Web Pages**: Built with Flask and Jinja2 templates.
- **Responsive Design**: Styled with Bootstrap for mobile and desktop compatibility.
- **Interactive Projects Section**: Filterable project showcase.
- **Video Showcase**: Embedded video player with thumbnail navigation.
- **Skills Overview**: Visual representation of technical and creative skills.

## Technologies Used

- **Frontend**: HTML, CSS (Bootstrap, custom styles), JavaScript
- **Backend**: Python (Flask)
- **Containerization**: Docker
- **CI/CD**: GitHub Actions

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/kavangajjar/portfolio.git
   cd portfolio
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python app.py
   ```

4. Open your browser and navigate to `http://127.0.0.1:5000`.

## Usage

- **Home Page**: Overview of Kavan Gajjar's expertise and featured projects.
- **Projects**: Explore detailed project showcases with filtering options.
- **Skills**: Visualize technical and creative skills.
- **Resume**: View professional experience and qualifications.
- **About**: Learn more about Kavan's journey and approach.

## Project Structure

```
KavanPortfolio/
├── app.py               # Flask application
├── Dockerfile           # Docker configuration
├── requirements.txt     # Python dependencies
├── static/              # Static assets (CSS, images, videos)
├── templates/           # HTML templates
├── .github/workflows/   # CI/CD pipeline
```

## Deployment to AWS EC2

This project includes a GitHub Actions workflow for automated deployment to an AWS EC2 instance. The deployment process involves the following steps:

1. **Pre-requisites**:
   - Ensure the `kavan.pem` file (your EC2 key pair) is present in the project root.
   - Update the EC2 instance's public IP address in the `.github/workflows/ci-cd.yml` file.

2. **Workflow Steps**:
   - On every push to the `master` branch, the workflow will:
     - SSH into the EC2 instance using the `kavan.pem` key.
     - Pull the latest code from the repository.
     - Build and run the Docker container.

3. **Access the Application**:
   - After deployment, the application will be accessible at `http://<EC2-Public-IP>`.

**Note**: For security reasons, avoid committing sensitive files like `.pem` keys to public repositories.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

Feel free to contribute or reach out for collaboration opportunities!