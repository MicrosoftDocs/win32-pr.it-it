---
title: Funzione RtmAddRoute (RTM. h)
description: La funzione RtmAddRoute aggiunge una voce di route o aggiorna una voce di route esistente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RAS funzione RtmAddRoute
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301915"
---
# <a name="rtmaddroute-function"></a>RtmAddRoute (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmAddRoute** aggiunge una voce di route o aggiorna una voce di route esistente.

## <a name="syntax"></a>Sintassi


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientHandle* \[ in\]
</dt> <dd>

Handle che identifica il client e, di conseguenza, il protocollo di routing che ha aggiunto o aggiornato la route. Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Route* \[ in\]
</dt> <dd>

Puntatore a una struttura specifica della famiglia di protocolli che specifica la route nuova o aggiornata. I campi seguenti vengono utilizzati da Gestione tabelle di routing per aggiornare la tabella di routing:



| Valore                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_Rete RR**</dt> </dl>                                                     | Specifica il numero di rete di destinazione.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**\_INTERFACEID RR**</dt> </dl>                                     | Specifica l'indice dell'interfaccia tramite la quale è stata ricevuta la route.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**\_NEXTHOPADDRESS RR**</dt> </dl>                         | Specifica l'indirizzo del router di hop successivo.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**\_FAMILYSPECIFICDATA RR**</dt> </dl>         | Specifica i dati specifici della famiglia di protocolli. Sebbene i dati siano trasparenti per Gestione tabelle di routing, vengono considerati quando si confrontano le route per determinare se le informazioni sulla route sono state modificate. I dati vengono inoltre utilizzati per impostare i valori delle metriche indipendenti dal protocollo di routing. Di conseguenza, questi dati vengono utilizzati per determinare il percorso migliore per la rete di destinazione.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**\_PROTOCOLSPECIFICDATA RR**</dt> </dl> | Specifica i dati specifici del protocollo di routing che ha fornito la route.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**\_Timestamp RR**</dt> </dl>                                             | Specifica l'ora di sistema corrente. Questo campo viene impostato da Gestione tabelle di routing.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[ in\]
</dt> <dd>

Specifica il numero di secondi per cui la route specificata deve essere mantenuta nella tabella di routing. Se questo parametro è impostato su infinite, la route viene mantenuta fino a quando non viene eliminata in modo esplicito. Il limite corrente per *TimeToLive* è 2147483 sec (24 + giorni).

</dd> <dt>

*Flag* \[ out\]
</dt> <dd>

Puntatore a una variabile **DWORD** . Il valore di questa variabile viene impostato da Gestione tabelle di routing. Il valore indica il tipo di modifica e le informazioni che sono state restituite nei buffer forniti. Questo parametro è uno dei seguenti.



| Flags                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**\_Nessuna \_ modifica RTM**</dt> </dl>             | L'aggiunta o l'aggiornamento non ha modificato alcun parametro di route significativo oppure la voce della route interessata non è la migliore route tra le voci per la rete di destinazione.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_route RTM \_ aggiunta**</dt> </dl>       | La route è stata aggiunta per la rete di destinazione. Il parametro *CurBestRoute* punta alle informazioni per la route aggiunta.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_route RTM \_ modificata**</dt> </dl> | Almeno uno dei parametri significativi è stato modificato per la migliore route alla rete di destinazione. I parametri significativi sono: <br/> Identificatore di protocollo<br/> Indice dell'interfaccia<br/> Indirizzo hop successivo<br/> Dati specifici della famiglia di protocolli (incluse le metriche di route)<br/> |



 

Il parametro *PrevBestRoute* punta alle informazioni della route come prima della modifica. Il parametro *CurBestRoute* punta alle informazioni sulla route correnti, ovvero dopo la modifica.

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni sulla route migliore correnti, se presenti. Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **null** per questo parametro, non vengono restituite le informazioni relative alla route più recenti.

</dd> <dt>

*PrevBestRoute* \[ out\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni sulla route migliore precedenti, se presenti. Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica un **valore null** per questo parametro, non vengono restituite le informazioni sulla route migliore precedenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei codici seguenti.



| Valore                                                                                                       | Descrizione                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Nessun \_ errore**</dt> </dl>                    | La route è stata aggiunta o aggiornata correttamente.<br/>                 |
| <dl> <dt>**ERRORE \_ handle non valido \_**</dt> </dl>       | Il parametro dell'handle client non è un handle valido.<br/>           |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>    | La struttura di route contiene un parametro non valido.<br/>           |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/> |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl>   | La memoria disponibile non è sufficiente per allocare la voce di route.<br/>    |



 

## <a name="remarks"></a>Commenti

La funzione genera un messaggio di modifica della route se la route migliore a una rete di destinazione è cambiata in seguito a questa operazione. Tuttavia, il messaggio di modifica della route non viene inviato al client che effettua questa chiamata. Al contrario, le informazioni rilevanti vengono restituite direttamente da questa funzione a tale client tramite i parametri *Flags*, *CurBestRoute* e *PrevBestRoute* .

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

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





