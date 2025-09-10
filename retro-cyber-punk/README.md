---
tags:
  - home
---

# PERSONAL KNOWLEDGE MANAGEMENT SYSTEM

Este sistema PKM opera bajo un `pipeline` de datos `ELT` (`Extract-Load-Transform`), conceptualizando el aprendizaje como un proceso de desarrollo de software. Desde la `ingestión` de información en bruto hasta el despliegue de `assets` de conocimiento curado en "producción".

[[05-Docs/docs-pkm_system/doc-pkm_system|doc-pkm_system]] - [doc-link](05-Docs/docs-pkm_system/doc-pkm_system.md)

### **⚒️ INBOX ⚒️**
_Contenido esperando clasificación o procesamiento._
```dataview

TABLE status

FROM "Inbox"

SORT file.name

```

### **🚧 WORK IN PROGRESS 🚧**
_Notas y tareas activas que están siendo trabajadas._
``` dataview

TABLE status

FROM "InProgress"

SORT file.name

```


### **⚒️ LEARNING TASKS ⚒️**
_Notas y tareas activas que están siendo trabajadas._

```tasks

description includes #kai-input 
filter by function ! task.isDone

```


### ☢️ **DIRECTORY INDEX** ☢️ 
*Homepage para los diferentes directorios*
```dataview

LIST 
FROM ""
WHERE startswith(file.name, "_index-")
SORT file.name ASC

```


### **🗒️ TEMPLATES 🗒️**
_Colección de plantillas estandarizadas para asegurar la consistencia._
``` dataview
LIST 

FROM "_templates"

SORT file.name

```
