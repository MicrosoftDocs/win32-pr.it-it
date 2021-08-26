---
title: Funzione RtmRegisterClient (Rtm.h)
description: La funzione RtmRegisterClient registra un client come gestore del protocollo specificato. Stabilisce un meccanismo di notifica della modifica della route per il client e imposta le opzioni del protocollo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- Funzione RtmRegisterClient RAS
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
ms.openlocfilehash: db58fc9457195c2149fd8d34a8a65a6d5085135275e1c878633f64cb742b02cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081041"
---
# <a name="rtmregisterclient-function"></a>Funzione RtmRegisterClient

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **funzione RtmRegisterClient** registra un client come gestore del protocollo specificato. Stabilisce un meccanismo di notifica della modifica della route per il client e imposta le opzioni del protocollo.

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

*ProtocolFamily* \[ Pollici\]
</dt> <dd>

Specifica la famiglia di protocolli del protocollo di routing da registrare.

</dd> <dt>

*RoutingProtocol* \[ Pollici\]
</dt> <dd>

Specifica l'identificatore del protocollo di routing, uguale a quello utilizzato durante la registrazione con gestione router. Vedere [**RegisterProtocol.**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)

</dd> <dt>

*ChangeEvent* \[ Pollici\]
</dt> <dd>

Specifica che è stata modificata una route migliore verso una rete nella tabella. Il gestore tabelle di routing segnala questo evento dopo una modifica alla route migliore a qualsiasi rete nella tabella. Per altre informazioni sulla notifica di modifica della route, vedere [**RtmDequeueRouteChangeMessage.**](rtmdequeueroutechangemessage.md)

Questo parametro è facoltativo. Se il chiamante specifica **NULL per** questo parametro, il gestore delle tabelle di routing non notifica al client le modifiche nello stato di route migliore.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Specifica varie opzioni per la gestione speciale del protocollo di routing. Il valore seguente è attualmente supportato.



| Flags                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**ROUTE SINGOLA \_ DEL \_ PROTOCOLLO RTM \_**</dt> </dl> | Il gestore tabelle di routing mantiene una sola route per rete di destinazione per il protocollo di routing. In altre parole, il gestore tabelle di routing sostituisce le voci di route con gli stessi numeri di rete di destinazione anziché aggiungerne di nuove.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce un **valore HANDLE** che identifica il client nelle chiamate successive al gestore tabelle di routing.

Un handle **NULL** indica che il gestore tabelle di routing non è riuscito a registrare il client. Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere il motivo dell'errore.



| Valore                                                                                                         | Descrizione                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ CLIENT \_ GIÀ \_ ESISTENTE**</dt> </dl> | Un altro client è già registrato per gestire il protocollo specificato.<br/>              |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>      | La famiglia di protocolli specificata non è supportata o il *parametro Flags* non è valido.<br/> |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl>   | Risorse insufficienti per eseguire l'operazione.<br/>                                   |
| <dl> <dt>**ERRORE \_ MEMORIA \_ \_ INSUFFICIENTE**</dt> </dl>     | Memoria insufficiente per allocare strutture di dati per il client.<br/>                      |



 

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

[**Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Identificatori della famiglia di protocolli RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

