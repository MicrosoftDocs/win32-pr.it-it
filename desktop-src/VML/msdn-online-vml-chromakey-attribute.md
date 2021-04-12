---
title: Attributo Chromakey di la
description: Attributo Chromakey di la
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338142"
---
# <a name="vml-chromakey-attribute"></a>Attributo Chromakey di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il valore del colore dell'immagine che verrà considerato trasparente. Proprietà di lettura/scrittura. **VgColor**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* Chromakey = " *Expression* " >

**Sintassi dello script**

*element* . Chromakey = "*Expression*"

*espressione* = *elemento*. Chromakey

**Osservazioni:**

Utilizzare questo attributo per rendere trasparente le parti di un'immagine mediante l'impostazione della trasparenza su un colore specifico. Se, ad esempio, il valore **Chromakey** è **nero**, qualsiasi parte dell'immagine che è nera sarà trasparente e il colore di riempimento verrà visualizzato nella parte dell'immagine.

*Attributo standard la*

**Esempio**

Le aree dell'immagine che sono nere a tinta unita diventeranno trasparenti, consentendo di visualizzare il colore di riempimento verde attraverso tali aree.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 