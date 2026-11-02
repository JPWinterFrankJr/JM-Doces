# JM Doce Sabor — Vitrine 3D Premium

Site estático, responsivo e otimizado para publicar na Netlify, sem dependências de compilação. Desenvolvido em HTML, CSS e JavaScript, com aprimoramentos opcionais de Motion.dev.

## Como visualizar
Abra `index.html` no navegador ou publique a pasta inteira na Netlify. Para testar localmente pelo terminal, dentro da pasta execute `python -m http.server 8000` e abra `http://localhost:8000`.

## O que há no site
- 10 geladinhos, **um por sabor**, em imagens hiper-realistas geradas especificamente para a JM Doce Sabor (não são fotografias dos produtos reais).
- Os arquivos `assets/img/<sabor>.webp` têm fundo transparente e são exibidos em um carrossel com **perspectiva tridimensional CSS**, profundidade, transição, flutuação e navegação por arraste, setas e teclado. **Não são malhas 3D rotacionáveis em 360°**, mas fotografias geradas integradas a uma cena com efeito 3D.
- Carrinho com quantidades, subtotal e endereço. Pedido formatado automaticamente para WhatsApp.
- Informações explícitas: **frete informado no WhatsApp** e **pagamento combinado no WhatsApp**.
- Acessibilidade com preferência por movimento reduzido, navegação por teclado e avisos descritivos.

## Obrigatório antes de publicar
Abra `assets/js/config.js` e altere:
- `WHATSAPP`: número oficial da loja (DDI + DDD + número, só números), por exemplo `5547999999999`.
- `price`: **os preços de R$ 10,90 a R$ 12,90 são demonstrativos**; confirme todos antes de publicar.

Sem número WhatsApp configurado, o site mostra um aviso e **não envia o pedido**, evitando direcionar clientes para um número errado.

## Organização
```text
index.html
netlify.toml
assets/
  css/style.css
  js/config.js    # preços, sabores e WhatsApp
  js/app.js       # carrossel, carrinho, checkout
  js/motion.js    # animações opcionais
  img/
    nome-do-sabor.webp        # produto recortado, fundo transparente
    nome-do-sabor-photo.webp  # imagem com fundo de estúdio
    logo-jm.svg
    favicon.svg
    cardapio-referencia.jpg
```

## Observação comercial
As imagens são representações **geradas por IA** a partir do cardápio e descrições dos sabores. Elas não devem ser apresentadas como fotos fiéis de produtos já fabricados. Ajuste as imagens e informações com a confeitaria antes do lançamento.
