---
description: I metodi Image::Save e Image::SaveAdd della classe Image ricevono un oggetto EncoderParameters che contiene una matrice di oggetti EncoderParameter.
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Costanti del codificatore di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a47f533a490fe3428964c9e469df6fbe89800f95bfe89daf7bf05d6c49a75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248885"
---
# <a name="image-encoder-constants"></a>Costanti del codificatore di immagini

I [metodi Image::Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) e [Image::SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) della classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ricevono un oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) che contiene una matrice di [**oggetti EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) Ogni **oggetto EncoderParameter** ha un membro dati GUID che specifica la categoria di parametri. Le costanti seguenti, definite in Gdiplusimaging.h, rappresentano GUID che specificano le varie categorie di parametri.

-   EncoderChrominanceTable
-   EncoderColorDepth
-   EncoderColorSpace
-   CodificatoreCompressione
-   EncoderLuminanceTable
-   EncoderQuality
-   EncoderRenderMethod
-   EncoderSaveFlag
-   EncoderScanMethod
-   EncoderTransformation
-   EncoderVersion
-   EncoderImageItems
-   EncoderSaveAsCMYK

 

 
