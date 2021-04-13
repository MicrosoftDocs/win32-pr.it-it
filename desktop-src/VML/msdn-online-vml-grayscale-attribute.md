---
title: LA-attributo in scala di grigi
description: LA-attributo in scala di grigi
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399237"
---
# <a name="vml-grayscale-attribute"></a>LA-attributo in scala di grigi

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un'immagine verrà visualizzata in modalità scala di grigi. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *elemento* scala di grigi = " *espressione* " >

**Sintassi dello script**

*element* . scalece = "*Expression*"

*espressione* = *elemento*. scala di grigi

**Osservazioni:**

Se **true**, l'immagine verrà visualizzata in grigio anziché in colore. Il valore predefinito è **False**.

Il valore è basato sulla raccomandazione CCIR 709, che favorisce un peso più verde e produce risultati più soddisfacenti per il colore naturale.

*Attributo standard la*

**Esempio**

L'immagine verrà visualizzata in scala di grigi anziché in colore.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 