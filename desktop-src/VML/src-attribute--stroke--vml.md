---
title: Attributo src (Stroke) (la)
description: Attributo src (Stroke) (la)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727543"
---
# <a name="src-attribute-strokevml"></a>Attributo src (Stroke) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'immagine di origine da caricare per un riempimento del tratto. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* src = " *Expression* " >

**Sintassi dello script**

*element* . src = "*Expression*"

*espressione* = *elemento*. src

**Osservazioni:**

URL di un'immagine da caricare per le compilazioni di immagini e modelli. Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine. Se questo attributo viene visualizzato da solo, ovvero senza **href** o **title**, l'immagine viene collegata.

*Attributo standard la*

**Esempio**

Il tratto viene creato con l'immagine specificata dal file di cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 