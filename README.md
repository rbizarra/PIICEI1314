## Manipulação interativa de layers alojadas no Geoserver

Projecto realizado no âmbito da cadeira de PIICEI 2013-2014

### Funcionalidades

- Carregamento de layers do Geoserver;
- Adicionar/Remover polígonos (features) duma layer;
- Editar feature: mover pontos da geometria ou os valores das propriedades inerentes à layer;
- Gravar as alterações efectuadas para o servidor local do Geoserver;
- Observar as coordenadas do rato à medida que se desloca no mapa.

### Requisitos

- <b>Geoserver</b>. Fazer download da versão mais recente a partir da <a href="http://geoserver.org/display/GEOS/Stable">página</a> do projecto (escolher "Instalar como serviço" para evitar problemas de ligação ao Geoserver). A instalação por omissão tem o seguinte endereço para o Geoserver: <a href="http://localhost:8080/geoserver">http://localhost:8080/geoserver</a>. Pode escolher uma porta qualquer, desde que não esteja ocupada, e depois altere o endereço no ficheiro de configuração para aquele que escolheu (este projecto usa o porto 9991).
- <b>OpenLayers</b> e <b>Jquery</b> (embebidos no ficheiro .html)

### Configuração

A página tem um formulário para escolher uma layer sem precisar de alterar o ficheiro de configuração nem de recarregar a página, mas essa funcionalidade está temporariamente desactivada.
Assim, para carregar uma nova layer, basta seguir estes passos (para mais ajuda ver estas imagens: <a href="https://db.tt/rLv4yx2N">(1)</a> e <a href="https://db.tt/2dESE8WH">(2)</a>):
- WFS_Protocol_Version: a versão do protocolo WFS usada para carregar a layer (<1.1.0 não é suportado);
- GeoserverURL: o URL que atribuiu ao Geoserver aquando da instalação;
- Layer_Name: o nome da layer tal e qual como está no Geoserver;
- Workspace: o nome do workspace que aloja essa layer;
- Workspace URI: o URI único que identifica o workspace;
- Geometry: o tipo de geometria associada à layer (geralmente é 'the_geom');
- EPSG_Code: o código EPSG que representa a projecção da layer (apenas colocar o número).
