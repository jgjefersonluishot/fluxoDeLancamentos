# Fluxo de Cálculo da Entrada do Imóvel
O cálculo da entrada do imóvel é realizado de forma estruturada, considerando **Ato**, **Parcelas** e **Reforços**.  
---
## Fórmulas Básicas
1. **Valor base de cada componente (ato/parcelas/reforços):**
2. **Valor unitário de cada componente:**
---
## Exemplo Completo

### Dados Iniciais
- **Valor do Imóvel:** R$ 382.822,83  
- **% do Ato:** 12%  
- **% das Parcelas:** 5%  
- **% dos Reforços:** 8%  
- **Parcelamento do Ato:** 1 + 4  
- **Quantidade de Parcelas:** 21  
- **Quantidade de Reforços:** 3  
---
### 1. Cálculo do Ato
382.822,83 x 12% = 45.938,83
45.938,83 ÷ (1+4) = 9.187,75
**Resultado:**
Ato = 1 + 4 parcelas de R$ 9.187,75
---
### 2. Cálculo das Parcelas
382.822,83 x 5% = 19.141,14
19.141,14 ÷ 21 = 911,48
makefile
Copiar código
**Resultado:**
Parcelas = 21 x R$ 911,48
---
### 3. Cálculo dos Reforços
382.822,83 x 8% = 30.625,82
30.625,82 ÷ 3 = 10.208,60
**Resultado:**
Reforços = 3 x R$ 10.208,60
### 4. Conferência do Valor da Entrada
9.187,75 + 19.141,14 + 30.625,82 = 95.705,69
### 5. Validação do Percentual da Entrada
382.822,83 x 25% = 95.705,69 ✔
### 6. Valor a Financiar
382.822,83 - 95.705,69 = 287.177,14

## Resumo em Tabela

| Componente | % aplicado | Valor Total (R$) | Qtde | Valor Unitário (R$) |
|------------|------------|------------------|------|----------------------|
| **Ato**       | 12%        | 45.938,83        | 1+4  | 9.187,75             |
| **Parcelas**  | 5%         | 19.141,14        | 21   | 911,48               |
| **Reforços**  | 8%         | 30.625,82        | 3    | 10.208,60            |
| **Total Entrada** | 25%   | **95.705,69**    | —    | —                    |
| **Financiamento** | —     | **287.177,14**   | —    | —                    |

---

## Fluxograma do Processo


    A[Valor do Imóvel] --> B{Ato %}
    A --> C{Parcelas %}
    A --> D{Reforços %}

    B --> B1[Valor do Ato]
    B1 --> B2[Dividido em 1+4]
    B2 --> B3[Parcelas do Ato]

    C --> C1[Valor Total das Parcelas]
    C1 --> C2[Dividido em 21]
    C2 --> C3[Valor de cada Parcela]

    D --> D1[Valor Total dos Reforços]
    D1 --> D2[Dividido em 3]
    D2 --> D3[Valor de cada Reforço]

    B3 --> E[Somatória Entrada]
    C3 --> E
    D3 --> E

    E --> F[Validação % da Entrada]
    F --> G[Valor a Financiar = Imóvel - Entrada]
