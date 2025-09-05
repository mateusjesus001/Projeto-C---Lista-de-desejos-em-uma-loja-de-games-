## Lista de desejos em uma loja de games (C)

Projeto em linguagem C que implementa um sistema simples de cadastro e gestão de uma lista de desejos (wishlist) para uma loja de games. Inclui rotinas de cadastro, listagem de itens e persistência em arquivo.

### Funcionalidades
- **Cadastro de jogos**: inclusão manual e por rotina de cadastro.
- **Lista encadeada (wishlist)**: inserção e listagem de itens desejados.
- **Persistência**: gravação/leitura dos dados em arquivo `.txt` na pasta `lista_de_desejos/output`.
- **Execução no Windows**: binários de exemplo já incluídos em `lista_de_desejos/output`.

### Estrutura do projeto
```text
Projeto-C---Lista-de-desejos-em-uma-loja-de-games-
├─ funções_iniciais_sem_estruturas_de_dados/
│  ├─ cadastro.c
│  └─ cadastro_manual.c
├─ lista_de_desejos/
│  ├─ cadatro_lista_encadeada.c
│  ├─ listagem_dos_itens.c
│  ├─ Projeto_final.c
│  └─ output/
│     ├─ cadatro_lista_encadeada.exe
│     ├─ dados_mateus.txt
│     └─ Projeto_final.exe
└─ projeto.c
```

### Pré-requisitos
- Windows 10/11
- Compilador C (recomendado: MinGW-w64 com `gcc`) ou uma IDE que inclua toolchain C (VS Code + Extensões C/C++, Code::Blocks, Dev-C++ etc.)

### Como compilar (PowerShell)
Abra o PowerShell na raiz do projeto e, se necessário, ajuste o codepage para UTF-8 para melhor visualização de acentos:

```powershell
chcp 65001 | Out-Null
```

Opção 1 — compilar apenas o executável principal a partir do arquivo final:

```powershell
gcc -O2 -Wall -Wextra -o .\lista_de_desejos\output\Projeto_final.exe .\lista_de_desejos\Projeto_final.c
```

Opção 2 — compilar vinculando também os módulos auxiliares (caso o `Projeto_final.c` dependa deles no seu ambiente):

```powershell
gcc -O2 -Wall -Wextra -o .\lista_de_desejos\output\Projeto_final.exe ^
  .\lista_de_desejos\Projeto_final.c ^
  .\lista_de_desejos\listagem_dos_itens.c ^
  .\lista_de_desejos\cadatro_lista_encadeada.c ^
  .\funções_iniciais_sem_estruturas_de_dados\cadastro.c ^
  .\funções_iniciais_sem_estruturas_de_dados\cadastro_manual.c
```

Observação: ajuste o comando conforme os `#include` e protótipos no seu código. Em muitos cenários, o `Projeto_final.c` já agrega e compila o restante.

### Como executar
Após compilar, rode o binário (há exemplos já na pasta `output`):

```powershell
.\lista_de_desejos\output\Projeto_final.exe
```

### Uso básico
1. Escolha a opção de cadastro para inserir jogos.
2. Adicione jogos à lista de desejos (estrutura encadeada).
3. Liste os itens cadastrados para conferir o conteúdo.
4. Salve/exporte os dados. Por padrão, o arquivo `dados_mateus.txt` fica em `lista_de_desejos/output`.

Exemplo de menu esperado (pode variar conforme a versão do código):
```text
1) Cadastrar jogo
2) Adicionar à lista de desejos
3) Listar itens
4) Salvar em arquivo
0) Sair
```

### Dicas
- Se tiver problemas com acentuação no terminal, use `chcp 65001` antes de executar o programa.
- Compile com `-Wall -Wextra` para receber avisos úteis do compilador e melhorar a qualidade do código.

### Contribuindo
Contribuições são bem-vindas! Siga este fluxo:
- Faça um fork do repositório
- Crie um branch de feature: `git checkout -b feature/minha-melhoria`
- Commit: `git commit -m "Descrição da melhoria"`
- Push: `git push origin feature/minha-melhoria`
- Abra um Pull Request descrevendo suas mudanças

### Licença
Defina aqui a licença do projeto (por exemplo, MIT). Se não houver uma ainda, considere adicionar um arquivo `LICENSE`.

### Autor
Projeto mantido por Mateus.


