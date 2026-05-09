# Dashboard – Territórios PAS Nordeste (Paraíba)

Dashboard interativo com mapa e gráficos dos municípios que compõem os Territórios PAS Nordeste no estado da Paraíba.

## 🔗 GitHub Pages

Após publicar no GitHub, acesse:  
`https://<seu-usuario>.github.io/<nome-do-repositorio>/`

## 📋 Funcionalidades

- **Mapa interativo** (Leaflet) com os 126 municípios da PB pertencentes aos territórios PAS Nordeste
- **Clique no município** para ver dados detalhados no painel lateral
- **Colorir mapa por**: Território · IDH · % Pobreza Extrema · Bioma · População
- **Filtros**: por território e por bioma
- **Legenda clicável** no mapa para filtrar por território
- **4 gráficos** (Plotly.js):
  - Barra: População por território
  - Dispersão: IDH × % Extremamente Pobres (por município)
  - Barra horizontal: Agricultura Familiar por território
  - Barra empilhada: Pop. Rural × Urbana por território
- **KPI cards** atualizados dinamicamente com os filtros

## 📁 Estrutura

```
index.html                          # Dashboard principal
data/
  municipios.json                   # Dados por município (126 registros)
  territorios.json                  # Dados agregados por território
  pb_municipios.geojson             # Polígonos dos municípios (GeoJSON)
  lista_composicao_territorios_pas_nordeste.xlsx  # Planilha original
```

## 🚀 Publicando no GitHub Pages

1. Crie um repositório no GitHub (pode ser público ou privado com Pages ativado)
2. Faça push de todos os arquivos para a branch `main`
3. Vá em **Settings → Pages → Source → Deploy from branch → main → / (root)**
4. Aguarde alguns minutos e acesse a URL gerada

## 📊 Dados

- **Fonte**: Ministério do Desenvolvimento Agrário (MDA) – Março/2026
- **Cobertura**: 126 municípios · 8 Territórios PAS · Estado da Paraíba
- **Geometrias**: IBGE (via biblioteca geobr) · EPSG:4674

## 🛠️ Tecnologias

| Biblioteca | Uso |
|---|---|
| [Leaflet 1.9](https://leafletjs.com) | Mapa interativo + GeoJSON |
| [Plotly.js 2.27](https://plotly.com/javascript/) | Gráficos |
| [Bootstrap 5.3](https://getbootstrap.com) | Layout responsivo |
| CartoDB Dark | Tiles do mapa base |
