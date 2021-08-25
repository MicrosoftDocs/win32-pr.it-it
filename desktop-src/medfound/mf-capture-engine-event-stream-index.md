---
description: Identifica il flusso che ha generato un evento di acquisizione.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7e8f5f78c6364c27cc4efc2296e7fd1b79a923b0a10f4dd0242d8157882a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060811"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a>Attributo MF \_ CAPTURE ENGINE EVENT STREAM \_ \_ \_ \_ INDEX

Identifica il flusso che ha generato un evento di acquisizione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

## <a name="remarks"></a>Commenti

Questo attributo viene visualizzato in alcuni eventi del motore di acquisizione. Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32 sull'oggetto**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) evento. L'oggetto evento viene passato all'applicazione tramite il [**metodo IMFCaptureEngineOnEventCallback::OnEvent.**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)

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

[**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




