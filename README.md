<td style="width: 20%;"><img src="https://github.com/Epaminondaslage/Automacao-industrial-e-residencial-Ecossistema-didatico/blob/main/img/Logo_CEFET-MG.png" width="20%"></td>
<p><strong>Home Assiatant-ESP32-ESP8266-ESPHome </strong></p>
<p><strong>Prof Epaminondas Lage</strong></p>
<a href="http://lattes.cnpq.br/7787341723868111"> Currículo Lattes LAGE, E. S.</a> 

# Índice 
* [ESPHome](#ESPHome)
* [Comparação ESP32 e ESP8266](#Comparação-ESP32-e-ESP8266)

# ESPHome  

ESPHome é uma estrutura de firmware de código aberto para microcontroladores como ESP8266 e ESP32. Ele permite a configuração e integração de dispositivos IoT personalizados por meio de uma linguagem de configuração baseada em YAML. Suporta uma variedade de componentes, como sensores, atuadores e interfaces de comunicação, incluindo MQTT e API REST. Ela oferece recursos avançados, como atualização OTA (Over-The-Air) para facilitar a atualização remota do firmware dos dispositivos.

O ESPHome é especialmente popular entre os desenvolvedores e entusiastas de IoT, pois permite o desenvolvimento de dispositivos personalizados e a integração com outros sistemas de automação residencial, como o Home Assistant. Com o ESPHome, é possível criar sensores, interruptores e outros dispositivos inteligentes controlados por Wi-Fi.

Graças à sua flexibilidade e extensibilidade, o ESPHome torna o processo de desenvolvimento de dispositivos IoT mais acessível a uma ampla gama de usuários. Ele fornece controle total sobre o firmware, permitindo personalizar os dispositivos conforme necessário. O ESPHome simplifica o desenvolvimento de soluções de IoT, proporcionando uma base sólida para a criação de dispositivos conectados e sistemas de automação residencial.

Veja o Git https://github.com/Epaminondaslage/HomeAssistant-ESPHome para entender como instalar e configurar o ESPHome no Home assistant assim como conectar um novo dispositivo.

# Protocolo de comunicação ESPHome

O ESPHome pode usar o protocolo MQTT para comunicação entre os dispositivos ESP8266/ESP32 e o Home Assistant, mas não é exclusivamente limitado a esse protocolo. O ESPHome suporta várias opções de comunicação, e MQTT é apenas uma delas.

Quando se trata de comunicação com o Home Assistant, o ESPHome possui duas opções principais:

1.	API Nativa: A API nativa é o método de comunicação padrão usado pelo ESPHome para integrar-se com o Home Assistant. Essa opção permite que o dispositivo ESPHome se comunique diretamente com o Home Assistant, tornando a integração mais direta e menos dependente de outras ferramentas.

2.	MQTT: O MQTT é um protocolo de mensagens leve e amplamente utilizado em sistemas de automação residencial e da Internet das Coisas (IoT). O ESPHome também suporta a comunicação via MQTT, o que significa que você pode configurar seus dispositivos ESPHome para se comunicarem com o Home Assistant usando o protocolo MQTT. Ao utilizar o MQTT, o ESPHome publica e/ou subscreve tópicos MQTT para enviar e receber dados do Home Assistant. Os dados enviados podem incluir leituras de sensores, estado de atuadores, informações de dispositivos e outras informações relevantes.
   
# Acionamento de Relé no ESP8266-NodeMCU conectando ao Home Assistant por ESPHome API nativa 

Passo 1: Escolher a placa a der sutilizada assim como o módulo DHT11 e porta do NodeMCU a ser utilizada.


Passo 2: Configurar o complemento ESPHome Dashboard

•	Depois de instalar o complemento, clique em "Configuração".
•	Aqui você pode ajustar as configurações do complemento, como a porta que ele usará.

Passo 3: Crie um arquivo de configuração YAML para o dispositivo ESP

•	No Home Assistant, acesse novamente o painel esquerdo e clique em "Supervisor", depois selecione "ESPHome Dashboard".
•	Clique no botão "+", localizado no canto inferior direito, para adicionar um novo dispositivo ESP.
•	Dê um nome para o dispositivo e, em seguida, clique em "Criar".

Passo 4: Preencha o arquivo de configuração YAML

•	Você será redirecionado para a página de edição do dispositivo. Aqui, você pode começar a preencher o arquivo de configuração YAML com as informações específicas do dispositivo e dos sensores que deseja adicionar.
•	O ESPHome oferece uma documentação abrangente sobre as configurações disponíveis que você pode adicionar ao arquivo YAML para personalizar o comportamento do dispositivo.

Passo 5: Verificar a configuração e compilar o firmware

•	Depois de preencher o arquivo YAML, clique em "Salvar" para verificar a configuração.
•	Se não houver erros, clique em "Compile" para criar o firmware personalizado para o dispositivo.

Passo 6: Flash do firmware para o dispositivo ESP

•	Após a compilação, o firmware estará disponível para download.
•	Você precisará conecta o dispositivo ESP ao computador via USB, para então utilizar uma ferramenta como o "esphome-flasher" para enviar o firmware para o dispositivo.

Passo 7: Monitorar o dispositivo no Home Assistant

•	Quando o dispositivo estiver conectado ao Home Assistant com o novo firmware, ele será automaticamente detectado e adicionado à interface do usuário do Home Assistant.
•	Agora você pode monitorar e controlar o dispositivo diretamente através do Home Assistant.

Lembre-se de que, ao adicionar ou modificar sensores no arquivo YAML do ESPHome, você precisará recompilar e reenviar o firmware para o dispositivo ESP.

# Acionamento de Rele no ESP8266 conectando ao Home Assistant por ESPHome MQTT  


# Acionamento de Rele duplo no ESP32 conectando ao Home Assistant por ESPHome API Nativa 

Passo 1: Escolher a placa a der sutilizada assim como o módulo redé e porta do NodeMCU a ser utilizada para acionar o Rede

Passo 2: Configurar o complemento ESPHome Dashboard

•	Depois de instalar o complemento, clique em "Configuração".
•	Aqui você pode ajustar as configurações do complemento, como a porta que ele usará.

Passo 3: Crie um arquivo de configuração YAML para o dispositivo ESP

•	No Home Assistant, acesse novamente o painel esquerdo e clique em "Supervisor", depois selecione "ESPHome Dashboard".
•	Clique no botão "+", localizado no canto inferior direito, para adicionar um novo dispositivo ESP.
•	Dê um nome para o dispositivo e, em seguida, clique em "Criar".

Passo 4: Preencha o arquivo de configuração YAML

•	Você será redirecionado para a página de edição do dispositivo. Aqui, você pode começar a preencher o arquivo de configuração YAML com as informações específicas do dispositivo e dos sensores que deseja adicionar.
•	O ESPHome oferece uma documentação abrangente sobre as configurações disponíveis que você pode adicionar ao arquivo YAML para personalizar o comportamento do dispositivo.

Passo 5: Verificar a configuração e compilar o firmware

•	Depois de preencher o arquivo YAML, clique em "Salvar" para verificar a configuração.
•	Se não houver erros, clique em "Compile" para criar o firmware personalizado para o dispositivo.

Passo 6: Flash do firmware para o dispositivo ESP

•	Após a compilação, o firmware estará disponível para download.
•	Você precisará conecta o dispositivo ESP ao computador via USB, para então utilizar uma ferramenta como o "esphome-flasher" para enviar o firmware para o dispositivo.

Passo 7: Monitorar o dispositivo no Home Assistant

•	Quando o dispositivo estiver conectado ao Home Assistant com o novo firmware, ele será automaticamente detectado e adicionado à interface do usuário do Home Assistant.
•	Agora você pode monitorar e controlar o dispositivo diretamente através do Home Assistant.

Lembre-se de que, ao adicionar ou modificar sensores no arquivo YAML do ESPHome, você precisará recompilar e reenviar o firmware para o dispositivo ESP.

# Acionamento de Rele duplo no ESP32 conectando ao Home Assistant por ESPHome MQTT 



# Sites relacionados ao ESP32, ESP8266 e ESPHome

* [Site do ESPhome](https://esphome.io/index.html)
* [Pinout ESP32](https://www.studiopieters.nl/esp32-pinout/)
* [ESP32 WROOM Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-wroom-32e_esp32-wroom-32ue_datasheet_en.pdf)
* 
  
# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)
