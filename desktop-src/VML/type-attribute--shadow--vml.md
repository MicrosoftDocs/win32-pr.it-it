---
title: Attributo Type (Shadow) (la)
description: Attributo Type (Shadow) (la)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399373"
---
# <a name="type-attribute-shadowvml"></a>Attributo Type (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica il tipo di ombreggiatura. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: tipo di *elemento* = " *Expression* " >

**Sintassi dello script**

*element* . Type = "*Expression*"

*espressione* = *element*. Type

**Osservazioni:**

I possibili valori sono:



| Valore           | Descrizione                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| single          | Singola ombreggiatura. Valore predefinito.                                                                                                                                                                              |
| double          | Un'ombreggiatura doppia. [Color2](color2-attribute--shadow--vml.md) viene usato per il colore della seconda ombreggiatura e [Offset2](msdn-online-vml-offset2-attribute.md) viene usato per l'offset della seconda ombreggiatura. |
| prospettiva     | Ombreggiatura della prospettiva.                                                                                                                                                                                |
| shapeRelative   | L'ombreggiatura viene creata in relazione alla forma.                                                                                                                                                         |
| drawingRelative | L'ombreggiatura viene creata in relazione al disegno.                                                                                                                                                       |
| rilievo          | L'ombreggiatura presenta un aspetto in rilievo.                                                                                                                                                                     |



 

**Attributo standard la**

**Esempio**

Viene creata una doppia ombreggiatura con la seconda ombreggiatura verde e l'offset 5 punta verso il basso e verso destra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 