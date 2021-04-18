---
description: Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di record.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: Attributo MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d1ce4d649c75106545eb2ff39d4f3ea742e6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526905"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a>\_Attributo degli esempi di record del motore di acquisizione MF \_ \_ \_ \_ \_ Max \_ elaborati \_

Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di record.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Per configurare questo attributo nel motore di acquisizione, aggiungerlo al parametro *pAttributes* quando si chiama [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Il valore massimo per questo attributo è 100.

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

 

 




