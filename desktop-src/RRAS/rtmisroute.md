---
title: Funzione RtmIsRoute (Rtm.h)
description: La funzione RtmIsRoute determina se esistono una o più route a una rete di destinazione specificata. In tal caso, la funzione restituisce informazioni per la route migliore a tale rete.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- Funzione RtmIsRoute RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312b43a7cf66e17cc6016fe3ad35bd21cd1e7ae19ecd7864a10de4d977a92ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073811"
---
# <a name="rtmisroute-function"></a>Funzione RtmIsRoute

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **funzione RtmIsRoute** determina se esistono una o più route a una rete di destinazione specificata. In tal caso, la funzione restituisce informazioni per la route migliore a tale rete.

## <a name="syntax"></a>Sintassi


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolFamily* \[ Pollici\]
</dt> <dd>

Specifica il tipo di struttura dei dati a cui punta il *parametro Network,* ad esempio [**IP \_ NETWORK,**](ip-network.md) [**IPX \_ NETWORK.**](ipx-network.md)

</dd> <dt>

*Rete* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura che specifica i dati relativi ai numeri di rete specifici della famiglia di protocolli. Questi dati identificano la rete per cui il chiamante cerca informazioni sulla route.

</dd> <dt>

*BestRoute* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura specifica della famiglia di protocolli che riceve le informazioni di route migliori correnti, se presenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei codici seguenti.



| Valore                                                                                                       | Descrizione                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>                         | Esiste almeno una route alla rete specificata. La route migliore viene restituita nella struttura a cui punta il *parametro BestRoute.*<br/>      |
| <dl> <dt>**False**</dt> </dl>                        | Non è presente alcuna route alla rete specificata oppure l'operazione non è riuscita. Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni:<br/> |
| <dl> <dt>**NESSUN \_ ERRORE**</dt> </dl>                    | L'operazione è riuscita, ma non esiste alcuna route per la rete specificata.<br/>                                                                      |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>    | Il valore del *parametro ProtocolFamily* non corrisponde ad alcuna famiglia di protocolli installata.<br/>                                             |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                                                                  |



 

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

[**RETE \_ IP**](ip-network.md)
</dt> <dt>

[**RETE \_ IPX**](ipx-network.md)
</dt> <dt>

[Identificatori della famiglia di protocolli RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

