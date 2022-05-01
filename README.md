Welcome to the AWS CodeStar sample web service
==================================================

This sample code helps get you started with a simple Java web service
deployed by AWS CodeDeploy and AWS CloudFormation to an Amazon EC2 server.

What's Here
-----------

This sample includes:

* README.md - this file
* appspec.yml - this file is used by AWS CodeDeploy when deploying the web
  service to EC2
* buildspec.yml - this file is used by AWS CodeBuild to build the web
  service
* pom.xml - this file is the Maven Project Object Model for the web service
* src/main - this directory contains your Java service source files
* src/test - this directory contains your Java service unit test files
* scripts/ - this directory contains scripts used by AWS CodeDeploy when
  installing and deploying your service on the Amazon EC2 instance
* template.yml - this file contains the description of AWS resources used by AWS
  CloudFormation to deploy your infrastructure
* template-configuration.json - this file contains the project ARN with placeholders used for tagging resources with the project ID

Getting Started
---------------

These directions assume you want to develop on your local computer, and not
from the Amazon EC2 instance itself. If you're on the Amazon EC2 instance, the
virtual environment is already set up for you, and you can start working on the
code.

To work on the sample code, you'll need to clone your project's repository to your
local computer. If you haven't, do that first. You can find instructions in the AWS CodeStar user guide at https://docs.aws.amazon.com/codestar/latest/userguide/getting-started.html#clone-repo.

1. Install maven.  See https://maven.apache.org/install.html for details.

2. Install tomcat.  See https://tomcat.apache.org/tomcat-8.0-doc/setup.html for
   details.

3. Build the service.

        $ mvn -f pom.xml compile
        $ mvn -f pom.xml package

4. Copy the built service to the Tomcat webapp directory.  The actual
   location of that directory will vary depending on your platform and
   installation.

        $ cp target/ROOT.war <tomcat webapp directory>

4. Restart your tomcat server

5. Open http://127.0.0.1:8080/ in a web browser to view your service.

What Do I Do Next?
------------------

Once you have a virtual environment running, you can start making changes to
the sample Java web service. We suggest making a small change to
/src/main/java/com/aws/codestar/projecttemplates/controller/HelloWorldController.java
first, so you can see how changes pushed to your project's repository are automatically
picked up by your project pipeline and deployed to the Amazon EC2 instance. (You can watch
the pipeline progress on your project dashboard.) Once you've seen how that works, start
developing your own code, and have fun!

To run your tests locally, go to the root directory of the sample code and run the
`mvn clean compile test` command, which AWS CodeBuild also runs through your `buildspec.yml` file.

To test your new code during the release process, modify the existing tests or add tests
to the tests directory. AWS CodeBuild will run the tests during the build stage of your
project pipeline. You can find the test results in the AWS CodeBuild console.

Learn more about Maven's [Standard Directory Layout](https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html).

Learn more about AWS CodeBuild and how it builds and tests your application here:
https://docs.aws.amazon.com/codebuild/latest/userguide/concepts.html

Learn more about AWS CodeStar by reading the user guide. Ask questions or make
suggestions on our forum.

User Guide: https://docs.aws.amazon.com/codestar/latest/userguide/welcome.html

Forum: https://forums.aws.amazon.com/forum.jspa?forumID=248

How Do I Add Template Resources to My Project?
------------------

To add AWS resources to your project, you'll need to edit the `template.yml`
file in your project's repository. You may also need to modify permissions for
your project's worker roles. After you push the template change, AWS CodeStar
and AWS CloudFormation provision the resources for you.

See the AWS CodeStar user guide for instructions to modify your template:
https://docs.aws.amazon.com/codestar/latest/userguide/how-to-change-project.html#customize-project-template

What Should I Do Before Running My Project in Production?
------------------

AWS recommends you review the security best practices recommended by the framework
author of your selected sample application before running it in production. You
should also regularly review and apply any available patches or associated security
advisories for dependencies used within your application.

Best Practices: https://docs.aws.amazon.com/codestar/latest/userguide/best-practices.html?icmpid=docs_acs_rm_sec

-----------------------------------------------------------------------------


Malan, boa tarde!

Segue o teste para vaga que está concorrendo.  


SOLUÇÃO ALUNOS 

Uma escola está precisando de uma aplicação web para cadastro de alunos.
A ideia é criar uma aplicação de demonstração a área da escola ver como será entregue nosso trabalho. Nesse primeiro instante a aplicação deverá contemplar cadastro e consulta, não nos preocuparemos com a alteração e exclusão. 
Na consulta, deverá consumir uma API já em produção que irá trazer uma lista de cursos no qual esse aluno será cadastrado. 
Contando com sua ajuda, desenvolva uma aplicação web para cadastro e consulta de alunos.  
O modelo Aluno deverá conter: 
•	Código do aluno; 
•	Nome do Aluno; 
•	CPF; 
•	Telefones celular; 
•	Status; 
•	Curso; (Lista da API) 
•	Data de matricula 

API para pegar a lista de cursos:   

Method GET 

URL: https://gatewayext.cruzeirodosul.edu.br/entrevista/teste/cursos 

 

Não deixe de utilizar: 
•	Maven; 
•	Java 8; 
•	Banco de dados ( H2, Mysql, Postgree, ou outro de sua preferência); 
•	Tomcat 9 (ou Embed Tomcat, caso utilize Spring Boot); 
•	JSF ou Spring boot. 

 
Fique livre para utilizar qualquer outra tecnologia ou framework em que você se sinta confortável em trabalhar ou que ache importante no projeto.  
Para frontend pode ser em JSF, Angular, Thymeleaf, ou qualquer outro da sua preferência. 
 
Caso se sinta mais a vontade de usar um objeto de banco de dados (function ou procedure) pode construir o cadastro ou consulta e depois chamar no JAVA. 
Será um diferencial a implementação de TDD, Designer Patterns e Clean Code. 
 
Ao final, para entregar seu projeto, responda a esse e-mail com: 
•	A Url do Github; 
•	Ou com o link do Dropbox ou Google Drive; 



Obrigada e sucesso! 

