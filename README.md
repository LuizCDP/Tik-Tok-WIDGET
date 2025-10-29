# 📱 Widget TikTok / YouTube / Discord e MAIS! — por CDP

## Introdução

Este projeto apresenta um **widget dinâmico, moderno e interativo** que exibe informações de perfis do TikTok, YouTube ou Discord. O componente é totalmente responsivo, estiloso e fácil de integrar a qualquer página web.

O widget foi desenvolvido por **CDP** e utiliza apenas **HTML, CSS e JavaScript puro**, sem dependências externas complicadas. Ele aplica efeitos visuais avançados, como hover animado, animação de logo, suporte a modo escuro e adaptação automática das informações conforme a plataforma.

---

## Funcionalidades Principais

- **Detecção automática de plataforma**: TikTok, YouTube ou Discord
- **Exibição de informações dinâmicas**:
  - TikTok: Seguidores, Seguindo, Curtidas
  - YouTube: Inscritos, Quantidade de vídeos
  - Discord: Nome do servidor, Membros
- **Atualização automática do logotipo**
- **Nome de usuário extraído da URL**
- **Animações e transições suaves**
- **Hover interativo** com mudanças de cor e opacidade
- **Compatibilidade com modo escuro**

---

## Estrutura do Widget

### HTML Base

```html
<a href="https://www.tiktok.com/@usuario" id="tiktok-link">
    <div class="tiktok-profile" id="tiktok-profile">
        <img src="{url-da-imagem}" alt="Foto de Perfil" id="perfil">
        <div class="info">
            <div class="username"><h5>{Nome de usuario}</h5></div>
            <div class="followers"><p>Seguindo: {numero}</p></div>
            <div class="followers"><p>Seguidores: {numero}</p></div>
            <div class="followers"><p>Curtidas: {numero}</p></div>
            <img src="" alt="Logo" id="tiktok-logo">
        </div>
    </div>
</a>
```

### CSS Base

```css
.tiktok-profile {
    width: auto;
    max-width: 400px;
    height: 200px;
    min-height: 200px;
    border-radius: 10px;
    display: flex;
    gap: 20px;
    border: 2px solid rgb(156, 156, 156);
    background-color: #ffffff;
    transition: all 0.3s;
    opacity: 0.5;
}

.tiktok-profile:hover {
    border: 2px solid rgb(255, 0, 111);
    opacity: 1;
}

.tiktok-profile #perfil {
    width: 50%;
    height: auto;
    border-radius: 50%;
    transition: all 0.3s;
    opacity: 0.8;
}

.tiktok-profile #perfil:hover {
    border-radius: 10px;
    opacity: 1;
    border-right: 2px solid rgb(255, 0, 111);
}

.tiktok-profile .username {
    font-family: 'Chakra Petch', sans-serif;
    font-size: 2rem;
    font-weight: bold;
    color: rgb(35, 35, 35);
}
```

---

## JavaScript

O JS faz **todo o trabalho dinâmico**:

```js
function updateLogo() {
    var link = document.getElementById('tiktok-link').href;
    var card = document.getElementById('tiktok-profile');

    if (link.includes('tiktok')) {
        card.innerHTML = `...`; // Conteúdo TikTok
    } else if (link.includes('youtube')) {
        card.innerHTML = `...`; // Conteúdo YouTube
    } else if (link.includes('discord')) {
        card.innerHTML = `...`; // Conteúdo Discord
    }
}
updateLogo();

function updateUsername() {
    var link = document.getElementById('tiktok-link').href;
    var username = link.split('@')[1];
    var usernameDiv = document.querySelector('.username');
    usernameDiv.textContent = username;
}
updateUsername();
```

---

## Exemplos de Uso

```html
<!-- TikTok -->
<a href="https://www.tiktok.com/@cdpoficial" id="tiktok-link">
    <div class="tiktok-profile" id="tiktok-profile"></div>
</a>

<!-- YouTube -->
<a href="https://www.youtube.com/@cdpoficial" id="tiktok-link">
    <div class="tiktok-profile" id="tiktok-profile"></div>
</a>

<!-- Discord -->
<a href="https://discord.gg/exemplo" id="tiktok-link">
    <div class="tiktok-profile" id="tiktok-profile"></div>
</a>
```

---

## Personalização

- Alterar cores e bordas no CSS
- Trocar fontes pelo Google Fonts
- Ajustar largura (`max-width`) e altura (`height`)
- Mudar animações do logo
- Adicionar efeitos de hover ou sombra

---

## Boas Práticas

1. Sempre use links **válidos** para TikTok, YouTube ou Discord.
2. Não modifique o JS se não tiver conhecimento, para evitar quebrar o widget.
3. Mantenha o crédito **CDP** visível no site. (seria legal!)
4. Teste em **modo escuro** e **modo claro**.

---

## Avisos Legais

> ❗ Este widget é **criação exclusiva de CDP**.
> É permitido apenas **uso integrado** em sites e plataformas, **não é permitido baixar e redistribuir o código**.

---

## Créditos

Feito com 💖 por **CDP**. HTML • CSS • JS • Criatividade • Inspiração em interfaces modernas e responsivas.

---

## Notas Finais

Este widget é perfeito para quem quer mostrar presença online de forma elegante. Pode ser usado em portfólios, dashboards, páginas pessoais ou para promoções de perfis de redes sociais.
