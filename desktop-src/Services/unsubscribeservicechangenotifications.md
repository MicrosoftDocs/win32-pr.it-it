---
description: Annulla la sottoscrizione alle notifiche di modifica dello stato del servizio.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Funzione UnsubscribeServiceChangeNotifications (Winsvcp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: 3e37f2b786d32ab9f42738e6a8522c6f4593aa6b21a490a6fdd969233b4a6dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888170"
---
# <a name="unsubscribeservicechangenotifications-function"></a>Funzione UnsubscribeServiceChangeNotifications

Annulla la sottoscrizione alle notifiche di modifica dello stato del servizio. Questa funzione usa le sottoscrizioni restituite [**da SubscribeServiceChangeNotifications.**](subscribeservicechangenotifications.md)

## <a name="syntax"></a>Sintassi


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSubscription* \[ Pollici\]
</dt> <dd>

Puntatore alla sottoscrizione di cui annullare la sottoscrizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

**UnsubscribeServiceChangeNotifications** non restituisce un risultato fino al completamento dei callback in-process in sospeso. Non è quindi possibile chiamare **UnsubscribeServiceChangeNotifications** all'interno del callback senza causare un deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Winsvcp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**Openservice**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




