---
description: Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Attributo MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226530"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>\_ \_ \_ \_ Attributo hint di risoluzione video finale del decodificatore MFT \_

Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo è supportato da alcuni decodificatori video. Un'applicazione può impostare questo attributo per indicare la larghezza e l'altezza dell'immagine dopo l'elaborazione video. Il decodificatore può usare queste informazioni per ottimizzare il processo di decodifica, soprattutto se le dimensioni dell'immagine finale sono molto più piccole delle dimensioni dell'immagine nativa. Ad esempio, il decodificatore potrebbe ignorare un filtro out-of-loop.

I 32 bit superiori contengono la larghezza e i 32 bit inferiori contengono l'altezza.

Per impostare l'attributo:

1.  Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel decodificatore per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chiamare [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) per aggiungere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




