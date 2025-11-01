# 🌴 Algarve Events

## Visão Geral

**Algarve Events** é uma plataforma que centraliza a descoberta de eventos na região do Algarve, permitindo planear deslocações, encontrar alojamento e enviar feedback em tempo real.  
A missão é simples: **garantir informação fiável, acessível e útil**, especialmente para visitantes com mobilidade reduzida e donos de animais de companhia.

O projeto nasce como **MVP** com uma visão de longo prazo — priorizando qualidade de dados, transparência e experiência de utilização.

---

## 🎯 Objetivo e Proposta de Valor

- **Descobrir eventos** por data, local, categoria e etiquetas (acessibilidade, pet friendly, sustentável).  
- **Planear deslocações** em transporte público ou privado, com estimativas de tempo, custo e pegada de carbono.  
- **Encontrar alojamento** integrado com APIs de reservas e listagens locais.  
- **Reportar e avaliar** experiências, problemas e acessibilidade no local.  

**Valor-chave:** dados verificados, informação de acessibilidade, sustentabilidade e fluxo de feedback simplificado.

---

## 👥 Público-Alvo

- Turistas nacionais e internacionais  
- Residentes locais  
- Pessoas com mobilidade reduzida e acompanhantes  
- Donos de animais de companhia  
- Municípios, promotores e alojamentos que pretendam visibilidade e feedback  

---

## 🧩 Funcionalidades Principais (MVP)

1. **Agregador de eventos** — indexação por data, local, categoria e etiquetas.  
2. **Planeador de deslocações** — transportes públicos/privados, horários, custos.  
3. **Busca de alojamento** — integração com APIs e listagens sustentáveis.  
4. **Report e feedback** — críticas, sugestões, relatórios de acessibilidade com fotos.  
5. **Perfil detalhado** — fichas de eventos/locais com contactos e reviews.  
6. **Filtros especiais** — “Acessível PRM” e “Pet Friendly”.  
7. **Notificações** — alterações, cancelamentos, novas edições.  

---

## 🗂️ Fontes de Dados e Pipeline

- **Fontes:** sites oficiais, APIs públicas, promotores culturais, redes sociais.  
- **Pipeline:** crawlers específicos → normalização → geocoding → verificação automática e humana.  
- **Ética:** respeito por *robots.txt*, termos de serviço e transparência de origem.

---

## ✅ Verificação de Qualidade

- **Automática:** deteção de duplicados e inconsistências.  
- **Humana:** revisão manual para eventos com baixa confiança.  
- **Colaborativa:** utilizadores e organizadores podem validar ou corrigir dados.  

---

## ♿ Acessibilidade (PRM)

- Dados: rampas, casas de banho acessíveis, elevadores, largura de portas, lugares reservados.  
- Verificação: níveis “verificado”, “indicado pelo organizador” ou “reportado por utilizadores”.  
- UX: filtros por nível de acessibilidade, mapas acessíveis e informação contextual.

---

## 🐾 Pet Friendly

- Informação padronizada: aceitação de animais, espaços verdes, regras e políticas.  
- Validação: tags visíveis e reviews com fotos.  
- Recomendações: alojamentos e serviços veterinários próximos.

---

## 🚆 Transporte e Mobilidade

- Integrações: CP, Rede Expressos, operadores regionais, serviços de mobilidade partilhada.  
- Funcionalidade: tempo, custo e pegada de carbono.  
- Acessibilidade: elevadores nas estações e espaço para cadeiras de rodas.

---

## 🏗️ Arquitectura Técnica (High-Level)

**Backend:**  
- Microserviços: ingestão, normalização, pesquisa, API pública.  
- Bases de dados: PostgreSQL + PostGIS; ElasticSearch.  

**Frontend:**  
- Next.js (TypeScript), Tailwind, mapas interativos, PWA.  

**Infraestrutura:**  
- Cloud com containers, CDN e cache.  
- Logs, métricas e alertas para falhas.  
- Conformidade com GDPR.  

---

## 🧱 Exemplo de Esquema de Dados

| Entidade | Campos principais |
|-----------|------------------|
| Evento | id, título, descrição, datas, local_id, categoria, preço, origem, tags[] |
| Local | id, nome, coordenadas, morada, acessibilidade{}, pet_friendly |
| Alojamento | id, nome, disponibilidade, políticas_pet, sustentabilidade_tags |
| Report | id, tipo, descrição, fotos[], data, utilizador_id, estado |

---

## 🧭 UX e Produto

- **Mapa** como centro da descoberta.  
- **Fluxo:** pesquisa → ficha → deslocação → alojamento → feedback.  
- **Modo rápido** de reporte no local.  
- Design minimalista e acessível.  

---

## 💰 Monetização e Sustentabilidade

- Subscrições premium para organizadores.  
- Listagens patrocinadas com transparência editorial.  
- Comissões por reservas (afiliados).  
- Parcerias com municípios e instituições locais.  

---

## 🗓️ Roadmap

**Fase 0 (4–8 semanas)** – MVP  
- Agregador básico, pesquisa e feedback.  

**Fase 1 (3 meses)** – Validação  
- Crawlers melhorados, filtros de acessibilidade, PWA.  

**Fase 2 (6 meses)** – Escala  
- Verificação humana, painel de organizadores, analytics.  

**Fase 3 (12 meses)** – Produto maduro  
- Monetização, bilheteiras, acordos institucionais.  

---

## 📊 Métricas de Sucesso

- ≥80% de eventos com *confidence score* > 0.8  
- Sessões por utilizador e tempo médio em ficha  
- Cliques em rotas e reservas  
- Relatórios de acessibilidade resolvidos  
- Tempo médio de deteção de novos eventos  

---

## ⚠️ Riscos e Mitigação

- **Dados errados:** validação automática + revisão humana.  
- **Limites legais:** uso de APIs oficiais e conformidade legal.  
- **Adoção limitada:** valor claro para organizadores e municípios.  
- **Dependência externa:** camadas de fallback e redundância.  

---

## ⚖️ Requisitos Legais e Éticos

- Conformidade total com **GDPR**.  
- Transparência na origem dos dados.  
- Políticas claras de moderação e privacidade.  

---

## 🔧 Próximos Passos

1. Mapear 10 fontes principais de eventos no Algarve.  
2. Criar protótipo de crawler + normalização.  
3. Implementar API e página de evento com geolocalização.  
4. Testes com utilizadores (mobilidade reduzida e donos de animais).  

---

## 🧠 Licença e Contribuição

Este projeto está sob licença **MIT**.  
Contribuições são bem-vindas: *issues*, *pull requests* e sugestões de fontes de dados.

---

**Autor:** F  
**Visão:** Transformar o Algarve num território de eventos verdadeiramente acessível e sustentável.
