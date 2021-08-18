---
description: Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847a2925f2249c741e9a45a1dcc4826a1cbe3d6bb12cda4d8017ee0fb5de0069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973140"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>Attributo MFT \_ DECODER \_ FINAL VIDEO RESOLUTION \_ \_ \_ HINT

Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo è supportato da alcuni decodificatori video. Un'applicazione può impostare questo attributo per indicare la larghezza e l'altezza dell'immagine dopo l'elaborazione video. Il decodificatore può usare queste informazioni per ottimizzare il processo di decodifica, soprattutto se le dimensioni dell'immagine finale sono molto inferiori alle dimensioni dell'immagine nativa. Ad esempio, il decodificatore potrebbe ignorare un filtro out-of-loop.

I 32 bit superiori contengono la larghezza e i 32 bit inferiori contengono l'altezza.

Per impostare questo attributo:

1.  Chiamare [**IMFTransform::GetAttributes sul**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) decodificatore per ottenere un [**puntatore IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Chiamare [**MFSetAttributeSize per**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) aggiungere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




