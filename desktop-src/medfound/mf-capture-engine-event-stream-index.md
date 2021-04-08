---
description: Identifica il flusso che ha generato un evento di acquisizione.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: Attributo MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880241"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a>\_Attributo di \_ \_ indice del flusso di eventi del motore di \_ acquisizione MF \_

Identifica il flusso che ha generato un evento di acquisizione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

## <a name="remarks"></a>Commenti

Questo attributo viene visualizzato in alcuni eventi del motore di acquisizione. Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) sull'oggetto evento. L'oggetto evento viene passato all'applicazione tramite il metodo [**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .

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

[**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




