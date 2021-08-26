---
title: Funzione RtmAddRoute (Rtm.h)
description: La funzione RtmAddRoute aggiunge una voce di route o aggiorna una voce di route esistente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- Funzione RtmAddRoute RAS
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
ms.openlocfilehash: d36b96e94ba2803664e3ff4c4fce6f4f95317c33ce5ab9ccd755c95c8d23fa21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035931"
---
# <a name="rtmaddroute-function"></a>Funzione RtmAddRoute

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **funzione RtmAddRoute** aggiunge una voce di route o aggiorna una voce di route esistente.

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

*ClientHandle* \[ Pollici\]
</dt> <dd>

Handle che identifica il client e quindi il protocollo di routing che ha aggiunto o aggiornato la route. Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Route* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura specifica della famiglia di protocolli che specifica la route nuova o aggiornata. I campi seguenti vengono usati da Gestione tabelle di routing per aggiornare la tabella di routing:



| Valore                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**Rete \_ RR**</dt> </dl>                                                     | Specifica il numero di rete di destinazione.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceID**</dt> </dl>                                     | Specifica l'indice dell'interfaccia tramite cui è stata ricevuta la route.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl>                         | Specifica l'indirizzo del router dell'hop successivo.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**RR \_ FamilySpecificData**</dt> </dl>         | Specifica i dati specifici della famiglia di protocolli. Anche se i dati sono trasparenti per il gestore tabelle di routing, vengono considerati quando si confrontano le route per determinare se le informazioni sulla route sono state modificate. I dati vengono usati anche per impostare i valori delle metriche indipendenti dal protocollo di routing. Di conseguenza, questi dati vengono usati per determinare la route migliore per la rete di destinazione.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**Protocollo \_ RRSpecificData**</dt> </dl> | Specifica i dati specifici del protocollo di routing che ha fornito la route.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**RR \_ TimeStamp**</dt> </dl>                                             | Specifica l'ora di sistema corrente. Questo campo viene impostato dal gestore tabelle di routing.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[ Pollici\]
</dt> <dd>

Specifica il numero di secondi in cui la route specificata deve essere mantenuta nella tabella di routing. Se questo parametro è impostato su INFINITE, la route viene mantenuta fino a quando non viene eliminata in modo esplicito. Il limite corrente per *TimeToLive* è 2147483 sec (più di 24 giorni).

</dd> <dt>

*Flag* \[ Cambio\]
</dt> <dd>

Puntatore a **una variabile DWORD.** Il valore di questa variabile viene impostato dal gestore tabelle di routing. Il valore indica il tipo di modifica e le informazioni restituite nei buffer forniti. Questo parametro è uno dei seguenti.



| Flags                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ NO \_ CHANGE**</dt> </dl>             | L'aggiunta o l'aggiornamento non ha modificato alcun parametro di route significativo oppure la voce di route interessata non è la route migliore tra le voci per la rete di destinazione.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**AGGIUNTA \_ DELLA ROUTE \_ RTM**</dt> </dl>       | La route è stata aggiunta per la rete di destinazione. Il *parametro CurBestRoute* punta alle informazioni per la route aggiunta.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**ROUTE RTM \_ \_ MODIFICATA**</dt> </dl> | Almeno uno dei parametri significativi è stato modificato per la route migliore verso la rete di destinazione. I parametri significativi sono: <br/> Identificatore di protocollo<br/> Indice dell'interfaccia<br/> Indirizzo dell'hop successivo<br/> Dati specifici della famiglia di protocolli (incluse le metriche di route)<br/> |



 

Il *parametro PrevBestRoute* punta alle informazioni sulla route così com'era prima della modifica. Il *parametro CurBestRoute* punta alle informazioni di route correnti (ovvero dopo la modifica).

</dd> <dt>

*CurBestRoute* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni sulla route migliore corrente, se presenti. Il tipo della struttura è specifico della famiglia di protocolli, ad esempio IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **NULL** per questo parametro, le informazioni sulla route migliore corrente non vengono restituite.

</dd> <dt>

*PrevBestRoute* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni precedenti sulla route migliore, se presenti. Il tipo della struttura è specifico della famiglia di protocolli, ad esempio IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **NULL** per questo parametro, le informazioni precedenti sulla route migliore non vengono restituite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei codici seguenti.



| Valore                                                                                                       | Descrizione                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**NESSUN \_ ERRORE**</dt> </dl>                    | La route è stata aggiunta o aggiornata correttamente.<br/>                 |
| <dl> <dt>**ERRORE \_ HANDLE NON \_ VALIDO**</dt> </dl>       | Il parametro dell'handle client non è un handle valido.<br/>           |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>    | La struttura della route contiene un parametro non valido.<br/>           |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/> |
| <dl> <dt>**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**</dt> </dl>   | Memoria insufficiente per allocare la voce di route.<br/>    |



 

## <a name="remarks"></a>Commenti

La funzione genera un messaggio di modifica della route se la route migliore verso una rete di destinazione è stata modificata come risultato di questa operazione. Tuttavia, il messaggio di modifica della route non viene inviato al client che effettua questa chiamata. Le informazioni rilevanti vengono invece restituite direttamente da questa funzione al client tramite i parametri *Flags*, *CurBestRoute* e *PrevBestRoute.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funzioni di Gestione tabelle di routing versione 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





