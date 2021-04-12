---
title: Attributo color2 (Stroke) (la)
description: Attributo color2 (Stroke) (la)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473763"
---
# <a name="color2-attribute-strokevml"></a>Attributo color2 (Stroke) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un secondo colore per i tratti. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* color2 = " *Expression* " >

Sintassi dello script

*element* . color2 = "*Expression*"

*espressione* = *elemento*. color2

**Osservazioni:**

Un secondo colore viene usato quando il tipo di riempimento di un tratto è un modello.

*Attributo standard la*

**Esempio**

Il tratto della forma è un riempimento di pattern in cui il riempimento viene definito dall'immagine di origine, ma lo sfondo trasparente viene definito dal secondo colore.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 