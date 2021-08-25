---
description: Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso video del sink di record.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f776dd795103fccf81da4c739b767131a03bf83245c3c79e724274dcb52dc0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956821"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>ATTRIBUTO MF \_ CAPTURE ENGINE RECORD SINK VIDEO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES

Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso video del sink di record.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Per configurare questo attributo nel motore di acquisizione, aggiungerlo al *parametro pAttributes* quando si chiama [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Il valore massimo per questo attributo è 17.

Dopo che il record ha memorizzato nel buffer il numero massimo di campioni non elaborato, specificato da MF \_ CAPTURE ENGINE RECORD SINK VIDEO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES, elimina la frequenza dei fotogrammi eliminando i campioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




