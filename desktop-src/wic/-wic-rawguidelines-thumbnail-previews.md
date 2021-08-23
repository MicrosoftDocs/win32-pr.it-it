---
description: Anteprime e anteprime
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Anteprime e anteprime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 110b0f4da08eaf2b17582dabec1ff7bd6d4f3ab4389c6bcf7654cdb5ca3198a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086884"
---
# <a name="thumbnails-and-previews"></a>Anteprime e anteprime

Windows Vista e il Windows Raccolta foto si basano su Windows Imaging Component (WIC) per eseguire il rendering di anteprime e anteprime veloci delle immagini. Per supportare il rendering rapido delle anteprime e dell'anteprima, i codec RAW devono implementare le interfacce [**WIC GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) e [**GetPreview.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) Per supportare un'esperienza utente reattiva, è consigliabile che queste interfacce restituiranno [**un oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) al chiamante in 200 millisecondi o meno.

Microsoft consiglia vivamente che i proprietari del formato di file RAW generino un'anteprima prerendered e la memorizzano nella cache nel file di immagine. Per un formato nel dispositivo, questa operazione viene in genere eseguita in fase di acquisizione. Tuttavia, le anteprime possono anche essere rigenerate e archiviate nel file di immagine ogni volta che le proprietà dell'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) vengono modificate, se non richiede troppo lavoro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



