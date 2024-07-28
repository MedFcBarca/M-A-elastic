Mini App
Cette mini application est développée en Node.js avec Express. Elle inclut des logs applicatifs et des tests unitaires, et est intégrée avec ESLint pour l'analyse de la qualité du code. Les tests unitaires et l'analyse de la qualité du code sont déclenchés automatiquement par un pipeline GitHub Actions lors d'un push sur la branche main.


Etape 1 installation:

Prérequis
Node.js (version 18 recommandée)
npm (version 6 ou supérieure)
Elasticsearch, Kibana et Logstash installés et configurés
Installation
Clonez le dépôt :

-npm install express supertest jest
-Exécuter l'application:
node index.js

-Tester l'application avec curl


curl -X POST http://localhost:3000/add -H "Content-Type: application/json" -d '{"a": 5, "b": 3}'

Étape 2 : Écrire des logs applicatifs dans un fichier local
Les logs sont déjà écrits dans un fichier app.log grâce au middleware dans index.js.

Etape 3:
./bin/elasticsearch
./bin/logstash -f config/logstash.conf
./bin/kibana
puis http://localhost:5601

pour les tests unitaires :
npm test
sinon npm test -- --detectOpenHandles
# M-A-elastic
