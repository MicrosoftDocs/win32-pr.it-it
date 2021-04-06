---
title: Funzione RtmRegisterClient (RTM. h)
description: La funzione RtmRegisterClient registra un client come gestore del protocollo specificato. Stabilisce un meccanismo di notifica delle modifiche della route per il client e imposta le opzioni del protocollo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RAS funzione RtmRegisterClient
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743111"
---
# <a name="rtmregisterclient-function"></a>RtmRegisterClient (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmRegisterClient** registra un client come gestore del protocollo specificato. Stabilisce un meccanismo di notifica delle modifiche della route per il client e imposta le opzioni del protocollo.

## <a name="syntax"></a>Sintassi


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Specifica la famiglia di protocolli del protocollo di routing da registrare.

</dd> <dt>

*RoutingProtocol* \[ in\]
</dt> <dd>

Specifica l'identificatore del protocollo di routing, uguale a quello utilizzato per la registrazione con gestione router. Vedere [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ in\]
</dt> <dd>

Specifica che è stata modificata una route migliore a una rete nella tabella. Il servizio di gestione delle tabelle di routing segnala questo evento dopo una modifica al percorso migliore per qualsiasi rete nella tabella. Per ulteriori informazioni sulla notifica di modifica di route, vedere [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) .

Questo parametro è facoltativo. Se il chiamante specifica **null** per questo parametro, il servizio di gestione delle tabelle di routing non comunica al client le modifiche nello stato della route migliore.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Specifica le opzioni varie per la gestione speciale del protocollo di routing. Il valore seguente è attualmente supportato.



| Flags                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**\_ \_ Single route del protocollo RTM \_**</dt> </dl> | Gestione tabelle di routing mantiene solo una route per rete di destinazione per il protocollo di routing. In altre parole, gestione tabelle di routing sostituisce le voci di route con gli stessi numeri di rete di destinazione invece di aggiungerne di nuove.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In esito positivo, restituisce un valore di **handle** che identifica il client nelle chiamate successive a gestione tabelle di routing.

Un handle **null** indica che Gestione tabelle di routing non è stato in grado di registrare il client. Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere la causa dell'errore.



| Valore                                                                                                         | Descrizione                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**il \_ client di errore \_ \_ esiste già**</dt> </dl> | Un altro client è già registrato per gestire il protocollo specificato.<br/>              |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>      | La famiglia di protocolli specificata non è supportata o il parametro *Flags* non è valido.<br/> |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl>   | Risorse insufficienti per eseguire l'operazione.<br/>                                   |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl>     | Memoria insufficiente per allocare strutture di dati per il client.<br/>                      |



 

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

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Identificatori della famiglia di protocolli RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

