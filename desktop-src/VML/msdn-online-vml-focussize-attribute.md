---
title: Attributo VmL FocusSize
description: Attributo VmL FocusSize
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322bea9f9d78ff76cd631cc36149939bb5b3db5f87dc9c80e9f2a5100f031c1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099261"
---
# <a name="vml-focussize-attribute"></a>Attributo VmL FocusSize

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce le dimensioni dello stato attivo per i riempimenti radiali. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *elemento* focussize=" *espressione* ">

**Sintassi dello script**

*element* .focussize="*expression*"

*expression* = *elemento*.focussize

**Osservazioni:**

I valori sono frazioni della larghezza e dell'altezza della forma. Il primo è una percentuale di riempimento sul bordo destro della forma e il secondo è una percentuale del riempimento alla fine della forma. Il valore predefinito è 0,0. Un **valore FocusSize** pari a 100%,100% e **focusPosition** pari a 0,0 rende color2 dominare completamente la fusione. Per le blend bilanciate sono consigliati valori di piccole dimensioni di circa il 10%,10%.

*Attributo standard VML*

**Esempio**

Il riempimento radiale creerà una sfumatura che inizia al centro come blu e diventa rossa su tutti e quattro i bordi. Il centro della fusione è definito da **FocusPosition** e le dimensioni del colore iniziale interno sono determinate da **FocusSize**.


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



 

 