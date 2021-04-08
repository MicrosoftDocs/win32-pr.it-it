---
title: Attributo StrokeWeight di la
description: Attributo StrokeWeight di la
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728071"
---
# <a name="vml-strokeweight-attribute"></a>Attributo StrokeWeight di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce lo spessore del pennello che accarezza il percorso di una forma. Proprietà di lettura/scrittura. **VGLength**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* StrokeWeight = " *Expression* " >

**Sintassi dello script**

*element* . StrokeWeight = "*Expression*"

*espressione* = *elemento*. StrokeWeight

**Osservazioni:**

Il valore viene duplicato dall'attributo **Weight** dell'elemento **Stroke** . Se viene specificato un numero, ma non vengono aggiunte unità, l'unità di misura predefinita è Emu. Se non viene specificato alcun valore, il valore predefinito è 1 pixel (1px).

Per gli script, tuttavia, l'unità di misura predefinita è in punti.

*Attributo standard la*

**Vedere anche**

[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [unità](msdn-online-vml-units.md)

**Esempio**

Lo spessore del tratto della forma è 1 punto.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo StrokeWeight](/previous-versions/bb264095(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 