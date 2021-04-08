---
title: Attributo Angle (Fill) (la)
description: Attributo Angle (Fill) (la)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047272"
---
# <a name="angle-attribute-fillvml"></a>Attributo Angle (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'angolo di un riempimento sfumato. Proprietà di lettura/scrittura. [VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* Angle = " *Expression* " >

**Sintassi dello script**

*element* . Angle = "*Expression*"

*espressione* = *elemento*. angolo

**Osservazioni:**

Il vettore di una sfumatura è perpendicolare al vettore della direzione di Blend da un colore a un altro. Il valore predefinito è 0 (zero) gradi, ovvero un vettore orizzontale da sinistra a destra. Gli angoli positivi ruotano la sfumatura in senso antiorario.

*Attributo standard la*

**Esempio**

Il riempimento della forma è costituito da una sfumatura di due colori, in esecuzione da blu a rosso a un angolo di 45 gradi. Il rosso sarà nell'angolo superiore sinistro e blu sarà nell'angolo inferiore destro.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 