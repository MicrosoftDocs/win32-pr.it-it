---
description: La classe Image fornisce metodi di base per il caricamento e la visualizzazione di immagini raster e vettoriali. La classe Metafile, che eredita dalla classe Image, fornisce metodi più specializzati per la registrazione, la visualizzazione e l'analisi di immagini vettoriali.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Caricamento e visualizzazione di metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049470"
---
# <a name="loading-and-displaying-metafiles"></a>Caricamento e visualizzazione di metafile

La classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce metodi di base per il caricamento e la visualizzazione di immagini raster e vettoriali. La classe [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , che eredita dalla classe **Image** , fornisce metodi più specializzati per la registrazione, la visualizzazione e l'analisi di immagini vettoriali.

Per visualizzare un'immagine vettoriale (Metafile) sullo schermo, sono necessari un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Passare il nome di un file (o un puntatore a un flusso) a un costruttore di **immagine** . Dopo aver creato un oggetto **immagine** , passare l'indirizzo dell'oggetto **immagine** al metodo **DrawImage** di un oggetto **Graphics** .

Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) da un file EMF (Enhanced Metafile), quindi viene disegnata l'immagine con l'angolo superiore sinistro in (60, 10):


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



Nella figura seguente viene illustrata l'immagine disegnata nella posizione specificata.

![Screenshot di una finestra che contiene un'immagine e specifica il punto di origine](images/imageposition2.png)

 

 



