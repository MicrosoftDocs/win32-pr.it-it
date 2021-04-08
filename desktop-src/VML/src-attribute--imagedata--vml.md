---
title: Attributo src (ImageData) (la)
description: Attributo src (ImageData) (la)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046807"
---
# <a name="src-attribute-imagedatavml"></a>Attributo src (ImageData) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un'origine per l'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* src = " *Expression* " >

**Sintassi dello script**

*element* . src = "*Expression*"

*espressione* = *elemento*. src

**Osservazioni:**

Questo attributo deve essere sempre utilizzato con l'elemento [ImageData](msdn-online-vml-imagedata-element.md) e puntare a dati di immagine validi per un'immagine da visualizzare. Se questo attributo viene visualizzato senza [href](https://www.bing.com/search?q=HRef) o [title](title-attribute--imagedata--vml.md), l'immagine viene collegata.

*Attributo standard la*

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



 

 