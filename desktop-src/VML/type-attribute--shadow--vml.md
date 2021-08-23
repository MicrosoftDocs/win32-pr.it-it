---
title: Attributo type (Shadow)(VML)
description: Attributo type (Shadow)(VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90a264cbaf77890e39f10d56103c8acdc84727de21d7f2de9946911b6df41dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513161"
---
# <a name="type-attribute-shadowvml"></a>Attributo type (Shadow)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica il tipo di ombreggiatura. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* type=" *expression* ">

**Sintassi dello script**

*element* .type="*expression*"

*expression* = *elemento*.type

**Osservazioni:**

I possibili valori sono:



| Valore           | Descrizione                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| single          | Ombreggiatura singola. Valore predefinito.                                                                                                                                                                              |
| double          | Doppia ombreggiatura. [Color2](color2-attribute--shadow--vml.md) viene usato per il colore della seconda ombreggiatura e [Offset2](msdn-online-vml-offset2-attribute.md) viene usato per l'offset della seconda ombreggiatura. |
| prospettiva     | Ombreggiatura prospettica.                                                                                                                                                                                |
| shapeRelative   | L'ombreggiatura viene creata in relazione alla forma.                                                                                                                                                         |
| drawingRelative | L'ombreggiatura viene creata rispetto al disegno.                                                                                                                                                       |
| Rilievo          | L'ombreggiatura ha un aspetto in rilievo.                                                                                                                                                                     |



 

**Attributo standard VML**

**Esempio**

Viene creata un'ombreggiatura doppia con la seconda ombreggiatura verde e l'offset di 5 punti verso il basso e a destra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 