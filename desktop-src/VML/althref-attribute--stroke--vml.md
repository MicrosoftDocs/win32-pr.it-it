---
title: Attributo AltHRef (Stroke)(VML)
description: Attributo AltHRef (Stroke)(VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cbdbe82330d154675b135f7e9f35869c8f47e25715680d97df05e5511a01e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867442"
---
# <a name="althref-attribute-strokevml"></a>Attributo AltHRef (Stroke)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica un riferimento alternativo per un'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* o:althref=" *expression* ">

**Sintassi dello script**

*element* .althref="*expression*"

*expression* = *elemento*.althref

**Osservazioni:**

Supporta la conservazione dei dati PICT tramite roundtripping HTML. In scrittura HTML, viene salvata la rappresentazione alternativa(ad esempio, i dati PICT originali se il file ha avuto origine da Macintosh). Nella lettura HTML **altHRef** è preferito rispetto a **Src**.

*Microsoft Office Attributo Extensions*

**Esempio**

Il tratto della forma ha un **altHRef** che punta a un file denominato myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 