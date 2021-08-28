---
title: Attributo VML Control2
description: Attributo VML Control2
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c0eee9ba861a73ec6d9f0fd07cca22a551c92c5add5498cd0e33522419fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999251"
---
# <a name="vml-control2-attribute"></a>Attributo VML Control2

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il secondo punto di controllo di una curva di Bézier. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintassi dei tag**

<v: *elemento* control2=" *espressione* ">

**Sintassi dello script**

*element* .control2="*expression*"

*expression* = *elemento*.control2

**Osservazioni:**

Definisce il secondo punto di controllo di una curva di Bézier cubica nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento VML, l'unità [predefinita](msdn-online-vml-units.md) è un pixel (ma è possibile specificare anche in, cm, mm, pt, pc). Il valore predefinito è 20.0.

*Attributo standard VML*

**Esempio**

La curva sorride. Inizia a sinistra e termina a destra. I due punti di controllo si trovano lungo la strada in modo da tirare la curva verso il basso per dare l'aspetto di un smile.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 