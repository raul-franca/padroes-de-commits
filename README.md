# Git mais usado no meu dia a dia

## Branches

1️⃣ **Criar e mudar para uma nova branch corretamente**

```bash
    git fetch origin
    git checkout main
    git pull origin main
    git checkout -b <branch>
```

• git fetch origin → Atualiza as referências do repositório remoto sem alterar nada no seu código.
• git checkout main → Garante que você está na branch main.
• git pull origin main → Pega as últimas atualizações do repositório remoto.
• git checkout -b <branch> → Agora sim, cria e muda para a nova branch baseada na versão mais atualizada da main.

2️⃣ **Fazer merge de outra branch**

```bash
    git checkout main
    git merge <branch>
```

3️⃣ **Push mudanças para o repositório remoto**

```bash
    git push origin main
```

⚠️ **Cuidado!**
Se a main já tiver sido atualizada por outros membros da equipe desde o último pull, o push pode falhar. Nesse caso, você pode precisar fazer:

```bash
    git pull origin main
```

4️⃣ **Limpar branches locais (opcional)**

```bash
    git branch -d <branch>
```

# 📌 Padrões para Nomeação de Branches no Git


| **Tipo**         | **Padrão de Nome**          | **Exemplo**                        | **Descrição**                                          |
| ---------------- | ---------------------------- | ---------------------------------- | -------------------------------------------------------- |
| **Feature**      | `feature/<descricao-curta>`  | `feature/adicionar-login-google`   | Usado para novas funcionalidades.                        |
| **Bugfix**       | `bugfix/<descricao-curta>`   | `bugfix/corrigir-erro-login`       | Correção de bugs identificados no código.             |
| **Hotfix**       | `hotfix/<descricao-curta>`   | `hotfix/corrigir-erro-em-producao` | Correção crítica para produção.                     |
| **Refactor**     | `refactor/<descricao-curta>` | `refactor/melhorar-arquitetura`    | Melhorias no código sem alterar funcionalidades.        |
| **Test**         | `test/<descricao-curta>`     | `test/cobertura-auth-service`      | Branch usada para implementação de testes.             |
| **Docs**         | `docs/<descricao-curta>`     | `docs/atualizar-readme`            | Alterações na documentação do projeto.               |
| **Release**      | `release/<versao>`           | `release/v1.2.0`                   | Preparação para uma nova versão.                      |
| **Experimental** | `exp/<descricao-curta>`      | `exp/nova-interface-ui`            | Testes ou experimentos de novas ideias.                  |
| **Chore**        | `chore/<descricao-curta>`    | `chore/atualizar-dependencias`     | Tarefas de manutenção, como atualizações de pacotes. |

# 📌 Comandos Git


| Comando Git                   | Descrição                                                                     |
| ----------------------------- | ------------------------------------------------------------------------------- |
| `git init`                    | Inicializa um novo repositório Git local                                       |
| `git clone <URL>`             | Clona um repositório remoto para o diretório local                            |
| `git add <arquivo>`           | Adiciona um arquivo específico ao staging area                                 |
| `git add .`                   | Adiciona todos os arquivos ao staging area                                      |
| `git commit -m "mensagem"`    | Cria um commit com uma mensagem descritiva                                      |
| `git status`                  | Exibe o status dos arquivos no repositório local                               |
| `git log`                     | Mostra o histórico dos commits do repositório                                 |
| `git log --oneline`           | Mostra o histórico de commits de forma resumida                                |
| `git diff`                    | Exibe as mudanças não adicionadas ao staging area                             |
| `git diff --staged`           | Mostra as mudanças que estão no staging area, mas ainda não foram commitadas |
| `git branch`                  | Lista todas as branches do repositório                                         |
| `git branch <nome-da-branch>` | Cria uma nova branch                                                            |
| `git checkout <branch>`       | Altera para a branch especificada                                               |
| `git checkout -b <branch>`    | Cria e muda para a nova branch especificada                                     |
| `git fetch origin`            | Atualiza as referências do repositório remoto sem alterar o código.          |
| `git merge <branch>`          | Faz o merge da branch especificada com a branch atual                           |
| `git pull`                    | Atualiza o repositório local com as mudanças do repositório remoto           |
| `git push`                    | Envia os commits locais para o repositório remoto                              |
| `git remote add origin <URL>` | Adiciona um repositório remoto                                                 |
| `git stash`                   | Armazena temporariamente as mudanças no diretório de trabalho                 |
| `git stash pop`               | Aplica as mudanças que estavam armazenadas                                     |
| `git reset --hard <commit>`   | Reseta o repositório para o estado do commit especificado                      |
| `git rebase <branch>`         | Reaplica commits em cima de outra branch                                        |
| `git tag <nome-da-tag>`       | Cria uma tag no commit atual                                                    |

---

## 📌 Padrões de commit


| Tipo        | Descrição                                                                                 |
| ----------- | ------------------------------------------------------------------------------------------- |
| `feat:`     | Uma nova funcionalidade.                                                                    |
| `fix:`      | Uma correção de bug.                                                                      |
| `docs:`     | Alterações na documentação.                                                             |
| `style:`    | Formatação, ajustes de código sem alterações na lógica (ex.: remoção de espaços).  |
| `refactor:` | Alterações no código que não corrigem bugs nem adicionam novas funcionalidades.         |
| `test:`     | Adição ou modificação de testes.                                                        |
| `chore:`    | Atualizações de tarefas de manutenção que não afetam o código (ex.: configurações). |


---

# 📌 Tabela de Gitmoji


| Emoji | Código                       | Descrição                                     | Exemplo de Uso                                          |
| ----- | ----------------------------- | ----------------------------------------------- | ------------------------------------------------------- |
| 🎨    | `:art:`                       | Melhoria na estrutura/formato do código        | `🎨 Melhora o estilo de código no componente X`        |
| 🐛    | `:bug:`                       | Correção de um bug                            | `🐛 Corrige erro no formulário de login`               |
| ✨    | `:sparkles:`                  | Adição de nova funcionalidade                 | `✨ Adiciona função de pesquisa avançada`            |
| 📝    | `:memo:`                      | Escrevendo documentação                       | `📝 Atualiza o README com instruções de instalação` |
| 🔥    | `:fire:`                      | Remoção de código ou arquivos                | `🔥 Remove dependências não utilizadas`               |
| 🚀    | `:rocket:`                    | Melhoria de performance                         | `🚀 Otimiza carregamento de imagens`                    |
| 💄    | `:lipstick:`                  | Atualização do layout e estilo da UI          | `💄 Ajusta cores no tema principal`                     |
| 🎉    | `:tada:`                      | Início de um projeto                           | `🎉 Commit inicial do projeto`                          |
| ✅    | `:white_check_mark:`          | Adição de testes                              | `✅ Adiciona testes unitários para o módulo Y`        |
| 🔖    | `:bookmark:`                  | Lançamento/Versão de tags                     | `🔖 Lança versão 1.0.0`                               |
| 🚑    | `:ambulance:`                 | Correção crítica em produção               | `🚑 Corrige crash na inicialização do app`            |
| ♻️  | `:recycle:`                   | Refatoração de código                        | `♻️ Refatora método de autenticação`               |
| ➕    | `:heavy_plus_sign:`           | Adição de dependência                        | `➕ Adiciona biblioteca Z ao projeto`                   |
| ➖    | `:heavy_minus_sign:`          | Remoção de dependência                       | `➖ Remove biblioteca X obsoleta`                       |
| 🔧    | `:wrench:`                    | Modificação em configurações                | `🔧 Atualiza configurações do webpack`                |
| 🔨    | `:hammer:`                    | Trabalhando em scripts de build                 | `🔨 Adiciona script de deploy`                          |
| 🌐    | `:globe_with_meridians:`      | Internacionalização                           | `🌐 Adiciona suporte ao idioma espanhol`                |
| ✏️  | `:pencil2:`                   | Correção de typos                             | `✏️ Corrige erro ortográfico no arquivo X`           |
| 💚    | `:green_heart:`               | Correção de build no CI                       | `💚 Ajusta pipeline do Travis CI`                       |
| ⬆️  | `:arrow_up:`                  | Atualização de dependências                  | `⬆️ Atualiza versão do React para 17.x`              |
| ⬇️  | `:arrow_down:`                | Downgrade de dependências                      | `⬇️ Reverte versão do Node para 12.x`                |
| 👷    | `:construction_worker:`       | Trabalhando em CI/CD                            | `👷 Configura GitHub Actions para testes`               |
| 📈    | `:chart_with_upwards_trend:`  | Adição de análises                           | `📈 Implementa tracking com Google Analytics`           |
| 🔒    | `:lock:`                      | Correção de problemas de segurança           | `🔒 Atualiza pacotes vulneráveis`                      |
| 🍎    | `:apple:`                     | Correções específicas para o sistema macOS   | `🍎 Corrige path no script para macOS`                  |
| 🐧    | `:penguin:`                   | Correções específicas para o Linux           | `🐧 Ajusta permissões de arquivo no Linux`             |
| 🏁    | `:checkered_flag:`            | Correções específicas para o Windows         | `🏁 Corrige bug no instalador para Windows`             |
| 🔀    | `:twisted_rightwards_arrows:` | Merge de branches                               | `🔀 Realiza merge da branch feature na develop`         |
| 🗃️  | `:card_file_box:`             | Migração de banco de dados                    | `🗃️ Adiciona migração para nova tabela`             |
| 📦    | `:package:`                   | Adição ou atualização de pacotes compilados | `📦 Atualiza pacotes npm`                               |
| 👽️  | `:alien:`                     | Ajustes devido a mudanças externas             | `👽️ Ajusta API para nova versão do provedor`         |
| 🚚    | `:truck:`                     | Movendo ou renomeando arquivos                  | `🚚 Move arquivos de utils para helpers`                |
| 📄    | `:page_facing_up:`            | Adição ou atualização de licenças          | `📄 Adiciona licença MIT`                              |
| 💥    | `:boom:`                      | Introdução de mudanças incompatíveis        | `💥 Remove suporte para Node 10`                        |
| 🍱    | `:bento:`                     | Adicionando ou atualizando assets               | `🍱 Adiciona novas imagens ao projeto`                  |
| ♿    | `:wheelchair:`                | Melhorias de acessibilidade                     | `♿ Adiciona labels em campos de formulário`           |
| 💬    | `:speech_balloon:`            | Atualização de textos e literais              | `💬 Corrige texto no modal de confirmação`            |
| 🗑️  | `:wastebasket:`               | Remoção de arquivos ou código inutilizado    | `🗑️ Remove logs de depuração`                       |
| 🚸    | `:children_crossing:`         | Melhoria na experiência do usuário            | `🚸 Adiciona feedback de carregamento`                  |
| 🏗️  | `:building_construction:`     | Trabalhando em arquitetura                      | `🏗️ Reestrutura pastas do projeto`                    |
| 📱    | `:iphone:`                    | Trabalhando em responsividade                   | `📱 Ajusta layout para dispositivos móveis`            |
| 🤡    | `:clown_face:`                | Mock de dados ou código de teste               | `🤡 Adiciona dados mock para testes`                    |
| 🥚    | `:egg:`                       | Adição de easter eggs                         | `🥚 Adiciona easter egg na página inicial`             |
| 🙈    | `:see_no_evil:`               | Ignorando arquivos ou diretórios               | `🙈 Adiciona .env ao .gitignore`                        |
| 📸    | `:camera_flash:`              | Adicionando ou atualizando snapshots            | `📸 Atualiza snapshots dos testes`                      |

---

