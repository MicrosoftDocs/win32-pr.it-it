---
title: Elemento VML Stroke
description: Elemento VML Stroke
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62048227fca074276b825ceedb793eaa9a5d84dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473390"
---
# <a name="vml-stroke-element"></a>Elemento VML Stroke

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un tratto per una forma.

Gli attributi seguenti modificano un tratto.



| Attributo                                                          | Descrizione                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [AltHRef](althref-attribute--stroke--vml.md)                      | Specifica un riferimento alternativo per un tratto.                |
| [Colore](color-attribute--stroke--vml.md)                          | Definisce il colore di un tratto.                                |
| [Color2](color2-attribute--stroke--vml.md)                        | Definisce un secondo colore per un tratto.                          |
| [DashStyle](msdn-online-vml-dashstyle-attribute.md)               | Specifica il punto e il tratteggio per un tratto.              |
| [EndArrow](msdn-online-vml-endarrow-attribute.md)                 | Definisce uno stile della freccia per la fine di un tratto.           |
| [EndArrowLength](msdn-online-vml-endarrowlength-attribute.md)     | Definisce una lunghezza della freccia per la fine di un tratto.          |
| [EndArrowWidth](msdn-online-vml-endarrowwidth-attribute.md)       | Definisce la larghezza della freccia per la fine di un tratto.           |
| [EndCap](msdn-online-vml-endcap-attribute.md)                     | Definisce lo stile della terminazione per la fine di un tratto.                |
| [Elemento FillType](msdn-online-vml-filltype-attribute.md)                 | Definisce il tipo di riempimento utilizzato per lo sfondo di un tratto. |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Definisce l'URL dell'immagine originale per il tratto.         |
| [ID](id-attribute--stroke--vml.md)                                | Definisce un identificatore univoco per il tratto.                   |
| [ImageAlignShape](msdn-online-vml-imagealignshape-attribute.md)   | Determina l'allineamento di un'immagine del tratto.                   |
| [ImageAspect](msdn-online-vml-imageaspect-attribute.md)           | Definisce il modo in cui verranno mantenute le proporzioni dell'immagine del tratto.  |
| [ImageSize](msdn-online-vml-imagesize-attribute.md)               | Definisce le dimensioni dell'immagine per il tratto.                 |
| [JoinStyle](msdn-online-vml-joinstyle-attribute.md)               | Definisce lo stile di join di una polilinea.                         |
| [LineStyle](msdn-online-vml-linestyle-attribute.md)               | Definisce lo stile di linea di un tratto.                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | Definisce la uniformità di una giunzione di un Miter.                      |
| [Sì](on-attribute--stroke--vml.md)                                | Determina se il tratto verrà visualizzato.              |
| [Opacità](opacity-attribute--stroke--vml.md)                      | Definisce la quantità di trasparenza di un tratto.               |
| [Src](src-attribute--stroke--vml.md)                              | Definisce l'immagine di origine da caricare per un riempimento del tratto.           |
| [StartArrow](msdn-online-vml-startarrow-attribute.md)             | Definisce la freccia per l'inizio di un tratto.              |
| [StartArrowLength](msdn-online-vml-startarrowlength-attribute.md) | Definisce la lunghezza della freccia per l'inizio di un tratto.       |
| [StartArrowWidth](msdn-online-vml-startarrowwidth-attribute.md)   | Definisce la larghezza della freccia per l'inizio di un tratto.        |
| [Title](title-attribute--stroke--vml.md)                          | Definisce il titolo di un tratto.                                |
| [Weight](msdn-online-vml-weight-attribute.md)                     | Definisce lo spessore di un tratto.                            |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Il codice seguente illustra come usare l'elemento **Stroke** per modificare una riga.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**esempi**

-   [Esempio di tratto semplice](/previous-versions/bb229466(v=vs.85))
-   [Esempio di immagine Stroke](/previous-versions/bb229468(v=vs.85))

 

 