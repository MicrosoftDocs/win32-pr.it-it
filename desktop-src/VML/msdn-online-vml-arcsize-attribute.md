---
title: Attributo VML ArcSize
description: Attributo VML ArcSize
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715440f56625d16ed5b4386120dbf50588ce861c1ba59772e3ec8f35a077dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755125"
---
# <a name="vml-arcsize-attribute"></a>Attributo VML ArcSize

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la quantità di arrotondamento per un rettangolo arrotondato. Proprietà di lettura/scrittura. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Si applica a**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Sintassi dei tag**

<v: *elemento* arcsize=" *espressione* ">

**Sintassi dello script**

*elemento* .arcSize="*expression*"

*expression* = *elemento*.arcSize

**Osservazioni:**

Definisce gli angoli arrotondati di un rettangolo arrotondato come percentuale della metà della dimensione più piccola della lunghezza e della larghezza di un rettangolo. Lo 0% avrebbe angoli quadrati e il 100% formerebbe angoli circolari. Un quadrato con **valore ArcSize** pari a 1,0 è un cerchio. Il valore predefinito è 0,2 (20%).

*Attributo standard VML*

**Esempio**

Il rettangolo arrotondato viene disegnato con angoli ristretti ma arrotondati.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 