# Phishing para captura de senhas do Facebook

### Ferramentas

- Kali Linux
- setoolkit

### Configurando o Phishing no Kali Linux

- Acesso root: ``` sudo su ```
- Iniciando o setoolkit: ``` setoolkit ```
- Tipo de ataque: ``` Social-Engineering Attacks ```
- Vetor de ataque: ``` Web Site Attack Vectors ```
- Método de ataque: ```Credential Harvester Attack Method ```
- Método de ataque: ``` Site Cloner ```
- Obtendo o endereço da máquina: ``` ifconfig ```
- URL para clone: http://www.facebook.com

### Resutados

![Alt text](./passwd.png "Optional title")

### Problema com o método padrão do SEToolkit:

O site clonado do SEToolkit usa um método simples de captura de credenciais baseado na interceptação de formulários. No entanto, sites como o Facebook usam HTTPS e recursos avançados de segurança, como CSP (Content Security Policy) e verificações de integridade, que dificultam a captura direta de credenciais por meio do clone.

### Subir uma página clone própria:

Criar uma página clone permite mais controle. Com isso, você pode capturar entradas diretamente e ajustar o comportamento do formulário

1- crie o diretorio  da pagina ```sudo mkdir /home/pagina_clone```
2- após criado, crie ou copie o arquivo da pagina clonada
  2.1-```nano /home/pagina_clone``` e dentro do arquivo cole o codigo da pagina clonada (https://github.com/Anoiim/cibersecurity-desafio-phishing/blob/Anoiim-patch-1/facebook_clone)
3- após os processos feitos os proximos oassi são:

- Tipo de ataque: ``` Social-Engineering Attacks ```
- Vetor de ataque: ``` Web Site Attack Vectors ```
- Método de ataque: ```Credential Harvester Attack Method ```
-```Custom Import```
-aperte enter
-aperte enter novamente
-passe o caminho do site clonado, neste caso ```/home/pagina_clone```
-aparte enter novamente (a ferramenta por padrão escohe o arquivo index.html que deve estar presente no diretorio
-após isso informe a url do site e aperte enter.
