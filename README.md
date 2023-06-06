# cit281-lab4
## Part 1: Create initial Fastify Node.js web server
// Require the Fastify framework and instantiate it
const fastify = require("fastify")();
// Handle GET verb for / route using Fastify
// Note use of "chain" dot notation syntax
fastify.get("/", (request, reply) => {
  reply
    .code(200)
    .header("Content-Type", "text/text; charset=utf-8")
    .send("<h1>Hello from Lab 4!</h1>");
});
// Start server and listen to requests using Fastify
const listenIP = "localhost";
const listenPort = 8080;
fastify.listen(listenPort, listenIP, (err, address) => {
  if (err) {
    console.log(err);
    process.exit(1);
  }
  console.log(`Server listening on ${address}`);
});
## Part 2: Initialize as a Node.js project folder using Node Package Manager (npm)
npm init -y
## Part 3: Add Fastify to project using npm, and test using Visual Studio Code (VSCode)
npm install fastify --save
## Part 4: Add git repo, exclude node_modules folder from git, make commits
<img width="184" alt="Screenshot 2023-06-06 at 9 19 10 AM" src="https://github.com/mmathes2/cit281-lab4/assets/134009490/e7d606d2-00f3-4c4b-8bf9-e7ee10f65c18">

## Part 5: Fix MIME error, test, and commit
<img width="472" alt="Screenshot 2023-06-06 at 9 22 52 AM" src="https://github.com/mmathes2/cit281-lab4/assets/134009490/2e12076e-814d-4b47-9152-46b391420174">

## Part 6: Add a second route with query parameters, test, and commit
http://127.0.0.1:8080/name?first=firstName&last=lastName
