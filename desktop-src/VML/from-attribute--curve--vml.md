---
title: From Attribute (Curve)(VML)
description: From Attribute (Curve)(VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df431e9239f185ce83771f7822fe98e5bf491bd84a1deb7b869df7d3d2f235e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905499"
---
# <a name="from-attribute-curvevml"></a>From Attribute (Curve)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il punto iniziale di una curva. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintassi dei tag**

<v: *element* from=" *expression* ">

**Sintassi dello script**

*element* .from="*expression*"

*expression* = *Elemento*.from

**Osservazioni:**

Definisce il punto iniziale di una curva di Bézier cubica nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è [](msdn-online-vml-units.md) un elemento VML, l'unità predefinita è un pixel (ma è possibile specificare anche in, cm, mm, pt, pc). Il valore predefinito è 0,0.

*Attributo VML Standard*

**Esempio**

La curva è sorridente. Inizia a sinistra e termina a destra. I due punti di controllo si trovano lungo il percorso in modo da strarre la curva verso il basso per dare l'aspetto di uno smile.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 