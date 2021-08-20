---
title: Attributo VML StrokeColor
description: Attributo VML StrokeColor
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a419813c5bd9db4370320f9f181477013136c70265f4ba1d8572a38ae9e3c473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124234"
---
# <a name="vml-strokecolor-attribute"></a>Attributo VML StrokeColor

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il colore del pennello che traccia il tracciato di una forma. Proprietà di lettura/scrittura. [Oggetto IVgColor.](msdn-online-vml-ivgcolor.md)

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* strokecolor=" *expression* ">

**Sintassi dello script**

*element* .strokecolor="*expression*"

*expression* = *elemento*.strokecolor

**Osservazioni:**

Il valore viene duplicato **dall'attributo Color** dell'elemento [Stroke.](msdn-online-vml-stroke-element.md)

*Attributo VML Standard*

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



[Esempio di attributo StrokeColor](/previous-versions/bb264093(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 