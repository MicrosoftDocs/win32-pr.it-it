---
title: Attributo la V-text-Kern
description: Attributo la V-text-Kern
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963292"
---
# <a name="vml-v-text-kern-attribute"></a>Attributo la V-text-Kern

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se la crenatura è attivata. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "v-text-Kern: *Expression* " >

**Sintassi dello script**

*element* . Style. v-text-Kern = "*Expression*"

*espressione* = *element*. Style. v-text-Kern

**Osservazioni:**

Se **true**, la crenatura è attivata. Il valore predefinito è **False**. La crenatura è la rimozione dello spazio tra alcune coppie di lettere per compensare i letterforms non uniformi. Ad esempio, se la crenatura è attivata, viene rimosso spazio aggiuntivo tra una "T" maiuscola e una "i" minuscola.

*Attributo standard la*

**Esempio**

La crenatura è attivata.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 