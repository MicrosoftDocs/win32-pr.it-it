---
description: Supporto per IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Supporto per IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa39aa339a3cd21c7ffa848a5ab1fe2dd6426981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232874"
---
# <a name="support-for-iwicdevelopraw"></a>Supporto per IWICDevelopRaw

Per consentire alle applicazioni di supportare l'elaborazione non ELABORAta, gli autori di codec sono vivamente invitati a implementare tutti i parametri di [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Per Windows 7, Windows Imaging Component (WIC) richiederà il supporto per tutti i [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Se il formato di file non supporta tutti questi parametri, è necessario rivedere il formato del file di immagine.

Per abilitare l'elaborazione non ELABORAta di base nelle applicazioni, i codec devono supportare le regolazioni a esposizione (ExposureCompensationSupport) e il colore, ad esempio KelvinWhitePointSupport e TintSupport. Inoltre, è consigliabile usare l'output per spazi colore e formati pixel specifici. Il supporto per altre rettifiche è naturalmente consigliato ed è necessario per Windows 7.

Il codec RAW deve fornire supporto di base per la rotazione delle immagini e l'anteprima rapida. La rotazione può essere specificata in due modi distinti:

-   Metodo [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Questo metodo imposta l'angolo di rotazione desiderato per l'output delle chiamate successive a [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels).
-   Metodo [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) . Il chiamante può impostare l'opzione dstTransform per indicare l'angolo di rotazione desiderato.

Questi due approcci sono diversi nei modi seguenti:

-   Solo le impostazioni [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) possono essere rese permanente tra le istanze dell'oggetto decodificatore.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) si applica solo a quella particolare chiamata; non esiste alcuna persistenza di alcun tipo.
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) offre un controllo granulare molto più preciso in rotazione. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) è vincolato a incrementi di 90 gradi.

Se la rotazione viene specificata sia in [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) che in [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), l'effetto di rotazione è cumulativo. Se, ad esempio, [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) specifica una rotazione di 25 gradi e [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) specifica una rotazione di 90 gradi, si verificherà quanto segue:

-   Le chiamate a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) devono applicare una rotazione di 25 gradi, ovvero solo la quantità specificata in [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw).
-   Le chiamate a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con una quantità dstTransform di 90 generano una rotazione di 115 gradi (25 + 90).
-   Anche in questo caso, è possibile salvare in modo permanente solo la rotazione di 25 gradi specificata tramite [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) .

In Windows Vista, i metodi [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) e [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) consentono ai chiamanti di ottenere le anteprime e le immagini di anteprima incorporate rispettivamente. Queste sono progettate per restituire anteprime e anteprime precalcolate dal flusso di file di immagine. La generazione di anteprime o anteprime "al volo" comporta una riduzione delle prestazioni in Esplora risorse e nel Visualizzatore foto. Il codec deve inoltre fornire un modo per restituire rapidamente un'immagine di risoluzione dello schermo aggiornata quando gli utenti eseguono il controllo interattivo delle impostazioni di elaborazione.

Le chiamate a [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) determineranno le chiamate successive a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) return (prediligendo velocità o qualità). Inoltre, l'interfaccia IWICBitmapSourceTransform può essere utilizzata per determinare se sottocampionando è necessario e può migliorare le prestazioni quando può essere applicato. La fedeltà dei colori di tutte le immagini deve essere confrontabile. Quando vengono apportate modifiche alle impostazioni di elaborazione, tutti i rendering devono riflettere le modifiche.

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

 

 



