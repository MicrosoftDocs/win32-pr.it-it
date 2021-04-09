---
title: Attributo elemento FillType di la
description: Attributo elemento FillType di la
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963434"
---
# <a name="vml-filltype-attribute"></a>Attributo elemento FillType di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il tipo di riempimento utilizzato per lo sfondo di un tratto. Proprietà di lettura/scrittura. **VgFillType**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* elemento FillType = " *Expression* " >

**Sintassi dello script**

*element* . elemento FillType = "*Expression*"

*espressione* = *elemento*. elemento FillType

**Osservazioni:**

I possibili valori sono:



| DashStyle | Descrizione                                    |
|-----------|------------------------------------------------|
| Tinta unita     | Il modello di riempimento è a tinta unita. Valore predefinito.      |
| Tile      | L'immagine di riempimento è affiancata.                       |
| Modello   | L'immagine di riempimento viene estesa per formare un modello. |
| Frame     | L'immagine di riempimento diventa un bordo per la forma. |



 

*Attributo standard la*

**Esempio**

Il tratto della forma ha una trama affiancata creata dall'immagine del cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 