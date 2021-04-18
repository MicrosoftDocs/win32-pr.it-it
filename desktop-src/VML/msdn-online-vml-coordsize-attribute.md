---
title: Attributo CoordSize di la
description: Attributo CoordSize di la
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299858"
---
# <a name="vml-coordsize-attribute"></a>Attributo CoordSize di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica le unità orizzontali e verticali del rettangolo che delimita una forma. Proprietà di lettura/scrittura. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* coordsize = " *Expression* " >

**Sintassi dello script**

*element* . coordsize = "*Expression*"

*espressione* = *elemento*. coordsize

**Osservazioni:**

Se non specificato, le dimensioni della coordinata corrispondono al riquadro delimitatore della forma.

Si noti che questo attributo è un vettore e che le unità sono relative alla lunghezza e alla larghezza del rettangolo di delimitazione.

Si noti inoltre che è possibile effettuare il mapping tra **coordsize** e il rettangolo di delimitazione. Assicurarsi che la **larghezza coordsize** e l' **altezza coordsize** corrispondano alla larghezza e all' **altezza** dello **stile** , se non si vuole distorcere la forma.

Durante lo scripting, poiché si tratta di un vettore 2D, è possibile accedere separatamente ai valori x e y e determinare anche il tipo di unità previste.

*Attributo standard la*

**Esempio**

La forma è 100 punti alti e 100 punti di larghezza, ma ogni unità orizzontale e verticale nello spazio delle coordinate è 1/10 di un punto.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo CoordSize](/previous-versions/bb229665(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 