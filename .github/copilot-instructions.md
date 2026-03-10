# Instruções para Agentes de IA - Portfólio Matheus Silva

## Visão Geral do Projeto
Este é um **portfólio web responsivo de uma página** (single-page) para Matheus Silva, engenheiro de software. A aplicação é estática, sem backend, composta por HTML5 semântico e CSS3 moderno com variáveis CSS.

**Estrutura**:
- [index.html](../index.html) - Arquivo principal com 5 seções: Header, Hero, About, Projects, Contact, Footer
- [style.css](../style.css) - Estilos globais com sistema de variáveis CSS e design responsivo

## Padrões Arquiteturais

### Organização de Seções
Cada seção maior segue o padrão `.container` com conteúdo centralizado:
```html
<section id="secao" class="secao">
    <div class="container">
        <!-- conteúdo -->
    </div>
</section>
```

### Sistema de Cores (CSS)
Variáveis definidas em `:root` (linhas 1-10 do style.css):
- `--primary-color`: #2c3e50 (texto e backgrounds escuros)
- `--secondary-color`: #34495e (texto secundário)
- `--accent-color`: #3498db (hover e destaques)
- `--background-color`: #f4f7f9 (fundo claro das seções)

**Ao adicionar elementos**: Use as variáveis existentes. Evite cores hardcoded.

### Design Responsivo
Breakpoints em CSS:
- **768px**: Ajustes para tablets (flex-direction, grid para 1 coluna)
- **480px**: Otimização para mobile (font-size reduzidos, grid 1fr)

Padrão: mobile-first nos componentes, media queries sobrescrevem.

## Convenções do Projeto

### Nomenclatura CSS
- Classes descritivas em kebab-case: `.hero-content`, `.project-card`, `.contact-form`
- Relacionais: `.hero-image`, `.hero-actions` (referem-se ao pai `.hero`)
- Estado/tipo: `.btn.primary`, `.btn.secondary`, `.github-icon`

### Elementos Interativos
- Todos os `.btn` reutilizam classes base `.btn` + modificador (`.primary` ou `.secondary`)
- Links têm `:hover` com transição 0.3s na cor: `transition: color 0.3s`
- Ícones FontAwesome 6.0+ (classes `fas`, `fab`) com tamanho padrão 1.2-2rem

### HTML Semântico
- Use `<section>` para divisões lógicas com `id` para navegação (#inicio, #sobre, etc)
- `<header>`, `<main>`, `<footer>` estruturam o layout top-level
- Anchor links com `href="#secao"` alimentam a navegação sticky

## Fluxos de Desenvolvimento Comuns

### Adicionar Nova Seção
1. Criar `<section id="novo" class="novo">` em `<main>`
2. Seguir padrão: `.container` com `.novo-header` e conteúdo
3. Em CSS: estilo base em tela grande, depois breakpoints
4. Adicionar link na navegação (.nav) se necessário

### Atualizar Formulário de Contato
Formulário em lines 170-185 do index.html. Mantém estrutura:
```html
<form>
    <div class="form-group">
        <label for="id">Rótulo</label>
        <input/textarea type="...">
    </div>
</form>
```
**Nota**: Form não tem backend conectado atualmente (action vazio).

### Adicionar Novo Projeto
Cards em grid `.projects-grid`. Template:
- `.project-image-placeholder` (200px height)
- `h4`, `p`, `.project-tech-tags` (spans de tecnologia)
- `.project-actions` com links e ícone GitHub

## Dependências Externas

- **FontAwesome 6.0-beta3**: CDN para ícones (linhas 8 do HTML)
- **Google Fonts**: Nenhuma (usa sistema font-family padrão)

Ao adicionar ícones: use classes `fas fa-*` (solid) ou `fab fa-*` (brand).

## Pontos de Integração Futura

- **Form submission**: Section contato, `<form>` sem handler (linha 177)
- **Project links**: `.project-btn` e `.github-icon` apontam para `#` (placeholder)
- **CV download**: Link em `<a href="Matheus_Silva_Currículo_atualizado2025.pdf">`

## Performance & Manutenção

- CSS organizado por componente (Header, Hero, About, Projects, Contact, Footer)
- Smooth scroll habilitado globalmente (`html { scroll-behavior: smooth }`)
- Sticky header com `position: sticky` (linhas 31-33 do CSS)
- Todas as imagens: verificar `alt` attribute (linha 41, hero-image)

**Validação**: Sempre testar em 3 breakpoints (1200px, 768px, 480px).
