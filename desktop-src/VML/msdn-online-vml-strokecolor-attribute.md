---
title: Attributo StrokeColor di la
description: Attributo StrokeColor di la
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046904"
---
# <a name="vml-strokecolor-attribute"></a>Attributo StrokeColor di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il colore del pennello che traccia il percorso di una forma. Proprietà di lettura/scrittura. [IVgColor](msdn-online-vml-ivgcolor.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* strokecolor = " *Expression* " >

**Sintassi dello script**

*element* . strokecolor = "*Expression*"

*espressione* = *elemento*. StrokeColor

**Osservazioni:**

Il valore viene duplicato dall'attributo **color** dell'elemento [Stroke](msdn-online-vml-stroke-element.md) .

*Attributo standard la*

**Esempio**

Il colore del tratto del rettangolo è rosso.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo StrokeColor](/previous-versions/bb264093(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 