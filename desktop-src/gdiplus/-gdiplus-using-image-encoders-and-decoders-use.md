---
description: Windows GDI+ fornisce la classe Image e la classe bitmap per archiviare le immagini in memoria e modificare le immagini in memoria.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Uso di codificatori e decodificatori di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129051"
---
# <a name="using-image-encoders-and-decoders"></a>Uso di codificatori e decodificatori di immagini

Windows GDI+ fornisce la classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e la classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) per archiviare le immagini in memoria e modificare le immagini in memoria. GDI+ scrive immagini sui file su disco con l'ausilio dei codificatori di immagini e carica immagini dai file su disco con l'ausilio di decodificatori di immagini. Un codificatore converte i dati in un oggetto **immagine** o **bitmap** in un formato di file su disco designato. Un decodificatore converte i dati in un file su disco nel formato richiesto dall' **immagine** e dagli oggetti **bitmap** . GDI+ include codificatori e decodificatori incorporati che supportano i tipi di file seguenti:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ dispone inoltre di decodificatori incorporati che supportano i tipi di file seguenti:

-   WMF
-   EMF
-   ICONA

Negli argomenti seguenti vengono illustrati in modo più dettagliato i codificatori e i decodificatori:

-   [Elenco di codificatori installati](-gdiplus-listing-installed-encoders-use.md)
-   [Elenco di decodificatori installati](-gdiplus-listing-installed-decoders-use.md)
-   [Recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Determinazione dei parametri supportati da un codificatore](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Conversione di un'immagine BMP in un'immagine PNG](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Impostazione del livello di compressione JPEG](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Trasformazione di un'immagine JPEG senza perdita di informazioni](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Creazione e salvataggio di un'immagine a più frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Copia di singoli frame da un'immagine Multiple-Frame](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



