---
description: Segnala i metadati e il buffer della maschera per una maschera di segmentazione dello sfondo che distingue tra lo sfondo e il primo piano di un fotogramma video.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK attributo (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691850"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>Attributo MF \_ CAPTURE METADATA FRAME BACKGROUND \_ \_ \_ \_ MASK

Segnala i metadati e il buffer della maschera per una maschera di segmentazione dello sfondo che distingue tra lo sfondo e il primo piano di un fotogramma video.

## <a name="data-type"></a>Tipo di dati

**Blob**

## <a name="remarks"></a>Commenti

I dati contenuti in questo attributo sono una struttura [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) che contiene informazioni sulle dimensioni della maschera di sfondo e sulla copertura del frame da cui viene dedotto, ovvero il frame restituito dal flusso. Contiene anche un buffer contiguo che rappresenta la maschera che l'app che utilizza per definire quali pixel sono considerati parte del primo piano o dello sfondo. Il ridimensionamento e la correlazione delle coordinate dell'immagine della maschera relativa al frame vengono gestiti dall'app che lo utilizza. 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Build 22000t<br/>                          |
| Server minimo supportato<br/> | Windows Build 22000<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 




