---
title: Attributo Src (ImageData)(VML)
description: Attributo Src (ImageData)(VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688bc1e82afbaf0747a03465c93feb1d760cc60eb441792654ef11ec59cee749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596683"
---
# <a name="src-attribute-imagedatavml"></a>Attributo Src (ImageData)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un'origine per l'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* src=" *expression* ">

**Sintassi dello script**

*element* .src="*expression*"

*expression* = *elemento*.src

**Osservazioni:**

Questo attributo deve essere sempre usato con [l'elemento ImageData](msdn-online-vml-imagedata-element.md) e puntare a dati immagine validi per visualizzare un'immagine. Se questo attributo viene visualizzato [senza HRef](https://www.bing.com/search?q=HRef) [o Title,](title-attribute--imagedata--vml.md)l'immagine è collegata.

*Attributo VML Standard*

**Esempio**

L'origine dell'immagine è un file denominato "kids.jpg".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 