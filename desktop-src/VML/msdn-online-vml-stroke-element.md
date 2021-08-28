---
title: Elemento VML Stroke
description: Elemento VML Stroke
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fa3b8293c8d540af47578ac522ff1cde179d8858c4f1e16aa95a0cd6e635e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513211"
---
# <a name="vml-stroke-element"></a>Elemento VML Stroke

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un tratto per una forma.

Gli attributi seguenti modificano un tratto.



| Attributo                                                          | Descrizione                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [AltHRef](althref-attribute--stroke--vml.md)                      | Specifica un riferimento alternativo per un tratto.                |
| [Colore](color-attribute--stroke--vml.md)                          | Definisce il colore di un tratto.                                |
| [Color2](color2-attribute--stroke--vml.md)                        | Definisce un secondo colore per un tratto.                          |
| [Dashstyle](msdn-online-vml-dashstyle-attribute.md)               | Specifica il motivo punto e trattino per un tratto.              |
| [EndArrow](msdn-online-vml-endarrow-attribute.md)                 | Definisce uno stile freccia per la fine di un tratto.           |
| [EndArrowLength](msdn-online-vml-endarrowlength-attribute.md)     | Definisce la lunghezza di una freccia per la fine di un tratto.          |
| [EndArrowWidth](msdn-online-vml-endarrowwidth-attribute.md)       | Definisce lo spessore di una freccia per la fine di un tratto.           |
| [Endcap](msdn-online-vml-endcap-attribute.md)                     | Definisce lo stile dell'estremità per la fine di un tratto.                |
| [FillType](msdn-online-vml-filltype-attribute.md)                 | Definisce il tipo di riempimento usato per lo sfondo di un tratto. |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Definisce l'URL dell'immagine originale per il tratto.         |
| [ID](id-attribute--stroke--vml.md)                                | Definisce un identificatore univoco per il tratto.                   |
| [ImageAlignShape](msdn-online-vml-imagealignshape-attribute.md)   | Determina l'allineamento di un'immagine del tratto.                   |
| [Oggetto ImageAspect](msdn-online-vml-imageaspect-attribute.md)           | Definisce il modo in cui verranno mantenute le proporzioni dell'immagine del tratto.  |
| [Imagesize](msdn-online-vml-imagesize-attribute.md)               | Definisce le dimensioni dell'immagine per il tratto.                 |
| [Stile join](msdn-online-vml-joinstyle-attribute.md)               | Definisce lo stile di join di una polilinea.                         |
| [LineStyle](msdn-online-vml-linestyle-attribute.md)               | Definisce lo stile della linea di un tratto.                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | Definisce la uniformità di un giunzione miter.                      |
| [Sì](on-attribute--stroke--vml.md)                                | Determina se il tratto verrà visualizzato.              |
| [Opacità](opacity-attribute--stroke--vml.md)                      | Definisce la quantità di trasparenza di un tratto.               |
| [Src](src-attribute--stroke--vml.md)                              | Definisce l'immagine di origine da caricare per un riempimento del tratto.           |
| [StartArrow](msdn-online-vml-startarrow-attribute.md)             | Definisce la freccia per l'inizio di un tratto.              |
| [StartArrowLength](msdn-online-vml-startarrowlength-attribute.md) | Definisce la lunghezza dell'indicatore di direzione per l'inizio di un tratto.       |
| [StartArrowWidth](msdn-online-vml-startarrowwidth-attribute.md)   | Definisce lo spessore della freccia per l'inizio di un tratto.        |
| [Title](title-attribute--stroke--vml.md)                          | Definisce il titolo di un tratto.                                |
| [Weight](msdn-online-vml-weight-attribute.md)                     | Definisce lo spessore di un tratto.                            |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un [elemento Shape.](shape-element--vml.md)

Il codice seguente illustra come usare **l'elemento Stroke** per modificare una linea.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**esempi**

-   [Esempio di tratto semplice](/previous-versions/bb229466(v=vs.85))
-   [Esempio di immagine del tratto](/previous-versions/bb229468(v=vs.85))

 

 