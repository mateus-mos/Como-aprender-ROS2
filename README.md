<h1>Como aprender ROS2<h1>
<img src="https://github.com/ros-infrastructure/artwork/blob/master/distributions/humble/HumbleHawksbill.png"
     alt="Markdown Monster icon"
     width="30%"
     height="30%"/>

<h2>1. Instalação</h2>


Para iniciar a instalação do ROS2 Humble, é importante seguir as instruções disponíveis no link [Ubuntu (Debian) - ROS 2 Documentation: Humble documentation](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html). Além disso, caso prefira, você pode assistir ao vídeo "[How to install ROS | Getting Ready to Build Robots with ROS #3](https://www.youtube.com/watch?v=uWzOk0nkTcI&list=PLunhqkrRNRhYYCaSTVP-qJnyUPkTxJnBt&index=3)", onde o processo de instalação do ROS2 Foxy é explicado - embora o processo seja quase o mesmo para o Humble.

É importante ressaltar que não é recomendado o uso do ROS2 no Windows, já que vários pacotes não oferecem suporte para esse sistema operacional. Além disso, o ROS2 foi desenvolvido originalmente para rodar no Linux, o que pode gerar problemas de compatibilidade.

Por fim, para instalar o ROS2 Humble, é necessário possuir um sistema baseado no Ubuntu Jammy. Certifique-se de atender a esse requisito antes de iniciar a instalação.

OBS: Para instalar o Gazebo(a nova versão) leia esse [link](https://gazebosim.org/docs/latest/ros_installation) e instale a versão Fortress do gazebo.
<h2>2. Conceitos Básicos do ROS2</h2>


Esse vídeo do canal **Articulated Robotics** ensina os conceitos básicos do ROS2, como nodes, services, parameters, remappings, launching e packages. O vídeo é "[10 things you need to know about ROS! | Getting Ready to Build Robots with ROS #4](https://www.youtube.com/watch?v=KAASuA3_4eg&list=PLunhqkrRNRhYYCaSTVP-qJnyUPkTxJnBt&index=4)".

Não precisa ficar preocupado em entender tudo que é falado no vídeo, porque é normal demorar um pouquinho para pegar o jeito dessas coisas. Mas com a prática e tentando escrever seus próprios nodes, você vai ficar mais craque!

Ah, não esqueça de dar uma olhada na documentação do ROS2. Lá tem tudo explicadinho com mais detalhes. Eu até fiz uma lista com os links dos conceitos que foram falados no vídeo para você poder consultar:



* [Understanding nodes](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Nodes/Understanding-ROS2-Nodes.html)
* [Understanding services](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Services/Understanding-ROS2-Services.html)
* [Understanding parameters](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Parameters/Understanding-ROS2-Parameters.html)
* [Launching nodes](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Launching-Multiple-Nodes/Launching-Multiple-Nodes.html)

Alguns outros conceitos básicos de ROS, mas não menos importantes incluem:



* Como configurar seu _enviroment_ - [Configuring environment](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Configuring-ROS2-Environment.html)
* [Understanding actions](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html#)

E tudo isso junto pode ser visto em [Beginner: CLI tools](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools.html).

<h2>3. Simulação com Gazebo</h2>


O Gazebo é um programa gratuito feito pela comunidade de robótica em 2002, com o intuito de ajudar no desenvolvimento de aplicativos avançados para robôs. Ele tem um ambiente 3D de simulação e ferramentas que ajudam na criação dos robôs. Muita gente usa o Gazebo porque ele é muito bom e fácil de usar.

Nesse tutorial, você vai aprender como instalar o **Gazebo Classic** "[Simulating Robots with Gazebo and ROS](https://www.youtube.com/watch?v=laWn7_cj434&list=PLunhqkrRNRhYYCaSTVP-qJnyUPkTxJnBt&index=9)". Mas atenção, nós vamos usar a **nova** versão do **Gazebo** que é ainda melhor, por isso o processo de instalação e utilização é diferente. Se você tiver instalado a versão mais nova do Gazebo no ROS2 Humble, você já pode seguir o tutorial "[Setting up a robot simulation (Gazebo)](https://docs.ros.org/en/humble/Tutorials/Advanced/Simulators/Gazebo.html)". Caso não tenha, você pode instalar o Gazebo seguindo esse tutorial “[Getting Started with Gazebo?](https://gazebosim.org/docs)”

Durante a instalação do Gazebo você pode se encontrar com o Rviz, porque ambos são usados juntos. Mas o que é o Rviz? O Rviz é uma ferramenta do ROS que mostra dados de sensores e modelos de robôs em uma visualização 3D em tempo real. Você pode ver imagens de câmeras, modelos de robôs e mapas de ocupação, além de customizar a aparência e interação dos objetos. Para mais informações acesse [Wiki - Rviz](http://wiki.ros.org/rviz).

E aí, qual é a diferença entre o Gazebo e o Rviz? De maneira simples, o Gazebo é utilizado para simular robôs e seus ambientes, enquanto o Rviz é usado para ver e monitorar os dados dos sensores e modelos dos robôs enquanto o código é executado em hardware real ou em simulação.

<h2>4. Aplicação de conceitos básicos</h2>


Nesse ponto eu assumo que você tenha uma base conceitual de ROS, e que saiba dizer mesmo que não tão bem o que é um node, quais são os tipos de nodes, por que essa estrutura usada pelo ROS2 é ótima, o que é Gazebo, Rviz, etc.

Para fazer as atividades propostas aqui você pode seguir a documentação “[Beginner: Client libraries](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries.html)” .

Um aviso, como estamos usando a nova versão do ROS2 a Humble, alguns dos comandos e processos dos vídeos citados aqui podem ser diferentes, então na dúvida consulte a documentação.

<h3>4.1 Criar um ROS package</h3>


Nesse tópico sua tarefa é criar um simples _package_,  esse vídeo mostra esse processo “[Making Your First ROS Package](https://www.youtube.com/watch?v=Y_SyQXTL2XU&list=PLunhqkrRNRhYYCaSTVP-qJnyUPkTxJnBt&index=6)”. Recomendo também você ler e executar os tutorias da documentação do ROS2 “[Beginner: Client libraries](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries.html)” até o “_Creating a package_”.

<h3>4.2 Criar um Publisher e Subscriber</h3>


Você pode seguir esse tutorial para realizar essa tarefa [Writing a simple publisher and subscriber (Python)](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Py-Publisher-And-Subscriber.html#), se você desejar pode fazer isso em C++ também, mas o código é mais complicado. Esse vídeo pode te ajudar a realizar essa tarefas “[Hands-On ROS2 - Part 1 (Publisher/Subscriber)](https://www.youtube.com/watch?v=8407qTyBRe0)”.

<h3>4.3 Criar um Service e um Client</h3>


Esse tutorial da documentação explica bem esse processo “[Writing a simple service and client (Python)](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Py-Service-And-Client.html)”, você pode também seguir as intruções desse vídeo “[Hands-On ROS2 - Part 2 (Service/Client)](https://www.youtube.com/watch?v=RJFoM-vnDJo)”.

## Alguns possível erros
### E: The repository '...' does not have a Release file.

Caso você esteja usando Mint você pode se deparar com o seguinte erro(ou algo parecido) instalando o Gazebo ou o ROS2:

E: The repository 'http://packages.osrfoundation.org/gazebo/ubuntu-stable vanessa Release' does not have a Release file.

Isso ocorre porque o "alias" que o Mint usa para o Jammy do Ubuntu é Vanessa(nesse caso), porém não existe esse package no ubuntu-stable. Para resolver isso você deve alterar o "vanessa" para "jammy" no caminho "/etc/apt/sources.list.d/gazebo-stable.list". Depedendo do package o caminho é diferente.




