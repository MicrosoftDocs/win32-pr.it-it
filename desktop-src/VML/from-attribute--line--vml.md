---
title: Attributo from (line) (la)
description: Attributo from (line) (la)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730007"
---
# <a name="from-attribute-linevml"></a>Attributo from (line) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il punto iniziale di una linea. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Linea](msdn-online-vml-line-element.md)

**Sintassi Tag**

<v: *elemento* da = " *Expression* " >

**Sintassi dello script**

*element* . from = "*Expression*"

*espressione* = *elemento*. from

**Osservazioni:**

Definisce il punto iniziale della riga nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC. Il valore predefinito è 0, 0.

*Attributo standard la*

**Esempio**

La riga inizia in una posizione 10 punta verso il basso e 10 punta a destra dell'angolo superiore sinistro dello spazio padre.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 