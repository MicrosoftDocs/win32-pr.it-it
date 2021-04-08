---
title: LA V-text-Reverse-attributo
description: LA V-text-Reverse-attributo
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047049"
---
# <a name="vml-v-text-reverse-attribute"></a>LA V-text-Reverse-attributo

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se l'ordine di layout delle righe è invertito. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "v-text-Reverse: *Expression* " >

**Sintassi dello script**

*element* . Style. v-text-Reverse = "*Expression*"

*espressione* = *element*. Style. v-text-Reverse

**Osservazioni:**

Se **true**, l'ordine di layout delle righe viene invertito. Questo attributo viene utilizzato per il layout di testo verticale. Il valore predefinito è **False**.

*Attributo standard la*

**Esempio**

L'ordine di layout è invertito.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 