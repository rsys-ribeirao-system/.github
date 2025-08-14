# Bem-vindo(a) à Organização da Ribeirão System (Rsys)! 👋

Este é o espaço central para todos os repositórios de código, projetos e inovações da **Ribeirão System**. Nossa missão
é desenvolver soluções de software robustas, eficientes e de alta qualidade que impulsionam o sucesso dos nossos
clientes.

Este documento serve como um guia fundamental, definindo as políticas, os padrões e as boas práticas que devem ser
seguidas por todos os membros e colaboradores. A adesão a estas diretrizes é essencial para mantermos a consistência, a
qualidade e a segurança do nosso trabalho.

---

## 📜 Nossas Políticas e Diretrizes Fundamentais

A seguir estão as regras não negociáveis que governam o desenvolvimento de software na Rsys.

### 1. Propriedade Intelectual e Confidencialidade

Todo o código-fonte, scripts, bancos de dados, documentação técnica, artefatos de design e quaisquer outros materiais
produzidos no âmbito dos projetos da Ribeirão System são de **propriedade exclusiva da empresa**.

- **Confidencialidade:** É estritamente proibido compartilhar, copiar ou distribuir qualquer parte do código ou da
  documentação para fora dos canais oficiais da empresa sem autorização explícita.
- **Contribuições:** Ao contribuir para qualquer repositório desta organização, você reconhece que sua contribuição se
  torna propriedade intelectual da Rsys.

### 2. Estratégia de Branches (Git Flow Simplificado)

Para garantir um ciclo de vida de desenvolvimento organizado e seguro, todos os repositórios **devem** obrigatoriamente
seguir a seguinte estrutura de branches:

- **`main`**: Esta branch representa o código em **produção**. É a versão estável, testada e validada que está em uso
  pelos clientes.
    - **🚫 É terminantemente proibido enviar commits ou fazer merge diretamente na `main`**. O processo de deploy para
      produção é gerenciado através de um fluxo específico de *release*.

- **`dev`**: Esta é a branch de **desenvolvimento** e integração. Todo o novo desenvolvimento (novas funcionalidades,
  correções de bugs, refatorações) é integrado aqui. Ela deve representar uma versão potencialmente lançável do
  software.

- **Branches de Funcionalidade/Correção (`feature/*`, `fix/*`, `chore/*`)**:
    - Todo novo trabalho deve começar em uma nova branch, criada a partir da `dev`.
    - Utilize uma nomenclatura clara e descritiva, como `feature/autenticacao-oauth2` ou `fix/correcao-bug-login`.

### 3. Fluxo de Trabalho com Pull Requests (PRs)

**Toda e qualquer alteração** de código, sem exceção, deve ser submetida através de um **Pull Request**.

1. Crie sua `feature/` ou `fix/` branch a partir da `dev`.
2. Desenvolva e faça commit das suas alterações na sua branch.
3. Quando o trabalho estiver concluído, abra um Pull Request da sua branch para a `dev`.
4. O PR deve ter um **título claro** e uma **descrição detalhada**, explicando o que foi feito e por quê. Se resolver
   uma *issue*, mencione-a.
5. O PR passará por revisões de código (*code review*) por outros membros da equipe e por checagens automatizadas (
   CI/CD).
6. Somente após a aprovação, o PR poderá ser "mergeado" na `dev`.

### 4. Padrão de Commits: Semantic Commits

Adotamos o padrão de **Semantic Commits** para manter nosso histórico de versões limpo, legível e automatizável. Isso
facilita a geração de changelogs e a compreensão do progresso do projeto.

A estrutura de um commit deve ser: `tipo(escopo): descrição curta`

**Principais `tipos`:**

* **`feat`**: Uma nova funcionalidade (feature).
* **`fix`**: Uma correção de bug.
* **`docs`**: Alterações apenas na documentação.
* **`style`**: Alterações de formatação, espaços em branco, etc. (sem impacto na lógica).
* **`refactor`**: Refatoração de código que não corrige um bug nem adiciona uma feature.
* **`test`**: Adição ou correção de testes.
* **`chore`**: Atualizações de tarefas de build, gerenciadores de pacotes, etc.

*Exemplo:*

```bash
git commit -m "feat(api): implementar endpoint para cadastro de usuários"
````

```bash
git commit -m "fix(auth): corrigir validação de token expirado"
```

### 5\. Evitando o "Branch Hell"

O "Branch Hell" (inferno de branches) ocorre quando há um excesso de branches ativas, antigas e com grandes divergências
entre si, tornando a integração um processo caótico e propenso a erros. Para evitar isso:

- **Mantenha as branches com vida curta:** crie branches para tarefas pequenas e específicas. Integre-as via PR assim
  que estiverem prontas.
- **Atualize a sua branch constantemente:** Faça `git pull origin dev` ou `git rebase origin/dev` na sua branch de feature
  com frequência para evitar grandes conflitos no futuro.
- **Delete branches após o merge:** Após seu PR ser integrado, delete a branch. Ela já cumpriu seu propósito.
- **Use uma nomenclatura clara:** Facilita a identificação do propósito e do dono da branch.

-----

## ✨ Boas Práticas Adicionais

Além das políticas obrigatórias, incentivamos fortemente as seguintes práticas para elevar a qualidade do nosso
trabalho:

- **Qualidade de Código**: Utilize linters e formatadores (como ESLint, Prettier, Black, etc.) configurados no projeto
  para garantir um padrão de código consistente.
- **Testes**: Código sem teste é código legado desde o seu nascimento. Escreva testes unitários, de integração e, quando
  aplicável, de ponta a ponta (E2E) para garantir a estabilidade do seu código.
- **Documentação**: Cada repositório deve ter o seu próprio `README.md` explicando o que o projeto faz, como configurá-lo,
  como executá-lo localmente e como rodar os testes. Comente trechos complexos do código quando a lógica não for
  autoexplicativa.
- **Revisão de Código Construtiva**: Ao revisar um PR, seja respeitoso e construtivo. O objetivo é melhorar o código,
  não criticar o autor. Foque em pontos objetivos, sugira melhorias e compartilhe conhecimento.

-----

## 💬 Comunicação

A comunicação clara e eficiente é a chave para o sucesso de projetos complexos. Nosso canal principal para discussões
técnicas, dúvidas rápidas, anúncios e colaboração em tempo real é o Discord.

➡️ **Junte-se à nossa comunidade de desenvolvedores no Discord:** *
* [Deploys Rsys](https://discord.gg/jFpxThFP)
* [RIBEIRÃO SYSTEM DISCORD OFICIAL](https://discord.gg/kbj3EeaR)

-----
