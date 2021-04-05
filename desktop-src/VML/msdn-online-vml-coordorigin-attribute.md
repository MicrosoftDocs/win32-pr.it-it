---
title: Attributo CoordOrigin di la
description: Attributo CoordOrigin di la
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872573"
---
# <a name="vml-coordorigin-attribute"></a>Attributo CoordOrigin di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica l'origine dell'unità di coordinate del rettangolo che delimita una forma. Proprietà di lettura/scrittura. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* coordorigin = " *Expression* " >

**Sintassi dello script**

*element* . coordorigin = "*Expression*"

*espressione* = *elemento*. coordorigin

**Osservazioni:**

Se non specificato, le coordinate di origine sono (0,0) nell'angolo superiore sinistro del rettangolo di delimitazione della forma.

Il valore x di **CoordSize** viene aggiunto al valore x di **CoordOrigin** per determinare l'intervallo dei valori orizzontali. Se, ad esempio, il valore x di **CoordOrigin** è-100 e il valore x di **CoordSize** è 200, le unità orizzontali variano da-100 a + 100. Se il valore x di **CoordOrigin** è 100 e il valore x di **CoordSize** è 200, le unità orizzontali variano da 100 a 300, tutte all'interno del rettangolo di selezione. Lo stesso vale per i valori y.

Si noti che questo attributo è un vettore e che le unità sono dello stesso tipo di unità di [CoordSize](msdn-online-vml-coordsize-attribute.md) .

Durante lo scripting, poiché si tratta di un vettore 2D, è possibile accedere separatamente ai valori x e y e determinare anche il tipo di unità previste.

*Attributo standard la*

**Esempio**

Il centro del rettangolo di delimitazione sarà l'origine (0,0) del percorso per la forma. Poiché **CoordOrigin** è "-500-500" e **CoordSize** è "1000 1000", le unità orizzontali e verticali variano da-500 a + 500. L'angolo sinistro e superiore del tracciato sarà al centro del rettangolo di delimitazione definito dai punti sinistro e superiore, come definito dallo **stile**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo CoordOrigin](/previous-versions/bb229664(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 