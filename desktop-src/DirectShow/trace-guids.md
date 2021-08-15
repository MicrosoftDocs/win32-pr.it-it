---
description: I GUID seguenti vengono usati per la traccia degli eventi in DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID di traccia (PerfStruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 89465996c57e1f1f97f2c101c8dfee99a00219f992a4e68681f76465d21bef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951550"
---
# <a name="trace-guids"></a>GUID di traccia

I GUID seguenti vengono usati per la traccia degli eventi in DirectShow.



| GUID                                                                                                                                                                   | Descrizione                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ AUDIOBREAK**</dt> </dl>    | Evento di interruzione audio. Gli eventi di questo tipo usano la [**struttura PERFINFO \_ DSHOW \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) per i dati degli eventi.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**GUID \_ DSHOW \_ CTL**</dt> </dl>      | DirectShow provider di eventi.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ STREAMTRACE**</dt> </dl> | Evento di streaming generale. Gli eventi di questo tipo usano la struttura [**\_ PERFINFO DSHOW \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) per i dati degli eventi.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ VIDEOREND**</dt> </dl>       | Evento di rendering video. Gli eventi di questo tipo usano la [**struttura \_ \_ AVREND DSHOW PERFINFO**](perfinfo-dshow-avrend.md) per i dati degli eventi.<br/>             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PerfStruct.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Traccia eventi in DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




