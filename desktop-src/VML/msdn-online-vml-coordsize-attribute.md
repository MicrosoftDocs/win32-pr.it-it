---
title: Attributo VML CoordSize
description: Attributo VML CoordSize
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9ce79507e789c38512e775100aa27eda25dc61d5f2af56f9a677daf04d238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999191"
---
# <a name="vml-coordsize-attribute"></a>Attributo VML CoordSize

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica le unità orizzontali e verticali del rettangolo che delimita una forma. Proprietà di lettura/scrittura. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* coordsize=" *expression* ">

**Sintassi dello script**

*element* .coordsize="*expression*"

*expression* = *elemento*.coordsize

**Osservazioni:**

Se non viene specificato, le dimensioni delle coordinate sono le stesse del rettangolo di selezione della forma.

Si noti che questo attributo è un vettore e che le unità sono relative alla lunghezza e alla larghezza del rettangolo di delimitazione.

Si noti anche che il mapping **tra coordsize** e il rettangolo di selezione può essere reso anisotropo. Assicurarsi che la larghezza e l'altezza  **coordsize** siano uguali  alla larghezza e all'altezza dello stile se non si vuole distorcere la forma. 

Nello scripting, poiché si tratta di un vettore 2D, è possibile accedere separatamente ai valori x e y e determinare il tipo di unità previsto.

*Attributo standard VML*

**Esempio**

La forma è alta 100 punti e larga 100 punti, ma ogni unità orizzontale e verticale nello spazio delle coordinate è 1/10 di punto.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo CoordSize](/previous-versions/bb229665(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 