# Testes manuais de login — SwagLabs (SauceDemo)

🌐 **Sistema testado:** O [SwagLabs (SauceDemo)](https://www.saucedemo.com/) é uma aplicação web de e-commerce utilizada para prática de testes de software, permitindo validar funcionalidades como login, navegação de produtos, carrinho e checkout em um ambiente controlado.

🎯 **Objetivo:** Realizar testes manuais na tela de login para garantir a qualidade, usabilidade e segurança do sistema.

🔬 **Tipos de testes realizados:** 
<br> • Teste funcional 
<br> • Testes negativos 
<br> • Testes de borda 
<br> • Teste de segurança
<br> • Teste de acessibilidade 
<br><br>

### 🧪 **CASOS DE TESTE**

| **ID** | CT-01 |
| --- | --- |
| **Título** | Login com dados válidos |
| **Pré-condição** | • Sistema disponível <br> • Usuário possuir cadastro |
| **Passos** | 1. Acessar página de login <br> 2. Inserir username válido <br> 3. Inserir password correto <br> 4. Clicar em “Login” |
| **Resultado esperado** | Login realizado com sucesso e redirecionado para tela principal da aplicação |
| **Resultado** | ✅ Passou |
| **Comentários** |  |
| **Executor(a)** | Débora Taveira |
<br><br>

| **ID** | CT-02 |
| --- | --- |
| **Título** | Tentativa de login com password incorreto |
| **Pré-condição** | Sistema disponível |
| **Passos** | 1. Acessar página de login <br> 2. Inserir username válido <br> 3. Inserir password incorreto <br> 4. Clicar em “Login” |
| **Resultado esperado** | Login não realizado e exibição de mensagem de erro de usuário não encontrado |
| **Resultado** | ✅ Passou |
| **Comentários** |  |
| **Executor(a)** | Débora Taveira |
<br><br>

| **ID** | CT-03 |
| --- | --- |
| **Título** | Tentativa de login com username incorreto |
| **Pré-condição** | Sistema disponível |
| **Passos** | 1. Acessar página de login <br> 2. Inserir username inválido <br> 3. Inserir password correto <br> 4. Clicar em “Login” |
| **Resultado esperado** | Login não realizado e exibição de mensagem de erro de usuário não encontrado |
| **Resultado** | ✅ Passou |
| **Comentários** |  |
| **Executor(a)** | Débora Taveira |
<br><br>

| **ID** | CT-04 |
| --- | --- |
| **Título** | Tentativa de login com campos vazios |
| **Pré-condição** | Sistema disponível |
| **Passos** | 1. Acessar página de login <br> 2. Deixar campo username vazio <br> 3. Deixar campo password vazio <br> 4. Clicar em “Login” |
| **Resultado esperado** | Login não realizado e exibição de mensagem de erro dos campos obrigatórios |
| **Resultado** | ✅ Passou |
| **Comentários** |  |
| **Executor(a)** | Débora Taveira |
<br><br>

| **ID** | CT-05 |
| --- | --- |
| **Título** | Tentativa de login com SQL Injection |
| **Pré-condição** | Sistema de login disponível |
| **Passos** | 1. Acessar página de login <br> 2. Inserir no campo username: `' OR '1'='1` <br> 3. Inserir no campo password qualquer valor <br> 4. Clicar em “Login” |
| **Resultado esperado** | • Login não deve ser realizado <br> • Deve exibir mensagem de erro de usuário não encontrado <br> • Não deve exibir erro técnico como SQL error <br> • Não deve quebrar a aplicação |
| **Resultado** | ✅ Passou |
| **Comentários** |  |
| **Executor(a)** | Débora Taveira |
<br><br>

| **ID** | CT-06 |
| --- | --- |
| **Título** | Login com espaços em branco no início e fim do username |
| **Pré-condição** | • Sistema de login disponível <br> • Usuário cadastrado |
| **Passos** | 1. Acessar página de login <br> 2. Inserir username com espaços no início e fim: ` standard_user ` <br> 3. Inserir password correto <br> 4. Clicar em “Login” |
| **Resultado esperado** | • Sistema deve remover espaços automaticamente <br> • Login realizado com sucesso |
| **Resultado** | ❌ Não passou |
| **Comentários** | Sistema não realiza remoção de espaços no campo username, causando falha de autenticação mesmo com credenciais válidas. |
| **Executor(a)** | Débora Taveira |
<br><br>

| **ID** | CT-07 |
| --- | --- |
| **Título** | Login com espaços em branco no meio do username |
| **Pré-condição** | • Sistema de login disponível <br> • Usuário cadastrado |
| **Passos** | 1. Acessar página de login <br> 2. Inserir username com espaços no meio: `stand  ard_user` <br> 3. Inserir password correto <br> 4. Clicar em “Login” |
| **Resultado esperado** | • Sistema não deve remover espaços no meio do username <br> • Login não realizado <br> • Deve exibir mensagem de erro de usuário não encontrado |
| **Resultado** | ✅ Passou |
| **Comentários** |  |
| **Executor(a)** | Débora Taveira |

| **ID** | CT-08 |
| --- | --- |
| **Título** | Acessibilidade no login somente por teclas |
| **Pré-condição** | • Sistema de login disponível <br> • Usuário cadastrado |
| **Passos** | 1. Acessar página de login <br> 2. Clicar na tecla **Tab** --> ativar campo username <br> 3. Inserir username válido <br> 4. Clicar na tecla **Tab** --> ativar campo password <br> 5. Inserir password correto <br> 4. Clicar na tecla **Enter** --> ativar botão “Login” |
| **Resultado esperado** | Login realizado com sucesso e redirecionado para tela principal da aplicação |
| **Resultado** | ✅ Passou |
| **Comentários** |  |
| **Executor(a)** | Débora Taveira |