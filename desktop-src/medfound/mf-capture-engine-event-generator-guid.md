---
description: Identifica il componente che ha generato un evento di acquisizione.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88efff7cea540c1fae2c14d44dd7676c4f523b562a66a4c4f4bc4dffea59d5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474469"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>Attributo GUID DEL \_ GENERATORE DI EVENTI del \_ \_ \_ MOTORE \_ DI ACQUISIZIONE MF

Identifica il componente che ha generato un evento di acquisizione.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo viene visualizzato in alcuni eventi del motore di acquisizione. Per ottenere questo attributo, chiamare [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) sull'oggetto evento. L'oggetto evento viene passato all'applicazione tramite il [**metodo IMFCaptureEngineOnEventCallback::OnEvent.**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)

Il valore è un identificatore di interfaccia per il componente che ha generato l'evento. Ad esempio, il **valore IID \_ IMFCapturePreviewSink** indica il sink di anteprima ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). Non tutti gli eventi di acquisizione contengono questo attributo.

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

 

 




