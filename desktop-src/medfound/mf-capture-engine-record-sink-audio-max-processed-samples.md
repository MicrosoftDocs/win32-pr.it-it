---
description: Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di registrazione.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b4478ebecfc873c612e8deb0106cba5462e77cd56d5d818b03d74e88679c8b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245039"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a>ATTRIBUTO MF \_ CAPTURE ENGINE RECORD SINK AUDIO MAX PROCESSED \_ \_ \_ \_ \_ \_ \_ SAMPLES

Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di registrazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Per configurare questo attributo nel motore di acquisizione, aggiungerlo al *parametro pAttributes* quando si chiama [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Il valore massimo per questo attributo è 100.

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

 

 




