---
title: Attributo Control1 di la
description: Attributo Control1 di la
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299824"
---
# <a name="vml-control1-attribute"></a>Attributo Control1 di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il primo punto di controllo di una curva di Bezier. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintassi Tag**

<v: *element* Control1 = " *Expression* " >

**Sintassi dello script**

*element* . Control1 = "*Expression*"

*espressione* = *elemento*. Control1

**Osservazioni:**

Definisce il primo punto di controllo di una curva di Bezier cubica nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC. Il valore predefinito è 10, 10.

*Attributo standard la*

**Esempio**

La curva è sorridente. Inizia a sinistra e termina a destra. I due punti di controllo si trovano lungo il modo in cui è possibile estrarre la curva per dare l'impressione di sorridere.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 