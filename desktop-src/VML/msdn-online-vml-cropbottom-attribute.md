---
title: Attributo VML CropBottom
description: Attributo VML CropBottom
ms.assetid: 9548d0fa-1708-4206-90d8-1d90cb42de87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667e5501f43d55dcc6a489406e4b10397c1a39773fad2fce7dc6f8601bf45024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601954"
---
# <a name="vml-cropbottom-attribute"></a>Attributo VML CropBottom

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la percentuale di rimozione dell'immagine dal lato inferiore. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* cropbottom=" *expression* ">

**Sintassi dello script**

*element* .cropbottom="*expression*"

*expression* = *elemento*.cropbottom

**Osservazioni:**

La quantità di ritaglio può variare da -1,0 a 1,0. Il valore predefinito è 0. Si noti che il valore 1 non visualizza alcuna immagine. I valori negativi comporteranno che l'immagine venga ritagliata verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato verrà riempito dal colore di riempimento della forma). I valori positivi minori di 1 comportano l'estensione dell'immagine rimanente per adattarla alla forma.

Attributo VML Standard

**Esempio**

Non verrà visualizzata alcuna immagine perché l'immagine è ritagliata al 100% dal basso.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropbottom="1" src="kids.jpg"/>
   </v:shape>
```



 

 