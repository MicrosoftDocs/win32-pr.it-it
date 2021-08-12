---
title: Attributo VML CoordOrigin
description: Attributo VML CoordOrigin
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf568f2c305108a651d56a891a96890154f9493cbadd80a9c5610414c88f4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601943"
---
# <a name="vml-coordorigin-attribute"></a>Attributo VML CoordOrigin

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Specifica l'origine dell'unità di coordinata del rettangolo che delimita una forma. Proprietà di lettura/scrittura. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* coordorigin=" *espressione* ">

**Sintassi dello script**

*element* .coordorigin="*expression*"

*expression* = *elemento*.coordorigin

**Osservazioni:**

Se non specificato, le coordinate di origine sono (0,0) nell'angolo superiore sinistro del rettangolo di selezione della forma.

Il valore x di **CoordSize** viene aggiunto al valore x di **CoordOrigin** per determinare l'intervallo dei valori orizzontali. Ad esempio, se il valore x di **CoordOrigin** è -100 e il valore x di **CoordSize** è 200, le unità orizzontali saranno da -100 a +100. Se il valore x di **CoordOrigin** è 100 e il valore x di **CoordSize** è 200, le unità orizzontali saranno da 100 a 300, tutte all'interno del rettangolo di selezione. Lo stesso vale per i valori y.

Si noti che questo attributo è un vettore e che le unità sono dello stesso tipo di unità [di CoordSize](msdn-online-vml-coordsize-attribute.md) .

Nello scripting, poiché si tratta di un vettore 2D, è possibile accedere separatamente ai valori x e y e determinare il tipo di unità previsto.

*Attributo standard VML*

**Esempio**

Il centro del rettangolo di selezione sarà l'origine (0,0) del percorso per la forma. Poiché **CoordOrigin** è "-500 -500" e **CoordSize** è "1000 1000", le unità orizzontali e verticali variano da -500 a +500. L'angolo sinistro e superiore del tracciato si trova al centro del rettangolo di selezione definito dai punti sinistro e superiore, come definito da **Stile**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo CoordOrigin](/previous-versions/bb229664(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 