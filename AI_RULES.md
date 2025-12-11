# Regras de Desenvolvimento e Stack Tecnológica

Este documento define a pilha de tecnologia (tech stack) e as regras de uso de bibliotecas para garantir a consistência, manutenibilidade e elegância do projeto BarberPro.

## 1. Resumo da Pilha de Tecnologia

O projeto BarberPro é uma aplicação web moderna e minimalista, focada em experiência mobile, construída com a seguinte stack:

*   **Framework:** React (v19+), utilizando componentes funcionais e hooks.
*   **Linguagem:** TypeScript para tipagem estática e maior segurança de código.
*   **Roteamento:** React Router (v6+), configurado com `HashRouter` em `App.tsx`.
*   **Estilização:** Tailwind CSS, utilizado exclusivamente para todos os aspectos de layout e design. O design deve ser responsivo (mobile-first).
*   **Componentes UI:** Componentes customizados seguindo a filosofia shadcn/ui (localizados em `src/components/ui/`).
*   **Ícones:** Lucide React.
*   **Gerenciamento de Estado:** React Context API para estados globais (e.g., Autenticação, Tema).
*   **Estrutura de Arquivos:** Componentes em `src/components/`, telas em `src/screens/`, e contextos em `src/context/`.

## 2. Regras de Uso de Bibliotecas e Componentes

Para manter a coesão do projeto, siga as seguintes diretrizes ao implementar novas funcionalidades:

1.  **Componentes de Interface (UI):**
    *   Priorize o uso dos componentes existentes em `src/components/ui/` (e.g., `Button`, `Input`, `Switch`).
    *   Se um componente necessário não existir, crie-o em um novo arquivo dentro de `src/components/ui/`. Mantenha o estilo minimalista e utilize Tailwind CSS.
    *   **Proibido:** Instalar bibliotecas de componentes UI externas (como Material UI, Ant Design, etc.).

2.  **Estilização:**
    *   Utilize **apenas** classes do Tailwind CSS para estilizar componentes.
    *   Evite estilos inline ou arquivos CSS separados.

3.  **Ícones:**
    *   Todos os ícones devem ser importados do pacote `lucide-react`.

4.  **Roteamento:**
    *   Utilize os hooks e componentes do `react-router-dom` para toda a navegação e definição de rotas.

5.  **Dados e Tipos:**
    *   Defina interfaces TypeScript em `types.ts`.
    *   Mantenha dados estáticos e constantes (como listas de barbeiros, serviços, horários) em `constants.ts`.

6.  **Estrutura de Código:**
    *   Crie um novo arquivo para cada novo componente ou hook, mantendo os arquivos pequenos e focados.
    *   Mantenha a estrutura de pastas: `src/components/`, `src/screens/`, `src/context/`.