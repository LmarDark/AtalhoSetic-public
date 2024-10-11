<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

# AtalhoSetic

Desenvolvido com Laravel por LmarDark.

- [Introdução](#)
- [Funcionalidades](#)
- [Sobre as tecnologias usadas](#)
- [Aprendizados e obstáculos](#)
- [Finalização]

🔍 Principais funcionalidades:

° Atalhos para aplicações/sites do governo: Proporciona acesso rápido a portais essenciais do governo, agilizando as rotinas e otimizando o tempo dos servidores.
° Banimento de IPs de Firewall: Permite o bloqueio de endereços IP diretamente pela aplicação, facilitando a gestão de segurança da rede.
° Checador de Portas: Ferramenta para verificar portas abertas, ajudando na gestão e manutenção eficiente dos servidores.
° DIG IP: Funcionalidade para realizar consultas DNS, permitindo que os usuários obtenham informações sobre endereços IP e domínios.
° Verificador de Certificado: Monitoramento do status dos certificados digitais, alertando os servidores quando um certificado estiver prestes a expirar.
° Armazenador de Scripts: Permite que a gerência de DataCenter armazene e organize scripts utilizados com frequência, facilitando o acesso e a reutilização.
° Funcionalidades personalizáveis: Usuários com permissões da Gerência de DataCenter podem criar suas próprias funcionalidades dentro da aplicação, sem a necessidade de modificar o código-fonte, tornando o sistema flexível e adaptável às necessidades específicas.
° Orquestração de Permissões
° E dentro outros

💻 Sobre as tecnologias e bibliotecas utilizadas:

Backend: Laravel (PHP)
O Laravel é uma poderosa ferramenta que adota o padrão MVC (Model-View-Controller) em sua arquitetura. Neste projeto, utilizamos principalmente o Controller, que gerencia toda a lógica do código, sendo fundamental para a implementação do CRUD (Create, Read, Update, Delete) do Painel do Administrador.

Frontend: Vue.js, Tailwind CSS e Inertia.js
Seguindo o padrçao MVC temos o View, aqui posso citar Blade que foi usada em situações restritamente específicas para criar as Views dos módulos, visto que o roteamento dinâmico é mais otimizado nessa configuração(Estou aberto a sugestões sobre como implementar rotas dinâmicas de forma mais eficaz utilizando Inertia e Vue). O Vue.js, em combinação com o Tailwind CSS e o Inertia SSR, destacou-se como uma escolha excelente, permitindo a construção de uma interface de usuário interativa e responsiva. O Tailwind CSS proporcionou um design moderno e adaptável, enquanto o Inertia.js garantiu transições suaves e rápidas entre as páginas, resultando em uma experiência fluida e eficiente, característica de aplicações SPA (Single-Page Application). Juntas, essas tecnologias formaram a base sólida para o desempenho e a escalabilidade da aplicação.

Banco de Dados: SQLite
O SQLite foi escolhido devido à sua simplicidade e desempenho, especialmente considerando que o AtalhoSetic não armazena senhas ou informações sensíveis dos usuários, mas sim permissões e dados necessários para o funcionamento da aplicação.

Bibliotecas: LdapRecord, DarkMode e outros
Visto que a forma de Login do AtalhoSetic é restritamente feita para servidores da SETIC, o LdapRecord foi um dos pontos iniciais e chaves deste projeto, onde pude armazenar os grupos e usuários para a orquestração de permissões dos usuários.
O Dark Mode do VueJs me proporcionou fazer de forma simplificada junto ao Tailwind CSS o modo escuro da página do Atalhos. 

Outros: Python
O Python foi utilizado exclusivamente para desenvolver módulos, como o Port-Scan e o DIG IP, agregando funcionalidades importantes ao sistema.

👨‍💻 Aprendizados:

Desenvolver o AtalhoSetic me proporcionou uma imersão profunda nas tecnologias como Laravel, Vue.js, Inertia.js, Tailwind CSS e, principalmente, em Linux e Dockerização.

Além de adquirir conhecimento, enfrentei diversos desafios ao longo do processo. Um dos principais obstáculos foi lidar com um framework PHP sem ter muita experiência prévia. O AtalhoSetic foi desenvolvido e refeito três vezes, pela minha frustação de pensar que não estava bom o suficiente, por não saber se estava utilizando corretamente de forma eficiente o Laravel, porém lendo documentação e vendo vídeos em casa consegui extrair o que a ferramenta proporciona.

Quero expressar minha gratidão aos meus mestres que foram fundamentais nesse percurso. Agradeço sinceramente a @caiozera, @ramisexo e @andremesquitadomine, que me ajudaram a entender e me explicaram muitos conceitos relacionados a Docker e boas práticas de programação.

Essa jornada foi uma valiosa oportunidade de aprendizado, e estou ansioso para aplicar todo esse conhecimento em futuros projetos!

Além de obter conhecimento, claramente tive obstáculos, uma delas foi pegar um framework de PHP e não ter muito conhecimento da tecnologia, o AtahoSetic foi feito e refeito 3 vezes,  

Quero expressar minha gratidão aos meus mestres que me ensinaram conceitos fundamentais, tanto de redes, linux, dockerização e programação muito obrigado @caiozera @ramisexo @andremesquitadomine.

Segue algumas imagens:


## 💻 Sobre as tecnologias usadas:
Segue documentação oficial das tecnologias usadas Laravel, PHP, Vue.js, Inertia e Tailwind

**PHP** - *https://www.php.net/manual/pt_BR/*

**BLADE** - *https://laravel-docs.readthedocs.io/en/latest/blade/*

Tendo terminado o seu módulo, você pode estar adicionando seu arquivo diretamente na aplicação indo em *"Admin"* depois em *"Módulos"*.


## Contribuidores

Obrigado por considerar contribuir com este projeto!
- Caio T.
- Lucas M.


## Melhorias ou vulnerabilidades

Caso encontre qualquer tipo de vulnerabilidade ou deseja fazer melhorias, fique a vontade para fazer a contribuição.


## License

 
