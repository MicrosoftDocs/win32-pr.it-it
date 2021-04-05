---
description: Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso video del sink di record.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: Attributo MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752455"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a>\_Attributo per \_ il \_ \_ \_ \_ numero massimo di \_ campioni elaborati \_ del motore di acquisizione MF video

Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso video del sink di record.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Per configurare questo attributo nel motore di acquisizione, aggiungerlo al parametro *pAttributes* quando si chiama [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Il valore massimo per questo attributo è 17.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




