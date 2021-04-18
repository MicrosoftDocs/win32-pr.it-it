---
title: Attributo EndArrowLength di la
description: Attributo EndArrowLength di la
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299854"
---
# <a name="vml-endarrowlength-attribute"></a>Attributo EndArrowLength di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una lunghezza della freccia per la fine di una riga. Proprietà di lettura/scrittura. **VgArrowheadLength**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* endarrowlength = " *Expression* " >

**Sintassi dello script**

*element* . endarrowlength = "*Expression*"

*espressione* = *elemento*. endarrowlength

**Osservazioni:**

I possibili valori sono:

-   Short
-   Media (impostazione predefinita)
-   long

*Attributo standard la*

**Esempio**

Una linea viene disegnata con una freccia classica breve alla fine del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 