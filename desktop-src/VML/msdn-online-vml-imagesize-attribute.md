---
title: Attributo ImageSize di la
description: Attributo ImageSize di la
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728087"
---
# <a name="vml-imagesize-attribute"></a>Attributo ImageSize di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce le dimensioni dell'immagine per il tratto. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* ImageSize = " *Expression* " >

**Sintassi dello script**

*element* . ImageSize = "*Expression*"

*espressione* = *elemento*. ImageSize

**Osservazioni:**

Il valore predefinito corrisponde alla dimensione dell'immagine.

*Attributo standard la*

**Esempio**

L'immagine del tratto sarà una dimensione di 10 per 10 punti.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 