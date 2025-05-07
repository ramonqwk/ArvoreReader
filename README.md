<a href="#">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=150&color=2c2f33&text=Árvore%20Reader&fontSize=40&fontAlignY=33&fontColor=ffffff"/>
</a>

<div align="center">
  <img src="https://i.imgur.com/RcTh2Dg.png?maxwidth=520&shape=thumb&fidelity=high" width="100px" alt="Alura Logo"/>
</div>

<h2 align="center"><strong>Árvore Reader</strong></h2>

<p align="center"><strong>📖 ÁrvoreReader: Automatiza a leitura de livros na plataforma Árvore, passando páginas automaticamente com intervalos configuráveis.</strong></p>

<p align="center"><strong>Para usar, copie o código abaixo:</strong></p>

<div align="center">

<pre>
<code>
javascript:(function(){let isStopped=true;const arvoreReader=()=>{const nextPageButton=document.querySelector('#root > main > div.sc-gTRrQi.cFSQkY > div:nth-child(3) > button');const pageCount=document.querySelector('#footer-nav > div.sc-dSJDGZ.gTLZcZ > div.sc-iVCKna.dpHZdz > span');const floatingButton=document.createElement('div');floatingButton.style.position='fixed';floatingButton.style.top='20px';floatingButton.style.right='20px';floatingButton.style.width='70px';floatingButton.style.height='70px';floatingButton.style.borderRadius='50%';floatingButton.style.background='#ffffff';floatingButton.style.display='flex';floatingButton.style.alignItems='center';floatingButton.style.justifyContent='center';floatingButton.style.cursor='pointer';floatingButton.style.boxShadow='0 4px 10px rgba(0, 0, 0, 0.2)';floatingButton.style.zIndex='1000';const img=document.createElement('img');img.src='https://i.imgur.com/RcTh2Dg.png';img.style.width='40px';img.style.height='auto';img.style.borderRadius='50%';img.style.objectFit='cover';floatingButton.appendChild(img);document.body.appendChild(floatingButton);let isDragging=false;let offsetX,offsetY;floatingButton.addEventListener('mousedown',(e)=>{isDragging=true;offsetX=e.clientX-floatingButton.getBoundingClientRect().left;offsetY=e.clientY-floatingButton.getBoundingClientRect().top;document.body.style.userSelect='none';});document.addEventListener('mousemove',(e)=>{if(isDragging){floatingButton.style.top=`${e.clientY-offsetY}px`;floatingButton.style.left=`${e.clientX-offsetX}px`;}});document.addEventListener('mouseup',()=>{isDragging=false;document.body.style.userSelect='';});const createMenu=()=>{const menu=document.createElement('div');menu.style.position='fixed';menu.style.top='80px';menu.style.right='20px';menu.style.width='320px';menu.style.backgroundColor='#ffffff';menu.style.padding='20px';menu.style.borderRadius='15px';menu.style.boxShadow='0 10px 20px rgba(0, 0, 0, 0.15)';menu.style.display='none';menu.style.zIndex='1000';menu.style.transition='all 0.3s ease';const title=document.createElement('h2');title.innerText='ÁrvoreReader';title.style.textAlign='center';title.style.color='#333';menu.appendChild(title);const speedLabelMin=document.createElement('label');speedLabelMin.innerText='Tempo Mínimo (Segundos):';menu.appendChild(speedLabelMin);const speedMinInput=document.createElement('input');speedMinInput.type='number';speedMinInput.value=5;speedMinInput.step=1;speedMinInput.min=1;speedMinInput.style.width='100%';speedMinInput.style.marginBottom='10px';menu.appendChild(speedMinInput);const speedLabelMax=document.createElement('label');speedLabelMax.innerText='Tempo Máximo (Segundos):';menu.appendChild(speedLabelMax);const speedMaxInput=document.createElement('input');speedMaxInput.type='number';speedMaxInput.value=10;speedMaxInput.step=1;speedMaxInput.min=1;speedMaxInput.style.width='100%';menu.appendChild(speedMaxInput);const startButton=document.createElement('button');startButton.innerText='Iniciar Leitura';startButton.style.backgroundColor='#808080';startButton.style.color='white';startButton.style.padding='10px';startButton.style.border='none';startButton.style.borderRadius='5px';startButton.style.cursor='pointer';startButton.style.width='100%';menu.appendChild(startButton);const footer=document.createElement('div');footer.innerHTML='Feito por <strong>Ramon</strong>';footer.style.textAlign='center';menu.appendChild(footer);document.body.appendChild(menu);const secondsToMilliseconds=(seconds)=>seconds*1000;const randomAtRange=(min,max)=>Math.floor(Math.random()*(max-min+1))+min;const read=()=>{const actualPage=pageCount?.textContent?.split('/')[0];const lastPage=pageCount?.textContent?.split('/')[1];if(!isStopped){if(actualPage!==lastPage){nextPageButton.click();setTimeout(read,secondsToMilliseconds(randomAtRange(Number(speedMinInput.value),Number(speedMaxInput.value))))}else{isStopped=true;startButton.innerText='Reiniciar Leitura';const backButton=document.querySelector('button[aria-label="Sair da leitura"]');const markAsReadButton=[...document.querySelectorAll('button')].find(el=>el.textContent==='Marcar como lido e sair');if(markAsReadButton)markAsReadButton.click();else if(backButton)backButton.click();else history.back();}}};startButton.addEventListener('click',()=>{if(isStopped){isStopped=false;startButton.innerText='Parar Leitura';read();}else{isStopped=true;startButton.innerText='Iniciar Leitura';}});floatingButton.addEventListener('click',()=>{menu.style.display=(menu.style.display==='none'||menu.style.display==='')?'block':'none';});};createMenu();};if(location.hostname!=='e-reader.arvore.com.br'){window.open('https://e-reader.arvore.com.br','_blank');}else{arvoreReader();}})();
</code>
</pre>

</div>

### Método 2: Criando um bookmarklet (PC/Mobile)
1. Crie um novo favorito/bookmark
2. No campo de URL, cole o código JavaScript acima
3. Salve e clique nele quando estiver na página de leitura

<p align="center">
<sub><i>Clique abaixo para entrar no servidor do Discord ou doar</i></sub>
</p>

<p align="center">
    <a href="https://discord.gg/cZVtWmWsUE"><img width="15%" alt="Discord (CS)" title="Discord (Kahoot Answer)" src="https://i.imgur.com/r0YUgMR.png"/></a>
  &nbsp;
    <a href="https://pixgg.com/Ramon"><img width="15%" alt="Doar" title="Doar" src="https://i.imgur.com/yLUUqaa.png"/></a>
</p>

<p align="center">
  <a href="#"><img src="https://komarev.com/ghpvc/?username=Ramonqwk&style=for-the-badge&label=Views:&color=gray"/></a>
</p>

---

<!-- Créditos -->
<div align="center">
  <img src="https://i.imgur.com/gi0h7c1.jpeg" width="150px" alt="Ramon Profile"/>
  <h3 style="color: #e86a04; animation: pulse 2s infinite;">Criado por Ramon!</h3>
</div>

<a href="#"><img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=150&color=ffffff&section=footer"/></a>

## ⚠️ Aviso Legal

Este script é apenas para fins educacionais. Use por sua conta e risco e respeite os termos de serviço da plataforma.
