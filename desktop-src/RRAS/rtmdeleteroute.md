---
title: Funzione RtmDeleteRoute (RTM. h)
description: La funzione RtmDeleteRoute Elimina una voce di route.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RAS funzione RtmDeleteRoute
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
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964446"
---
# <a name="rtmdeleteroute-function"></a>RtmDeleteRoute (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmDeleteRoute** Elimina una voce di route.

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

*ClientHandle* \[ in\]
</dt> <dd>

Handle che identifica il client e quindi il protocollo di routing della route aggiunta o aggiornata. Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Route* \[ in\]
</dt> <dd>

Puntatore a una struttura specifica della famiglia di protocolli che specifica la route nuova o aggiornata. I campi seguenti vengono utilizzati da Gestione tabelle di routing per aggiornare la tabella di routing:



| Valore                                                                                                                                                                                                         | Significato                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_Rete RR**</dt> </dl>                             | Specifica il numero di rete di destinazione. <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**\_INTERFACEID RR**</dt> </dl>             | Specifica l'indice dell'interfaccia tramite la quale è stata ricevuta la route.<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**\_NEXTHOPADDRESS RR**</dt> </dl> | Specifica l'indirizzo di rete del router di hop successivo.<br/>                      |



 

</dd> <dt>

*Flag* \[ out\]
</dt> <dd>

Puntatore a un set di flag che indicano il tipo del messaggio di modifica e le informazioni inserite nei buffer specificati. Questo parametro è uno dei valori seguenti.



| Flags                                                                                                                                                                      | Significato                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**\_Nessuna \_ modifica RTM**</dt> </dl>             | L'eliminazione della route non influisce sul percorso migliore per qualsiasi rete di destinazione. In altre parole, un'altra voce rappresenta una route per la stessa rete di destinazione e ha una metrica inferiore.<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_route RTM \_ eliminata**</dt> </dl> | La route eliminata è l'unica route disponibile per una determinata rete di destinazione.<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_route RTM \_ modificata**</dt> </dl> | Una volta eliminata questa route, un'altra route è stata il percorso migliore a una determinata rete di destinazione. *CurBestRoute* punta alle informazioni per la nuova route migliore.<br/>               |



 

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni sulla route migliore correnti, se presenti. Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **null** per questo parametro, non vengono restituite le informazioni relative alla route più recenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito **non è un \_ errore**.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ handle non valido \_**</dt> </dl>       | Il parametro dell'handle client non è un handle valido.<br/>                                          |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>    | La struttura di route a cui fa riferimento il parametro di *Route* contiene un valore del membro.<br/>            |
| <dl> <dt>**ERRORE \_ di \_ tale \_ Route**</dt> </dl>       | Non sono presenti voci nella tabella di routing che corrispondono ai parametri della route specificata.<br/> |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione. <br/>                                 |



 

## <a name="remarks"></a>Commenti

La funzione genera un messaggio di modifica della route se la route migliore a una rete di destinazione è cambiata in seguito all'eliminazione. Tuttavia, il messaggio di modifica della route non viene inviato al client che effettua questa chiamata. Al contrario, le informazioni rilevanti vengono restituite direttamente da questa funzione a tale client.

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

[**RtmAddRoute**](rtmaddroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





