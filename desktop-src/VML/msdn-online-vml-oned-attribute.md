---
title: Attributo VML OnEd
description: Attributo VML OnEd
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ef444037a0cd05a7cfbed5a97bb93ed7e8236a9d9f66bf1f7bd77b92b82e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999151"
---
# <a name="vml-oned-attribute"></a>Attributo VML OnEd

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se i punti di controllo aggiuntivi di una forma sono nascosti. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* o:oned=" *espressione* ">

**Osservazioni:**

Nasconde tutti i quadratini di ridimensionamento della forma tranne quelli in alto a sinistra e in basso a destra. gli stessi handle usati per un segmento di linea retta. Il valore predefinito è **False**.

*Microsoft Office Attributo Extensions*

**Esempio**

Tutti i punti di controllo della forma, ad esempio i punti di controllo superiore sinistro e inferiore destro, sono nascosti.


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 