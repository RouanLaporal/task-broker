## 1. Problem
Une application doit pouvoir sous traité un traitement lourd sans avoir à attendre un résultat.
## 2. Goals
L'objectif est de pouvoir enregistrer les jobs reçus, qui seront ensuite traité par des worker.
## 3. Non-goals
## 4. Job lifecycle
Un job aura le cylce de vie suivant : QUEUED --> PROCESSING -->COMPLETED/FAILED
## 5. Initial API
l'API exposera les endpoints : 
    GET /health
    POST /jobs
    GET /jobs/:id
## 6. Technical constraints
Les frameworks HTTP sont interdits :
Express
Fastify
NestJS
Hono
Koa
## 7. Architecture
Clinet --> HTTP Server-->Application-->Queue