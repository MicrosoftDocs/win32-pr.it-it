---
title: Attributo BlackLevel di la
description: Attributo BlackLevel di la
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046955"
---
# <a name="vml-blacklevel-attribute"></a>Attributo BlackLevel di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'intensità del nero in un'immagine. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* blacklevel = " *Expression* " >

**Sintassi dello script**

*element* . blacklevel = "*Expression*"

*espressione* = *elemento*. blacklevel

**Osservazioni:**

Consente di modificare il livello di colore in modo che i neri appaiano come veri neri, mentre tutti gli altri colori sono visibili come ombreggiatura sopra il nero. Il valore predefinito è 0. Mentre è consentito un numero compreso tra infinito positivo e negativo, i valori minori di-0,5 vengono visualizzati come tutti i neri e i valori maggiori di 0,5 vengono visualizzati come tutti i bianchi.

*Attributo standard la*

**Esempio**

L'immagine verrà visualizzata con toni molto scuri.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 