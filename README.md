
Devops / SRE TakeHome Hiring Process

---

## Challenge Introduction
It is designed to challenge and provide an instructive and fun experience.
It should demonstrate that you understand the world of containers and microservices.

We know that you are probably very busy, and we won't discard your submission because of that. Feel free to just describe your solutions if you run out of time, but we'd prefer code and a working environment. Even if you describe your solution, make sure to include plenty of detail to help to show exactly what factors you have considered.

Feel free to ask questions, and we will respond to you on your board.
Feel free to contact us for any further information about the role.

## In general:

- Take as much time as you want but we wish to hear from you within a week. 
- Please, explain your solutions in detail, to allow us to see everything that you have considered.
- You don't need to finish all the tasks. Share your results even if you don't finish.
- Small, meaningful commits are recommended.
- Your workflow is important as it shows us that you are systematic in your approach to work.

All the best!

---

## Components

### 1. Simple Service Webapp

We have a `as simple as possible` Golang application, and your first mission is to create a Docker image for it. 

Checkout the project: https://github.com/Onefootball/simple-service.git

- Create a `Dockerfile` for it.
- Push it to an **container repository** (ecr, gcr, docker-hub etc) of your choice. Why? Needed in `[2]`

Please use the private `GitHub` repository created for you and commit your work there.
So, In the end, we will review your steps and decide the next step in the interview process.

---

### 2. Setup Kubernetes

- Install `kubeadm` or `minikube` in your local workstation to deploy image build in `[1]`.
- Create K8s' `Service` running with `HPA` configured to use CPU for scaling.
- Deploy a `StatefulSet pod` which needs persistency. You can deploy anything, for ex: Mysql, Redis, PostgreSQL, RabbitMQ and so on.
- Extend the app built in `[1]` or create another app (if you are not comfortable with golang) which can do simple interaction (for ex: [redis ping-pong](https://redis.io/commands/ping)) with the stateful pod.

---

### 3. Monitoring (Prometheus/Grafana)

- Setup basic `monitoring` for the StatefulSet pod (**sidecar container** can be helpful if container natively doesn't expose metrics) which can be scraped by prometheus engine.
- Deploy `Prometheus` for monitoring targets (only stateful services)
- `[BONUS]` Deploy `Grafana` to plot dashboard. Grafana community has dashboards which can be used in this case. 

Examples:
- https://grafana.com/grafana/dashboards/763
- https://grafana.com/grafana/dashboards/4279
- https://grafana.com/grafana/dashboards/4031

---

### Feedback

Even if you are not able to complete, please give us feedback on how was your experience with this assignment in a `.md` file.

```
# FEEDBACK.md
- Did you like the test? To difficult, To easy, Ah! Its Okay
- How much time did you spend?
- What can be improved? Ex: Better explanations of the challenge.
```
