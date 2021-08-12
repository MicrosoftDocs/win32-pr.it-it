---
title: To Attribute (Curve)(VML)
description: To Attribute (Curve)(VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1d2a4c7fd91652ca59707ff00b67a8215d754134bc150402d72e833f249f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596242"
---
# <a name="to-attribute-curvevml"></a>To Attribute (Curve)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce il punto finale di una curva. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintassi dei tag**

<v: *element* to=" *expression* ">

**Sintassi dello script**

*elemento* .to="*expression*"

*expression* = *elemento*.to

**Osservazioni:**

Definisce il punto finale di una curva di Bézier cubica nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento VML, l'unità [predefinita](msdn-online-vml-units.md) è un pixel (ma è possibile specificare anche in, cm, mm, pt, pc). Il valore predefinito è 30,20.

**Attributo standard VML**

**Esempio**

La curva sorride. Inizia a sinistra e termina a destra. I due punti di controllo si trovano lungo la strada in modo da tirare la curva verso il basso per dare l'aspetto di un smile.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 