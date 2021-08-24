---
title: Funzione RtmGetNetworkCount (Rtm.h)
description: La funzione RtmGetNetworkCount recupera il numero di reti a cui il gestore tabelle di routing dispone di route.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- Funzione RtmGetNetworkCount RAS
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
ms.openlocfilehash: c721605988f15661030ddbeaadf4140fb716a089c87cc46fc2a8316bc2de9e42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035671"
---
# <a name="rtmgetnetworkcount-function"></a>Funzione RtmGetNetworkCount

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **funzione RtmGetNetworkCount** recupera il numero di reti a cui il gestore tabelle di routing dispone di route.

## <a name="syntax"></a>Sintassi


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolFamily* \[ Pollici\]
</dt> <dd>

Specifica per quale tipo di rete ottenere informazioni sulla route, ad esempio IP o IPX.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è il numero di reti, il numero di reti note ai protocolli di routing della famiglia di protocolli specificata.

Se il valore restituito è zero, non sono disponibili route oppure l'operazione non è riuscita. Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni.



| Valore                                                                                                    | Descrizione                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NESSUN \_ ERRORE**</dt> </dl>                 | L'operazione è riuscita, ma non sono disponibili route.<br/>                                             |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl> | Il valore del *parametro ProtocolFamily* non corrisponde ad alcuna famiglia di protocolli installata.<br/> |



 

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

[Identificatori della famiglia di protocolli RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

