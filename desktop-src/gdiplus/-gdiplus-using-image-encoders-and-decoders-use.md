---
description: Windows GDI+ fornisce la classe Image e la classe Bitmap per l'archiviazione delle immagini in memoria e la modifica delle immagini in memoria.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Uso di codificatori e decodificatori di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3509b8fc48ff8c9ef2c52093a6fd06a4349602c6e904df24cf7e528e9f8e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977281"
---
# <a name="using-image-encoders-and-decoders"></a>Uso di codificatori e decodificatori di immagini

Windows GDI+ fornisce la [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e la [**classe Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) per l'archiviazione delle immagini in memoria e la modifica delle immagini in memoria. GDI+ scrive immagini in file su disco con l'aiuto dei codificatori di immagini e carica le immagini dai file su disco con l'aiuto dei decodificatori di immagini. Un codificatore converte i dati in un **oggetto Image** o **Bitmap** in un formato di file su disco designato. Un decodificatore converte i dati in un file su disco nel formato richiesto dagli oggetti **Image** e **Bitmap.** GDI+ sono disponibili codificatori e decodificatori predefiniti che supportano i tipi di file seguenti:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ include anche decodificatori predefiniti che supportano i tipi di file seguenti:

-   WMF
-   EMF
-   Icona

Gli argomenti seguenti illustrano i codificatori e i decodificatori in modo più dettagliato:

-   [Elenco dei codificatori installati](-gdiplus-listing-installed-encoders-use.md)
-   [Elenco dei decodificatori installati](-gdiplus-listing-installed-decoders-use.md)
-   [Recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Determinazione dei parametri supportati da un codificatore](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Conversione di un'immagine BMP in un'immagine PNG](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Impostazione del livello di compressione JPEG](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Trasformazione di un'immagine JPEG senza perdita di informazioni](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Creazione e salvataggio di un'immagine a più frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Copia di singoli fotogrammi da un'Multiple-Frame predefinita](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



