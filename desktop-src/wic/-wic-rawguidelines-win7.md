---
description: Requisiti dei codec RAW per Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Requisiti dei codec RAW per Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314448"
---
# <a name="raw-codec-requirements-for-windows-7"></a>Requisiti dei codec RAW per Windows 7

Le funzionalità di codec seguenti sono obbligatorie almeno:

Tutte le funzionalità necessarie per il supporto di Shell e raccolta foto di Windows Vista: anteprima, anteprima e rotazione (permanente). Per impostazione predefinita, l'elaborazione non ELABORAta deve avere le impostazioni appropriate.

Il supporto per i metadati di base (lettura e scrittura), i metadati non EXIF, oltre ai metadati EXIF, deve essere reso permanente all'interno di formati di file non ELABORAti senza usare i file sidecar.

Supporto per l'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Per Windows 7, Windows Imaging Component (WIC) WIC richiede l'implementazione di tutte le interfacce di parametro esposte da [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .

Supporto stato orientamento:

-   è necessario applicare le rotazioni delle immagini di livello 90 usando il metodo [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Le applicazioni e Windows utilizzano questo metodo per ruotare le immagini (e anteprime e anteprime memorizzate nella cache).
-   L'applicazione della rotazione tramite questa API deve anche essere resa permanente dal codec (vedere in precedenza in questo articolo).
-   Le applicazioni possono usare le funzionalità di rotazione dell'API [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , ma il codec non serializza le impostazioni di rotazione sull'API, quindi le rotazioni eseguite con [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) non saranno rese permanente.

Supporto per l'estrazione di anteprime e anteprime ad alta velocità. Se la dimensione massima in pixel dell'anteprima (larghezza o altezza) è inferiore a 1024 pixel, Windows Vista richiederà un rendering per l'anteprima dello schermo:

-   Il metodo [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) deve supportare almeno le modalità [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) e [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) per consentire il rendering più veloce di anteprime e anteprime rispetto alla modalità di qualità completa.
-   Windows chiamerà [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con le dimensioni di risoluzione dello schermo richieste.
-   Le dimensioni di risoluzione dello schermo devono essere supportate nell'API precedente.
-   È richiesta l'elaborazione coerente di immagini di anteprime, anteprime e bit di immagini complete da [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .

Formati pixel HDR (High Dynamic Range).

Stampa XPS (XML Paper Specification).

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

 

 



