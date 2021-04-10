---
title: Attributo la V-text-align
description: Attributo la V-text-align
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6efb96bde980a4831f400ada7032f9ee37f1d976
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963202"
---
# <a name="vml-v-text-align-attribute"></a>Attributo la V-text-align

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'allineamento del testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "v-text-align: *Expression* " >

**Sintassi dello script**

*element* . Style. v-text-align = "*Expression*"

*espressione* = *element*. Style. v-text-align

**Osservazioni:**

I possibili valori sono:

-   **Left** (impostazione predefinita)
-   **Ok**
-   **Center**
-   **giustificare**
-   **lettera-giustificazione**
-   **Stretch-giustifica**

*Attributo standard la*

**Esempio**

Il testo verrà esteso per adattarsi al percorso, ma lo spazio aggiuntivo verrà inserito tra ogni lettera.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 