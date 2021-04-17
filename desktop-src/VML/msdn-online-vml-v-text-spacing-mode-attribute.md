---
title: LA V-text-modalità di spaziatura (attributo)
description: LA V-text-modalità di spaziatura (attributo)
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474171"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>LA V-text-modalità di spaziatura (attributo)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la modalità per letterSpacing. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *element* Style = "v-text-spaziation-Mode: *Expression* " >

**Sintassi dello script**

*element* . Style. v-text-spaziatura-modalità = "*espressione*"

*espressione* = *element*. Style. v-text-modalità spaziatura

**Osservazioni:**

I valori includono

-   **compattazione** (impostazione predefinita)
-   **Tracking**

Questo attributo determina se lo spazio verrà rimosso tra ogni lettera (stretta) o aggiunta tra ogni lettera (rilevamento). La quantità di modifiche letterSpacing è definita dall'attributo [V-text-spaziatura](msdn-online-vml-v-text-spacing-attribute.md) .

*Attributo standard la*

**Esempio**

Il letterSpacing tra ogni lettera viene aumentato di 200 unità.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 