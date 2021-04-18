---
title: Attributo FillColor di la
description: Attributo FillColor di la
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300401"
---
# <a name="vml-fillcolor-attribute"></a>Attributo FillColor di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il colore del pennello che riempie il percorso chiuso di una forma. Proprietà di lettura/scrittura. [IVgColor](msdn-online-vml-ivgcolor.md) .

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* FillColor = " *Expression* " >

**Sintassi dello script**

*element* . FillColor = "*Expression*"

*espressione* = *elemento*. FillColor

**Osservazioni:**

Il valore **FillColor** viene duplicato dall'attributo **color** dell'elemento **Fill** .

*Attributo standard la*

**Vedere anche**

[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)

**Esempio**

Il colore di riempimento del rettangolo è rosso.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo FillColor](/previous-versions/bb229668(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 