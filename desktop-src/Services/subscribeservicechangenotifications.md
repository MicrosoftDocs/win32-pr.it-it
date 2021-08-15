---
description: Sottoscrive le notifiche di modifica dello stato del servizio usando una funzione di callback.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Funzione SubscribeServiceChangeNotifications (Winsvcp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: 83bd7bc3f937794f14cbe1d2877bc53ce7d347a8f45fd4f0ddb3e9d0ee9a52a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888457"
---
# <a name="subscribeservicechangenotifications-function"></a>Funzione SubscribeServiceChangeNotifications

Sottoscrive le notifiche di modifica dello stato del servizio usando una funzione di callback.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hService* \[ Pollici\]
</dt> <dd>

Handle per il servizio o handle di Gestione controllo servizi (SCM) per monitorare le modifiche.

Gli handle ai servizi vengono restituiti [**dalla funzione OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) e [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e devono avere il diritto **di accesso SERVICE QUERY \_ \_ STATUS.** Gli handle per il gestore di controllo del servizio vengono restituiti dalla [**funzione OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) e devono avere il diritto **di accesso SC MANAGER ENUMERATE \_ \_ \_ SERVICE.**

</dd> <dt>

*eEventType* \[ Pollici\]
</dt> <dd>

Specifica il tipo di modifiche dello stato che devono essere segnalate. Questo parametro è impostato su uno dei valori specificati in [**SC \_ EVENT \_ TYPE**](sc-event-type.md). Il comportamento di questa funzione è diverso a seconda del tipo di evento, come indicato di seguito.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_ MODIFICA \_ DEL DATABASE \_ EVENTI**</dt> <dt>0</dt> </dl> | Un servizio è stato aggiunto o eliminato. Il *parametro hService* deve essere un handle per SCM.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_ MODIFICA \_ DELLA PROPRIETÀ \_ DELL'EVENTO**</dt> <dt>1</dt> </dl> | Una o più proprietà del servizio sono state aggiornate. Il *parametro hService* deve essere un handle per il servizio.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_ MODIFICA \_ DELLO STATO \_ DELL'EVENTO**</dt> <dt>2</dt> </dl>       | Lo stato di un servizio è stato modificato. Il *parametro hService* deve essere un handle per il servizio.<br/>              |



 

</dd> <dt>

*pCallback* \[ Pollici\]
</dt> <dd>

Specifica la funzione di callback. Il callback deve essere definito come di tipo **SC \_ NOTIFICATION \_ CALLBACK**. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*pCallbackContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore che rappresenta il contesto per questo callback di notifica.

</dd> <dt>

*pSubscription* \[ Cambio\]
</dt> <dd>

Restituisce un puntatore alla sottoscrizione risultante dalla registrazione del callback di notifica. Il chiamante è responsabile della chiamata [**di UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) per interrompere la ricezione delle notifiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **ERROR \_ SUCCESS**.

Se la funzione ha esito negativo, il valore restituito è uno dei codici [di errore di sistema](/windows/desktop/Debug/system-error-codes).

## <a name="remarks"></a>Commenti

La funzione di callback viene dichiarata come segue:


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



La funzione di callback riceve un puntatore al contesto fornito dal chiamante. Il callback viene richiamato come risultato dell'evento di modifica dello stato del servizio. Quando viene richiamato, il callback viene fornito con una maschera di bit dei valori **SERVICE \_ NOTIFY \_ *XXX*** che indicano il tipo di modifica dello stato del servizio. Quando il callback viene fornito con zero anziché un valore **SERVICE \_ NOTIFY \_ *XXX*** valido, l'applicazione deve verificare cosa è stato modificato.

La funzione di callback non deve bloccare l'esecuzione. Se si prevede che l'esecuzione della funzione di callback richiede tempo, eseguire l'offload del lavoro eseguito nella funzione di callback in un thread separato tramite l'accodamento di un elemento di lavoro a un thread in un pool di thread. Alcuni tipi di lavoro che possono richiedere tempo alla funzione di callback includono l'esecuzione di operazioni di I/O di file, l'attesa di un evento e l'esecuzione di chiamate di procedura remota esterne.

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

[**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

