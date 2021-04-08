---
title: Attributo punti la
description: Attributo punti la
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046839"
---
# <a name="vml-points-attribute"></a>Attributo punti la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un set di punti che costituiscono una polilinea. Proprietà di lettura/scrittura. [IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .

**Si applica a**

[Polilinea](msdn-online-vml-polyline-element.md)

**Sintassi Tag**

<v: *elemento* Points = " *Expression* " >

**Sintassi dello script**

*element* . Points = "*Expression * * *"**

*espressione* = *elemento*. Points

**Osservazioni:**

Definisce un set di segmenti di linea retta costituiti da una serie di punti. Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC. Il valore predefinito è "0, 0 10, 10". Si noti che le virgole non sono necessarie, ma rendono più semplice la leggibilità.

*Attributo standard la*

**Esempio**

La polilinea inizia in corrispondenza del punto 10, 10 e termina con 100.100, con i valori in punti.


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 