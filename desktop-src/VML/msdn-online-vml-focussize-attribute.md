---
title: Attributo FocusSize di la
description: Attributo FocusSize di la
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047337"
---
# <a name="vml-focussize-attribute"></a>Attributo FocusSize di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce le dimensioni dello stato attivo per i riempimenti radiali. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* focussize = " *Expression* " >

**Sintassi dello script**

*element* . focussize = "*Expression*"

*espressione* = *elemento*. focussize

**Osservazioni:**

I valori sono frazioni della larghezza e dell'altezza della forma. Il primo è una percentuale del riempimento al bordo destro della forma e la seconda è una percentuale del riempimento nella parte inferiore della forma. Il valore predefinito è 0,0. Un valore **FocusSize** pari a 100%, 100% e un **FocusPosition** di 0, 0 renderebbe il totale di color2 che dominano completamente la Blend. Per le miscele bilanciate è consigliabile utilizzare valori di dimensioni ridotte di circa il 10%.

*Attributo standard la*

**Esempio**

Il riempimento radiale creerà una Blend che inizia al centro come blu e diventa rossa su tutti e quattro i bordi. Il centro della Blend viene definito da **FocusPosition** e la dimensione del colore iniziale interno è determinata da **FocusSize**.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 