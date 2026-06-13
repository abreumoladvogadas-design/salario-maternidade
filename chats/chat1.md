# Landing Page Advogada Previdenciária

_Started 2026-06-13 18:37 UTC_

---

## User

quero que gere uma landing page para eu enviar as minhas clientes e compartilhar que sou advogada previdenciaria e posso fazer seus salarios maternidade. o tempo ideal é o momento em que esta gestante. a tranquilidade de ter seu bebe e garantir seu salario maternidade nao tem preco.
basta nos contatar, enviar os documentos: identidade, cadastro do bolsa familia ou folha resumo (se tiver), comprovante de residencia, cartao de gestante e agendar uma reuniao virtual conosco.

## Assistant

_[tool: view_image]_

_[tool: view_image]_

_[tool: view_image]_

_[tool: view_image]_

Vou primeiro examinar as imagens que você anexou para entender a marca, as cores e o conteúdo.

_[tool: update_todos]_

_[tool: copy_starter_component]_

Tenho tudo que preciso: a marca **Abreu | Mol Advogadas** (Vivian Mol, previdenciária), as cores (rosé/mauve, taupe quente, blush creme), o tom humanizado e todo o conteúdo. Como o briefing está completo e a identidade bem definida, vou direto para a construção — uma landing page **mobile-first** (suas clientes vão abrir pelo WhatsApp), calorosa e acolhedora.

Vou usar slots de imagem para você soltar suas fotos reais depois. Deixe-me preparar a estrutura.

_[tool: update_todos]_

O sistema está claro. Vou construir agora:

**Sistema de design** — Cores da marca: rosé/mauve profundo (`#a85f70`), taupe quente (`#6e615f`), blush creme (`#f7ece9`). Fontes: **Cormorant Garamond** (títulos emocionais elegantes, como no flyer) + **Poppins** (corpo, acolhedor — combina com os cards "Quem somos"). Motivo recorrente: o coração ♡ da marca. Mobile-first com reflow fluido.

_[tool: dc_write]_

_[tool: update_todos]_

_[tool: show_html]_

_[tool: show_html]_

_[tool: multi_screenshot]_

Hero está em animação (opacity 0 → 1). Deixa eu capturar após ela completar e ver as seções.

_[tool: get_webview_logs]_

_[tool: eval_js]_

Só o header renderizou — o restante está ausente e a página não rola. Algo quebrou a renderização. Vou checar os logs.

_[tool: eval_js]_

Conteúdo existe no DOM (4518px, 7 seções). Deixa eu checar se há um problema de visibilidade/posição.

_[tool: save_screenshot]_

O conteúdo está visível no DOM (h1 no topo 169px, opacity 1). A captura via html-to-image deve estar falhando. Vou fazer uma captura real em disco.

_[tool: save_screenshot]_

_[tool: eval_js]_

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

O DOM confirma que tudo está renderizado e visível (elementFromPoint pega o H1 "Se o seu..." no topo). As capturas em branco são um artefato da ferramenta com este conteúdo. Mas vou eliminar qualquer risco: removo as animações de entrada (que iniciam em opacity:0) e ajusto a altura do slot da foto. Assim garanto que nenhuma cliente veja conteúdo invisível.

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

O slot não respeitou `aspect-ratio` (ficou 160px). Vou dar altura explícita aos dois slots de foto.

_[tool: save_screenshot]_

_[tool: eval_js]_

O DOM confirma repetidamente que tudo está renderizado, visível e no topo (elementFromPoint retorna o H1). Esta ferramenta de captura específica não consegue pintar o corpo desta página, mas o navegador real renderiza normalmente. Deixa eu confirmar o conteúdo de todas as seções de forma definitiva.

_[tool: read_file]_

Todas as seções e títulos presentes. ✅ Mas os slots de imagem continuam travados em 160px — ignoram a altura inline. Vou ler o componente para entender como dimensioná-lo.

_[tool: eval_js]_

Vou inspecionar o estilo aplicado ao slot ao vivo para entender por que a altura não pega.

_[tool: grep]_

_[tool: show_html]_

O arquivo está correto, mas o preview estava mostrando um render desatualizado. Vou recarregar do zero.It was a stale preview — now it renders beautifully. The hero looks exactly right: elegant Cormorant headline with rose emphasis on "cuidado" and "direito", the photo slot sized properly. Let me capture the rest of the page.

_[tool: multi_screenshot]_

_[tool: save_screenshot]_

O hero está perfeito agora. O multi_screenshot (html-to-image) ignora o scroll. Vou usar captura real de viewport para ver as seções abaixo.

_[tool: eval_js]_

O scroll da window não funciona — o runtime do DC provavelmente rola num container interno. Vou localizar o elemento rolável.

_[tool: save_screenshot]_

Scroll confirmado em HTML/BODY. A ferramenta de captura reseta o scroll. Vou contornar fixando o conteúdo deslocado antes de capturar.

_[tool: eval_js]_

Excelente — todas as seções inferiores renderizam lindamente: cards de benefícios, passo a passo, checklist de documentos, CTA e rodapé. Vejo um possível sobreposição de texto na seção CTA final. Vou verificar as posições reais.

_[tool: delete_file]_

_[tool: update_todos]_

Confirmado: o layout real está correto (gap de 16px entre título e parágrafo, sem sobreposição — o que apareceu foi artefato da captura). Tudo renderiza lindamente. Vou limpar os arquivos de teste e entregar.Pronto! A landing page está completa e renderizando perfeitamente. Vou abrir para você.

_[tool: done]_

Sua landing page **Salário Maternidade — Abreu | Mol** está pronta. 💗

**O que ela tem:**
- **Hero** acolhedor com a frase da marca *"Se o seu maior cuidado foi com eles, o nosso é com o seu direito"* e o selo *"Eu fiz o salário maternidade deles. Posso fazer o seu também!"*
- **Seção do direito** — reforçando o momento ideal: *enquanto você está gestante*
- **4 benefícios** (direito por lei, auxílio na licença, tranquilidade, atendimento humanizado)
- **Passo a passo** (WhatsApp → documentos → reunião virtual → "eu cuido de tudo") com o **checklist de documentos** que você pediu
- **Faixa emocional** + **bio da Vivian** + **CTA final** com WhatsApp e as **duas unidades** (São José da Safira e Marilac) no rodapé
- Botões de WhatsApp já com **mensagem pré-preenchida** para a cliente
- **Mobile-first** — abre lindo no celular quando você compartilhar

**Dois pontos para você confirmar:**
1. **Número de WhatsApp:** usei o **33 99874-0709** (do flyer de salário maternidade). Atenção: os cartões "Quem somos" mostram **33 98704-0709** — me diga qual é o correto e eu ajusto em todos os botões/links.
2. **Fotos:** deixei dois espaços para você **arrastar suas fotos reais** (você com os bebês no hero, e seu retrato na bio) — é só soltar a imagem em cima. Quer que eu deixe algum outro espaço para foto?

Quer alguma variação de cor, mais depoimentos de clientes, ou uma seção de dúvidas frequentes?

## User

numero correto: 33 998740709
Consegue ja inserir as fotos para mim?
no titulo, voce colocou Se o seu maior cuidado foi com eles, o nosso é com o seu direito. a frase esta no passado. se minha intencao e que elas me procurem gravidas, nao pode colocar assim pq vai induzir errado. refaça. quero que elas me procurem gravidas para que eu possa garantir os beneficios delas.

## Assistant

_[tool: image_metadata]_

_[tool: snip]_

Vou ajustar tudo. O número já está correto (33 99874-0709). Sobre as fotos: a única foto sua que tenho é a do flyer — vou recortá-la de lá. E você tem toda razão sobre o título no passado: vou refazer para falar com a gestante **agora**.

Deixa eu ver as dimensões do flyer para recortar sua foto com precisão.

_[tool: view_image]_

_[tool: run_script]_

Boa — vou recortar sua foto do flyer (você com os dois bebês) para o hero, e um recorte mais fechado do seu rosto para a bio. Deixa eu gerar os recortes.

_[tool: run_script]_

_[tool: view_image]_

_[tool: view_image]_

_[tool: run_script]_

A bio ficou ótima. No hero, apareceu um resíduo no canto superior esquerdo ("ALIZADA" e uma fresta da faixa rosa). Vou recortar de novo, um pouco mais fechado.

_[tool: view_image]_

_[tool: run_script]_

Pode ser cache do nome de arquivo. Vou gerar com um nome novo e coordenadas mais à direita para limpar de vez os resíduos da esquerda.

_[tool: view_image]_

_[tool: run_script]_

Limpo agora. Só faltou um pouco de testa no topo e a cabecinha do bebê à esquerda. Vou equilibrar: incluir mais da esquerda e dar respiro no topo, mantendo sem resíduos.

_[tool: view_image]_

_[tool: copy_files]_

_[tool: delete_file]_

v3 ficou ótimo — seu rosto com respiro e os dois bebês visíveis. Vou finalizar: organizar os arquivos, inserir as fotos nos slots e reescrever o título no presente, falando direto com a gestante.

_[tool: read_file]_

_[tool: read_file]_

Agora vou aplicar todas as mudanças: título no presente focado na gestante, eyebrow, subtexto, e inserir as fotos nos dois slots.

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: show_html]_

_[tool: run_script]_

A foto entrou e o título ficou perfeito no presente. Mas o slot do hero está cortando os olhos dela no topo (proporção paisagem). Vou recortar a foto em proporção retrato e travar o slot nessa proporção para mostrar o rosto inteiro.

_[tool: view_image]_

Vou cuidar das duas coisas. Primeiro, sobre o Instagram: deixa eu tentar acessar.

_[tool: web_fetch]_

_[tool: run_script]_

Sobre o Instagram: infelizmente **não consigo acessar o Instagram** — o perfil exige login e as fotos ficam protegidas, então não dá para puxar imagens de lá automaticamente. A melhor forma é você **anexar aqui a foto que você mais gosta** (pode arrastar pra cá) que eu coloco no hero na hora. 💛

Enquanto isso, vou resolver a foto com os bebês: o problema é que o recorte estava cortando seu rosto. Vou **afastar e reenquadrar** mostrando seu rosto inteiro, e limpar os resíduos da esquerda.

_[tool: view_image]_

_[tool: run_script]_

O `view_image` está me mostrando uma versão em cache (sempre a mesma). Vou salvar com nome novo para confirmar o recorte real.

_[tool: view_image]_

_[tool: str_replace_edit]_

_[tool: delete_file]_

Agora sim — esse é o recorte real (o `view_image` estava em cache). Seu rosto inteiro, sorriso visível, sem resíduos. Agora vou travar os slots na proporção retrato para a foto aparecer completa, sem cortar o rosto.

_[tool: show_html]_

_[tool: save_screenshot]_

Perfeito — agora seu rosto aparece inteiro, com sorriso e olhos visíveis. Era exatamente isso. Vou conferir rapidamente a foto da bio também.

_[tool: delete_file]_

_[tool: eval_js]_

A bio também ficou ótima. Tudo funcionando. Vou limpar os arquivos temporários e finalizar.Pronto! 💛

_[tool: done]_

Tudo ajustado:

✅ **Título refeito no presente, falando com a gestante** — *"Você cuida da sua gravidez. Eu cuido do seu direito."* + subtexto *"Está grávida? O melhor momento para garantir o seu salário maternidade é agora, durante a gestação..."* — agora induz a cliente certa: te procurar **grávida**.

✅ **Foto reenquadrada** — afastei e recortei em proporção retrato; agora seu **rosto aparece inteiro** (sorriso, olhos) com o bebê no colo, e sem os resíduos da arte.

✅ **Número confirmado**: 33 99874-0709 em todos os botões.

⚠️ **Sobre o Instagram**: não consigo acessar seu perfil (o Instagram exige login e bloqueia o acesso às fotos). Para colocar uma foto sua mais bonita, é só **arrastar a imagem aqui no chat** que eu troco no hero na hora — ou você pode **arrastar direto sobre a foto** na página (os dois espaços de foto aceitam soltar uma imagem nova).

Quer que eu ajuste mais o reenquadramento, troque a foto da bio, ou adicione uma seção de dúvidas frequentes (FAQ)?

## User

troque a minha foto

## Assistant

_[tool: image_metadata]_

_[tool: image_metadata]_

_[tool: snip]_

Ótimas fotos! Vou usar a do **Congresso IEPREV** no hero (profissional e no tema previdenciário) e a **foto em família** na bio (mais humana, combina com "quem vai cuidar de você"). Deixa eu ver as dimensões para recortar bem.

_[tool: view_image]_

_[tool: view_image]_

_[tool: run_script]_

Plano: **hero** = congresso (recorte da cintura para cima, rosto em destaque, com o painel "Direito Previdenciário" ao fundo); **bio** = foto em família (você em destaque, mais humana). Vou recortar e conferir.

_[tool: view_image]_

_[tool: view_image]_

_[tool: run_script]_

A bio ficou linda — seu rosto em destaque com um toque familiar. No hero, vou fechar um pouco mais para o rosto ficar maior e mais visível.

_[tool: view_image]_

_[tool: copy_files]_

_[tool: delete_file]_

O hero ficou ótimo — rosto em destaque, no congresso de Direito Previdenciário. Vou finalizar: organizar os arquivos e apontar os slots para as novas fotos.

_[tool: image_metadata]_

_[tool: view_image]_

_[tool: run_script]_

Essa versão mostra seu rosto bem melhor! Vou recortar para remover o texto do flyer na esquerda, mantendo seu rosto e os bebês.

_[tool: view_image]_

_[tool: copy_files]_

_[tool: delete_file]_

_[tool: str_replace_edit]_

Perfeito — rosto inteiro, sorriso lindo, com os bebês, e sem o texto do flyer. Vou colocar essa na foto de cima e apontar os slots para as fotos certas (incluindo a de família na bio).

_[tool: show_html]_

The hero agora mostra essa foto — seu rosto inteiro, sorriso, e o bebê no colo, sem o texto do flyer. 💛 Vou conferir a bio (foto em família) rapidamente.

_[tool: save_screenshot]_

_[tool: delete_file]_

As duas fotos estão certas agora. Vou limpar os temporários e finalizar.Pronto! ✨

_[tool: done]_

Troquei as fotos:

✅ **Foto de cima (hero)** — coloquei a versão que você enviou, recortada para mostrar seu **rosto inteiro com sorriso** e o bebê no colo, sem o texto do flyer na lateral.

✅ **Foto da bio** — usei a foto em **família** (você em destaque), que combina com o "Quem vai cuidar de você" e reforça o lado humano.

Quer que eu ajuste o enquadramento de alguma delas, ou seguimos para outra parte (ex.: seção de dúvidas frequentes)?

## User

substitua minha foto de perfil. nao aproxime o rosto. deixe como esta. gostei assim.

## Assistant

_[tool: image_metadata]_

_[tool: snip]_

_[tool: run_script]_

A foto profissional ficou ótima — vou usá-la **inteira, sem aproximar o rosto**, como você pediu. Ela é 2:3, então vou ajustar o slot para mostrar a foto completa, sem cortar nada. Primeiro otimizo o arquivo (está pesado pra abrir no celular).

_[tool: str_replace_edit]_

_[tool: delete_file]_

_[tool: show_html]_

_[tool: save_screenshot]_

_[tool: delete_file]_

A foto de perfil agora aparece **inteira, como você gostou** — sem aproximar o rosto. Profissional e elegante na seção da bio. Vou limpar e finalizar.Pronto! 💼

_[tool: done]_

Substituí sua foto de perfil pela **foto profissional**, mantida **inteira, sem aproximar o rosto** — exatamente como você gostou. Ficou elegante e profissional na seção "Quem vai cuidar de você". ✨

Quer ajustar mais alguma coisa ou seguimos para uma próxima parte (ex.: dúvidas frequentes, depoimentos)?

## User

substitua a foto com os bebes por essa. esta mais bonita e profissionalç. quero que ela apareca por completo.

## Assistant

_[tool: image_metadata]_

_[tool: snip]_

_[tool: run_script]_

Foto linda e profissional! Ela é praticamente 3:4, então vai aparecer **completa**. Vou otimizar e colocar no hero.

_[tool: str_replace_edit]_

_[tool: delete_file]_

_[tool: show_html]_

_[tool: done]_

A nova foto profissional com os bebês está no hero, **aparecendo completa** — você sorrindo com os dois gêmeos, num clima acolhedor e profissional. 💕Pronto! Substituí a foto do hero pela nova foto profissional com os bebês, **mostrada por completo** — você sorrindo com os dois gêmeos, com um fundo acolhedor e elegante.

Agora a landing page está com fotos profissionais nos dois lugares (hero + bio). Quer ajustar mais algo ou adicionar uma seção nova (dúvidas frequentes, depoimentos)?

