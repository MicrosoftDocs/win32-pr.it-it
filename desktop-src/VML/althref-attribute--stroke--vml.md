---
title: Attributo AltHRef (Stroke) (la)
description: Attributo AltHRef (Stroke) (la)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300280"
---
# <a name="althref-attribute-strokevml"></a>Attributo AltHRef (Stroke) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica un riferimento alternativo per un'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* o:althref = " *Expression* " >

**Sintassi dello script**

*element* . althref = "*Expression*"

*espressione* = *elemento*. althref

**Osservazioni:**

Supporta la conservazione dei dati PICT tramite Roundtripping HTML. Nella scrittura HTML la rappresentazione alternativa, ovvero i dati PICT originali se il file proviene da Macintosh, viene salvata. In HTML Read, **AltHRef** è favorito tramite **src**.

*Attributo Microsoft Office Extensions*

**Esempio**

Il tratto della forma ha un **AltHRef** che punta a un file denominato myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 