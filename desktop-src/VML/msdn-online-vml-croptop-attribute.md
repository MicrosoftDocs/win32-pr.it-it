---
title: Attributo VML CropTop
description: Attributo VML CropTop
ms.assetid: b54939b6-0505-43b0-bf82-c3df82dc2633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c66351941c789216eb484ee2a25c090d95df0d2c67a60133bbe7ac4cab44a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601508"
---
# <a name="vml-croptop-attribute"></a>Attributo VML CropTop

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la percentuale di rimozione dell'immagine dal lato superiore. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* croptop=" *expression* ">

**Sintassi dello script**

*element* .croptop="*expression*"

*expression* = *elemento*.croptop

**Osservazioni:**

La quantità di ritaglio può variare da -1,0 a 1,0. Il valore predefinito è 0. Si noti che il valore 1 non visualizza alcuna immagine. I valori negativi comporteranno che l'immagine venga ritagliata verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato verrà riempito dal colore di riempimento della forma). I valori positivi minori di 1 comportano l'estensione dell'immagine rimanente per adattarla alla forma.

*Attributo VML Standard*

**Esempio**

L'immagine verrà ritorta in uno sliver stretto nella parte inferiore della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata croptop="-.8" src="kids.jpg"/>
   </v:shape>
```





 

 