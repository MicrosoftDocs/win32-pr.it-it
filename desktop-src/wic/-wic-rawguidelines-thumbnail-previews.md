---
description: Anteprime e anteprime
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Anteprime e anteprime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315940"
---
# <a name="thumbnails-and-previews"></a>Anteprime e anteprime

Windows Vista e la raccolta foto di Windows si basano su Windows Imaging Component (WIC) per eseguire il rendering di anteprime e anteprime veloci delle immagini. Per supportare il rendering rapido di anteprime e anteprime, i codec non ELABORAti devono implementare le interfacce WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) e [**getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) . Per supportare un'esperienza utente reattiva, è consigliabile che queste interfacce restituiscano un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) al chiamante in 200 millisecondi o meno.

Microsoft consiglia vivamente ai proprietari del formato di file non elaborato di generare un'anteprima prerenderizzata e di memorizzarla nella cache del file di immagine. Per un formato nel dispositivo, questa operazione viene in genere eseguita in fase di acquisizione. Tuttavia, le anteprime possono anche essere rigenerate e archiviate nel file di immagine ogni volta che vengono modificate le proprietà dell'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , in caso contrario.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida per WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



