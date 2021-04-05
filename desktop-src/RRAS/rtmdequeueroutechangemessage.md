---
title: Funzione RtmDequeueRouteChangeMessage (RTM. h)
description: La funzione RtmDequeueRouteChangeMessage restituisce il successivo messaggio di modifica della route nella coda associata al client specificato.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RAS funzione RtmDequeueRouteChangeMessage
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120243"
---
# <a name="rtmdequeueroutechangemessage-function"></a>RtmDequeueRouteChangeMessage (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmDequeueRouteChangeMessage** restituisce il successivo messaggio di modifica della route nella coda associata al client specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientHandle* \[ in\]
</dt> <dd>

Handle che identifica il client per il quale viene eseguita l'operazione. Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Flag* \[ out\]
</dt> <dd>

Puntatore a una variabile **DWORD** . Il valore di questa variabile viene impostato da Gestione tabelle di routing. Il valore specifica il tipo del messaggio di modifica e le informazioni che sono state restituite nei buffer forniti. Questo parametro è uno dei seguenti.



| Flags                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_route RTM \_ aggiunta**</dt> </dl>       | La prima route è stata aggiunta per una determinata rete di destinazione. Il parametro *CurBestRoute* punta alle informazioni per la route aggiunta.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_route RTM \_ eliminata**</dt> </dl> | L'unica route disponibile per una determinata rete di destinazione è stata eliminata. Il parametro *PrevBestRoute* punta alle informazioni per la route eliminata.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_route RTM \_ modificata**</dt> </dl> | Almeno uno dei parametri significativi è stato modificato per una route migliore a una determinata rete di destinazione. I parametri significativi sono: <br/> Identificatore di protocollo<br/> Indice dell'interfaccia<br/> Indirizzo hop successivo<br/> Dati specifici della famiglia di protocolli (incluse le metriche di route)<br/> |



 

Il parametro *PrevBestRoute* punta alle informazioni della route come prima della modifica. Il parametro *CurBestRoute* punta alle informazioni della route Current (ovvero after-Change).

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni sulla route migliore correnti (se presenti). Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **null** per questo parametro, non vengono restituite le informazioni relative alla route più recenti.

</dd> <dt>

*PrevBestRoute* \[ out\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni sulla route migliore precedenti, se presenti. Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **null** per questo parametro, le informazioni precedenti sulla route migliore non vengono restituite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei codici seguenti.



| Valore                                                                                                       | Descrizione                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Nessun \_ errore**</dt> </dl>                    | Questo messaggio è stato l'ultimo messaggio nella coda del client. L'oggetto evento viene reimpostato.<br/>                                                                                                                                               |
| <dl> <dt>**ERRORE \_ handle non valido \_**</dt> </dl>       | Il parametro *ClientHandle* non è un handle valido o alla registrazione il client non ha fornito un oggetto evento per la notifica dei messaggi di modifica (vedere [**RtmRegisterClient**](rtmregisterclient.md)).<br/>                           |
| <dl> <dt>**\_altri \_ messaggi di errore**</dt> </dl>        | La coda del client contiene messaggi aggiuntivi. Il client deve chiamare nuovamente **RtmDequeueRouteChangeMessage** il prima possibile per consentire a gestione tabelle di routing di liberare le risorse associate ai messaggi in sospeso.<br/> |
| <dl> <dt>**ERRORE \_ nessun \_ messaggio**</dt> </dl>          | La coda del client non contiene messaggi; la chiamata non è stata richiesta. L'evento viene reimpostato.<br/>                                                                                                                                            |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento di gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funzioni di Routing Table Manager versione 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





