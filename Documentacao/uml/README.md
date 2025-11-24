# Diagramas UML do Projeto SET

Esta pasta contém todos os diagramas UML do projeto SET (Software Estimation Tool) em formato PlantUML.

## Lista de Diagramas

### Diagramas de Arquitetura
1. **01-component-architecture.puml** - Diagrama de componentes mostrando a arquitetura geral do sistema

### Diagramas de Classes
2. **02-class-estimator.puml** - Pacote estimator (motor de estimativas)
3. **03-class-ai.puml** - Pacote ai (integração OpenAI)
4. **04-class-storage.puml** - Pacote storage (persistência BoltDB)
5. **05-class-github.puml** - Pacote github (integração GitHub API)
6. **06-class-config.puml** - Pacote config (gerenciamento de configuração)

### Diagramas de Sequência
7. **07-sequence-estimate.puml** - Fluxo de estimativa de tarefa única
8. **08-sequence-batch.puml** - Fluxo de processamento em lote
9. **09-sequence-sync.puml** - Fluxo de sincronização com GitHub

## Como Visualizar os Diagramas

### Opção 1: PlantUML Online (Mais Fácil)

1. Acesse: http://www.plantuml.com/plantuml/uml/
2. Copie o conteúdo de qualquer arquivo `.puml`
3. Cole na caixa de texto
4. Veja o diagrama renderizado

### Opção 2: Visual Studio Code (Recomendado)

1. Instale a extensão "PlantUML" por jebbs
2. Abra qualquer arquivo `.puml`
3. Pressione `Alt+D` para preview ao vivo
4. Ou clique com botão direito > "Preview Current Diagram"

**Nota**: Você precisará de Java instalado e GraphViz (opcional, mas recomendado para melhores resultados)

### Opção 3: IntelliJ IDEA / PyCharm

1. Instale o plugin "PlantUML integration"
2. Abra qualquer arquivo `.puml`
3. Verá o preview automaticamente no painel lateral

### Opção 4: Linha de Comando

```bash
# Instalar PlantUML (requer Java)

# macOS
brew install plantuml

# Ubuntu/Debian
sudo apt-get install plantuml

# Windows
# Baixe de: https://plantuml.com/download

# Gerar imagens PNG
plantuml *.puml

# Gerar imagens SVG (melhor qualidade)
plantuml -tsvg *.puml
```

### Opção 5: Ferramentas Online Alternativas

- **PlantText**: https://www.planttext.com/
- **PlantUML QEditor**: Editor offline standalone
- **Draw.io**: Pode importar PlantUML (File > Import > PlantUML)

## Exportar para Outros Formatos

### Gerar Imagens PNG

```bash
# Todos os diagramas
plantuml *.puml

# Diagrama específico
plantuml 01-component-architecture.puml
```

### Gerar SVG (Vetor - Melhor para Documentação)

```bash
plantuml -tsvg *.puml
```

### Gerar PDF

```bash
plantuml -tpdf *.puml
```

### Inserir no Word/PowerPoint

1. Gere imagens PNG ou SVG usando comandos acima
2. Insira as imagens no documento
3. Ou use a extensão VS Code para copiar como imagem

## Dicas

### Para Melhor Visualização

- **SVG** é melhor para zoom sem perda de qualidade
- **PNG** é mais compatível com todas as ferramentas
- **PDF** é ideal para documentação impressa

### Para Edição

1. Mantenha os arquivos `.puml` versionados no Git
2. Gere imagens apenas para apresentações/documentação
3. Não commite imagens geradas (adicione `*.png`, `*.svg` ao `.gitignore`)

### Personalização

Você pode personalizar os diagramas editando os arquivos `.puml`:

- **Cores**: Modifique `skinparam` no início dos arquivos
- **Estilo**: Altere `skinparam componentStyle`
- **Layout**: Adicione direções como `left to right direction`

Exemplo:
```plantuml
@startuml
skinparam backgroundColor transparent
skinparam classBackgroundColor LightBlue
left to right direction

' Seu diagrama aqui
@enduml
```

## Integração com Documentação

Estes diagramas são referenciados no arquivo principal de documentação:
- `../Documentacao-de-Projeto-v2.md`

Cada diagrama está documentado em detalhe na seção correspondente da documentação.

## Atualizações

Ao modificar a arquitetura ou componentes do sistema:

1. Atualize os diagramas `.puml` correspondentes
2. Regenere as imagens se necessário
3. Atualize referências na documentação principal
4. Commit os arquivos `.puml` atualizados

## Ferramentas Adicionais

### PlantUML Cheat Sheet
- https://plantuml.com/guide

### Sintaxe PlantUML
- **Diagramas de Classe**: https://plantuml.com/class-diagram
- **Diagramas de Sequência**: https://plantuml.com/sequence-diagram
- **Diagramas de Componentes**: https://plantuml.com/component-diagram

### Conversores
- **PlantUML to Draw.io**: https://github.com/qjebbs/vscode-plantuml/wiki/
- **PlantUML to Mermaid**: Ferramentas online disponíveis

## Suporte

Se encontrar problemas ao visualizar os diagramas:

1. Verifique se o arquivo `.puml` está bem formatado
2. Certifique-se de que tem Java instalado (necessário para PlantUML)
3. Tente abrir no PlantUML Online primeiro
4. Consulte a documentação oficial: https://plantuml.com/

---

**Criado por**: Inácio Moraes da Silva
**Data**: Janeiro 2025
**Última Atualização**: 2025-01-09
