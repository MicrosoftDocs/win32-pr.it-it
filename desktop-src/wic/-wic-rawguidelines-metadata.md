---
description: Supporto dei metadati
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Supporto dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315944"
---
# <a name="metadata-support"></a>Supporto dei metadati

I formati RAW devono supportare anche gli scenari di lettura e scrittura dei metadati comuni per le immagini di Windows. Microsoft ha sviluppato un set di provider di metadati nativi per i metadati di file di immagine scambiabili (EXIF), International Press Telecommunications Council (IPTC) ed Extensible Metadata Platform (XMP) attualmente richiamati solo per i contenitori TIFF e JPEG. Se l'immagine non ELABORAta è archiviata in uno di questi formati di contenitore, è consigliabile usare i provider di metadati predefiniti di Windows. Tuttavia, l'autore del codec è responsabile della configurazione corretta. Per i file non ELABORAti non basati su un contenitore TIFF, potrebbe essere necessario implementare i writer EXIF, IPTC o XMP perché i reader e i writer incorporati si aspettano che i dati siano conformi alle specifiche del layout su disco EXIF, IPTC e XMP. Gli autori di codec possono inoltre implementare i propri provider per eventuali metadati personalizzati.

A causa dell'architettura di Windows Imaging Component (WIC), i writer dei metadati possono essere richiamati solo tramite un'istanza di un codificatore di immagini. Pertanto, i proprietari del formato RAW devono creare almeno un codificatore "Stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , anche se la codifica effettiva di pixel in un formato non elaborato non è implementata. L'autore del codec deve richiamare i gestori di metadati appropriati:

-   [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) sia nel decodificatore che nel decodificatore di frame, nel modo appropriato.
-   [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sia nel codificatore che nel codificatore di frame, a seconda dei casi.

Per supportare tutti gli scenari previsti nelle applicazioni di creazione di immagini in Windows Vista, è consigliabile che i fornitori di codec supportino almeno quanto segue:

-   Lettura EXIF
-   Scrittura EXIF parziale (per consentire agli aggiornamenti di acquisire data e ora)
-   Lettura e scrittura XMP (inclusa l'opzione IPTC Core per XMP)
-   Lettura e scrittura di IPTC IIMv4

La maggior parte degli accessi ai metadati (sia di lettura che di scrittura) in Windows Vista viene eseguita tramite l'interfaccia [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) o [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Pertanto, per partecipare all'esperienza dei metadati di Windows Vista, gli autori di codec non ELABORAti devono implementare i metodi [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

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

 

 



