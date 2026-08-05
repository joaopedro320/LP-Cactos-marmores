# LP Cactos Mármores

Estrutura:

```
cactos-lp-vercel/
├── index.html      # a landing page inteira (CSS e JS inline)
├── vercel.json     # cache das imagens + headers
├── img/            # 34 arquivos .webp
└── README.md
```

## Subir na Vercel

Opção 1, arrastar a pasta em vercel.com/new (deploy estático, sem build).

Opção 2, pela CLI:

```
cd cactos-lp-vercel
vercel --prod
```

Framework preset: Other. Build command: vazio. Output directory: raiz do projeto.

## Antes de publicar

1. Trocar `GTM-XXXXXXX` pelo ID real do Google Tag Manager (aparece 2 vezes no index.html: no script do head e no noscript).
2. Conferir o número do WhatsApp `5574981428722` caso mude.
3. Depoimentos: os três da seção "O que dizem nossos parceiros" precisam ser substituídos por prints ou textos reais do cliente.
4. Favicon já está em `img/favicon.webp`. Se quiser .ico, converter e trocar a tag `link rel="icon"`.

## Eventos

Todos os CTAs disparam `clique_cta` no dataLayer com o parâmetro `local` (header, hero, materiais, ambientes, confianca, processo, projetos, faq, contato, formulario, final, rodape, flutuante e material-nome-da-pedra).
