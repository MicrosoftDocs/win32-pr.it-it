---
title: Attributo CropLeft di VML
description: Attributo CropLeft di VML
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26112aa969e95c6bfb1ec715024aca9eb17b2dbfc2d7d214fb3679cf7ab77447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754851"
---
# <a name="vml-cropleft-attribute"></a>Attributo CropLeft di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce la percentuale di rimozione dell'immagine dal lato sinistro. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* cropleft=" *expression* ">

**Sintassi dello script**

*element* .cropleft="*expression*"

*expression* = *elemento*.cropleft

**Osservazioni:**

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Si noti che il valore 1 non visualizza alcuna immagine. I valori negativi comporteranno che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato verrà riempito dal colore di riempimento della forma). I valori positivi minori di 1 comportano l'estensione dell'immagine rimanente per adattarla alla forma.

*Attributo standard VML*

**Esempio**

Il 20% dell'immagine verrà rimosso sul lato sinistro e l'immagine rimanente verrà adattata alla forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 