## Teste de web crawling/scraping
---
Teste proposto:
- Acesse o link http://www.freeproxylists.net e capture a lista de proxies ( até a página 7 ), considere usar threads para melhorar o tempo de execução.
- Realize o parser dos dados de ip,porta,protocolo,país e uptime.
- Save a lista de proxies em um arquivo com nome proxies.json.
- Imprima a quantidade de proxies capturados e o tempo de execução.
#### Sobre o projeto e a teoria considerada
O programa foi desenvolvido no jupyeter notebook. 
Foi utilizada uma VPN para alterar meu IP para evitar o bloqueio e o recaptcha foi resolvido manualmente. 

O ideal é evitar que os captchas apareçam e para isso existem práticas que ajudam. Seguem algumas abaixo.

Práticas para evitar block e aparecimento de recaptcha ao realizar scraping:   
- Rotação de IPs:

  Os proxies atuam como intermediários entre o solicitante e o servidor.Quando acessamos muitas vezes pelo menos IP o site detecta a automatização, já que o envio de muitas requests de um único endereço IP é uma indicação clara de que você está automatizando
  Na pasta "Rotação de ips" fiz um programa que simula como seria, mas como os IPs em sua maioria falham, (são free proxies), ficou só como teste. Existem serviços pagos que oferencem servidores proxies para fazer isso. 
  
- Rotação de user agents:

  User Agent é uma string enviada pelo navegador web do usuário para um servidor web no cabeçalho HTTP para identificar o tipo de navegador em uso, sua versão e o sistema operacional, ou seja, tendo uma lista de agentes para rotacionar, pode ajudar a mascarar seu raspador como um navegador da web.
  
- Desativar sinalizadores do WebDriver do indicador de automação. Exemplos abaixo.
  
        navigator.webdriver :A propriedade navigator.webdriver é uma propriedade do objeto navigator que normalmente é definida como true quando o navegador está sendo controlado por um WebDriver, como o Selenium. Ela é frequentemente usada pelos sites para detectar o uso automatizado e impedir o acesso a determinados recursos.

        useAutomationExtension :A extensão de automação do usuário é uma extensão do Google Chrome que é carregada automaticamente quando o navegador é controlado por meio de automação, como o Selenium WebDriver. Essa extensão pode ser responsável por alterar o comportamento padrão do navegador em relação à automação, o que pode resultar em detecção e bloqueio por parte de sites ou aplicativos.

- Usar tempos mais parecidos com o que um humano levaria. Fazer uso de esperas com tempos diferentes, rolagem mais lenta etc.Exemplos abaixo:
  
       time.sleep() 
       WebDriverWait() 
Sobre o arquivo requirements.txt, é possível ver que existem bibliotecas que não usei no código postado, mas durante meu aprendizado e tentativas de usa-las, acabei instalando no kernel que usei para desenvolver o projeto. Mesmo se não presentes no código, são usadas em web-scraping.
