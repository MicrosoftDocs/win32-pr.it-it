---
description: Annulla la sottoscrizione delle notifiche di modifica dello stato del servizio.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Funzione UnsubscribeServiceChangeNotifications (Winsvcp. h)
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
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883270"
---
# <a name="unsubscribeservicechangenotifications-function"></a>UnsubscribeServiceChangeNotifications (funzione)

Annulla la sottoscrizione delle notifiche di modifica dello stato del servizio. Questa funzione usa le sottoscrizioni restituite da [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).

## <a name="syntax"></a>Sintassi


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSubscription* \[ in\]
</dt> <dd>

Puntatore alla sottoscrizione di cui annullare la sottoscrizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

**UnsubscribeServiceChangeNotifications** non restituisce alcun risultato finché non vengono completate le richiamate in-process. Pertanto, non è possibile chiamare **UnsubscribeServiceChangeNotifications** all'interno del callback senza causare un deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




