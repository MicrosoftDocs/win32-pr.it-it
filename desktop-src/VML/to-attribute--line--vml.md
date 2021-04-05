---
title: Per attribuire (riga) (la)
description: Per attribuire (riga) (la)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730130"
---
# <a name="to-attribute-linevml"></a>Per attribuire (riga) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il punto finale di una linea. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Linea](msdn-online-vml-line-element.md)

**Sintassi Tag**

<v: *elemento* a = " *Expression* " >

**Sintassi dello script**

*element* . to = "*Expression*"

*espressione* = *elemento*. to

**Osservazioni:**

Definisce il punto finale della riga nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC. Il valore predefinito è 10, 10.

**Attributo standard la**

**Esempio**

La riga termina in una posizione 100 punta verso il basso e 100 punta a destra dell'angolo superiore sinistro dello spazio padre.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 