---
title: Attributo tratteggiato la
description: Attributo tratteggiato la
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118383"
---
# <a name="vml-stroked-attribute"></a>Attributo tratteggiato la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce se il percorso verrà tracciato. Proprietà di lettura/scrittura. [VgTriState](msdn-online-vml-vgtristate.md) .

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* stroked = " *Expression* " >

**Sintassi dello script**

*element* . stroked = "*Expression*"

*espressione* = *elemento*. stroked

**Osservazioni:**

Il valore viene duplicato dall'attributo **on** dell'elemento [Stroke](msdn-online-vml-stroke-element.md) .

*Attributo standard la*

**Esempio**

Il percorso della forma viene tracciato.


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo stroked](/previous-versions/bb264094(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 