---
title: Attributo CropRight di VML
description: Attributo CropRight di VML
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d695bb3fd9e88c3357343860dcbbff820e5a49a22100d59fe46c502b642e31d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796301"
---
# <a name="vml-cropright-attribute"></a>Attributo CropRight di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce la percentuale di rimozione dell'immagine dal lato destro. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* cropright=" *expression* ">

**Sintassi dello script**

*element* .cropright="*expression*"

*expression* = *elemento*.cropright

**Osservazioni:**

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Si noti che il valore 1 non visualizza alcuna immagine. I valori negativi comporteranno che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato verrà riempito dal colore di riempimento della forma). I valori positivi minori di 1 comportano l'estensione dell'immagine rimanente per adattarla alla forma.

*Attributo standard VML*

**Esempio**

L'immagine verrà compressa dal lato destro del 20% della larghezza. Lo spazio vuoto tra l'immagine e il bordo destro verrà riempito dal colore di riempimento della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 