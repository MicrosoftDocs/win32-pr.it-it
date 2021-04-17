---
title: Attributo ArcSize di la
description: Attributo ArcSize di la
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300022"
---
# <a name="vml-arcsize-attribute"></a>Attributo ArcSize di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la quantità di arrotondamento per un rettangolo arrotondato. Proprietà di lettura/scrittura. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Si applica a**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Sintassi Tag**

<v: *element* arcsize = " *Expression* " >

**Sintassi dello script**

*element* . arcSize = "*Expression*"

*espressione* = *elemento*. arcSize

**Osservazioni:**

Definisce gli angoli arrotondati di un rettangolo arrotondato come percentuale della metà della dimensione minore della lunghezza e della larghezza di un rettangolo. 0% avrebbe gli angoli quadrati e il 100% costituirebbe angoli circolari. Un quadrato con un valore **ArcSize** di 1,0 sarebbe un cerchio. Il valore predefinito è 0,2 (20%).

*Attributo standard la*

**Esempio**

Il rettangolo arrotondato viene disegnato con angoli stretti e arrotondati.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 