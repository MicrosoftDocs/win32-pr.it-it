---
title: Attributo Size (Fill)(VML)
description: Attributo Size (Fill)(VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26568151961fb2186f8cf49ae25d9f2835665b8fd52a96a4d3a79e954c50ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754146"
---
# <a name="size-attribute-fillvml"></a>Attributo Size (Fill)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce le dimensioni dell'immagine per il riempimento. Proprietà di lettura/scrittura. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* size=" *expression* ">

**Sintassi dello script**

*element* .size="*expression***"**

*expression* = *elemento*.size

**Osservazioni:**

Il valore predefinito è la dimensione dell'immagine originale. Le dimensioni maggiori della forma visualizzano una versione ingrandita ma ritagliata dell'immagine.

*Attributo standard VML*

**Esempio**

Anche se le dimensioni originali dell'immagine sono di 50 per 50 punti, l'immagine verrà visualizzata come immagine 10 per 10 al centro del riempimento.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 