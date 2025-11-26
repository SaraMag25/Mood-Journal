# Blueprint: Mood Tracker App

## Visão Geral

Um aplicativo minimalista e bonito onde o usuário pode registrar seu humor diário e, eventualmente, receber insights sobre seus padrões emocionais ao longo do tempo. O design será limpo, moderno e focado na experiência do usuário, seguindo as melhores práticas de design da Material 3.

## Estilo, Design e Recursos (Versão Inicial)

### **Design e Estilo**

*   **Paleta de Cores**: Usará `ColorScheme.fromSeed` com uma cor base calmante (por exemplo, `Colors.blueGrey`) para gerar esquemas de cores harmoniosos para os modos claro and escuro.
*   **Tipografia**: Utilizará o pacote `google_fonts` para fontes personalizadas, como *Montserrat* para títulos e *Roboto* para o corpo do texto, garantindo legibilidade e apelo estético.
*   **Componentes**:
    *   **Botões de Humor**: Botões de ícone com emojis para representar os humores (Feliz, Neutro, Triste). Os botões terão um feedback visual sutil ao serem pressionados.
    *   **Layout**: Layout limpo e espaçado, com um `Scaffold` central e conteúdo centralizado.
*   **Tema**: Suporte total para os modos claro e escuro, com um botão de alternância no `AppBar`.

### **Recursos**

*   **Registro de Humor**: O usuário pode selecionar seu humor para o dia atual.
*   **Alternância de Tema**: O usuário pode alternar entre os temas claro e escuro.
*   **Navegação**: Estrutura de navegação básica implementada com `go_router`.

## Plano de Implementação Atual

1.  **Configurar o Projeto**:
    *   Adicionar as dependências necessárias: `provider`, `google_fonts`, `go_router`.
2.  **Estruturar o Código**:
    *   `lib/main.dart`: Ponto de entrada principal do aplicativo, configuração do `Provider` e `MaterialApp.router`.
    *   `lib/theme.dart`: Definir `ThemeData` para os modos claro e escuro e o `ThemeProvider`.
    *   `lib/router.dart`: Configurar as rotas do `go_router`.
    *   `lib/screens/home_screen.dart`: Construir a interface do usuário da tela inicial.
    *   `lib/models/mood_entry.dart`: Definir a classe do modelo de dados para uma entrada de humor.
    *   `lib/services/mood_service.dart`: Criar um serviço para gerenciar a lógica de negócios relacionada aos humores.
3.  **Implementar a Interface do Usuário**:
    *   Desenvolver a tela inicial com um `AppBar` que inclui um botão para alternar o tema.
    *   Criar a seção de "Como você está se sentindo hoje?".
    *   Adicionar os botões de emoji para a seleção de humor.
4.  **Implementar o Gerenciamento de Estado**:
    *   Usar o `ChangeNotifierProvider` para o `ThemeProvider`.
    *   Usar o `ChangeNotifierProvider` para o `MoodService` para gerenciar o estado do humor.
