---
title: Attributo la V-same-Letter-Heights
description: Attributo la V-same-Letter-Heights
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727762"
---
# <a name="vml-v-same-letter-heights-attribute"></a>Attributo la V-same-Letter-Heights

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se tutte le lettere saranno della stessa altezza indipendentemente dal caso iniziale. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "v-same-Letter-Heights: *Expression* " >

**Sintassi dello script**

*element* . Style. v-same-Letter-Heights = "*Expression*"

*espressione* = *element*. Style. v-same-Letter-Heights

**Osservazioni:**

Se **true**, le lettere minuscole vengono allungate all'altezza delle lettere maiuscole. Il valore predefinito è **False**.

*Attributo standard la*

**Esempio**

Tutte le lettere saranno della stessa altezza, indipendentemente dalla distinzione tra maiuscole e minuscole.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 