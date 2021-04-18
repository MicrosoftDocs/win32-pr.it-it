---
description: I GUID seguenti vengono usati per la traccia eventi in DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID di traccia (PerfStruct. h)
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
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331430"
---
# <a name="trace-guids"></a>GUID di traccia

I GUID seguenti vengono usati per la traccia eventi in DirectShow.



| GUID                                                                                                                                                                   | Descrizione                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ AUDIOBREAK**</dt> </dl>    | Evento di break audio. Per gli eventi di questo tipo viene utilizzata la struttura [**\_ \_ AUDIOBREAK dshow PERFINFO**](perfinfo-dshow-audiobreak.md) per i dati dell'evento.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**\_dshow GUID \_ CTL**</dt> </dl>      | Provider di eventi DirectShow.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ STREAMTRACE**</dt> </dl> | Evento di streaming generale. Per gli eventi di questo tipo viene utilizzata la struttura [**\_ \_ STREAMTRACE dshow PERFINFO**](perfinfo-dshow-streamtrace.md) per i dati dell'evento.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ VIDEOREND**</dt> </dl>       | Evento di rendering video. Per gli eventi di questo tipo viene utilizzata la struttura [**\_ \_ AVREND dshow PERFINFO**](perfinfo-dshow-avrend.md) per i dati dell'evento.<br/>             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PerfStruct. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Traccia eventi in DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




