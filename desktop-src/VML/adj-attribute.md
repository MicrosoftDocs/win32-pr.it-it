---
title: Attributo Adj
description: Attributo Adj
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85869500cc3e9f86e0f48e67f63cfd9e6ed2cff5580caa04994169a9e4b50df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137144"
---
# <a name="adj-attribute"></a>Attributo Adj

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica un valore di rettifica utilizzato per definire i valori per una formula. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* adj=" *expression* ">

**Sintassi dello script**

*element* .adj="*expression*"

*expression* = *elemento*.adj

**Osservazioni:**

**Adj** viene usato per fornire punti regolabili per una formula. Se usato nei tag, **Adj** è una stringa delimitata da virgole con un massimo di 8 valori. Alcuni valori possono essere omessi. Ad esempio, "0,1,2,,4,5,7" sarebbe una stringa valida, ma il quarto e il settimo elemento non avrebbero valori (gli elementi vengono conteggiati a partire da 0).

Per lo scripting, **Adj** usa il tipo di dati [IVgAdjustments.](msdn-online-vml-ivgadjustments-data-type.md)

*Attributo standard VML*

**Vedere anche**

[Formula](msdn-online-vml-formulas-element.md)

**Esempio**

Viene creato un quadrato semplice con modifiche. Prima viene creata la stringa **Adj** per definire otto valori di rettifica. A ogni valore di rettifica viene fatto riferimento da una delle otto formule, con ogni valore di rettifica precetto da un simbolo di numero ( \# ). Infine, un percorso è definito da una stringa che fa riferimento alle formule, con ogni formula precescita dal simbolo "at" (@).


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



[Esempio di attributo Adj](/previous-versions/bb229662(v=vs.85)) (richiede Microsoft Internet Explorer 5 o versione successiva).

 

 