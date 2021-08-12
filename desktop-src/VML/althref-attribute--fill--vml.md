---
title: Attributo AltHRef (fill)(VML)
description: Attributo AltHRef (fill)(VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181f98ace80403668f8f67c6f8412091271fdfcf2abcb5a1320d0685853d92bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603004"
---
# <a name="althref-attribute-fillvml"></a>Attributo AltHRef (fill)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un riferimento alternativo per un'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* o:althref=" *expression* ">

**Sintassi dello script**

*element* .althref="*expression*"

*expression* = *elemento*.althref

**Osservazioni:**

Supporta la conservazione dei dati PICT tramite roundtripping HTML. In scrittura HTML, viene salvata la rappresentazione alternativa (i dati PICT originali se il file ha origine da Apple Macintosh). In lettura **HTML, AltHRef** è preferito rispetto a **Src**.

*Microsoft Office Attributo Extensions*

**Esempio**

Il riempimento della forma ha un **altHRef** che punta a un file denominato myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 