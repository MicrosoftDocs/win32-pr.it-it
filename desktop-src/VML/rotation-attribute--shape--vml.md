---
title: Attributo Rotation (Shape) (la)
description: Attributo Rotation (Shape) (la)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047310"
---
# <a name="rotation-attribute-shapevml"></a>Attributo Rotation (Shape) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'angolo di rotazione di una forma. Proprietà di lettura/scrittura. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "Rotation: *Expression* " >

**Sintassi dello script**

*element* . Rotation = "*Expression*"

*espressione* = *elemento*. Rotation

**Osservazioni:**

Il valore in gradi può essere positivo o negativo e i valori maggiori di 360 vengono modulati in un cerchio di 360 gradi. Gli angoli positivi sono in senso orario. Il valore predefinito è 0.

Si noti che la forma viene riposizionata dopo la rotazione in modo da riflettere le nuove coordinate del rettangolo di delimitazione.

Si noti inoltre che, per gli script, l'attributo di **stile** non viene utilizzato e che la **rotazione** viene considerata come un attributo diretto della forma.

L'attributo **Rotation** è simile all'attributo standard di **rotazione** HTML per gli stili.

*Attributo standard la*

**Vedere anche**

**Esempio**

Il rettangolo verrà inclinato di 45 gradi.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Esempio di attributo Rotation](/previous-versions/bb264091(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 