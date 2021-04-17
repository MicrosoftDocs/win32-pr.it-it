---
title: Elemento ImageData di la
description: Elemento ImageData di la
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b416a53f97efc8a1f1875eda0e842c4cfbe96bf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299981"
---
# <a name="vml-imagedata-element"></a>Elemento ImageData di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un'immagine per una forma.

Gli attributi seguenti modificano un'immagine.



| Attributo                                                          | Descrizione                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | Specifica un riferimento alternativo per un'immagine.                        |
| [Bilivello](msdn-online-vml-bilevel-attribute.md)                   | Determina se un'immagine viene visualizzata in bianco e nero.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Determina l'intensità del nero in un'immagine.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Definisce il colore in palatte che verrà considerato trasparente. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Definisce la percentuale di rimozione dell'immagine dal lato inferiore.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Definisce la percentuale di rimozione dell'immagine dal lato sinistro.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Definisce la percentuale di rimozione dell'immagine dal lato destro.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Definisce la percentuale di rimozione dell'immagine dal lato superiore.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Determina se verrà rilevato un clic del mouse.                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | Definisce il colore per gli effetti cromatici in rilievo.                         |
| [Ottenere](msdn-online-vml-gain-attribute.md)                         | Definisce l'intensità di tutti i colori in un'immagine.                      |
| [Gamma](msdn-online-vml-gamma-attribute.md)                       | Definisce la quantità di contrasto per un'immagine.                          |
| [Grigi](msdn-online-vml-grayscale-attribute.md)               | Determina se un'immagine viene visualizzata in modalità scala di grigi.          |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Definisce un URL per un'immagine.                                           |
| [ID](id-attribute--image--vml.md)                                 | Definisce un identificatore univoco per un'immagine.                             |
| [Film](msdn-online-vml-movie-attribute.md)                       | Definisce un puntatore a un'immagine di film.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Archivia l'ID OLE di un'immagine.                                        |
| [Src](src-attribute--imagedata--vml.md)                           | Definisce un'origine per l'immagine.                                       |
| [Title](title-attribute--imagedata--vml.md)                       | Definisce il titolo di un'immagine.                                        |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Inoltre, l'attributo [**src**](src-attribute--imagedata--vml.md) deve puntare a un'immagine.

Di seguito è riportato il codice minimo necessario per produrre un'immagine.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> Nelle versioni non definitive di la, questo elemento è stato chiamato **Image** .

 

**esempi**

-   [Esempio di ImageData semplice](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Esempio di ImageData dinamico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 