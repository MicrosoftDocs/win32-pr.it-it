---
title: Elemento VmL Imagedata
description: Elemento VmL Imagedata
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3a307dd36daf0ff08d2fab7cd9086a3bc07447872cf36cb41972e4aa5a4d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600292"
---
# <a name="vml-imagedata-element"></a>Elemento VmL Imagedata

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un'immagine per una forma.

Gli attributi seguenti modificano un'immagine.



| Attributo                                                          | Descrizione                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | Specifica un riferimento alternativo per un'immagine.                        |
| [Bilevel](msdn-online-vml-bilevel-attribute.md)                   | Determina se un'immagine verrà visualizzata in bianco e nero.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Determina l'intensità del nero in un'immagine.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Definisce il colore nella palata che verrà considerato trasparente. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Definisce la percentuale di rimozione dell'immagine dal lato inferiore.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Definisce la percentuale di rimozione dell'immagine dal lato sinistro.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Definisce la percentuale di rimozione dell'immagine dal lato destro.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Definisce la percentuale di rimozione dell'immagine dal lato superiore.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Determina se verrà rilevato un clic del mouse.                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | Definisce il colore per gli effetti di colore in rilievo.                         |
| [Guadagno](msdn-online-vml-gain-attribute.md)                         | Definisce l'intensità di tutti i colori in un'immagine.                      |
| [Gamma](msdn-online-vml-gamma-attribute.md)                       | Definisce la quantità di contrasto per un'immagine.                          |
| [Grigi](msdn-online-vml-grayscale-attribute.md)               | Determina se un'immagine verrà visualizzata in modalità scala di grigi.          |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Definisce un URL per un'immagine.                                           |
| [ID](id-attribute--image--vml.md)                                 | Definisce un identificatore univoco per un'immagine.                             |
| [Film](msdn-online-vml-movie-attribute.md)                       | Definisce un puntatore a un'immagine del film.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Archivia l'ID OLE di un'immagine.                                        |
| [Src](src-attribute--imagedata--vml.md)                           | Definisce un'origine per l'immagine.                                       |
| [Title](title-attribute--imagedata--vml.md)                       | Definisce il titolo di un'immagine.                                        |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un [elemento Shape.](shape-element--vml.md)

Inoltre, [**l'attributo Src**](src-attribute--imagedata--vml.md) deve puntare a un'immagine.

Di seguito è riportato il codice minimo necessario per produrre un'immagine.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> Nelle versioni non definitiva di VML, questo elemento è stato denominato **Image** .

 

**esempi**

-   [Esempio di ImageData semplice](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Esempio di Dynamic ImageData](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 