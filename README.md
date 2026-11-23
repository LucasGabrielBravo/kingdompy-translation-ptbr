# Português (Brasil) — Kingdom.py

Mod de idioma que traduz o **Kingdom.py** para **português do Brasil (pt-BR)**.

A tradução cobre a interface do jogo, a campanha e a documentação — incluindo menus, mensagens
do sistema, erros, diálogos e os textos didáticos (por exemplo, as explicações sobre Python que
aparecem no console). São cerca de **7.900 strings** traduzidas em um catálogo
[gettext](https://www.gnu.org/software/gettext/) (`.po`), sem nenhuma entrada pendente.

## O que é o Kingdom.py

O Kingdom.py é um jogo de estratégia/administração em que o jogador governa um reino escrevendo
**scripts em Python**: os habitantes, os recursos e os eventos do reino reagem ao código que você
escreve. Este mod não altera a jogabilidade nem o código do jogo — ele apenas troca os textos
exibidos para português.

## Conteúdo do repositório

```
kingdompy-translation-ptbr/
├── mod.json          # Manifesto do mod (id, título e descrição)
├── lang/
│   └── pt_BR.po      # Catálogo de tradução: msgid (inglês) → msgstr (português)
├── LICENSE           # Licença MIT
└── README.md
```

- **`mod.json`** — identifica o mod e o idioma para o jogo.
- **`lang/pt_BR.po`** — arquivo gettext com todos os textos traduzidos. É o único arquivo que
  precisa ser editado para corrigir ou melhorar a tradução.

## Como usar

### Instalação

1. Baixe este repositório (ou clone com `git clone`).
2. Copie a pasta **`pt-br`** para dentro da pasta de mods do jogo:

   ```
   C:\Users\NOME_DO_USUARIO\Documents\My Games\Kingdom.py\mods\
   ```

   O resultado deve ficar assim:

   ```
   C:\Users\NOME_DO_USUARIO\Documents\My Games\Kingdom.py\mods\
   └── pt-br\
       ├── mod.json
       ├── README.md
       └── lang\
           └── pt_BR.po
   ```

   > Troque `NOME_DO_USUARIO` pelo nome do seu usuário no Windows. Se a pasta `mods` ainda não
   > existir, crie-a dentro de `Documents\My Games\Kingdom.py\`.

3. Abra o jogo, vá até as **configurações de idioma** e selecione **Português (Brasil)**.
4. Reinicie o jogo, se necessário, para que todos os textos sejam recarregados.

> O caminho acima é o padrão no Windows. Se a sua instalação usar a opção de manter os dados
> junto do jogo (portable), a pasta de mods fica em `Kingdom.py\mods\` na pasta de instalação.
> Se o jogo já tiver uma tradução parcial instalada, remova a pasta de idioma antiga antes de
> copiar esta, para evitar conflitos.

### Desinstalação

Apague a pasta `pt-br` de `Documents\My Games\Kingdom.py\mods\` e volte a selecionar o idioma
original nas configurações do jogo.

### Atualização

Substitua a pasta `pt-br` dentro de `Documents\My Games\Kingdom.py\mods\` pela versão nova. Se
você tiver edições locais na tradução, faça backup de `lang\pt_BR.po` antes.

## Como contribuir

Correções de tradução, sugestões de termos e ajustes de consistência são bem-vindos.

1. Faça um fork do repositório e crie um branch para a sua alteração.
2. Edite **`lang/pt_BR.po`** mantendo os `msgid` intactos e alterando apenas os `msgstr`.
3. Verifique se o arquivo continua válido, por exemplo:

   ```bash
   msgfmt --check -o /dev/null lang/pt_BR.po
   ```

4. Abra um Pull Request descrevendo o que foi corrigido.

**Convenções do projeto:**

- Português do Brasil, com acentuação correta e tom próximo ao original (sem inventar conteúdo).
- Mantenha os **`{0}`, `{1}`, `%s`, `\n`** e demais marcadores exatamente como estão no original.
- Preserve espaços no início/fim das strings — muitos textos são concatenados pelo jogo.
- Não traduza nomes de funções, módulos, comandos ou termos de código (`print`, `str`, `int` etc.).
- Use **você** como tratamento padrão.

## Licença

Distribuído sob a **licença MIT**. Veja [LICENSE](LICENSE) para o texto completo.

## Aviso sobre o uso de IA

Esta tradução foi gerada com o auxílio de inteligência artificial.

Encontrou algum erro ou tem uma sugestão? Contribua com uma correção via Pull Request ou abra uma
issue.
