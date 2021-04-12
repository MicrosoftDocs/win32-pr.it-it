---
title: Attributo MiterLimit di la
description: Attributo MiterLimit di la
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473430"
---
# <a name="vml-miterlimit-attribute"></a>Attributo MiterLimit di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la uniformità del giunto smussato. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* MiterLimit = " *Expression* " >

**Sintassi dello script**

*element* . MiterLimit = "*Expression*"

*espressione* = *elemento*. MiterLimit

**Osservazioni:**

Distanza massima tra il punto interno e il punto esterno di una giunzione. Questo numero è un multiplo dello spessore della linea.

Il valore predefinito è 8.

*Attributo standard la*

**Esempio**

I giunti sulla polilinea sono sgolato con un limite di 10, ovvero 5 volte 2 punti.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 