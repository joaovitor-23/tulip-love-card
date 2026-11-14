# 🌷 Cartão Vivo — Buquê de Tulipas & Coração de Amor

Um cartão digital interativo feito em **HTML5 Canvas** e **JavaScript puro (Vanilla JS)** que une duas animações procedurais em tempo real: um buquê de 13 tulipas amarelas desabrochando em 3D projetado e um coração pulsante formado pela frase *"Eu te amo"* em 20 idiomas, acompanhado de partículas douradas, mensagem personalizada e trilha sonora de fundo.

---

## ✨ Recursos

- **Buquê Procedural 3D (`Uint32Array` + *Painter's Algorithm*):** 13 tulipas amarelas e 11 folhas distribuídas em leque com iluminação direcional, nervuras, curvatura orgânica e balanço suave.
- **Coração Multilíngue:** Desenho paramétrico preenchido dinamicamente com *"Eu te amo"* em 20 idiomas diferentes, com animação de entrada, brilho cintilante (*shimmer*) e batimento suave.
- **Mensagem Personalizável:** Exibição elegante de dedicatória e assinatura configuráveis diretamente no código.
- **Trilha Sonora Flexível:** Suporte nativo para **arquivos de áudio locais** (`.mp3`, `.ogg`, `.wav`, `.m4a`) e links do **YouTube / YouTube Music** via *IFrame Player API*.
- **Interatividade & Performance:**
  - Toque ou clique em qualquer ponto da tela para soltar faíscas douradas e corações (`♥`).
  - **Espaço:** Pausa ou retoma a animação.
  - **R:** Reinicia a animação desde o início.
  - Arquivo único (`.html`), sem dependências externas ou etapas de *build*.

---

## 🚀 Como Usar e Personalizar

1. Baixe ou clone este repositório.
2. Abra o arquivo `index.html` (ou `tulipas_coracao_cartao.html`) em qualquer editor de texto.
3. No início da tag `<script>`, edite o objeto `CONFIG_CARTAO` conforme desejar:

```javascript
const CONFIG_CARTAO = {
  mostrarTexto: true,
  mensagem: "Cada pétala que desabrocha guarda um pouco do carinho que sinto por você.",
  assinatura: "Com todo o meu amor ♥",

  // Aceita arquivo local ("musica.mp3"), link direto ou URL do YouTube
  musicaUrl: "nossa_musica.mp3",
  inicioSegundos: 0,
  volumeMusica: 0.60,
  repetirMusica: true,
  mostrarBotaoSom: true
};
```

## 🛠️ Tecnologias Utilizadas

- **HTML5 Canvas API** (`ImageData` / `Uint32Array` para renderização de pixels em alta velocidade)
- **JavaScript (ES6+)** com geradores pseudoaleatórios determinísticos (*Mulberry32* e *Park-Miller*)
- **YouTube IFrame Player API** & **HTML5 Audio API**
- **CSS3** responsivo (adaptado para desktop e dispositivos móveis)
