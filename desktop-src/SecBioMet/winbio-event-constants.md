---
title: Costanti WINBIO_EVENT (tipi WinBio \_ . h)
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
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517475"
---
# <a name="winbio_event-constants"></a>\_Costanti evento WINBIO

Le costanti seguenti possono essere utilizzate nella funzione [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) per specificare i tipi di notifiche degli eventi del provider di servizi da monitorare.



| Costante                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**\_evento WINBIO \_ FP non \_ recuperato**</dt> </dl>                             | Il sensore ha rilevato una striscia da dito che non è stata richiesta dall'applicazione o dalla finestra che attualmente ha lo stato attivo. Il Windows Biometric Framework chiama la funzione di callback per indicare che si è verificato un dito sfiorato ma non tenta di identificare l'impronta digitale.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**\_identificazione non \_ \_ richiesta FP dell'evento \_ WINBIO**</dt> </dl> | Il sensore ha rilevato una striscia da dito che non è stata richiesta dall'applicazione o dalla finestra che attualmente ha lo stato attivo. Il Windows Biometric Framework tenta di identificare l'impronta digitale e passa il risultato di tale processo alla funzione di callback.<br/>                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





