---
title: Funzione RtmDeleteRoute (Rtm.h)
description: La funzione RtmDeleteRoute elimina una voce di route.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- Funzione RtmDeleteRoute RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efe2e34345cc335b8214b781da4dce608dddcc4c2f77e80d8c86f76007c2855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073851"
---
# <a name="rtmdeleteroute-function"></a>Funzione RtmDeleteRoute

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **funzione RtmDeleteRoute** elimina una voce di route.

## <a name="syntax"></a>Sintassi


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientHandle* \[ Pollici\]
</dt> <dd>

Handle che identifica il client e quindi il protocollo di routing della route aggiunta o aggiornata. Ottenere questo handle chiamando [**RtmRegisterClient.**](rtmregisterclient.md)

</dd> <dt>

*Route* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura specifica della famiglia di protocolli che specifica la route nuova o aggiornata. I campi seguenti vengono usati dal gestore tabelle di routing per aggiornare la tabella di routing:



| Valore                                                                                                                                                                                                         | Significato                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**Rete \_ RR**</dt> </dl>                             | Specifica il numero di rete di destinazione. <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceID**</dt> </dl>             | Specifica l'indice dell'interfaccia tramite cui è stata ricevuta la route.<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl> | Specifica l'indirizzo di rete del router dell'hop successivo.<br/>                      |



 

</dd> <dt>

*Flag* \[ Cambio\]
</dt> <dd>

Puntatore a un set di flag che indicano il tipo del messaggio di modifica e le informazioni inserite nei buffer forniti. Questo parametro è uno dei valori seguenti.



| Flags                                                                                                                                                                      | Significato                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ NO \_ CHANGE**</dt> </dl>             | L'eliminazione della route non influisce sulla route migliore verso una rete di destinazione. In altre parole, un'altra voce rappresenta una route alla stessa rete di destinazione e ha una metrica inferiore.<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**ROUTE RTM \_ \_ ELIMINATA**</dt> </dl> | La route eliminata era l'unica route disponibile per una particolare rete di destinazione.<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**ROUTE RTM \_ \_ MODIFICATA**</dt> </dl> | Dopo l'eliminazione di questa route, un'altra route è diventata la route migliore per una determinata rete di destinazione. *CurBestRoute* punta alle informazioni per la nuova route migliore.<br/>               |



 

</dd> <dt>

*CurBestRoute* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni correnti sulla route migliore, se presenti. Il tipo della struttura è specifico della famiglia di protocolli, ad esempio IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **NULL per** questo parametro, le informazioni correnti sulla route migliore non vengono restituite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **NO \_ ERROR.**

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ HANDLE NON \_ VALIDO**</dt> </dl>       | Il parametro dell'handle client non è un handle valido.<br/>                                          |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>    | La struttura di route a cui punta il *parametro Route* contiene un valore del membro.<br/>            |
| <dl> <dt>**ERRORE: \_ NESSUNA ROUTE DI QUESTO \_ \_ TIPO**</dt> </dl>       | Nella tabella di routing non sono presenti voci corrispondenti ai parametri della route specificata.<br/> |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione. <br/>                                 |



 

## <a name="remarks"></a>Commenti

La funzione genera un messaggio di modifica della route se la route migliore verso una rete di destinazione è stata modificata in seguito all'eliminazione. Tuttavia, il messaggio di modifica della route non viene inviato al client che effettua questa chiamata. Al contrario, le informazioni rilevanti vengono restituite da questa funzione direttamente a tale client.

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

[**RtmAddRoute**](rtmaddroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





