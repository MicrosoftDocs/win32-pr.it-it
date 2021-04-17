---
title: ADJ (attributo)
description: ADJ (attributo)
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299983"
---
# <a name="adj-attribute"></a>ADJ (attributo)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica un valore di regolazione utilizzato per definire i valori per una formula. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* ADJ = " *Expression* " >

**Sintassi dello script**

*element* . ADJ = "*Expression*"

*espressione* = *elemento*. ADJ

**Osservazioni:**

**ADJ** viene usato per fornire punti regolabili per una formula. Se usato nei tag, **ADJ** è una stringa delimitata da virgole con un massimo di 8 valori. Alcuni valori possono essere omessi. Ad esempio, "0, 1, 2,, 4, 5,, 7" è una stringa valida, ma il quarto e il settimo elemento non contengono valori (gli elementi vengono conteggiati a partire da 0).

Per gli script, **ADJ** usa il tipo di dati [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .

*Attributo standard la*

**Vedere anche**

[Formula](msdn-online-vml-formulas-element.md)

**Esempio**

Un quadrato semplice viene creato con le regolazioni. Viene creata prima di tutto la stringa **ADJ** per definire otto valori di regolazione. Quindi, a ogni valore di regolazione viene fatto riferimento da una delle otto formule, con ogni valore di regolazione precedute da un simbolo di cancelletto ( \# ). Infine, un percorso è definito da una stringa che fa riferimento alle formule, con ogni formula precedute dal simbolo "chiocciola" (@).


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



[Esempio di attributo ADJ](/previous-versions/bb229662(v=vs.85)) (richiede Microsoft Internet Explorer 5 o versione successiva).

 

 