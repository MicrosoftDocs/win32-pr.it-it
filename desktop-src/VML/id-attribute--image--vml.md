---
title: Attributo ID (Image) (la)
description: Attributo ID (Image) (la)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399682"
---
# <a name="id-attribute-imagevml"></a>Attributo ID (Image) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un nome che fornisce un identificatore univoco per un'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* ID = " *Expression* " >

**Sintassi dello script**

*element* . ID = "*Expression*"

*espressione* = *elemento*. ID

**Osservazioni:**

Usare **ID** per fare riferimento a un'immagine specifica. Dopo aver creato un'immagine e avergli assegnato un ID, è possibile usare il nome ID quando si vuole modificare l'immagine.

**Attributo standard la**

**Esempio**

La forma ha un ID **ImageData** denominato "immagine".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 