# Feedback do Projeto

Este arquivo documenta os pontos de melhoria destacados pelo professor Thiago Trojahn do IFSP São Carlos no projeto. Esses feedbacks serão revisados e corrigidos em versões futuras.

---

## Erros e Melhorias

### 1. **Links para Arquivos Externos**
- **Problema**: Os links dos arquivos CSS e imagens utilizam caminhos absolutos (começando com `/`), o que pode quebrar ao hospedar o site em um servidor com diretórios diferentes.
  - **Exemplo Problemático**:
    ```html
    <link rel="stylesheet" href="/estilos/stylegeral.css">
    <img src="/imagens/logo.png" alt="Lendas do futebol LOGO">
    ```
  - **Correção Sugerida**:
    Use caminhos relativos, como:
    ```html
    <link rel="stylesheet" href="../estilos/stylegeral.css">
    <img src="../imagens/logo.png" alt="Lendas do futebol LOGO">
    ```

---

### 2. **Uso Excessivo de `<br>`**
- **Problema**: Uso de várias quebras de linha (`<br>`) em textos longos. Isso é considerado uma má prática e pode ser substituído por múltiplos parágrafos (`<p>`).
  - **Exemplo Problemático**:
    ```html
    <p>Texto 1<br>Texto 2<br>Texto 3<br></p>
    ```
  - **Correção Sugerida**:
    ```html
    <p>Texto 1</p>
    <p>Texto 2</p>
    <p>Texto 3</p>
    ```

---

### 3. **Uso Inadequado de Tags HTML**
- **Problemas Encontrados**:
  1. Uso de `<div>` dentro de um `<section>` quando deveria ser um `<header>`.
     - **Exemplo Problemático**:
       ```html
       <section>
           <div>
               <h4>Início da Carreira</h4>
           </div>
           ...
       </section>
       ```
     - **Correção Sugerida**:
       ```html
       <section>
           <header>
               <h4>Início da Carreira</h4>
           </header>
           ...
       </section>
       ```
  2. Uso desnecessário de `<section>` para envolver apenas um `<header>`. O `<header>` sozinho é suficiente.
     - **Exemplo Problemático**:
       ```html
       <aside>
           <section>
               <header>...</header>
           </section>
       </aside>
       ```
     - **Correção Sugerida**:
       ```html
       <aside>
           <header>...</header>
       </aside>
       ```

---

### 4. **Regras CSS Duplicadas**
- **Problema**: Regras CSS repetidas em diferentes arquivos. Por exemplo, a classe `.headergeral` foi encontrada tanto em `stylecontato.css` quanto em `stylegeral.css`.
  - **Correção Sugerida**: Consolidar as regras duplicadas em um único arquivo para evitar redundância e facilitar a manutenção.

---

### 5. **Uso de Seletores Mais Simples**
- **Sugestão**: Em vez de criar classes específicas para tags que podem ser selecionadas diretamente no CSS, use seletores apropriados.
  - **Exemplo Melhorado**:
    ```css
    body > header {
        /* Estilos aplicados ao header diretamente */
    }
    ```

---

Esses pontos serão revisados e corrigidos nas próximas versões do projeto. Obrigado pelo feedback, professor!
