---
title: Attributo CropLeft di la
description: Attributo CropLeft di la
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff01af761e7177d866b46ed48e5d633506aa63fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223934"
---
# <a name="vml-cropleft-attribute"></a>Attributo CropLeft di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la percentuale di rimozione dell'immagine dal lato sinistro. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* CropLeft = " *Expression* " >

**Sintassi dello script**

*element* . CropLeft = "*Expression*"

*espressione* = *elemento*. CropLeft

**Osservazioni:**

La quantità di ritaglio può variare da-1,0 a 1,0. Il valore predefinito è 0. Si noti che il valore 1 non visualizza alcuna immagine. I valori negativi comportano la compressione dell'immagine verso l'interno dal bordo che viene ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato verrà riempito con il colore di riempimento della forma). I valori positivi minori di 1 comportano l'estensione dell'immagine rimanente per adattarla alla forma.

*Attributo standard la*

**Esempio**

il 20% dell'immagine verrà rimossa sul lato sinistro e l'immagine rimanente verrà allungata per adattarsi alla forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 