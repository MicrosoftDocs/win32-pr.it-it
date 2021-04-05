---
title: LA (attributo Flip)
description: LA (attributo Flip)
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730146"
---
# <a name="vml-flip-attribute"></a>LA (attributo Flip)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Cambia l'orientamento di una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "Flip: *Expression* " >

**Sintassi dello script**

*element* . Style. Flip = "*Expression*"

*espressione* = *element*. Style. Flip

**Osservazioni:**

I possibili valori sono:



| Valore | Descrizione                                           |
|-------|-------------------------------------------------------|
| x     | Capovolge lungo l'asse y, invertendo le coordinate *x*. |
| y     | Capovolge lungo l'asse *x*, invertendo le coordinate y. |
| xy    | Capovolgere gli assi y e *x*.                  |
| YX    | Capovolgere gli assi *x* e *y*.                |



 

*Attributo standard la*

**Vedere anche**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Esempio**

La forma viene capovolta lungo l'asse *y* invertendo le coordinate *x* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Esempio di attributo Flip](/previous-versions/bb229670(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 