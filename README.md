# Commit Standardization Guide
Este repositório é um guia para ajudar desenvolvedores a padronizar suas mensagens de commit utilizando a especificação Conventional Commits.

## Por que Padronizar Commits?
- Entender o histórico de mudanças.
- Automatizar versionamento e changelogs.
- Colaborar com outros desenvolvedores de forma mais eficaz.

## Por que Padronizar Commits?
- Introdução: Por que padronizar commits é importante.
- Configuração: Como configurar ferramentas como Husky e Commitlint.
- Exemplos: Exemplos práticos de commits padronizados.
- Avançado: Automação e hooks para garantir a qualidade das mensagens de commit.

## Configuração

1. Instale os pacotes necessários:

```bash
npm install husky @commitlint/config-conventional @commitlint/cli --save-dev
```

2. Configure o Husky:

```bash
npx husky install
```

3. Crie um arquivo de configuração do Commitlint chamado .commitlintrc.json:

```bash
{
  "extends": ["@commitlint/config-conventional"]
}
```

4. Adicione um hook do Husky para garantir que as mensagens de commit estejam no formato correto:

```bash
npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
```

## Tipos de commits

| Tipo       | Descrição                                                      | Exemplo de Commit                                |
|------------|----------------------------------------------------------------|--------------------------------------------------|
| `feat`     | Adição de nova funcionalidade                                  | `feat: implement user profile page`              |
| `fix`      | Correção de bug                                                | `fix: resolve login page crash issue`            |
| `docs`     | Mudança na documentação                                        | `docs: update README with setup instructions`    |
| `style`    | Mudança que não afeta o código (apenas formatação)             | `style: format code according to linting rules`  |
| `refactor` | Refatoração do código sem adicionar funcionalidade             | `refactor: improve performance of user data processing` |
| `test`     | Adição ou modificação de testes                                | `test: add unit tests for login functionality`   |
| `chore`    | Atualizações gerais e manutenção                               | `chore: update dependencies`                     |
| `perf`     | Mudança de código que melhora o desempenho                     | `perf: optimize image loading time`              |
| `ci`       | Mudanças na configuração de integração contínua (CI)           | `ci: add GitHub Actions for automated testing`   |
| `build`    | Mudanças que afetam o sistema de build ou dependências externas| `build: upgrade Node.js to version 14`           |
| `revert`   | Reversão de um commit anterior                                 | `revert: undo commit 1234abcd`                   |
| `hotfix`   | Correção urgente de um bug em produção                         | `hotfix: fix critical bug in payment processing` |
| `security` | Ajustes de segurança                                           | `security: patch vulnerability in user login`    |
| `env`      | Modificações no ambiente ou variáveis de ambiente              | `env: update environment variables for staging`  |
| `config`   | Mudanças na configuração de arquivos ou ferramentas            | `config: update eslint configuration`            |
