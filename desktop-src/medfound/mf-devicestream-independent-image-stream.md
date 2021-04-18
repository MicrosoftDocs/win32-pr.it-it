---
description: Specifica se il flusso di immagini in un'origine di acquisizione video è indipendente dal flusso video.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Attributo MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309570"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>\_Attributo del \_ \_ flusso immagine indipendente MF DEVICESTREAM \_

Specifica se il flusso di immagini in un'origine di acquisizione video è indipendente dal flusso video.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Alcune fotocamere USB espongono un flusso che produce ancora immagini. In alcune fotocamere, il flusso dell'immagine restituisce semplicemente il frame successivo dal flusso video. In altre fotocamere, il flusso di immagini funziona indipendentemente dal flusso video. Se la fotocamera ha un flusso di immagini indipendente, l'origine multimediale per il dispositivo di acquisizione imposta questo attributo su **true** nel flusso di immagini.

Per ottenere questo attributo, procedere come segue:

1.  Eseguire una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.
3.  Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere l'attributo.

Questo attributo si applica solo quando l'attributo del [ \_ \_ \_ flusso dell'immagine MF DEVICESTREAM](mf-devicestream-image-stream.md) è **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




