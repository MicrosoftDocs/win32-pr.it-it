---
description: Le funzioni seguenti riguardano gli oggetti del tipo di supporto.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Funzioni helper del tipo di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530529"
---
# <a name="media-type-helper-functions"></a>Funzioni helper del tipo di supporto

Le funzioni seguenti riguardano gli oggetti del tipo di supporto.



| Funzione                                                                     | Descrizione                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcola la frequenza dei fotogrammi dalla durata media di un frame video. |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Recupera le dimensioni dell'immagine per un formato video non compresso.            |
| [**MFCompareFullToPartialMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | Confronta un tipo di supporto completo con un tipo di supporto parziale.                   |
| [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | Crea un tipo di supporto vuoto.                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Converte una frequenza di fotogrammi video in una durata del fotogramma.                    |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Recupera lo stride minimo della superficie per un formato video.              |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Esegue una query se un codice FOURCC o un valore **D3DFORMAT** è un formato YUV. |
| [**MFValidateMediaTypeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | Convalida la dimensione di un buffer per un blocco di formato video.              |
| [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | Crea un tipo di supporto che esegue il wrapping di un altro tipo di supporto.                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Conversioni di tipi di supporto](media-type-conversions.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 



