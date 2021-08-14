---
title: Attributo VML Control1
description: Attributo VML Control1
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b4c57a936a2820e5189be78cab119b4455d20af22735a47a66c444f721723f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601934"
---
# <a name="vml-control1-attribute"></a>Attributo VML Control1

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il primo punto di controllo di una curva di Bézier. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintassi dei tag**

<v: *element* control1=" *expression* ">

**Sintassi dello script**

*element* .control1="*expression*"

*expression* = *elemento*.control1

**Osservazioni:**

Definisce il primo punto di controllo di una curva di Bézier cubica nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è [](msdn-online-vml-units.md) un elemento VML, l'unità predefinita è un pixel (ma è possibile specificare anche in, cm, mm, pt, pc). Il valore predefinito è 10,10.

*Attributo VML Standard*

**Esempio**

La curva è sorridente. Inizia a sinistra e termina a destra. I due punti di controllo si trovano lungo il percorso in modo da strarre la curva verso il basso per dare l'aspetto di uno smile.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 