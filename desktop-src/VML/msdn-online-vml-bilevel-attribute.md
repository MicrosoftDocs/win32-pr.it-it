---
title: Attributo bilevel la
description: Attributo bilevel la
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728311"
---
# <a name="vml-bilevel-attribute"></a>Attributo bilevel la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un'immagine verrà visualizzata in bianco e nero. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* bilevel = " *Expression* " >

**Sintassi dello script**

*element* . bilevel = "*Expression*"

*espressione* = *element*. bilevel

**Osservazioni:**

Se **true**, l'immagine verrà visualizzata utilizzando due colori (nero e bianco). Il valore predefinito è **False**. In questo modo viene creato un effetto simile alla posterzzazione.

*Attributo standard la*

**Esempio**

L'immagine verrà visualizzata solo in bianco e nero.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 