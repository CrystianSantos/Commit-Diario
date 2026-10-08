🟩 AutomatizadorCommit

Um script simples que eu criei pra fazer um commit automático por dia no GitHub e manter meu gráfico de contribuições sempre verde.

Fiz pra uso pessoal, rodando na minha própria máquina, sem depender de servidor nem de nada complicado. Se você quiser usar também, o passo a passo está logo abaixo.

Por que eu fiz isso?

Eu estou estudando e construindo projetos todo dia, mas nem sempre dá pra subir código novo. Queria algo prático que mantivesse a constância no GitHub sem eu precisar lembrar de fazer isso manualmente. Também foi uma ótima desculpa pra praticar automação, Git e o Agendador de Tarefas do Windows.

Como funciona
O script entra na pasta de um repositório local.
Faz uma pequena modificação em um arquivo (registra a data do dia).
Roda git add, git commit e git push.
O Agendador de Tarefas do Windows executa tudo isso sozinho, todo dia, no horário que eu escolhi (12:00).
O que você precisa ter
Windows
Git instalado e configurado com seu usuário do GitHub
Python 3 instalado
Uma conta no GitHub
VS Code ou IntelliJ (opcional, só pra editar o script se quiser)
Como instalar na sua máquina

1. Baixe o projeto

Pelo botão verde Code → Download ZIP aqui no repositório, ou clonando:

bash
git clone https://github.com/SEU-USUARIO/AutomatizadorCommit.git

Guarde a pasta em um lugar fixo, por exemplo C:\Projetos\AutomatizadorCommit.

2. Crie um repositório só pra isso

No GitHub, crie um repositório novo (eu chamei o meu de atividade-diaria) e clone na sua máquina:

bash
git clone https://github.com/SEU-USUARIO/atividade-diaria.git

3. Ajuste o caminho no script

Abra o script no VS Code ou IntelliJ e troque o caminho do repositório pelo da sua máquina, por exemplo:

python
REPO_PATH = r"C:\Users\SEU-USUARIO\Documents\atividade-diaria"

4. Teste na mão

No terminal, dentro da pasta do projeto:

bash
python automatizador.py

Se aparecer um novo commit no seu repositório no GitHub, deu certo. ✅

5. Agende pra rodar sozinho

Abra o Agendador de Tarefas do Windows.
Clique em Criar Tarefa Básica.
Dê um nome (ex.: AutomatizadorCommit) e escolha Diariamente, no horário que preferir.
Em Ação, escolha Iniciar um programa.
Em Programa/script, coloque o caminho do Python (ex.: python) e, em Adicione argumentos, o caminho completo do script.
Em Iniciar em, coloque a pasta do projeto.
Salve e clique com o botão direito na tarefa → Executar pra testar. Se o resultado for 0x0, está tudo certo.
Dicas
Use sempre o mesmo repositório pra não bagunçar seus outros projetos.
Seu PC precisa estar ligado e com internet no horário agendado (dá pra marcar a opção de executar assim que possível caso ele estivesse desligado).
Se o git push pedir senha, configure um token de acesso pessoal do GitHub ou o Git Credential Manager.
Tecnologias usadas

Python · Git · GitHub · Agendador de Tarefas do Windows · VS Code · IntelliJ

Aviso

Esse projeto é só uma automação pessoal pra manter a rotina e praticar. O que realmente conta é continuar estudando e construindo coisas de verdade. 😄

Feito por Crystian 💻 Se curtiu, deixa uma ⭐ no repositório!
