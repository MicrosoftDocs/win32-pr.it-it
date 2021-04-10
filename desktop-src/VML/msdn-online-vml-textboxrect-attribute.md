---
title: Attributo TextBoxRect di la
description: Attributo TextBoxRect di la
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046812"
---
# <a name="vml-textboxrect-attribute"></a>Attributo TextBoxRect di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una o più caselle di testo all'interno di una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi Tag**

<v: *element* textboxrect = " *Expression* " >

**Sintassi dello script**

*element* . textboxrect = "*Expression*"

*espressione* = *elemento*. textboxrect

**Osservazioni:**

Una casella di testo viene definita da uno o più set di numeri che specificano (in ordine) i punti sinistro, superiore, destro e inferiore del rettangolo. Più set sono delimitati da un punto e virgola. Il valore predefinito è lo stesso valore della dimensione del rettangolo che lo contiene. Se è definita più di una casella di testo, i set di quadrupli delimitati da virgole che definiscono ogni casella di testo sono separati da punti e virgola. Normalmente le caselle di testo vengono impostate in set di 1, 2, 3 o 6 rettangoli su una forma.

*Attributo standard la*

**Esempio**

Una casella di testo di 95 unità per 95 unità è definita e posizionata 5 unità all'interno dell'angolo superiore sinistro della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 