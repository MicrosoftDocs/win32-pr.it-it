---
description: Identifica il componente che ha generato un evento di acquisizione.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Attributo MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307980"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>\_ \_ \_ \_ Attributo GUID generatore eventi motore di acquisizione \_ MF

Identifica il componente che ha generato un evento di acquisizione.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo viene visualizzato in alcuni eventi del motore di acquisizione. Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) sull'oggetto evento. L'oggetto evento viene passato all'applicazione tramite il metodo [**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .

Il valore è un identificatore di interfaccia per il componente che ha generato l'evento. Ad esempio, il valore **IID \_ IMFCapturePreviewSink** indica il sink di anteprima ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). Non tutti gli eventi di acquisizione contengono questo attributo.

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

 

 




