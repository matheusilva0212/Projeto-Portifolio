# Portfólio — Matheus Silva

Portfólio profissional desenvolvido com HTML, CSS e JavaScript puro. Apresenta minha experiência, projetos e habilidades como Engenheiro de Software.

## Funcionalidades

- **Modo escuro/claro** — detecta automaticamente o tema do sistema operacional, com opção de alternar manualmente
- **Efeito typewriter** — animação de digitação no título da hero section
- **Anel gradiente animado** — animação CSS no avatar de perfil
- **Stats animadas** — contadores que animam ao entrar na viewport (Intersection Observer)
- **Scroll spy** — navegação destaca a seção ativa durante a rolagem
- **Barra de progresso de scroll** — indicador visual no topo da página
- **Seção de experiência** — timeline com histórico profissional
- **Logos de tecnologias** — ícones via Devicon CDN nas skills
- **Formulário de contato** — integrado ao Supabase
- **Painel admin** — gerenciamento de mensagens recebidas (`admin.html`)
- **Download do CV** — arquivo `.docx` otimizado para ATS

## Tecnologias

- HTML5 / CSS3 / JavaScript (Vanilla)
- [Inter](https://fonts.google.com/specimen/Inter) — Google Fonts
- [Font Awesome 6](https://fontawesome.com/) — ícones
- [Devicon](https://devicon.dev/) — logos de tecnologias
- [Supabase](https://supabase.com/) — backend do formulário de contato
- [QRCode.js](https://github.com/davidshimjs/qrcodejs) — geração de QR code

## Estrutura

```
/
├── assets/
│   ├── docs/Matheus_Silva_CV.docx   # CV otimizado para ATS
│   └── img/profile.jpg              # Foto de perfil
├── .github/                         # Configurações do GitHub
├── admin.html                       # Painel de gerenciamento de contatos
├── debug-admin.html                 # Página de debug do admin
├── index.html                       # Página principal
└── style.css                        # Estilos globais
```

## Como rodar localmente

Basta abrir o `index.html` em um navegador — não há dependências de build ou instalação.

Para desenvolvimento, recomenda-se usar a extensão **Live Server** no VS Code.

## Contato

- GitHub: [matheusilva0212](https://github.com/matheusilva0212)
- LinkedIn: linkedin.com/in/matheus-s-088826253
