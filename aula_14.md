# Websockets
- Comunicação full-duplex sobre uma única conexão TCP
- RFC de 2011, envolvendo IEFT e W3C
- HTTP e Websockets atuam na camada 7  do Modelo de Referencia ISO/OSI (Ambos dependem do TCP)
- Websockets compatível com HTTP
- Habilita interação e o navegador e servidor web com baixa sobrecarga, facilitando a transferência de dados em tempo real (De/Para do navegador/Web server)
- Enviar conteúdo para o navegador, sem esse último solicitar, mantem a conexão ativa (trafego bi-direcional)
- Trafego sobre as portas 80 e 443 (conexões encriptadas-TLS). Bom para firewall.
- Suporte : Chrome, Safari, Explorer, Firefox.
- concorrente direto é o AJAX.

# CoAP
Constrained applications protocol

WSN - wireless sensor networks - roda dentro de sensores que usam wsn. 
Redes de sensores são extremamente sensíveis em relação à consumo energético, ou seja, é muito importante que tenham baixo consumo.
Sensores neste tipo de rede utilizam modo de comunicação P2P adhoc.

ele atende um dos requerimentos que é multicast, com overhead baixo e simples.
é muito importante então no IoT, com comunicação M2M.
A rede é Ipv6 - o que traz baixo overhead. 
pode ter comunicação confirmável e não-confirmável, já que é UDP, o confirmável é feito no nível de aplicação.

publisher subscriber
protocolo da camada de aplicação
Websocket é TCP, CoAP é UDP.

# MQTT

- sistema de comunicação é diferente, ao contrário de request/reply, é no modo publish/subscribe. conversa indireta pois tem um broker interfaceando. Baixinho footprint, - ruim para sistema wireless bastante ruidoso.
Mais utilizado no mundo IoT. 
Quando eu preciso de um Pub Sub - IOT - médico/paciente, professor/aluno, comunicação one-to-many dirigida a eventos.


# Revisão para prova

## VLAN
	Quando utilizar? tagged, untagger. > de 1 switch. divide o dominio de broadcast, um domínio não consegue "sniffar" dados de outro dominio.
## 5G - 4 cenários de uso de 5G, rádio cognitivo
	Existe porque LTE não é escalável. (pelo menos descrever dois ou três cenários). - Lembrar de desalocar latência e largura de banda. ou seja, baixissimo overhead das camadas e alta taxa de transmissão.
	CPS - cyber physical system - não precisa de largura de banda.
	Streaming de vídeo - precisa só de largura de banda
	rádio cognitivo - o espectro de frequencia é fatiado para diversos tipos de utilização, no cognitivo a frequencia é definida em tempo de execução para melhor utilização, aprendendo por exemplo a usar faixas de frequencia não usadas para ter escalabilidade.
## Internet do Futuro
	- ID / LOC - forte acoplamento no caso do IP, é uma hora ID e outra hora Localizador. Não consigo manter a mesma identificação se eu trocar de rede (transitar). Ou seja, é preciso desacoplar o conceito ID/LOC.
	- Sistema de nomes seria a solução, SCN - self certified names. nomes auto-certificados através de hashes, ID que é o localizador único. Isto possibilita a assinatura digital. 
	- SDN - redes estão passando por processos de virtualização (openflow: redes programáveis). Exposição para toda a rede.
	Exposição é feita através de um serviço de descoberta, um serviço de broker e um serviço de flooding (o hash precisa ser conhecido por toda a rede), o problema do flooding é receber a informação de vários pontos várias vezes, a solução é colocar id nas mesnagens e ignorar elas depois.
	- Tracking : mudança entre brokers.

## IoT
	- Desafios - identificação, big data, segurança (privacidade), escalabilidade.
	- Protocolos - saber o escopo de cada um deles.
	- Frameworks que habilitam : 3 player - software, middleware, hardware. 2 players: sensores, atuadores, gateway.

	gateway > 1 protocolo.
	na nuvem tem load balancing, elasticiidade, machine learning.

### Estratégias:
	EPC Global, Coap, websockets, mqtt


