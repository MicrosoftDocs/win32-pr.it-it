---
title: Attributo TEXTBoxRect di VML
description: Attributo TEXTBoxRect di VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644d4a89effa54a991d04de4c97c4f9d86876a78d86149d9b99c3a8161585b44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597483"
---
# <a name="vml-textboxrect-attribute"></a>Attributo TEXTBoxRect di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce una o più caselle di testo all'interno di una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *elemento* textboxrect=" *expression* ">

**Sintassi dello script**

*element* .textboxrect="*expression*"

*expression* = *elemento*.textboxrect

**Osservazioni:**

Una casella di testo è definita da uno o più set di numeri che specificano (nell'ordine) i punti sinistro, superiore, destro e inferiore del rettangolo. Più set sono delimitati da un punto e virgola. Il valore predefinito è lo stesso valore di dimensione del rettangolo contenitore. Se sono definite più caselle di testo, i set quadrupli delimitati da virgole che definiscono ogni casella di testo sono separati da punti e virgola. In genere le caselle di testo sono in set di 1, 2, 3 o 6 rettangoli in una forma.

*Attributo standard VML*

**Esempio**

Viene definita una casella di testo di 95 unità per 95 unità e posizionata 5 unità all'interno dell'angolo superiore sinistro della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 