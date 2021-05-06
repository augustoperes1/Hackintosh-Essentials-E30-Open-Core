# Hackintosh no Samsung Essentials E30
<img src="https://i.imgur.com/iiuBNML.png" height="300"> <img src="https://i.imgur.com/QZrrss8.png" height="300">

EFI configurada para Hackintosh no Samsung Essentials E30 NP350XAA-KF3BR (modelo nacional) usando o Open Core Bootloader na variante RELEASE

<h4>AVISOS IMPORTANTES:</h4>
<ol>
<li><p><i>Eu <b>NÃO</b> testei essa EFI no Big Sur, apenas no Catalina 10.15.7 (versão que estou utilizando no momento) e no Mojave 10.14.6 e ambas funcionaram muito bem</i></p></li>
<li><p><i>Eu <b>NÃO</b> me responsabilizo por quaisquer danos que o procedimento possa causar, entenda que o Hackintosh ainda é uma "gambiarra", por isso recomendo um pendrive bootável com a ISO do Windows 10 e um backup prévio dos arquivos caso você não consiga bootar ou fazer algo de errado.</i></p></li>
<li><p><i>Isso <b>NÃO</b> é um tutorial de instalação do macOS, você ainda terá que baixar a imagem de recuperação do macOS <a href="https://dortania.github.io/OpenCore-Install-Guide/installer-guide/">aqui</a>, e colocar os arquivos na raíz do pendrive.</i></p></li>
<li><p><i><b>NÃO</b> vem com SMBIOS configurado, então recomendo fortemente você baixar o GENSMBIOS <a href="https://github.com/corpnewt/GenSMBIOS">aqui</a> e gerar o seu próprio SMBIOS checando no <a href="https://checkcoverage.apple.com/br/pt/">site da Apple</a> para ver se o SMBIOS gerado é válido. UTILIZE MacBookPro14,1 como System Product Name</i></p></li>
  </ol>

<h2>Vamos conferir o hardware desse notebook:</h2>
<ul>
  <li><h4>Processador Intel Core i3 Dual-Core 7020U com clock de 2,3Ghz</h4></li>
  <h6>Processadores com final U são conhecidos como processadores mobile, ou seja: de baixo custo e com baixo consumo de energia</h6></ul>
<ul>
  <li><h4>Memória RAM de 4GB com frequência de 2400Mhz em único slot</h4></li>
  <h6>Recomendo fazer um upgrade para 8 ou 16gb de memória RAM, assim o macOS trabalha com folga e sem engasgos. Com 4GB funciona, mas eu não recomendo instalar as últimas versões como Catalina ou Big Sur. Instale uma versão mais antiga como o High Sierra, ou até o Mojave se você quiser o suporte ao tema escuro</h6>
</ul>
<ul>
  <li><h4>Placa de vídeo Intel HD Graphics 620 geração Kaby Lake</h4></li>
  <h6>É a placa padrão dos notebooks com o processador U da 7ª geração da Intel, sendo assim, tem um ótimo suporte da Apple, além de estar bem configurada para o E30, portanto não recomendo mecher muito.</h6>
</ul>
<ul>
  <li><h4>HD mecânico com 1TB de armazenamento e funcionando a 5400 RPM</h4></li>
  <h6>Recomendo fortemente que você compre um SSD NVME M.2 (pois esse notebook tem suporte a esse tipo de SSD) e instale o macOS nele. Eu tenho atualmente um SSD NVME M.2 de 256GB onde está instalado o macOS Catalina, uso o HD mecânico original dele apenas para armazenar arquivos.</h6></ul>
  
  Como pode ver, ele é um notebook mediano, mas com alguns upgrades, como os citados acima, ele fica perfeito para o Hackintosh em quesito de performance, dá para trabalhar e estudar tranquilamente nele.
  
<h2>O que está funcionando e o que não está funcionando?</h2>
<ul>
  <li><h4>✅   Tela Full HD funcionando muito bem</h4></li>
  <li><h4>✅   Placa de áudio Realtek funcionando muito bem</h4></li>
  <li><h4>✅   Teclado e Mouse USB funcionando bem</h4></li>
  <li><h4>✅   Rede Ethernet (internet via cabo)</h4></li>
  <li><h4>✅   Placa gráfica funcionando e com aceleração via GPU funcionando</h4></li>
  <li><h4>❌   Touchpad ATMEL3000 NÃO FUNCIONA até o momento</h4></li>
  <h6>Um mouse USB é a melhor alternativa</h6>
  <li><h4>❌   Placa de Wi-Fi Qualcomm Atheros QCA9377 não funciona de jeito nenhum</h4></li>
  <h6>Se quiser usar a internet, há três opções: ou usando pelo cabo Ethernet (como eu), ou comprando um dongle Wi-Fi (recomendo o TL-WN725N da TP-LINK e em seguida baixar o driver correspondente no <a href="https://www.tp-link.com/br/support/download/tl-wn725n/v3/#Driver">site deles</a>), ou usando o Tethering USB em um telefone Android, baixando <a href="https://github.com/jwise/HoRNDIS/releases"> este driver</a> para macOS.</h6>

<h2>Outras prints:</h2>
<img src="https://i.imgur.com/4Qdtl6B.png" height="400">
<img src="https://i.imgur.com/agcdYxE.png" height="400">
<img src="https://i.imgur.com/WjPzggp.png" height="400">
<img src="https://i.imgur.com/lrzJQGD.png" height="400">
<img src="https://i.imgur.com/d5IU0lN.png" height="400">
