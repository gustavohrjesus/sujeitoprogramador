# LANDING PAGE - PETDEV - SUJEITO PROGRAMADOR
[Criar LANDING PAGE profissional do ZERO + Next JS - Sujeito Programador](https://www.youtube.com/watch?v=5tpX4iTdg5A&t=4024s)

[Material de apoio](https://sujeitoprogramador.com/projeto-petshop-assets/)

[Git do projeto - pelo autor devfraga](https://github.com/devfraga/petshop-youtube/tree/main)

## Criando o projeto
`npx create-next-app@latest petdev`

> TypeScript: Yes

> ESLint: No

> Tailwind CSS: Yes

> src/ directory: Yes

> App Router: Yes

> Turbopack: No

> import alias (`@/*`by default): Yes

> What import alias would you like configured? ...0/*

## Instalando SHADCN ao projeto
Pare a execução do projeto. Então 
[Acesse a guia de instalação do SHADCN usando NEXT](https://ui.shadcn.com/docs/installation/next)
Após, selecione em **1. Create project**, a aba _npm_ e copie o código para instalar o shadcn ao projeto:
`npx shadcn@latest init`

> style: New York

> base color: Neutral

> css variables: yes

> dependency issues react-19: use --force

## SHADCN - criando um componente button
[Acesse a guia _Components_ e, entao, localize o componente **button**, no menu lateral.](https://ui.shadcn.com/docs/components/button)
Após, copie o código para instalar o componente **button**, conforme a seguir: 
`npx shadcn@latest add button`

> dependency issues react-19: use --force

## PHOSPHOR-ICONS - ADICIONANDO ICONES (WHATSAPP,...) NO PROJETO
[PHOSPHOR-ICONS](https://phosphoricons.com/)
`npm install @phosphor-icons/react`

## EMBLA CAROUSEL - Biblioteca de carrossel
[EMBLA-CAROUSEL](https://www.embla-carousel.com/)
`npm install embla-carousel-react --force`

## AOS - Animate On Scroll Library - biblioteca de animação usando o scroll
[AOS -Animate On Scroll Library](https://michalsnik.github.io/aos/)

`npm install aos --force`

`npm i --save-dev @types/aos`

Apos, criar o arquivo de inicializacao da biblioteca Aos. Criamos este no seguinte diretorio: *_src/app/components/aos_init.tsx_*, com o conteúdo abaixo:

```
"use client"

import { useEffect } from "react";
import Aos from "aos"
import 'aos/dist/aos.css'

export function AosInit(){

    useEffect( () => {
        Aos.init({
            duration: 800,
            once: true
        })
    }, [] )

    return null;
}
```

E importamos a mesma no arquivo *layout.tsx*, em *_src/app_*