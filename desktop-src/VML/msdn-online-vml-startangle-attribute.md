---
title: Attributo StartAngle di la
description: Attributo StartAngle di la
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046989"
---
# <a name="vml-startangle-attribute"></a>Attributo StartAngle di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il punto iniziale dell'arco. Lettura/scrittura. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .

**Si applica a**

[Arc](msdn-online-vml-arc-element.md)

**Sintassi Tag**

<v: *elemento* inpenzoloni = " *Expression* " >

**Sintassi dello script**

*elemento* . inciondolate = "*Expression*"

*espressione* = *elemento*.

**Osservazioni:**

L'arco è definito come tratto tracciato lungo un ovale delimitato dagli attributi di **stile** di una forma. L'inizio del tratto è definito da un angolo misurato da verticale (12 ore) in senso orario. Il valore predefinito è 0 gradi.

Attributo standard la

**Esempio**

L'arco è sorridente. Il punto iniziale si trova in corrispondenza del punto di 90 gradi di un ovale indicato all'interno del rettangolo di delimitazione della forma. Il punto finale si trova in corrispondenza del punto di 270 gradi dell'ovale.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 