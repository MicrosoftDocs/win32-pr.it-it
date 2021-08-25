---
title: Funzione RtmCreateEnumerationHandle (Rtm.h)
description: La funzione RtmCreateEnumerationHandle restituisce un handle da usare con RtmEnumerateGetNextRoute per analizzare tutte le route o un subset di route note al gestore tabelle di routing.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- Funzione RtmCreateEnumerationHandle RAS
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
ms.openlocfilehash: 635bc169b1f68e2ef29e85e9e7ef800868453dd7221d08eda7953eda277ae423
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035911"
---
# <a name="rtmcreateenumerationhandle-function"></a>Funzione RtmCreateEnumerationHandle

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **funzione RtmCreateEnumerationHandle** restituisce un handle da usare con [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) per analizzare tutte le route o un subset di route note al gestore tabelle di routing.

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

*ProtocolFamily* \[ Pollici\]
</dt> <dd>

Specifica la famiglia di protocolli delle route da enumerare.

</dd> <dt>

*EnumerationFlags* \[ Pollici\]
</dt> <dd>

Specifica le route da enumerare. Questo parametro limita il set di route restituito dall'API di enumerazione a un subset definito dai flag seguenti e ai valori nei membri corrispondenti della struttura a cui punta il *parametro CriteriaRoute.* Questo parametro può avere uno dei valori seguenti.



| EnumerationFlags                                                                                                                                                                              | Significato                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**RTM \_ SOLO \_ QUESTA \_ RETE**</dt> </dl>       | Enumerare solo le route con lo stesso numero di rete del membro di rete RR della struttura a cui \_ punta CriteriaRoute.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**RTM \_ SOLO \_ QUESTA \_ INTERFACCIA**</dt> </dl> | Enumerare solo le route ottenute tramite l'interfaccia specificata dal campo RR InterfaceID della struttura a cui \_ punta CriteriaRoute.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**RTM \_ SOLO \_ QUESTO \_ PROTOCOLLO**</dt> </dl>    | Enumerare solo le route aggiunte dal protocollo di routing specificato dal campo RoutingProtocol RR della struttura a \_ cui punta CriteriaRoute.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**SOLO ROUTE MIGLIORI \_ \_ RTM \_**</dt> </dl>          | Enumerare solo le route migliori per ognuna delle reti nel set.<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura di route specifica della famiglia di protocolli ([**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)). I valori dei membri in questa struttura corrispondono ai flag specificati dal *parametro EnumerationFlags.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **un HANDLE** da usare con chiamate di enumerazione successive.

Se la funzione ha esito negativo o non esistono route con i criteri specificati, il valore restituito è **NULL.** Chiamare [**GetLastError per**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ottenere altre informazioni.



| Valore                                                                                                       | Descrizione                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ NESSUNA \_ ROUTE**</dt> </dl>            | Non sono presenti route con i criteri specificati.<br/>                                                             |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>    | Uno o più parametri di input non sono validi, ad esempio la famiglia di protocolli sconosciuta e i flag di enumerazione non validi.<br/> |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                                      |
| <dl> <dt>**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**</dt> </dl>   | Memoria insufficiente per allocare l'handle.<br/>                                                              |



 

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

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

