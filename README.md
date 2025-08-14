# Claude Code Agents

Uma coleção de agentes personalizados para Claude Code, projetados para aprimorar fluxos de trabalho de desenvolvimento e automatizar tarefas comuns.

## Autor

**Samuel Rizzo**  
GitHub: [@samuelrizzo](https://github.com/samuelrizzo)

## Repositório

[https://github.com/samuelrizzo/cc-agents](https://github.com/samuelrizzo/cc-agents)

## Agentes Disponíveis

### 🔍 CodeRabbit Review Handler
**Arquivo**: `.claude/agents/coderabbit-review-handler.md`  
**Modelo**: Sonnet

Analisa reviews de pull requests do CodeRabbit e implementa correções ou fornece justificativas técnicas.

**Características:**
- Avalia a validade do feedback de revisão de código gerado por IA
- Cria planos de implementação para feedback válido
- Fornece justificativas técnicas para feedback inválido
- Segue um framework de decisão estruturado
- Referencia documentação do projeto (CLAUDE.md) para contexto

### 🔧 Lint Fixer
**Arquivo**: `.claude/agents/lint-fixer.md`  
**Modelo**: Sonnet  
**Cor**: Azul

Identifica e corrige automaticamente erros de linting em bases de código.

**Características:**
- Escaneia e categoriza violações de linting
- Cria planos de correção KISS (Keep It Simple, Stupid)
- Executa correções sistemáticas (auto-corrigíveis primeiro)
- Valida que as mudanças não quebram funcionalidades
- Suporta ESLint, Prettier, TypeScript, React/Next.js

### ✅ Pre-Commit Reviewer
**Arquivo**: `.claude/agents/pre-commit-reviewer.md`  
**Modelo**: Sonnet

Revisa mudanças de código antes do commit para garantir conformidade com diretrizes do projeto.

**Características:**
- Lê diretrizes do projeto de `/.cursor/rules` e `/CLAUDE.md`
- Corrige automaticamente problemas de linting antes da revisão manual
- Analisa conformidade com TypeScript, React/Next.js, Tailwind CSS
- Verifica padrões de arquitetura, acessibilidade, práticas de segurança
- Cria planos de correção quando problemas são encontrados

## Estrutura do Repositório

```
cc-agents/
├── .claude/
│   └── agents/
│       ├── coderabbit-review-handler.md
│       ├── lint-fixer.md
│       └── pre-commit-reviewer.md
└── README.md
```

## Como Usar

1. Clone este repositório em seu ambiente de desenvolvimento
2. Os agentes serão automaticamente disponibilizados no Claude Code
3. Use os agentes conforme necessário em seu fluxo de trabalho:
   - **CodeRabbit Review Handler**: Após receber reviews do CodeRabbit
   - **Lint Fixer**: Quando encontrar erros de linting
   - **Pre-Commit Reviewer**: Antes de fazer commits importantes

## Contribuições

Sinta-se à vontade para enviar issues e solicitações de melhorias!