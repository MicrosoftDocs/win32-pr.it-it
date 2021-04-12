---
title: Attributo CropRight di la
description: Attributo CropRight di la
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21604fb341840847690e9e086386d46f7124908a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473214"
---
# <a name="vml-cropright-attribute"></a>Attributo CropRight di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la percentuale di rimozione dell'immagine dal lato destro. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* CropRight = " *Expression* " >

**Sintassi dello script**

*element* . CropRight = "*Expression*"

*espressione* = *elemento*. CropRight

**Osservazioni:**

La quantità di ritaglio può variare da-1,0 a 1,0. Il valore predefinito è 0. Si noti che il valore 1 non visualizza alcuna immagine. I valori negativi comportano la compressione dell'immagine verso l'interno dal bordo che viene ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato verrà riempito con il colore di riempimento della forma). I valori positivi minori di 1 comportano l'estensione dell'immagine rimanente per adattarla alla forma.

*Attributo standard la*

**Esempio**

L'immagine verrà compressa dal lato destro del 20% della larghezza. Lo spazio vuoto tra l'immagine e il bordo destro sarà riempito dal colore di riempimento della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 