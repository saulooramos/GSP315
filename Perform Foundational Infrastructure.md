## Perform Foundational Infrastructure Tasks in Google Cloud: Challenge Lab ##

>You are now asked to help a newly formed development team with some of their initial work on a new project around storing and organizing photographs, called memories. You have been asked to assist the memories team with initial configuration for their application development environment; you receive the following request to complete the following tasks:

* Create a bucket for storing the photographs.
* Create a Pub/Sub topic that will be used by a Cloud Function you create.
* Create a Cloud Function.
* Remove the previous cloud engineer’s access from the memories project.
* Some Jooli Inc. standards you should follow:

1. Create all resources in the us-east1 region and us-east1-b zone, unless otherwise directed.
2. Use the project VPCs.
3. Naming is normally team-resource, e.g. an instance could be named kraken-webserver1
4. Allocate cost effective resource sizes. Projects are monitored and excessive resource use will result in the containing project's termination (and possibly yours), so beware. This is the guidance the monitoring team is willing to share; unless directed, use f1-micro for small Linux VMs and n1-standard-1 for Windows or other applications such as Kubernetes nodes.
5. Each task is described in detail below, good luck!

> Task 1 - Criando um Bucket

1. Primeiro, é importante setar o projeto: `gcloud config set project` **NOME DO SEU PROJETO**
2. Para criar um Bucket é só utilizar o console na página do Cloud Storage
3. Sugestão de nome para o seu bucket: `SeuNomeGCPBucket`

>Task 2 - Criando um Pub/Sub topic

1. Primeiro, persquise por pub/sub
2. Para criar um tópico é só utilizar o console na página do Pub/Sub
3. Sugestão de nome para o seu topic: `SeuNomeTopic`

>Task 3 - Criando o Thumbnail no CloudFunctions

1. Primeiro, pesquise por cloud functions
2. Quando for setar o Trigger, selecione Cloud Storage, evento: Finalize/Create e selecione o bucket criado
3. Selecione Node.js 14 (conforme solicitado)
4. Escreva `thumbnail`no Entry point
5. Copie o código da função e cole na parte do código da cloud function (lembrando de trocar o ID do tópico no código)
6. Copie também o código do package.json e cole na parte do código da cloud function

>Task 4 - Retire o acesso de Cloud engineer do memories project

>Task 5 - Faça upload de uma imagem para o bucket

1. Utilize o link disponibilizado, clique com o botão direito > salvar.
2. Faça o upload da imagem baixada para o bucket criado.
