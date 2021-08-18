---
description: Specifica se il flusso di immagini in un'origine di acquisizione video è indipendente dal flusso video.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52392839c5f196159692bc9c4624cbda67b869471d6737c4cff60c847f890e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956681"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>Attributo \_ MF DEVICESTREAM \_ INDEPENDENT \_ IMAGE \_ STREAM

Specifica se il flusso di immagini in un'origine di acquisizione video è indipendente dal flusso video.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Alcune videocamere USB espongono un flusso che produce immagini fisse. In alcune fotocamere, il flusso di immagini restituisce semplicemente il fotogramma successivo dal flusso video. In altre fotocamere, il flusso di immagini funziona indipendentemente dal flusso video. Se la fotocamera ha un flusso di immagini indipendente, l'origine multimediale per il dispositivo di acquisizione imposta questo attributo su **TRUE** nel flusso dell'immagine.

Per ottenere questo attributo, eseguire le operazioni seguenti:

1.  Eseguire una query sull'origine multimediale per [**l'interfaccia IMFMediaSourceEx.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
2.  Chiamare [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un [**puntatore IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.
3.  Chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere l'attributo.

Questo attributo si applica solo quando [l'attributo \_ MF DEVICESTREAM \_ IMAGE \_ STREAM](mf-devicestream-image-stream.md) è **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




