---
description: Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di record.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5f6d2a2bcd592d5a6991028af90af008a827940903084054933558ed7088c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060831"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>Attributo MF \_ CAPTURE ENGINE RECORD SINK AUDIO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES

Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di record.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Per configurare questo attributo nel motore di acquisizione, aggiungerlo al *parametro pAttributes* quando si chiama [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Il valore massimo per questo attributo è 100.

Dopo che il record ha memorizzato nel buffer il numero massimo di campioni non processati, specificato da MF \_ CAPTURE ENGINE RECORD SINK AUDIO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES, elimina la frequenza dei fotogrammi eliminando i campioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




