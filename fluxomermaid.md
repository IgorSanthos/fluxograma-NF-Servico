```
config:
  themeVariables:
    nodeBorder: '#1E90FF'
    mainBkg: '#ADD8E6'
    tertiaryColor: '#1E90FF'
---

flowchart TD
    A("Emissão de nota<br>") -.-> BA("Pessoa Física") & PJ("Pessoa Jurídica")
    BA -.-> B("Sem Retenção de IRRF e CSRF")
    PJ -.-> C("Empresa Simples Nacional?") & OG("Orgao Publico")
    OG -. Não .-> N("Não")
    OG -. Sim .-> CONT("Entre em contato com a contabilidade")
    C -. Sim .-> D("Nota Fiscal maior que R$ 666,00?")
    D -. Sim .-> E("Retenção de IRRF")
    D -. Não .-> F("Sem Retenção de IRRF")
    C -.-> N
    N -.-> G("Nota Fiscalmaior que R$ 666,00?") & GG("Nota Fiscal maior que R$ 215,00?")
    G -. Sim .-> H("Retenção de IRRF")
    G -.-> I("Sem Retenção de IRRF")
    GG -. sim .-> J("Retenção de CSRF")
    GG -. Não .-> L("Sem Retenção de CSRF")

```