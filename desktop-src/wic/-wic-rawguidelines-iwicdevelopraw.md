---
description: Supporto per IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Supporto per IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6436eb9d9422da6f5a29c196df10c97014df6beff178bb584b70e45d207dd50d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709731"
---
# <a name="support-for-iwicdevelopraw"></a>Supporto per IWICDevelopRaw

Per consentire alle applicazioni di supportare l'elaborazione RAW, gli autori di codec sono fortemente invitati a implementare tutti i parametri di [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Per Windows 7, Windows Imaging Component (WIC) richiederà il supporto per tutti [**i componenti IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Se il formato di file non supporta tutti questi parametri, è necessario rivedere il formato del file di immagine.

Per abilitare l'elaborazione RAW di base nelle applicazioni, i codec devono supportare le modifiche all'esposizione (ExposureCompensationSupport) e al colore (ad esempio KelvinWhitePointSupport e TintSupport). È inoltre consigliabile eseguire l'output in spazi colori e formati pixel specifici. Il supporto per altre modifiche è ovviamente consigliato ed è necessario per Windows 7.

Il codec RAW deve fornire il supporto di base per la rotazione delle immagini e l'anteprima rapida. La rotazione può essere specificata in due modi distinti:

-   [**Metodo IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) Questo metodo imposta l'angolo di rotazione desiderato per l'output delle chiamate successive [**a CopyPixels.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)
-   [**Metodo IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) Il chiamante può impostare l'opzione dstTransform per indicare l'angolo di rotazione desiderato.

Questi due approcci sono diversi nei modi seguenti:

-   Solo [**le impostazioni IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) possono essere rese persistenti tra le istanze dell'oggetto decodificatore.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) si applica solo a tale chiamata specifica. non esiste alcuna persistenza di alcun tipo.
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) offre un controllo con granularità molto più fine nella rotazione. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) è vincolato a incrementi di 90 gradi.

Se la rotazione viene specificata sia in [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) che [**in IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)l'effetto di rotazione è cumulativo. Ad esempio, se [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) specifica una rotazione di 25 gradi e [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) specifica una rotazione di 90 gradi, si verifica quanto segue:

-   Le chiamate a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) devono applicare una rotazione di 25 gradi, ovvero solo la quantità specificata in [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
-   Le chiamate a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con un valore dstTransform di 90 comportano quindi una rotazione di 115 gradi (25 + 90).
-   Anche in questo caso, solo la rotazione di 25 gradi specificata tramite [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) può essere mantenuta.

In Windows Vista, i [**metodi IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) e [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**i metodi GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) consentono ai chiamanti di ottenere rispettivamente anteprime incorporate e immagini di anteprima. Che hanno lo scopo di restituire anteprime e anteprime precalcolate dal flusso del file di immagine. La generazione di anteprime o anteprime "in tempo reale" comporta una riduzione delle prestazioni in Windows Explorer e Visualizzatore foto. Il codec deve anche fornire un modo per restituire rapidamente un'immagine aggiornata della risoluzione dello schermo quando gli utenti esereranno il controllo interattivo delle impostazioni di elaborazione.

Le chiamate a [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) determineranno le chiamate successive a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) restituiscono (favorendo velocità o qualità). Inoltre, l'interfaccia IWICBitmapSourceTransform può essere usata per determinare se il downsampling è necessario e può aumentare le prestazioni quando può essere applicato. La fedeltà del colore di tutte le immagini deve essere confrontabile. Quando vengono apportate modifiche alle impostazioni di elaborazione, tutti questi rendering devono riflettere le modifiche.

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

 

 



