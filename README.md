# Tropical Drums GL (Groove Lab) Maker

Sequenciador visual em HTML para criar ritmos de bateria e exportar padrões compatíveis com o plugin **Tropical Drum GL (Groove Lab)** no MuseScore.

<img width="920" height="883" alt="image" src="https://github.com/user-attachments/assets/94c55979-cb3a-4e42-988d-59bceaa2a8e0" />


# README — Tropical Drum GL (Groove Lab) Maker

## Visão geral

O **Tropical Drum GL (Groove Lab) Maker** é um sequenciador visual para criação de grooves de bateria voltado ao ecossistema do **MuseScore 4**. O aplicativo permite:

* Criar ritmos em grade (step sequencer)
* Editar grooves visualmente
* Trabalhar com diferentes fórmulas de compasso
* Criar acentos com dinâmica
* Exportar automaticamente um plugin `.qml`
* Importar grooves previamente gerados
* Inserir ritmos diretamente em pautas de bateria no MuseScore

O sistema já inclui diversos presets de ritmos brasileiros e internacionais:

* Samba
* Baião
* Xote
* Bossa nova
* Maracatu
* Frevo
* Reggae
* Funk
* Salsa
* Cumbia
* Blues shuffle
* Jazz waltz
* Entre outros

Desenvolvido pelo professor Glauber Santiago — DAC/UFSCar. 

---

# Funcionalidades

## Sequenciador visual

O aplicativo utiliza uma grade de passos (“step sequencer”) onde:

* Cada linha representa uma peça da bateria
* Cada coluna representa uma subdivisão temporal
* Clique simples = nota normal
* Shift + clique = acento

Peças disponíveis:

* Bumbo
* Caixa
* Borda
* Chimbal fechado
* Chimbal aberto
* Chimbal de pé
* Tons
* Surdo
* Ride
* Crash
* Splash

---

# Fórmulas de compasso suportadas

* 4/4
* 3/4
* 2/4
* 6/8
* 12/8

---

# Resoluções rítmicas

O sistema permite:

* Semicolcheias (16)
* Colcheias (8)

---

# Recursos de edição rápida

## Novo ritmo

Cria um groove vazio.

## Duplicar

Duplica o groove atual.

## Excluir

Remove o groove selecionado.

## Limpar

Apaga todas as notas do padrão atual.

## Chimbal 8ªs

Preenche automaticamente o chimbal em colcheias.

## Beat básico

Cria automaticamente um groove pop/rock básico.

---

# Importação e exportação

## Exportar plugin

O botão:

```text
Baixar .qml
```

gera automaticamente um plugin compatível com o MuseScore.

---

## Copiar código

O botão:

```text
Copiar código
```

copia o código QML completo para a área de transferência.

---

## Importar grooves

O sistema permite:

* Importar adicionando grooves
* Importar substituindo a coleção atual

Os dados são embutidos no próprio arquivo `.qml`.

---

# Estrutura do projeto

## Tecnologias utilizadas

* HTML5
* CSS3
* JavaScript Vanilla
* Qt/QML para plugins MuseScore

---

# Como executar o app

## Método simples

Basta abrir o arquivo:

```text
index.html
```

em qualquer navegador moderno.

Recomendado:

* Google Chrome
* Microsoft Edge
* Firefox

---

## Método com servidor local (recomendado)

### Python

```bash
python -m http.server 8000
```

Depois acesse:

```text
http://localhost:8000
```

---

# Como gerar o plugin do MuseScore

## Passo 1 — Criar o groove

Monte o ritmo no sequenciador.

---

## Passo 2 — Exportar

Clique em:

```text
Baixar .qml
```

O arquivo será salvo como:

```text
Tropical Drum GL - Groove Lab.qml
```

---

# Como instalar o plugin no MuseScore 4

## Localização da pasta de plugins

No MuseScore 4:

```text
Plugins → Gerenciador de Plugins
```

Depois clique em:

```text
Abrir pasta de plugins
```

---

## Caminhos padrão

### Windows

```text
C:\Users\SEU_USUARIO\Documents\MuseScore4\Plugins
```

---

### Linux

```text
~/Documents/MuseScore4/Plugins
```

---

### macOS

```text
~/Documents/MuseScore4/Plugins
```

---

# Instalação do plugin

## Passo 1

Copie o arquivo:

```text
Tropical Drum GL - Groove Lab.qml
```

para a pasta de plugins do MuseScore.

---

## Passo 2

Abra o MuseScore 4.

---

## Passo 3

Vá em:

```text
Plugins → Gerenciador de Plugins
```

---

## Passo 4

Ative:

```text
Tropical Drum GL (Groove Lab)
```

---

# Como usar o plugin no MuseScore 4

## Passo 1 — Criar pauta de bateria

No MuseScore:

```text
Adicionar → Instrumentos
```

Escolha:

```text
Drumset
```

ou qualquer instrumento de percussão GM.

---

## Passo 2 — Selecionar posição de inserção

Clique no compasso onde o groove será inserido.

IMPORTANTE:

* O plugin insere as notas a partir da posição selecionada.
* É necessário existir uma seleção válida na partitura.

---

## Passo 3 — Abrir o plugin

Vá em:

```text
Plugins → Tropical Drum GL (Groove Lab)
```

---

## Passo 4 — Escolher o groove

Clique em qualquer ritmo listado.

O plugin irá:

* Inserir automaticamente as notas
* Criar acordes de bateria
* Inserir pausas corretamente
* Preservar a duração musical

---

# Sistema de duração automática

O plugin calcula automaticamente:

* Durações
* Agrupamentos
* Pausas
* Avanço temporal

Utilizando funções internas como:

* `durationFromSteps`
* `nextHitStep`
* `addDrumChordAtCursor`



---

# Sistema MIDI / GM

O plugin utiliza mapeamento MIDI General MIDI (GM).

Exemplos:

| Instrumento     | Pitch MIDI |
| --------------- | ---------- |
| Bumbo           | 36         |
| Caixa           | 38         |
| Chimbal fechado | 42         |
| Chimbal aberto  | 46         |
| Ride            | 51         |
| Crash           | 49         |



---

# Compatibilidade

## Compatível

* MuseScore 4
* Plugins QML MuseScore
* Windows
* Linux
* macOS

---

# Observações importantes

## Mapeamento de bateria

O resultado visual depende:

* Do instrumento selecionado
* Do drumset
* Do mapa de percussão ativo no MuseScore

---

## Seleção obrigatória

O plugin necessita de:

* Partitura aberta
* Cursor válido
* Ponto de inserção selecionado

Caso contrário:

```text
Nenhuma partitura aberta.
```



---

# Presets inclusos

O app já inclui diversos grooves prontos, entre eles:

* Samba
* Samba-reggae
* Bossa nova
* Baião
* Xote
* Maracatu
* Frevo
* Funk brasileiro
* Reggae one drop
* Ska
* Salsa / Cáscara
* Cumbia
* Merengue
* Blues 12/8
* Swing shuffle
* Jazz waltz
* Rock 16s



---

# Estrutura do plugin exportado

O arquivo `.qml` contém:

* Interface gráfica QML
* Funções de geração musical
* Dados serializados dos grooves
* Botões automáticos para cada ritmo
* Integração com a API do MuseScore

---

# Créditos

Desenvolvido por:

**Professor Glauber Santiago**
DAC/UFSCar

* servidores.ufscar.br/glauber/
* sites.google.com/view/glauberia


