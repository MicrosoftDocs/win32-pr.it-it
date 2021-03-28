---
description: Per visualizzare un'immagine raster (bitmap) sullo schermo, sono necessari un oggetto immagine e un oggetto Graphics.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Caricamento e visualizzazione di bitmap
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "104982843"
---
# <a name="loading-and-displaying-bitmaps"></a>Caricamento e visualizzazione di bitmap

Vedere anche l' [app di esempio GDI+ visualizzatore WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).

Per visualizzare un'immagine raster (bitmap) sullo schermo, sono necessari un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Passare il nome di un file (o un puntatore a un flusso) a un costruttore di **immagine** . Dopo aver creato un oggetto **immagine** , passare l'indirizzo dell'oggetto **immagine** al metodo **DrawImage** di un oggetto **Graphics** .

Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) da un file JPEG, quindi viene disegnata l'immagine con l'angolo superiore sinistro in (60, 10):

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

Nella figura seguente viene illustrata l'immagine disegnata nella posizione specificata.

![Screenshot di una finestra che contiene un'immagine, con un callout per il punto di origine ](images/imageposition1.png)

La classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce metodi di base per il caricamento e la visualizzazione di immagini raster e vettoriali. La classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , che eredita dalla classe **Image** , fornisce metodi più specializzati per il caricamento, la visualizzazione e la manipolazione delle immagini raster. È ad esempio possibile costruire un oggetto **bitmap** da un handle di icona (HICON).

Nell'esempio seguente viene ottenuto un handle per un'icona e quindi viene utilizzato tale handle per costruire un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . Il codice Visualizza l'icona passando l'indirizzo dell'oggetto **bitmap** al metodo **DrawImage** di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>Vedi anche

[App di esempio GDI+ visualizzatore WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
