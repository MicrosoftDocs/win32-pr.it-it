---
title: Attributo VML Bilevel
description: Attributo VML Bilevel
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b84f77777cfa21a5bd5c80cb59e447c5a5ce1da78875cc9bd5ff07548690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602871"
---
# <a name="vml-bilevel-attribute"></a>Attributo VML Bilevel

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se un'immagine verrà visualizzata in bianco e nero. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* bilevel=" *expression* ">

**Sintassi dello script**

*element* .bilevel="*expression*"

*expression* = *elemento*.bilevel

**Osservazioni:**

Se **True,** l'immagine verrà visualizzata con due colori (bianco e nero). Il valore predefinito è **False**. In questo modo viene creato un effetto simile alla posterizzazione.

*Attributo VML Standard*

**Esempio**

L'immagine verrà visualizzata solo in bianco e nero.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 