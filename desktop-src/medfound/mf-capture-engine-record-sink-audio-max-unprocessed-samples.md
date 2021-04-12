---
description: Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di record.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Attributo MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344581"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>\_Attributo degli \_ \_ esempi non \_ \_ \_ \_ elaborati dell'audio \_ di acquisizione del motore di acquisizione MF max

Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di record.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Per configurare questo attributo nel motore di acquisizione, aggiungerlo al parametro *pAttributes* quando si chiama [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Il valore massimo per questo attributo è 100.

Una volta che il record ha memorizzato nel buffer il numero massimo di campioni non elaborati, specificato dal motore di acquisizione record del motore di acquisizione di un numero massimo di campioni \_ \_ \_ \_ \_ \_ \_ non elaborati \_ , Elimina la frequenza dei fotogrammi eliminando gli esempi.

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

 

 




