---
title: Funzione RtmCreateEnumerationHandle (RTM. h)
description: La funzione RtmCreateEnumerationHandle restituisce un handle da usare con RtmEnumerateGetNextRoute per analizzare tutte le route o un subset di route, noto a gestione tabelle di routing.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RAS funzione RtmCreateEnumerationHandle
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119222"
---
# <a name="rtmcreateenumerationhandle-function"></a>RtmCreateEnumerationHandle (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmCreateEnumerationHandle** restituisce un handle da usare con [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) per analizzare tutte le route o un subset di route, noto a gestione tabelle di routing.

## <a name="syntax"></a>Sintassi


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Specifica la famiglia di protocolli delle route da enumerare.

</dd> <dt>

*EnumerationFlags* \[ in\]
</dt> <dd>

Specifica le route da enumerare. Questo parametro limita il set di route restituite dall'API di enumerazione a un subset definito dai flag seguenti e i valori nei membri corrispondenti della struttura a cui punta il parametro *CriteriaRoute* . Questo parametro può avere uno dei valori seguenti.



| EnumerationFlags                                                                                                                                                                              | Significato                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**\_solo RTM \_ questa \_ rete**</dt> </dl>       | Enumerare solo le route che hanno lo stesso numero di rete del \_ membro di rete RR della struttura a cui punta CriteriaRoute.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**\_solo RTM \_ questa \_ interfaccia**</dt> </dl> | Enumerare solo le route ottenute tramite l'interfaccia specificata dal campo RR \_ InterfaceID della struttura a cui punta CriteriaRoute.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**\_solo RTM \_ questo \_ protocollo**</dt> </dl>    | Enumerare solo le route aggiunte dal protocollo di routing specificato dal \_ campo RR RoutingProtocol della struttura a cui punta CriteriaRoute.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**\_ \_ Route migliori solo per RTM \_**</dt> </dl>          | Enumerare solo le route migliori a ognuna delle reti nel set.<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[ in\]
</dt> <dd>

Puntatore a una struttura di route specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)). I valori dei membri in questa struttura corrispondono ai flag specificati dal parametro *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un **handle** da usare con le successive chiamate di enumerazione.

Se la funzione ha esito negativo o non esistono route con i criteri specificati, il valore restituito è **null**. Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere ulteriori informazioni.



| Valore                                                                                                       | Descrizione                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ Nessuna \_ Route**</dt> </dl>            | Non sono presenti route con i criteri specificati.<br/>                                                             |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>    | Uno o più parametri di input non sono validi (ad esempio, la famiglia di protocolli sconosciuta, i flag di enumerazione non validi).<br/> |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                                      |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl>   | Memoria insufficiente per l'allocazione dell'handle.<br/>                                                              |



 

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

[**\_route IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_Route IPX \_ RTM**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

