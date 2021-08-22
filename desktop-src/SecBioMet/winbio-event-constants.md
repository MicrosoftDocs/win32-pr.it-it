---
title: WINBIO_EVENT costanti (Winbio \_ types.h)
description: Specificare i tipi di notifiche degli eventi del provider di servizi da monitorare.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a871022c51a906bd078125ae6aa6aa30c2e97024279f3309ca4ece58c00a88f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910659"
---
# <a name="winbio_event-constants"></a>Costanti DI EVENTO WINBIO \_

Le costanti seguenti possono essere usate nella [**funzione WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) per specificare i tipi di notifiche degli eventi del provider di servizi da monitorare.



| Costante                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**EVENTO WINBIO \_ \_ FP NON \_ RECLAMATO**</dt> </dl>                             | Il sensore ha rilevato un dito che non è stato richiesto dall'applicazione o dalla finestra che ha attualmente lo stato attivo. Il Windows Biometric Framework chiama la funzione di callback per indicare che si è verificato uno scorrimento del dito ma non tenta di identificare l'impronta digitale.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED \_ IDENTIFY**</dt> </dl> | Il sensore ha rilevato un dito che non è stato richiesto dall'applicazione o dalla finestra che ha attualmente lo stato attivo. Il Windows Biometric Framework tenta di identificare l'impronta digitale e passa il risultato di tale processo alla funzione di callback.<br/>                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





