---
description: Informazioni sull'uso di immagini, bitmap e metafile. Windows GDI+ fornisce la classe Image per l'uso di immagini raster (bitmap) e immagini vettoriali (metafile).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Uso di immagini, bitmap e metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcb0a4d4bad09a931e62da8fe33e27638fede528ad8b29ec3b49417c7bd6e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466411"
---
# <a name="using-images-bitmaps-and-metafiles"></a>Uso di immagini, bitmap e metafile

Windows GDI+ fornisce la [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) per l'uso di immagini raster (bitmap) e immagini vettoriali (metafile). La [**classe Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e la classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) ereditano entrambe dalla **classe** Image. La **classe Bitmap** espande le funzionalità della classe **Image** fornendo metodi aggiuntivi per il caricamento, il salvataggio e la modifica di immagini raster. La **classe Metafile** espande le funzionalità della classe **Image** fornendo metodi aggiuntivi per la registrazione e l'analisi delle immagini vettoriali.

Gli argomenti seguenti descrivono in modo più dettagliato le classi [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e [**Metafile:**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)

-   [Caricamento e visualizzazione di bitmap](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [Caricamento e visualizzazione di metafile](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [Registrazione di metafile](-gdiplus-recording-metafiles-use.md)
-   [Ritaglio e ridimensionamento di immagini](-gdiplus-cropping-and-scaling-images-use.md)
-   [Rotazione, riflessione e inclinazione delle immagini](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [Uso della modalità di interpolazione per controllare la qualità delle immagini durante il ridimensionamento](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [Creazione di immagini di anteprima](-gdiplus-creating-thumbnail-images-use.md)
-   [Uso di una bitmap memorizzata nella cache per migliorare le prestazioni](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [Miglioramento delle prestazioni evitando il ridimensionamento automatico](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [Lettura e scrittura di metadati](-gdiplus-reading-and-writing-metadata-use.md)

 

 



