---
title: Attributo AltHRef (Fill) (la)
description: Attributo AltHRef (Fill) (la)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473446"
---
# <a name="althref-attribute-fillvml"></a>Attributo AltHRef (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un riferimento alternativo per un'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* o:althref = " *Expression* " >

**Sintassi dello script**

*element* . althref = "*Expression*"

*espressione* = *elemento*. althref

**Osservazioni:**

Supporta la conservazione dei dati PICT tramite Roundtripping HTML. Nella scrittura HTML la rappresentazione alternativa, ovvero i dati PICT originali se il file proviene da Apple Macintosh, viene salvata. In HTML Read, **AltHRef** è favorito tramite **src**.

*Attributo Microsoft Office Extensions*

**Esempio**

Il riempimento della forma dispone di un **AltHRef** che punta a un file denominato myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 