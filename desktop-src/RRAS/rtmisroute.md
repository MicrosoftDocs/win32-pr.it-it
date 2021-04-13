---
title: Funzione RtmIsRoute (RTM. h)
description: La funzione RtmIsRoute determina se esistono una o più route per una rete di destinazione specificata. In tal caso, la funzione restituisce informazioni per la migliore route alla rete.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RAS funzione RtmIsRoute
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
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478221"
---
# <a name="rtmisroute-function"></a>RtmIsRoute (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmIsRoute** determina se esistono una o più route per una rete di destinazione specificata. In tal caso, la funzione restituisce informazioni per la migliore route alla rete.

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

*ProtocolFamily* \[ in\]
</dt> <dd>

Specifica il tipo di struttura dei dati a cui punta il parametro di *rete* , ad [**esempio \_ rete IP**](ip-network.md), [**\_ rete IPX**](ipx-network.md).

</dd> <dt>

*Rete* \[ in\]
</dt> <dd>

Puntatore a una struttura che specifica i dati del numero di rete specifici della famiglia di protocolli. Questi dati identificano la rete per cui il chiamante Cerca le informazioni sulla route.

</dd> <dt>

*BestRoute* \[ out\]
</dt> <dd>

Puntatore a una struttura specifica della famiglia di protocolli che riceve le informazioni sulla route migliore correnti, se presenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei codici seguenti.



| Valore                                                                                                       | Descrizione                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>                         | Esiste almeno una route per la rete specificata. La route migliore viene restituita nella struttura a cui punta il parametro *BestRoute* .<br/>      |
| <dl> <dt>**FALSE**</dt> </dl>                        | Non è presente alcuna route per la rete specificata oppure l'operazione non è riuscita. Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere ulteriori informazioni:<br/> |
| <dl> <dt>**Nessun \_ errore**</dt> </dl>                    | L'operazione è stata completata, ma non è presente alcuna route per la rete specificata.<br/>                                                                      |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>    | Il valore del parametro *ProtocolFamily* non corrisponde ad alcuna famiglia di protocolli installata.<br/>                                             |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                                                                  |



 

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

[**\_rete IP**](ip-network.md)
</dt> <dt>

[**\_rete IPX**](ipx-network.md)
</dt> <dt>

[Identificatori della famiglia di protocolli RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

