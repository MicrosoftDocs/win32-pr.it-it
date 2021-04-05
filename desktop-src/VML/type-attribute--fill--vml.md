---
title: Attributo Type (Fill) (la)
description: Attributo Type (Fill) (la)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728807"
---
# <a name="type-attribute-fillvml"></a>Attributo Type (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina il tipo di riempimento. Proprietà di lettura/scrittura. **VgFillType**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: tipo di *elemento* = " *Expression* " >

**Sintassi dello script**

*element* . Type = "*Expression*"

*espressione* = *element*. Type

**Osservazioni:**

I possibili valori sono:



| Tipo           | Descrizione                                                             |
|----------------|-------------------------------------------------------------------------|
| solido          | Il modello di riempimento è a tinta unita. Valore predefinito.                                     |
| gradiente       | I colori di riempimento vengono combinati in una sfumatura lineare, dal basso verso l'alto. |
| gradientradial | I colori di riempimento vengono combinati in una sfumatura radiale.                    |
| tile           | L'immagine di riempimento è affiancata.                                                |
| pattern        | L'immagine viene usata per creare un modello usando i colori di riempimento.            |
| frame          | L'immagine viene adattata per riempire la forma.                               |



 

**Attributo standard la**

**Esempio**

Viene creato un riempimento in primo piano rosso e sfondo blu usando il modello dell'immagine myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 