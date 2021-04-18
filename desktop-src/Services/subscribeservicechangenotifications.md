---
description: Sottoscrive le notifiche di modifica dello stato del servizio utilizzando una funzione di callback.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Funzione SubscribeServiceChangeNotifications (Winsvcp. h)
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
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316089"
---
# <a name="subscribeservicechangenotifications-function"></a>SubscribeServiceChangeNotifications (funzione)

Sottoscrive le notifiche di modifica dello stato del servizio utilizzando una funzione di callback.

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

*hService* \[ in\]
</dt> <dd>

Handle per il servizio o un handle per Gestione controllo servizi (SCM) per monitorare le modifiche.

Gli handle ai servizi vengono restituiti dalla funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) e [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e devono avere il diritto di accesso **\_ \_ stato query del servizio** . Gli handle per Gestione controllo servizi vengono restituiti dalla funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) ed è necessario che il **\_ gestore SC \_ enumera \_** il diritto di accesso al servizio.

</dd> <dt>

*eEventType* \[ in\]
</dt> <dd>

Specifica il tipo di modifiche di stato da segnalare. Questo parametro è impostato su uno dei valori specificati nel [**tipo di \_ evento \_ SC**](sc-event-type.md). Il comportamento di questa funzione è diverso a seconda del tipo di evento, come indicato di seguito.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_ \_ \_ Modifica database evento**</dt> <dt>0</dt> </dl> | Un servizio è stato aggiunto o eliminato. Il parametro *hService* deve essere un handle per SCM.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_ \_ \_ Modifica proprietà evento**</dt> <dt>1</dt> </dl> | Una o più proprietà del servizio sono state aggiornate. Il parametro *hService* deve essere un handle per il servizio.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_ \_ \_ Modifica stato evento**</dt> <dt>2</dt> </dl>       | Lo stato di un servizio è stato modificato. Il parametro *hService* deve essere un handle per il servizio.<br/>              |



 

</dd> <dt>

*pCallback* \[ in\]
</dt> <dd>

Specifica la funzione di callback. Il callback deve essere definito come avente un tipo **di \_ \_ callback di notifica SC**. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*pCallbackContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore che rappresenta il contesto per questo callback di notifica.

</dd> <dt>

*pSubscription* \[ out\]
</dt> <dd>

Restituisce un puntatore alla sottoscrizione risultante dalla registrazione del callback di notifica. Il chiamante è responsabile della chiamata di [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) per interrompere la ricezione delle notifiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**.

Se la funzione ha esito negativo, il valore restituito è uno dei [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

## <a name="remarks"></a>Commenti

La funzione di callback viene dichiarata come segue:


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



La funzione di callback riceve un puntatore al contesto fornito dal chiamante. Il callback viene richiamato in seguito all'evento di modifica dello stato del servizio. Quando viene richiamato, il callback viene fornito con una maschera di maschera dei valori del **servizio \_ Notify \_ * xxx*** che indica il tipo di modifica dello stato del servizio. Quando il callback viene fornito con zero invece di un valore valido per il **servizio \_ Notify \_ * xxx***, l'applicazione deve verificare cosa è stato modificato.

La funzione di callback non deve bloccare l'esecuzione. Se si prevede che l'esecuzione della funzione di callback abbia tempo, eseguire l'offload del lavoro eseguito nella funzione di callback in un thread separato tramite l'accodamento di un elemento di lavoro a un thread in un pool di thread. Alcuni tipi di lavoro che possono rendere la funzione di callback possono richiedere tempo, ad esempio l'esecuzione di operazioni di I/O di file, l'attesa di un evento e la creazione di chiamate a procedure remote esterne.

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

[**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

