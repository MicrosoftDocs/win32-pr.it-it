---
title: Attributo flip VML
description: Attributo flip VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5293bdff5ab888b13fdc095038e74fdbcf725bbfb1948a04018fbf5a22c5677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346635"
---
# <a name="vml-flip-attribute"></a>Attributo flip VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Cambia l'orientamento di una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="flip: *expression* ">

**Sintassi dello script**

*element* .style.flip="*expression*"

*expression* = *elemento*.style.flip

**Osservazioni:**

I possibili valori sono:



| Valore | Descrizione                                           |
|-------|-------------------------------------------------------|
| x     | Capovolgere lungo l'asse y, invertendo *le coordinate x.* |
| y     | Capovolgere lungo l'asse *x,* invertendo le coordinate y. |
| xy    | Capovolgere lungo l'asse y e *x.*                  |
| Yx    | Capovolgere *l'asse x* e *y.*                |



 

*Attributo VML Standard*

**Vedere anche**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Esempio**

La forma viene capovolta lungo *l'asse y* invertendo le *coordinate x.*


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Esempio di attributo Flip.](/previous-versions/bb229670(v=vs.85)) Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 