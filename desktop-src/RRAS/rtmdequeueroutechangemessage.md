---
title: Funzione RtmDequeueRouteChangeMessage (Rtm.h)
description: La funzione RtmDequeueRouteChangeMessage restituisce il successivo messaggio di modifica della route nella coda associata al client specificato.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- Funzione RTMDequeueRouteChangeMessage RAS
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
ms.openlocfilehash: 5ad69b711568fd8233a60e829da8fb6fd6ce5f74d3556afa82c721a835b98e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035881"
---
# <a name="rtmdequeueroutechangemessage-function"></a>Funzione RtmDequeueRouteChangeMessage

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **funzione RtmDequeueRouteChangeMessage** restituisce il successivo messaggio di modifica della route nella coda associata al client specificato.

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

*ClientHandle* \[ Pollici\]
</dt> <dd>

Handle che identifica il client per il quale viene eseguita l'operazione. Ottenere questo handle chiamando [**RtmRegisterClient.**](rtmregisterclient.md)

</dd> <dt>

*Flag* \[ Cambio\]
</dt> <dd>

Puntatore a **una variabile DWORD.** Il valore di questa variabile viene impostato dal gestore tabelle di routing. Il valore specifica il tipo del messaggio di modifica e le informazioni restituite nei buffer forniti. Questo parametro è uno dei seguenti.



| Flags                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**ROUTE RTM \_ \_ AGGIUNTA**</dt> </dl>       | La prima route è stata aggiunta per una particolare rete di destinazione. Il *parametro CurBestRoute* punta alle informazioni per la route aggiunta.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**ROUTE RTM \_ \_ ELIMINATA**</dt> </dl> | L'unica route disponibile per una determinata rete di destinazione è stata eliminata. Il *parametro PrevBestRoute* punta alle informazioni per la route eliminata.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**ROUTE RTM \_ \_ MODIFICATA**</dt> </dl> | Almeno uno dei parametri significativi è stato modificato per una route ottimale verso una determinata rete di destinazione. I parametri significativi sono: <br/> Identificatore di protocollo<br/> Indice dell'interfaccia<br/> Indirizzo hop successivo<br/> Dati specifici della famiglia di protocolli (incluse le metriche di route)<br/> |



 

Il *parametro PrevBestRoute* punta alle informazioni sulla route come prima della modifica. Il *parametro CurBestRoute* punta alle informazioni sulla route corrente (ovvero dopo la modifica).

</dd> <dt>

*CurBestRoute* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni correnti sulla route migliore (se presenti). Il tipo della struttura è specifico della famiglia di protocolli, ad esempio IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **NULL per** questo parametro, le informazioni correnti sulla route migliore non vengono restituite.

</dd> <dt>

*PrevBestRoute* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura che riceve le informazioni precedenti sulla route migliore, se presenti. Il tipo della struttura è specifico della famiglia di protocolli, ad esempio IP o IPX.

Questo parametro è facoltativo. Se il chiamante specifica **NULL per** questo parametro, le informazioni precedenti sulla route migliore non vengono restituite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei codici seguenti.



| Valore                                                                                                       | Descrizione                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NESSUN \_ ERRORE**</dt> </dl>                    | Questo è l'ultimo messaggio nella coda del client. L'oggetto evento viene reimpostato.<br/>                                                                                                                                               |
| <dl> <dt>**ERRORE \_ HANDLE NON \_ VALIDO**</dt> </dl>       | Il *parametro ClientHandle* non è un handle valido o al momento della registrazione il client non ha fornito un oggetto evento per la notifica del messaggio di modifica (vedere [**RtmRegisterClient).**](rtmregisterclient.md)<br/>                           |
| <dl> <dt>**ALTRI \_ \_ MESSAGGI DI ERRORE**</dt> </dl>        | La coda del client contiene messaggi aggiuntivi. Il client deve chiamare di nuovo **RtmDequeueRouteChangeMessage** appena possibile per consentire al gestore tabelle di routing di liberare le risorse associate ai messaggi in sospeso.<br/> |
| <dl> <dt>**ERRORE \_ NESSUN \_ MESSAGGIO**</dt> </dl>          | La coda del client non contiene messaggi. la chiamata non è richiesta. L'evento viene reimpostato.<br/>                                                                                                                                            |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                                                                                                                                                      |



 

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

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





