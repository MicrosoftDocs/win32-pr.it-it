---
title: Attributo FocusPosition di la
description: Attributo FocusPosition di la
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118427"
---
# <a name="vml-focusposition-attribute"></a>Attributo FocusPosition di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il centro di una sfumatura radiale. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* focusposition = " *Expression* " >

**Sintassi dello script**

*element* . focusposition = "*Expression*"

*espressione* = *elemento*. focusposition

**Osservazioni:**

Specifica le sfumature radiali al centro positionfor. Il vettore è una frazione della larghezza e dell'altezza della forma. Il primo è una percentuale del riempimento al bordo sinistro; il secondo è una percentuale del riempimento nella parte superiore. Il valore predefinito è 0,0. Per posizionare un riempimento radiale al centro di una forma, utilizzare il valore del 50%, del 50%.

*Attributo standard la*

**Esempio**

Il riempimento radiale verrà centrato in modo che il blu si avvii al centro e si irradia verso l'esterno, cambiando gradualmente in rosso nel momento in cui raggiunge i bordi esterni e gli angoli.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 