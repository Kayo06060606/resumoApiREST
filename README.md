
 # Api REST 

 API REST (Representational State Transfer); e um modelo de arquitetura de software que define boas práticas para o desenvolvimento de APIs. Ela atua como um guia, estabelecendo requisitos para a construção de APIs que conectam usuários a aplicações em nuvem. Os principais padrões utilizados pela REST incluem JSON, XML e GraphQL. O protocolo HTTP é o alicerce da API REST.Em resumo, a API REST fornece diretrizes para a criação de interfaces entre sistemas.

 # Api RESTFul

 A RESTful é uma implementação específica dos princípios da REST. Ela utiliza os padrões definidos pela API REST para desenvolver soluções ou serviços.Um bom exemplo e um empresário que deseja melhorar a experiência de seus clientes na sua loja virtual, oferecendo cupons de desconto ou filtros de busca mais efecientes.Para isso, ele precisaria desenvolver uma API RESTful seguindo os padrões originais da REST.Em resumo, a RESTful é a aplicação prática dos princípios da REST para criar soluções eficazes e interativas.

 ## Diferenças enre REST e RESTFul

 A arquitetura REST segue o princípio de *cliente-servidor*, mantendo as responsabilidades de cada parte separadas.Isso permite que o *front-end* (cliente) e o *back-end* (servidor) evoluam independentemente. A separação facilita a manutenção, escalabilidade e atualização das aplicações.Cada requisição é tratada como uma transação independente, sem dependência de requisições anteriores. Isso simplifica o desenvolvimento e torna as APIs mais flexíveis e ágeis.O uso de cache melhora a eficiência da comunicação entre diferentes aplicações.Dados frequentemente acessados podem ser armazenados em cache, reduzindo a necessidade de requisições repetidas. A REST define uma interface uniforme compartilhada entre cliente e servidor.Isso inclui padrões para URLs, métodos HTTP (como GET, POST, PUT, DELETE) e formatos de dados (como JSON ou XML).A uniformidade simplifica a integração e a interoperabilidade. As URIs (Uniform Resource Identifiers) seguem um padrão consistente. Os parâmetros são bem definidos, facilitando a construção de URLs claras e compreensíveis. A REST utiliza os métodos HTTP de forma eficiente. Por exemplo, o uso adequado de GET, POST, PUT e DELETE para operações específicas. A API REST permite a troca de informações com outras aplicações de maneira segura e ágil. Enquanto a  As APIs RESTful seguem critérios adicionais, garantindo uma *interface uniforme* e uma implementação mais *padronizada*. Isso facilita a manutenção, a integração e a compreensão das APIs. As APIs RESTful são projetadas para serem *escaláveis*, permitindo um melhor desempenho em cenários de alto tráfego. A separação entre cliente e servidor contribui para essa escalabilidade. Uma API RESTful oferece altos níveis de *liberdade e flexibilidade*. Ela permite que as representações enviadas pelo servidor estejam em diversos formatos, como *JSON, **XML, **Python*, etc. A RESTful organiza as funcionalidades em *recursos* bem definidos. Isso torna a estrutura da API mais clara e facilita a navegação. As URIs (Uniform Resource Identifiers) seguem um padrão consistente. Os parâmetros são bem definidos, facilitando a construção de URLs claras e compreensíveis. Em suma, a API REST é o guia, enquanto a RESTful é a construção concreta baseada nesse guia. Ambas são essenciais para a comunicação eficiente entre sistemas e aplicações.

 ## HTTP verbs 

 O protocolo HTTP define um conjunto de métodos de requisição responsáveis por indicar a ação a ser executada para um dado recurso. Embora esses métodos possam ser descritos como substantivos, eles também são comumente referenciados como Verbos HTTP. Aqui estão os principais verbos HTTP:
 GET: Solicita uma representação do recurso especificado. Usado para recuperar dados.
 HEAD: Similar ao GET, mas sem o corpo da resposta. Usado para obter informações do cabeçalho.
 POST: Submete uma entidade ao recurso especificado, geralmente causando uma mudança de estado no servidor.
 PUT: Substitui todas as representações atuais do recurso de destino com o conteúdo da requisição.
 DELETE: Remove o recurso especificado.
 CONNECT: Estabelece um túnel com o servidor identificado pelo recurso de destino.
 OPTIONS: Descreve as opções de comunicação para o recurso de destino.
 TRACE: Realiza um teste de loop-back de mensagem ao longo do caminho até o recurso de destino.
 PATCH: Aplica modificações parciais a um recurso.

 Esses verbos têm diferentes semânticas e características, como serem seguros, idempotentes ou cacheáveis. Por exemplo, o GET é seguro e idempotente, enquanto o POST não é idempotente e pode ter efeitos colaterais no servidor.

 ## HTTP Status Code

 Os códigos de status de resposta HTTP indicam se uma solicitação HTTP específica foi concluída com êxito.

 Respostas Informativas;
 100 Continue: Indica que o cliente deve continuar a solicitação ou ignorar a resposta se a solicitação já estiver concluída.
 101 Switching Protocols: Enviado em resposta ao cabeçalho de solicitação "Upgrade" do cliente e indica o protocolo ao qual o servidor está mudando.
 102 Processamento (WebDAV): Indica que o servidor recebeu e está processando a solicitação, mas ainda não há resposta disponível.
 103 Early Hints: Principalmente usado com o cabeçalho "Link", permitindo que o agente do usuário pré-carregue recursos enquanto o servidor prepara uma resposta ou pré-conecte a uma origem da qual a página precisará de recursos.

 Respostas bem-sucedidas
 200 OK: A solicitação foi bem-sucedida. O significado de "sucesso" depende do método HTTP:
    GET: O recurso foi buscado e transmitido no corpo da mensagem.
    HEAD: Os cabeçalhos de representação estão incluídos na resposta sem corpo da mensagem.
    PUT ou POST: A descrição do resultado da ação é transmitida no corpo da mensagem.
    TRACE: O corpo da mensagem contém a solicitação recebida pelo servidor.
 201 Created: A solicitação foi bem-sucedida e um novo recurso foi criado como resultado.
 202 Accepted: A solicitação foi recebida, mas ainda não foi executada. É não comprometedor, pois não há como enviar posteriormente uma resposta assíncrona indicando o resultado da solicitação.
 203 Informações não autorizadas: Os metadados retornados não são exatamente os mesmos que os disponíveis no servidor de origem, mas são coletados de uma cópia local ou de terceiros. O código 200 OK é preferido a esse status, exceto para casos específicos.
 204 No Content: Não há conteúdo a ser enviado para essa solicitação, mas os cabeçalhos podem ser úteis. O agente do usuário pode atualizar seus cabeçalhos em cache para esse recurso com os novos.
 205 Reset Content: Indica ao agente do usuário para redefinir o documento que enviou essa solicitação.
 206 Partial Content: Usado quando o cabeçalho "Range" é enviado pelo cliente para solicitar apenas parte de um recurso.
 207 Multi-Status : Fornece informações sobre vários recursos, em situações em que vários códigos de status podem ser apropriados¹⁵.

 Esses códigos de status são essenciais para estabelecer a comunicação entre um navegador da web e um servidor da web, informando o resultado da solicitação e fornecendo informações sobre a operação solicitada.

 ## Autor do resumo: Kayo de Freitas Gomes- Matrícula: 01556944.

