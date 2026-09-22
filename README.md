# telas-de-banco

Repositório de estudo com **templates de telas bancárias e de negócios financeiros** (internet banking, fintechs, corretoras), organizado para servir de repertório reutilizável de UI, requisitos e histórias de usuário — inclusive como referência para atuação como Product Owner (PO).

## O que tem aqui

- **Escopo do projeto**, com priorização **MoSCoW** das telas
- Para cada tela: **elementos obrigatórios**, **histórias de usuário** (funcional + segurança) e **critérios de aceite**
- **Rastreabilidade**: cada história de usuário está vinculada a um código de requisito (RF-xx / RNF-SEG-xx), permitindo mapear HU → Requisito → Tela
- Templates de tela pensados para reuso em projetos futuros (acadêmicos ou pessoais)

## Estrutura do repositório

```
/templates
  /must-have
    01-login
    02-dashboard
    03-extrato
    04-transferencia
    05-investimentos-lista
    06-investimentos-detalhe
    07-pagamentos
    08-cartoes
    09-perfil-seguranca
  /should-have
    10-onboarding
    11-simulador
    12-notificacoes
    13-suporte
  /could-have
    14-comparador
    15-metas-financeiras
    16-pontos-recompensas
    17-acessibilidade
/docs
  escopo.md                              # escopo geral e MoSCoW
  historias-usuario-must-have.md         # HUs das telas essenciais
  historias-usuario-should-could-have.md # HUs das telas complementares
  requisitos-seguranca.md                # tabela consolidada de requisitos (RNF-SEG-01 a 22)
```

Cada pasta de tela (`/templates/.../NN-nome-da-tela`) pode conter:
- Wireframe ou mock (imagem, link de Figma, etc.)
- Lista de componentes usados
- `README.md` local com as HUs específicas daquela tela (copiadas de `/docs`)

## Priorização (MoSCoW)

| Prioridade | Telas |
|---|---|
| **Must Have** | Login, Dashboard, Extrato, Transferência, Investimentos (lista/detalhe), Pagamentos, Cartões, Perfil/Segurança |
| **Should Have** | Onboarding, Simulador, Notificações, Suporte |
| **Could Have** | Comparador de produtos, Metas financeiras, Pontos/recompensas, Acessibilidade avançada |
| **Won't Have** (nesta rodada) | Backoffice administrativo, integrações avançadas de Open Finance, multi-idioma |

## Padrão de história de usuário

Cada tela possui pelo menos **2 histórias de usuário**: uma funcional e uma de segurança.

```
Como [persona], quero [ação], para [benefício]

Critérios de aceite:
- Dado [contexto], quando [ação], então [resultado esperado]

Requisito vinculado: RF-xx / RNF-SEG-xx
```

## Requisitos de segurança transversais

Aplicam-se a todas as telas, independente da prioridade:

- Dado sensível (saldo, número de cartão, CPF) deve poder ser mascarado/ocultado
- Toda ação financeira exige reautenticação (senha transacional, biometria ou MFA)
- Sessão expira por inatividade
- Validação de entrada no client **e** no servidor
- Toda comunicação via HTTPS/TLS
- Logs de auditoria para login, alterações cadastrais e transações

## Status do projeto

- [x] Escopo e MoSCoW definidos
- [x] Histórias de usuário — Must Have
- [x] Histórias de usuário — Should Have / Could Have
- [ ] Wireframes/mocks por tela
- [ ] Templates de código/componentes

## Uso

Este repositório é de estudo pessoal e serve como:
1. Referência de composição de telas bancárias para projetos próprios
2. Banco de histórias de usuário reutilizáveis em contextos de PO
3. Checklist de requisitos de segurança para produtos financeiros
