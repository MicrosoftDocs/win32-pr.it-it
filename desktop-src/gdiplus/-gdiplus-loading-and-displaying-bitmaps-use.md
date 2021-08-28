---
description: Per visualizzare un'immagine raster (bitmap) sullo schermo, sono necessari un oggetto Image e un oggetto Graphics.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Caricamento e visualizzazione di bitmap
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: db3ec9e1d586a585380123aa01d9553ad1f57f60efb93c28d2d974f54d56b249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115001"
---
# <a name="loading-and-displaying-bitmaps"></a>Caricamento e visualizzazione di bitmap

Vedere anche [l'app di esempio WIC Viewer GDI+.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)

Per visualizzare un'immagine raster (bitmap) sullo schermo, sono necessari un [**oggetto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e un [**oggetto Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Passare il nome di un file (o un puntatore a un flusso) a un **costruttore Image.** Dopo aver creato un **oggetto Image,** passa l'indirizzo di tale oggetto **Image** al **metodo DrawImage** di un **oggetto Graphics.**

L'esempio seguente crea un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) da un file JPEG e quindi disegna l'immagine con l'angolo superiore sinistro in corrispondenza di (60, 10):

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

La figura seguente mostra l'immagine disegnata nella posizione specificata.

![screenshot di una finestra che contiene un'immagine, con un callout per il punto di origine ](images/imageposition1.png)

La [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce metodi di base per caricare e visualizzare immagini raster e immagini vettoriali. La [**classe Bitmap,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) che eredita dalla **classe Image,** fornisce metodi più specializzati per il caricamento, la visualizzazione e la modifica di immagini raster. Ad esempio, è possibile costruire un **oggetto Bitmap** da un handle di icona (HICON).

L'esempio seguente ottiene un handle per un'icona e quindi lo usa per costruire un [**oggetto Bitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) Il codice visualizza l'icona passando l'indirizzo dell'oggetto **Bitmap** al **metodo DrawImage** di un [**oggetto**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics.

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>Vedi anche

[Visualizzatore WIC GDI+app di esempio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
