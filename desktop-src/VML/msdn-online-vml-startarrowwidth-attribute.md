---
title: Attributo StartArrowWidth di la
description: Attributo StartArrowWidth di la
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728538"
---
# <a name="vml-startarrowwidth-attribute"></a>Attributo StartArrowWidth di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la larghezza della freccia per l'inizio di una riga. Proprietà di lettura/scrittura. **VgArrowheadWidth**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* startarrowwidth = " *Expression* " >

**Sintassi dello script**

*element* . startarrowwidth = "*Expression*"

*espressione* = *elemento*. startarrowwidth

**Osservazioni:**

I possibili valori sono:

-   Limitare
-   Media (impostazione predefinita)
-   Largo

Attributo standard la

**Esempio**

Una linea viene disegnata con un'ampia freccia classica all'inizio del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 