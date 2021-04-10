---
title: Attributo Text-Decoration la
description: Attributo Text-Decoration la
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963152"
---
# <a name="vml-text-decoration-attribute"></a>Attributo Text-Decoration la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce lo stile dell'effetto di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "text-decoration: *Expression* " >

**Sintassi dello script**

*element* . Style. TextDecoration = "*Expression*"

*espressione* = *element*. Style. TextDecoration

**Osservazioni:**

I possibili valori sono:

-   Nessuno (valore predefinito)
-   sottolineato
-   linea sopra
-   line-through
-   blink

*Attributo standard la*

**Esempio**

Il testo sarà sottolineato.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 