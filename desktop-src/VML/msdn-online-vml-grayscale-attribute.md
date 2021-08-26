---
title: Attributo VML GrayScale
description: Attributo VML GrayScale
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683371e2441ffa93f96dc8f727e4eed293954b1897267db8848aa39ffa497af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099211"
---
# <a name="vml-grayscale-attribute"></a>Attributo VML GrayScale

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se un'immagine verrà visualizzata in modalità scala di grigi. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *elemento* grayscale=" *espressione* ">

**Sintassi dello script**

*element* .grayscale="*expression*"

*expression* = *elemento*.grayscale

**Osservazioni:**

Se **True**, l'immagine verrà visualizzata in scala di grigi anziché a colori. Il valore predefinito è **False**.

Il valore è basato sulla raccomandazione CCIR 709, che favorisce un peso più verde e produce risultati più gradevoli per il colore naturale.

*Attributo VML Standard*

**Esempio**

L'immagine verrà visualizzata in scala di grigi anziché a colori.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 