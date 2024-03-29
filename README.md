# Hackintosh no Samsung Essentials E30

Ajude-me a melhorar essa EFI também!

<img src="https://i.imgur.com/iiuBNML.png" height="290"> <img src="https://i.imgur.com/kk3rgpQ.png" height="290">
<img src="https://i.imgur.com/QZrrss8.png" height="280">

## Versão usada na EFI:

<p align="center">
<img src="https://i.imgur.com/OYA1y8h.png" height="100" alt="Versão do OpenCore usado nessa EFI" />
</p>

### EFI configurada para Hackintosh no Samsung Essentials E30 NP350XAA-KF3BR (modelo nacional) usando o Open Core Bootloader

<h4>AVISOS IMPORTANTES:</h4>
<ol>
<li><p><i>Eu <b>NÃO</b> testei essa EFI no Big Sur, apenas no Catalina 10.15.7 e no Mojave 10.14.6 e ambas funcionaram muito bem</i></p></li>
<li><p><i>Por se tratar de um hardware simplório, recomendo usar uma versão mais antiga do macOS — como o High Sierra. Caso opte por uma versão antiga, infelizmente, terá de carregar o ônus de não poder instalar alguns aplicativos direto da App Store como: Pages, Keynote, Xcode mais recente, Logic Pro, GarageBand, Final Cut entre outros (Caso queira usar algum aplicativo desses, terá de baixar versões anteriores que tenham compatibilidade com o seu macOS). <b>OBS.: NVMeFix.kext funciona no kernel Darwin 18 (macOS 10.14) em diante. Ela vem desativada por padrão, mas você pode ativar e testar :D</b></i></p></li>
<li><p><i>Eu <b>NÃO</b> me responsabilizo por quaisquer danos que o procedimento possa causar, entenda que o Hackintosh ainda é uma "gambiarra", por isso recomendo um pendrive bootável com a ISO do Windows 10 e um backup prévio dos arquivos caso você não consiga bootar ou fazer algo de errado.</i></p></li>
<li><p><i>Isso <b>NÃO</b> é um tutorial de instalação do macOS, você ainda terá que baixar a imagem de recuperação do macOS <a href="https://dortania.github.io/OpenCore-Install-Guide/installer-guide/">aqui</a>, e colocar os arquivos na raíz do pendrive. Se preferir baixar as imagens do Olarila e usar o <a href="https://www.balena.io/etcher/">balenaEtcher</a>, <a href="https://www.olarila.com/topic/6278-olarila-vanilla-images/">clique aqui</a>.</i></p></li>
<li><p><i><b>NÃO</b> vem com SMBIOS configurado, então recomendo fortemente você baixar o GenSMBIOS <a href="https://github.com/corpnewt/GenSMBIOS">aqui</a> e gerar o seu próprio número de série checando no <a href="https://checkcoverage.apple.com/br/pt/">site da Apple</a> para ver se o número de série gerado é inválido. UTILIZE MacBookPro14,1 como System Product Name. <b>OBS.: É fortemente recomendado cada um que baixar, gerar seu próprio SMBIOS, para não ter futuros erros nos iServices, como: FaceTime, iMessage, iCloud e etc...</b></i></p></li>
  </ol>
<h4>SOBRE ATUALIZAÇÕES DO MACOS:</h4>
<ul>
  <li><p>Realmente <b>NÃO É RECOMENDADO</b> atualizar para versões futuras, havendo assim, quebra de versão. Por exemplo: se você está no macOS 10.14, <b>NÃO ATUALIZE</b> para a 10.15, ou até mesmo para o 11 Big Sur!</p></li>
  <li><p>Atualizações de Segurança, Atualização do Safari, essas mais simples, que não exigem a quebra de versões major, pode fazer sem mais problemas.</p></li>
</ul>

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
  <h6>Recomendo fortemente que você compre um SSD NVME M.2 (pois esse notebook tem suporte a esse tipo de SSD) e instale o macOS nele. <b>Caso você queira comprar um SSD NVME, consulte <a href="https://dortania.github.io/Anti-Hackintosh-Buyers-Guide/Storage.html">esse site</a> para ver quais modelos você NÃO DEVE COMPRAR, pois pode dar conflito com o macOS.</b> Eu tenho atualmente um SSD NVME M.2 de 256GB onde está instalado o macOS Catalina, uso o HD mecânico original dele apenas para armazenar arquivos.</h6></ul>
  
  Como pode ver, ele é um notebook mediano, mas com alguns upgrades, como os citados acima, ele fica perfeito para o Hackintosh em quesito de performance, dá para trabalhar e estudar tranquilamente nele.
  
<h2>O que está funcionando e o que não está funcionando?</h2>
<ul>
  <li><h4>✅   Tela Full HD funcionando muito bem</h4></li>
  <li><h4>✅   Placa de áudio Realtek funcionando muito bem</h4></li>
  <li><h4>✅   Teclado e Mouse USB funcionando bem</h4></li>
  <li><h4>✅   Rede Ethernet (internet via cabo)</h4></li>
  <li><h4>✅   Placa gráfica funcionando e com aceleração via GPU funcionando</h4></li>
  <li><h4>❌   Touchpad ATML3000 NÃO FUNCIONA até o momento</h4></li>
  <h6>Um mouse USB é a melhor alternativa</h6>
  <li><h4>❌   Placa de Wi-Fi Qualcomm Atheros QCA9377 não funciona de jeito nenhum</h4></li>
  <h6>Ela é considerada uma placa morta no mundo Hackintosh, porque é antiga e mesmo assim não tem suporte e nenhum desenvolvedor se interessou em criar uma kext para ela</h6>
  <h6>Se quiser usar a internet, há três opções: ou usando pelo cabo Ethernet (como eu), ou comprando um dongle Wi-Fi (recomendo o TL-WN725N ou o TL-WN823N, ambos da TP-LINK e em seguida baixar o driver correspondente no <a href="https://www.tp-link.com/br/support/download/">site deles</a>), ou usando o Tethering USB em um telefone Android, baixando <a href="https://github.com/jwise/HoRNDIS/releases"> este driver</a> para macOS. OBS.: esse driver funciona até o macOS Mojave 10.14, no Catalina não funciona e creio que nem no Big Sur funcione.</h6>

<h2>Outras prints:</h2>
<img src="https://i.imgur.com/4Qdtl6B.png" height="400">
<img src="https://i.imgur.com/agcdYxE.png" height="400">
<img src="https://i.imgur.com/WjPzggp.png" height="400">
<img src="https://i.imgur.com/lrzJQGD.png" height="400">
<img src="https://i.imgur.com/d5IU0lN.png" height="400">

<img src="https://i.imgur.com/dC3DUw5.png" height="400">
<img src="https://i.imgur.com/YotKezR.png" height="400">
<img src="https://i.imgur.com/XLxNOvZ.png" height="400">
<img src="https://i.imgur.com/KXFKgyJ.png" height="400">

<h3>Agradecimentos:</h3>
<p>Para <a href="https://github.com/acidanthera">Acidanthera</a> pelo OpenCore em si, pelas ferramentas e pelas kexts;</p>
<p>Para <a href="https://github.com/corpnewt">CorpNewt</a> pelas excelentes e muito úteis ferramentas também;</p>
<p>Para <a href="https://github.com/RehabMan">RehabMan</a> e <a href="https://github.com/Sniki">Sniki</a> pela kext UsbInjectAll;</p>
<p>Para alguns desenvolvedores independentes que fizeram algumas kexts usadas.</p>
