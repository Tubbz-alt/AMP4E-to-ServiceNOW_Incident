# AMP4E-to-ServiceNOW_Incident

*This code utilizes the API capabilities from Cisco AMP for Endpoints to create ServiceNOW incidents*

---

**ToDo's:**

- [✓] Consider writing your README first.  Doing so helps you clarify your intent, focuses your project, and it is much more fun to write documentation at the beginning of a project than at the end of one, see:
    - [Readme Driven Development](http://tom.preston-werner.com/2010/08/23/readme-driven-development.html)
    - [GitHub Guides: Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [✓] Ensure you put the [license and copyright header](./HEADER) at the top of all your source code files.
- [✓] Be mindful of the third-party materials you use and ensure you follow Cisco's policies for creating and sharing Cisco Sample Code.

---

## Motivation

Working at various companies, ServiceNOW has been the ITSM tool of choice and often times, engineers and managers want some integration between various systems and tools into this platform. So the motivation is to provide an example of what can be accomplished with Cisco's platforms and other platforms.

## Show Me!

What visual, if shown, clearly articulates the impact of what you have created?  In as concise a visualization as possible (code sample, CLI output, animated GIF, or screenshot) show what your project makes possible.

## Features

- Go through all the AMP connectors installed in your environment and collect events that have a Malicious disposition and create an Incident for them into ServiceNOW.

## Technologies & Frameworks Used

The technologies used are Cisco's AMP for Endpoints, ServiceNOW for ITSM and optionally AWS Lambda to run the code in the cloud if desired.

**Cisco Products & Services:**

- Cisco AMP for Endpoints

**Third-Party Products & Services:**

- ServiceNOW (any current version)
- AWS Lambda

**Tools & Frameworks:**

- chalice

## Usage

Command line
```
$ python3 amp4e-servicenow-incident.py
```
On AWS Lambda executing every 120 seconds.
```
$ virtualenv venv
$ source venv/bin/activate
$ pip3 install chalice
$ pip3 install requests
$ chalice new-project lambda-AMP4E-ServiceNOW
$ cd lambda-AMP4E-ServiceNOW
## Replace the app.py file with the one in this git repo under the chalice directory. Also remember to put your own data in.
$ chalice deploy
## To remove run chalice delete
```

## Installation

Provide a step-by-step series of examples and explanations for how to install your project and its dependencies.

## Authors & Maintainers

Smart people responsible for the creation and maintenance of this project:

- George Seeto <geseeto@cisco.com>

## Credits
Credit to Cisco Dev-NET and the folks who hosted the Dev-NET workshop I was able to attend in December, 2018. In addition ServiceNOW inspiration comes from various companies I have come from where ServiceNOW was the main ITSM application of choice. 

## License

This project is licensed to you under the terms of the [Cisco Sample
Code License](./LICENSE).
