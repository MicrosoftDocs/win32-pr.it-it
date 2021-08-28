---
title: From Attribute (Line)(VML)
description: From Attribute (Line)(VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a8bf41462f698397b193835d08655f8d6acefb2df77b17e035ec170c3c4781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099311"
---
# <a name="from-attribute-linevml"></a>From Attribute (Line)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il punto iniziale di una linea. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Linea](msdn-online-vml-line-element.md)

**Sintassi dei tag**

<v: *element* from=" *expression* ">

**Sintassi dello script**

*element* .from="*expression*"

*expression* = *Elemento*.from

**Osservazioni:**

Definisce il punto iniziale della linea nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è [](msdn-online-vml-units.md) un elemento VML, l'unità predefinita è un pixel (ma è possibile specificare anche in, cm, mm, pt, pc). Il valore predefinito è 0,0.

*Attributo VML Standard*

**Esempio**

La linea inizia in una posizione 10 punti verso il basso e 10 punta a destra dell'angolo superiore sinistro dello spazio padre.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 