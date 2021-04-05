---
title: Funzione RtmGetNetworkCount (RTM. h)
description: La funzione RtmGetNetworkCount Recupera il numero di reti a cui sono indirizzate le route di gestione tabelle di routing.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RAS funzione RtmGetNetworkCount
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741410"
---
# <a name="rtmgetnetworkcount-function"></a>RtmGetNetworkCount (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmGetNetworkCount** Recupera il numero di reti a cui sono indirizzate le route di gestione tabelle di routing.

## <a name="syntax"></a>Sintassi


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Specifica per quale tipo di rete ottenere informazioni sulla Route, ad esempio IP o IPX.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è il conteggio della rete, il numero di reti note ai protocolli di routing della famiglia di protocolli specificata.

Se il valore restituito è zero, non sono disponibili route o l'operazione non è riuscita. Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere ulteriori informazioni.



| Valore                                                                                                    | Descrizione                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Nessun \_ errore**</dt> </dl>                 | L'operazione è stata completata, ma non sono disponibili route.<br/>                                             |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl> | Il valore del parametro *ProtocolFamily* non corrisponde ad alcuna famiglia di protocolli installata.<br/> |



 

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

[Identificatori della famiglia di protocolli RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

