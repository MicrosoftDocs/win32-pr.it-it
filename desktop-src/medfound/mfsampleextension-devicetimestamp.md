---
description: Contiene il timestamp del driver di dispositivo.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: MFSampleExtension_DeviceTimestamp attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3322f295908ae2bbdc095a21ab57ee2e0f2ed10dd2267eaea227b9248ddc226b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241126"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>Attributo DeviceTimestamp MFSampleExtension \_

Contiene il timestamp del driver di dispositivo.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Questo attributo è impostato sugli esempi di supporti creati da un'origine multimediale per un dispositivo di acquisizione. Il valore di questo attributo si trova nel dominio [**MFTIME,**](mftime.md) condividendo un periodo con il tempo del contatore delle prestazioni delle query (QPC) ed è sempre espresso in unità 100ns. Questo attributo è disponibile per i MFT inseriti nella pipeline di acquisizione.

Per ottenere il timestamp relativo all'inizio dello streaming, chiamare il [**metodo IMFSample::GetSampleTime.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Acquisizione audio/video in Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> </dl>

 

 




