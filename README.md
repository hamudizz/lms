<div align="center" markdown="1">

<img src=".github/lms-logo.png" alt="Lawh Learning logo" width="80" height="80"/>
<h1>Lawh Learning</h1>

**Easy to use, open source, Learning Management System**

![Tests](https://img.shields.io/endpoint?url=https://dashboard.cypress.io/badge/simple/vandxn/main&style=flat&logo=cypress)

</div>


<div align="center">
	<img src=".github/hero.png?v=5" alt="Hero Image" width="72%" />
</div>
<br />
<div align="center">
	<a href="https://Lawh.io/learning">Website</a>
	-
	<a href="https://docs.Lawh.io/learning">Documentation</a>
</div>

## Lawh Learning
Lawh Learning is an easy-to-use learning system that helps you bring structure to your content.

### Motivation
In 2021, we were looking for a Learning Management System to launch [Mon.School](https://mon.school) for FOSS United. We checked out Moodle, but it didn’t feel right. The forms were unnecessarily lengthy and the UI was confusing. It shouldn't be this hard to create a course right? So I started making a learning system for Mon.School which soon became a product in itself. The aim is to have a simple platform that anyone can use to launch a course of their own and make knowledge sharing easier.

### Key Features

- **Structured Learning**: Design a course with a 3-level hierarchy, where your courses have chapters and you can group your lessons within these chapters. This ensures that the context of the lesson is set by the chapter.

- **Live Classes**: Group learners into batches based on courses and duration. You can then create Zoom live class for these batches right from the app. Learners get to see the list of live classes they have to take as a part of this batch.

- **Quizzes and Assignments**: Create quizzes where questions can have single-choice, multiple-choice options, or can be open ended. Instructors can also add assignments which learners can submit as PDF's or Documents.

- **Getting Certified**: Once a learner has completed the course or batch, you can grant them a certificate. The app provides an inbuilt certificate template. You can use this or else create a template of your own and use that instead.

<details>
<summary>View Screenshots</summary>


![Batch](.github/batch.png)
<div align="center">
	<sub>
		Create batches to group your learners
	</sub>
</div>
<br>


![Quiz](.github/quiz.png)
<div align="center">
	<sub>
		Evaluate their knowledge by quizzes
	</sub>
</div>
<br>


![Cerficicate](.github/certificate.png)
<div align="center">
	<sub>
		Autenticate their work with certification
	</sub>
</div>
</details>


### Under the Hood

- [**Lawh Framework**](https://github.com/Lawh/Lawh): A full-stack web application framework.

- [**Lawh UI**](https://github.com/Lawh/Lawh-ui): A Vue-based UI library, to provide a modern user interface.

## Production Setup

### Managed Hosting

You can try [Lawh Cloud](https://Lawhcloud.com), a simple, user-friendly and sophisticated [open-source](https://github.com/Lawh/press) platform to host Lawh applications with peace of mind.

It takes care of installation, setup, upgrades, monitoring, maintenance and support of your Lawh deployments. It is a fully featured developer platform with an ability to manage and control multiple Lawh deployments.

<div>
	<a href="https://Lawhcloud.com/lms/signup" target="_blank">
		<picture>
			<source media="(prefers-color-scheme: dark)" srcset="https://Lawh.io/files/try-on-fc-white.png">
			<img src="https://Lawh.io/files/try-on-fc-black.png" alt="Try on Lawh Cloud" height="28" />
		</picture>
	</a>
</div>

### Self Hosting

Follow these steps to set up Lawh Learning in production:

**Step 1**: Download the easy install script

```bash
wget https://Lawh.io/easy-install.py
```

**Step 2**: Run the deployment command

```bash
python3 ./easy-install.py deploy \
    --project=learning_prod_setup \
    --email=your_email.example.com \
    --image=ghcr.io/Lawh/lms \
    --version=stable \
    --app=lms \
    --sitename subdomain.domain.tld
```

Replace the following parameters with your values:
- `your_email.example.com`: Your email address
- `subdomain.domain.tld`: Your domain name where Learning will be hosted

The script will set up a production-ready instance of Lawh Learning with all the necessary configurations in about 5 minutes.

**Note:** To avoid a `404 Page Not Found` error:
- If hosting on a **public server**, make sure your DNS **A record** points to your server's IP.
- If hosting **locally**, map your domain to `127.0.0.1` in your `/etc/hosts` file:

## Development Setup

### Docker

You need Docker, docker-compose and git setup on your machine. Refer [Docker documentation](https://docs.docker.com/). After that, follow below steps:

**Step 1**: Setup folder and download the required files

    mkdir Lawh-learning
    cd Lawh-learning

    # Download the docker-compose file
    wget -O docker-compose.yml https://raw.githubusercontent.com/Lawh/lms/develop/docker/docker-compose.yml

    # Download the setup script
    wget -O init.sh https://raw.githubusercontent.com/Lawh/lms/develop/docker/init.sh

**Step 2**: Run the container and daemonize it

    docker compose up -d

**Step 3**: The site [http://lms.localhost:8000/lms](http://lms.localhost:8000/lms) should now be available. The default credentials are:
- Username: Administrator
- Password: admin

### Local

To setup the repository locally follow the steps mentioned below:

1. Install bench and setup a `Lawh-bench` directory by following the [Installation Steps](https://Lawhframework.com/docs/user/en/installation)
1. Start the server by running `bench start`
1. In a separate terminal window, create a new site by running `bench new-site learning.test`
1. Map your site to localhost with the command `bench --site learning.test add-to-hosts`
1. Get the Learning app. Run `bench get-app https://github.com/Lawh/lms`
1. Run `bench --site learning.test install-app lms`.
1. Now open the URL `http://learning.test:8000/lms` in your browser, you should see the app running

## Learn and connect

- [Telegram Public Group](https://t.me/Lawhlms)
- [Discuss Forum](https://discuss.Lawh.io/c/lms/70)
- [Documentation](https://docs.Lawh.io/learning)
- [YouTube](https://www.youtube.com/channel/UCn3bV5kx77HsVwtnlCeEi_A)

<br>
<br>
<div align="center" style="padding-top: 0.75rem;">
	<a href="https://Lawh.io" target="_blank">
		<picture>
			<source media="(prefers-color-scheme: dark)" srcset="https://Lawh.io/files/Lawh-white.png">
			<img src="https://Lawh.io/files/Lawh-black.png" alt="Lawh Technologies" height="28"/>
		</picture>
	</a>
</div>
