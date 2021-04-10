---
title: Attributo size (Fill) (la)
description: Attributo size (Fill) (la)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963146"
---
# <a name="size-attribute-fillvml"></a>Attributo size (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce le dimensioni dell'immagine per il riempimento. Proprietà di lettura/scrittura. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* size = " *Expression* " >

**Sintassi dello script**

*element* . size = "*Expression * * *"**

*espressione* = *element*. size

**Osservazioni:**

Il valore predefinito corrisponde alla dimensione dell'immagine originale. Dimensioni maggiori di shapewill visualizzano una versione ingrandita ma ritagliata dell'immagine.

*Attributo standard la*

**Esempio**

Anche se le dimensioni originali dell'immagine sono 50 per 50 punti, l'immagine verrà visualizzata come immagine 10 per 10 al centro della riempita.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 