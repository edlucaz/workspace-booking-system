> **📌 Nota:** Este é um projeto histórico de 2021, desenvolvido para um processo seletivo quando eu estava começando na programação. Ele representa um marco importante na minha jornada de desenvolvimento.
> 
> **🚀 Versão Moderna:** Estou desenvolvendo uma versão atualizada e profissional deste projeto com tecnologias modernas. Confira em: [workspace-booking-system](https://github.com/edlucaz/workspace-booking-system)

---

# Landing-Page---Fcamara
  Esse projeto foi realizado para um processo seletivo do Grupo Fcamara para iniciantes no mundo da programação, sendo propositalmente feito após a Imersão Dev da Alura, evento no qual consiste em 10 aulas ao longo de 2 semanas para as pessoas aprenderem na prática como programar. 
  O processo seletivo consiste em um desafio com a seguinte problemática:

![Capturar](https://user-images.githubusercontent.com/91226344/135895582-b2c8f32e-698e-49df-b706-4bdc7da6cbc1.PNG)

# Proposta
  A ideia consiste na criação de uma Landing Page para que os colaboradores da FCamara agendassem possíveis idas aos escritórios da empresa, de modo que esse agendamento assegurasse o processo.

# Funcionamento da página
  Para o agendamento é necessário que o colaborador da FCamara preencha os dados apresentados no seguinte formulário.

  ![Imagem 2](https://user-images.githubusercontent.com/91226344/135896315-5a97915a-c899-46f8-a1cc-cc556fc2066d.PNG)

*Os dados requeridos no formulário são respectivos aos apresentados pela empresa no regulamento do processo seletivo.

  É importante ressaltar que são necessárias algumas condições para que a pessoa consiga fazer o agendamento, por exemplo:

      Não deixar o campo do nome vazio (alerta1);
      Não selecionar alguma estação de trabalho (alerta1);
      Não ter algum sintoma de Covid nas últimas 2 semanas (alerta2);

  Caso essas condições não seja cumpridas, serão exibidos os seguintes alertas:

![alerta 1](https://user-images.githubusercontent.com/91226344/135898064-85e923ea-4214-4840-8cdc-67d6cd0aef2a.PNG)![alerta 2](https://user-images.githubusercontent.com/91226344/135898056-44193f52-5d13-48e2-8c4a-771f83b91133.PNG)

  Selecionando estação de trabalho:
  
  Ao clicar no botão "Escolher" abrirá uma janela modal com uma planta do local contendo indicações númericas das respectivas estações de trabalho:

![Estacao de Trabalho](https://user-images.githubusercontent.com/91226344/135898618-aeaab446-0012-4bb4-885c-5c58928e37c7.PNG)

  *Planta meramente ilustrativa criada somente para exemplificar a seleção de estações de trabalho.
    
  Clicando em qualquer um dos números, o usuário voltará para tela do formuláro e a imagem inicial será trocada para a estação selecionada:

  ![Orange](https://user-images.githubusercontent.com/91226344/135899083-8d6b8a44-05a7-4868-a0c4-2eec52127c66.png) ---------> ![Orange 1](https://user-images.githubusercontent.com/91226344/135899129-e84a451d-fe70-4871-b9cc-d6317f69c481.png)

  Com todas as informações preenchidas, outra janela modal será aberta apresentando os informativos, disponibilizados pela empresa no regulamento do processo seletivo, seguidos de um botão de confirmação do agendamento:

![Informativos](https://user-images.githubusercontent.com/91226344/135900154-9cda84e1-afa1-4d6a-a2f4-a8e0a55a77b1.PNG)

  Ao clicar em "Não", a janela se fechará, mas os dados continuarão preenchidos caso o usuário queira tentar novamente.

  Ao clicar em "Sim", com todas as condições cumpridas, a janela se fechará e o formulário será trocado por um "comprovante" de agendamento contendo todas as informações inseridas.

![Comprovante](https://user-images.githubusercontent.com/91226344/135900758-04051a11-434f-4fe2-a442-7dfe31218103.PNG)

  Realizar outro agendamento:

  Juntamente com o comprovante de agendamento, existe um botão chamado "Novo Agendamento", ao clicar nele, a página será recarregada sendo possível agendar outro dia.

# Layout da Página:

  A página possui 2 temas, denominados "Modo Orange" e "Modo Grape", que podem ser alterados através dos botões no canto superior direito da tela:

![Modo Grape](https://user-images.githubusercontent.com/91226344/135903044-9ebad096-272a-44a8-8239-dc5f9e41db74.PNG) ![Modo Orange](https://user-images.githubusercontent.com/91226344/135903056-6ffa9cd5-df50-4194-9543-5f5dfb669909.PNG)

  Versão para telas menores:

![Modo Grape 2](https://user-images.githubusercontent.com/91226344/135903133-3b5ed884-2341-482d-86eb-cbc1332a5613.PNG) ![Modo Orange 2](https://user-images.githubusercontent.com/91226344/135903148-da474d59-33e2-42ee-966b-b399dbc4dca2.PNG)

  O layout da página foi baseado em elementos e cores respectivos a própria empresa FCamara. Todo o design da página foi baseado nas cores da imagem de fundo, esta que pode ser encontrada em diversas áreas do site da empresa que fazem referência ao podcast de Joel Backschat (CTO do Grupo FCamara) denominado Orange Juice. O primeiro tema chamado "Orange" faz referência a como são intitulados os colaboradores do Grupo FCamara, chamados de #SangueLaranjas. Pensando em algo que contrastasse isso, mas que ainda seguisse a mesma linha foi pensando o modo "Grape".

  Tema Orange:
  
![Tema Orange](https://user-images.githubusercontent.com/91226344/135905094-7f4a50ba-9a77-4a5a-b3c7-3fe6c08719e5.PNG)


  Tema Grape:
  
![Tema Grape](https://user-images.githubusercontent.com/91226344/135905127-85173671-bb01-42cd-8573-c2b07a2dd3e4.PNG)

  
  A ideia foi criar temas contrastantes, utilizando-se da inversão das cores principais, laranja e roxo, e as incluindos em elementos menores, como o espaço das entradas de texto, botões, logo da empresa e o contorno no recipiente do formulário.

  Rodapé da página:

  Para o rodapé a ideia foi deixar um design simples sem a utilização de cores e que remetesse ao rodapé do site da empresa:

![Rodapé](https://user-images.githubusercontent.com/91226344/135906386-ed39b8cf-3741-4aee-9ae3-4389e440b464.PNG)


  Além disso, todos os ícones abaixo do logo do GRUPO FCAMARA redirecionam o usuário para as redes sociais e plataformas da empresa, assim com o logo do rodapé e o logo fixo no canto inferior direito redirecionam o usuário para o site da empresa. Vale ressaltar que o usuário sempre será enviado através de uma nova aba para que não seja removido da Landing Page.

Outros Elementos:

Cabeçalho contendo logo e lema da empresa;

Título da página fazendo referência à volta dos funcionários as atividades presencial.

Vídeos:

Relembrando o que passamos - nome do vídeo: #JUNTOSADISTÂNCIA - Vídeo de março de 2020, disponível no YouTube do Grupo FCamara. Conteúdo: apelo para que as pessoas fiquem em casa nos primeiros meses da pandemia, juntamente com dicas para as pessoas se protegerem do vírus. Intuito na página: para que o colaborador lembre-se da importância que teve o período em que esteve afastado do escritório.

Negócios Pós Pandemia - nome do vídeo: [OMNI] Negócios Pós Pandemia - Vídeo de agosto de 2020, disponível no YouTube do Grupo FCamara. Conteúdo: Giovanna Zacchi, Head Commercial da Omnicommerce explicando um pouco sobre os cenários de negócios pós pandemia. Intuito na página: mostrar um pouco como a visão de trabalhar em HOME OFFICE mudou e como isso afeta os negócios no futuro.

# Responsividade da Página:
Alteração da estrutura da página para resolução com menos de 1100 pixels de largura:

![Responsividade](https://user-images.githubusercontent.com/91226344/135913156-22bcbf76-9cfc-4d52-83ca-2c44e736a515.PNG)

# Necessidades e Possíveis Melhorias:
     Interação com banco de dados da empresa;
     Planta do escritório real da empresa para seleção de estações de trabalho;
     Alterar o padrão de data para o brasileiro;
     Novo agendamento sem a necessidade de recarregar a página;
     Melhorar ainda mais a responsividade da página para diferentes tamanhos de tela;
    
# Tecnologias utilizadas
HTML5

CSS3

JAVASCRIPT
