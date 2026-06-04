# Roadmap Final de Obra

Mini app para acompanhar pendencias finais de obra por semana, com checklist e sincronizacao via Firebase.

## Publicacao

Este repositorio foi preparado para GitHub Pages. O arquivo principal e `index.html`.

Depois de publicar, lembre de adicionar o dominio do GitHub Pages em:

`Firebase > Authentication > Settings > Authorized domains`

Exemplo:

`mzapparoli.github.io`

## Regras do Firestore

O app salva o quadro inteiro no documento `roadmaps/final-obra`.

```txt
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /roadmaps/final-obra {
      allow read, write: if request.auth != null;
    }
  }
}
```
