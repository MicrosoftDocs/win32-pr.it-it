---
title: Attributo Origin (Fill) (la)
description: Attributo Origin (Fill) (la)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399677"
---
# <a name="origin-attribute-fillvml"></a>Attributo Origin (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il centro di un'immagine di riempimento. Proprietà di lettura/scrittura. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* Origin = " *Expression* " >

**Sintassi dello script**

*element* . Origin = "*Expression*"

*espressione* = *elemento*. Origin

**Osservazioni:**

Specifica un punto relativo all'angolo superiore sinistro dell'immagine; questo punto viene trattato come origine dell'immagine. Il valore predefinito è il centro dell'immagine. Il vettore è una frazione della larghezza e dell'altezza dell'immagine.

*Attributo standard la*

**Esempio**

L'immagine del riempimento viene spostata verso sinistra fino a un punto 50% della larghezza della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 