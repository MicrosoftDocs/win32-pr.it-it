---
title: To Attribute (Line)(VML)
description: To Attribute (Line)(VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d1e47261daf76103717476a84eea3bed99ddb0b514192df8a74cd0b69572a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654451"
---
# <a name="to-attribute-linevml"></a>To Attribute (Line)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il punto finale di una linea. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Linea](msdn-online-vml-line-element.md)

**Sintassi dei tag**

<v: *element* to=" *expression* ">

**Sintassi dello script**

*element* .to="*expression*"

*expression* = *elemento*.to

**Osservazioni:**

Definisce il punto finale della linea nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è [](msdn-online-vml-units.md) un elemento VML, l'unità predefinita è un pixel (ma è possibile specificare anche in, cm, mm, pt, pc). Il valore predefinito è 10,10.

**Attributo VML Standard**

**Esempio**

La linea termina in corrispondenza di una posizione di 100 punti verso il basso e di 100 punti a destra dell'angolo superiore sinistro dello spazio padre.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 