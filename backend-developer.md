# Desafio Back-end Developer
![image](https://www.fortics.com.br/wordpress/wp-content/uploads/2019/12/logo_fortics.svg)
# Sobre a Fortics Tecnologia
Fundada em 2003, a Fortics começou suas operações atuando em projetos para comunicação de dados e segurança da informação. Em 2006 ingressou no seguimento de comunicação unificada de voz e dados com soluções para telefonia IP e messageria multicanal. Em 2017 iniciou a vertical de soluções para computação em nuvem. [Aprenda mais sobre a Fortics no nosso site](https://www.fortics.com.br/).

# O que você deve esperar neste desafio de código?
Este desafio é o início de sua jornada na Fortics. É destinado a todos os candidatos, independentemente da experiência.
Depois que você terminar, revisaremos seu código, forneceremos feedback e seguiremos para as próximas etapas.

# Sobre o desafio
Sua tarefa é construir um back-end para a aplicação de bot. A aplicação é um serviço para a comunicação entre usuários (clientes) e agentes (atendentes) em tempo real.

O back-end deve ser construído seguindo as especificações das funcionalidades descritas abaixo.

# Funcionalidades
- Criar um bot telegram utilizando qualquer uma das seguintes linguagens: Go, Node com Typescript, Python ou Elixir. Onde deverá trocar mensagens de texto com a aplicação através de um pubsub (redis, rabbitmq, etc)
- Criar o servidor utilizando o Laravel 6+

## 1º Caso - Iniciando sessão
- Ao receber uma mensagem do contato, o bot irá enviar uma requisição para o servidor. Quando o servidor receber essa mensagem, ele deve criar uma nova sessão (conversa), se ela não existir, e gravar a mensagem na sessão em atendimento e retornar uma mensagem para o contato contendo `Reply: mensagem recebida`.

## 2º Caso - Consultando a sessão
- É necessário criar uma rota para consultar as sessões que estão em atendimento no momento.
- Também é possível realizar uma busca pelo nome do contato.

## 3º Caso - Finalizando a sessão
- É importante fornecer uma rota para finalizar a sessão que está em atendimento, ao ser finalizado a sessão deve ser excluída do banco retornado uma mensagem informando o contato da finalização.

## 4º Caso - Importando sessões
- Dentro desse repositório, no seguinte diretório `data/sessions.json` é possível encontrar um json com sessões que representaria os atendimentos que existem no momento. É necessário criar uma rota para realizar o upload desse arquivo, para que seja possível consultar essas sessões.
- Ao finalizar o upload do arquivo, é necessário enviar uma mensagem para um **canal** do telegram, sendo um campo fornecido na rota de upload junto com o arquivo.

# O mínimo necessário
- README.md contendo informações básicas do projeto e como executá-lo

# Requisitos
- Conteinerização da aplicação
- Ter uma cobertura de teste relativamente boa, a maior que você conseguir
- Deve ser possível importar sessões através de um upload csv
- Utilizar qualquer banco de dados (Relacional ou não) para registro da sessão

# Bônus
- Detalhes fazem uma tremenda diferença :)
- Uso de ferramentas externas que facilitem o seu trabalho
- Sugestões sobre o challenge embasadas em alguma argumentação
- Código modular

# Recomendações
- Se possível, dê preferência ao Mongo como banco de dados.
- Use boas práticas de programação
- Pensar em escalabilidade, pode ser uma quantidade muito grande de dados.
- Use as [melhores práticas do git](https://www.git-tower.com/learn/git/ebook/en/command-line/appendix/best-practices), com mensagens claras
- Tenha cuidado com os detalhes da API REST
- Tempo de resposta impacta significativamente na experiência do usuário :)
- Disponibilizar uma coleção da API no Postman ou Insomnia

# Processo de submissão
O desafio deve está disponível pelo [GitHub](https://github.com/). As bibliotecas ou pacotes de terceiros devem estar evidenciadas na documentação. 

Não será obrigatório, porém será visto com bons olhos, a utilização de alguma hospedagem para demonstrar o funcionamento da aplicação (**Heroku**, **AWS**, **Azure**, **Firebase**, etc).

Qualquer dúvida em relação ao desafio, responderemos por e-mail ou whatsapp.

Bom trabalho!
