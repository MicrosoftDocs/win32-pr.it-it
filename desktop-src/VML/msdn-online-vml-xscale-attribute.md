---
title: Attributo la XScale
description: Attributo la XScale
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337702"
---
# <a name="vml-xscale-attribute"></a>Attributo la XScale

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se verrà utilizzato un TextPath diretto al posto del percorso della forma. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "XScale: *Expression* " >

**Sintassi dello script**

*element* . Style. XScale = "*Expression*"

*espressione* = *element*. Style. XScale

**Osservazioni:**

Se **true**, il testo viene eseguito lungo aPath da sinistra verso destra lungo il valore x del limite inferiore della forma. Il valore predefinito è **False**.

*Attributo standard la*

**Esempio**

Il testo verrà visualizzato come se fosse stato disegnato su una linea orizzontale, anche se il percorso della forma è una diagonale.


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 