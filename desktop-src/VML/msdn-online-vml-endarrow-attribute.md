---
title: Attributo la
description: Attributo la
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542d6dbb3b30467c4bcad909f2b49d617f8bd886
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300404"
---
# <a name="vml-endarrow-attribute"></a>Attributo la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una freccia per la fine di una riga. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* di " *Expression* " >

**Sintassi dello script**

*element* . indarrow = "*Expression*"

*espressione* = *elemento*.

**Osservazioni:**

I possibili valori sono:

-   Nessuno (valore predefinito)
-   Blocca
-   Classic
-   Diamond
-   Ovale
-   Apri

*Attributo standard la*

**Esempio**

Una linea viene disegnata con una freccia classica alla fine del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 