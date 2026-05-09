# Dashboard – Diagnóstico Territorial PAS Paraíba

Dashboard interativo com mapa e gráficos dos municípios dos Territórios **Cariri Ocidental** e **Serra do Teixeira** no estado da Paraíba – Territórios PAS Nordeste.

## 👥 Equipe

| Nome | Função |
|---|---|
| Josias de Castro Galvão | Coordenador Institucional PB |
| Anieres Barbosa da Silva | Assessor |
| Julia Gonçalves da Silva Pereira | Bolsista IC |
| Francisca Nívia Costa de Vasconcelos | Articuladora Territorial |
| Jefferson Sant'anna Galvão | Geógrafo e Tecnólogo em TI |

**Fontes:** IBGE, MDA · 2026

## 🔗 GitHub Pages

Após publicar no GitHub, acesse a URL configurada em **Settings → Pages**.

## 📋 Funcionalidades

- **Mapa interativo** (Leaflet) com os 23 municípios dos 2 territórios PAS
- **Clique no município** para ver dados detalhados no painel lateral
- **Colorir mapa por**: Território · IDH · % Pobreza Extrema · Taxa de Alfabetização · Crescimento Pop. · População
- **Filtro** por território
- **Legenda clicável** no mapa para filtrar por território
- **4 gráficos** (Plotly.js):
  - Barra empilhada: Pop. Rural × Urbana por município
  - Dispersão: IDH × % Extremamente Pobres (por município)
  - Barra horizontal: Beneficiários de Agricultura Familiar por município
  - Misto barra+dispersão: Taxa de Alfabetização e Crescimento Populacional
- **6 KPI cards**: Municípios · Pop. Total · IDH Médio · % Ext. Pobres · Taxa Alfabetização · Pop. Quilombola/Indígena
- **Tabela sortável** com busca e exportação CSV (19 colunas de dados)
- **Sincronização bidirecional**: clique no mapa → destaca linha na tabela, e vice-versa

## 📁 Estrutura

```
index.html                          # Dashboard principal (página única)
data/
  municipios.json                   # Dados por município (23 registros)
  pb_municipios.geojson             # Polígonos dos municípios (GeoJSON – 23 features)
  diagnostico_territorial.xlsx      # Planilha fonte (DADOS + CAPA)
```

## 🚀 Publicando no GitHub Pages

1. Crie um repositório no GitHub
2. Faça push de todos os arquivos para a branch `main`
3. Vá em **Settings → Pages → Source → Deploy from branch → main → / (root)**
4. Aguarde alguns minutos e acesse a URL gerada

## 📊 Dados

- **Fonte**: IBGE, Ministério do Desenvolvimento Agrário (MDA) – 2026
- **Cobertura**: 23 municípios · 2 Territórios PAS (Cariri Ocidental e Serra do Teixeira) · Paraíba
- **Geometrias**: IBGE (via biblioteca geobr) · EPSG:4674

## 🛠️ Tecnologias

| Biblioteca | Uso |
|---|---|
| [Leaflet 1.9](https://leafletjs.com) | Mapa interativo + GeoJSON |
| [Plotly.js 2.27](https://plotly.com/javascript/) | Gráficos |
| [Bootstrap 5.3](https://getbootstrap.com) | Layout responsivo |
| CartoDB Dark | Tiles do mapa base |
