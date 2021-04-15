---
title: Funzione RtmBlockDeleteRoutes (RTM. h)
description: La funzione RtmBlockDeleteRoutes Elimina tutte le route nel subset specificato di route nella tabella.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RAS funzione RtmBlockDeleteRoutes
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477512"
---
# <a name="rtmblockdeleteroutes-function"></a>RtmBlockDeleteRoutes (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmBlockDeleteRoutes** Elimina tutte le route nel subset specificato di route nella tabella.

## <a name="syntax"></a>Sintassi


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientHandle* \[ in\]
</dt> <dd>

Handle che identifica il client e, di conseguenza, il protocollo di routing delle route da eliminare.

</dd> <dt>

*EnumerationFlags* \[ in\]
</dt> <dd>

Specifica le route da enumerare. Questo parametro limita il set di route eliminate a un subset definito dai seguenti flag e i valori dei membri corrispondenti della struttura a cui punta il parametro *CriteriaRoute* . I flag sono identici a quelli usati in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , ad eccezione del fatto che RTM \_ solo le \_ \_ Route migliori sono ridondanti per **RtmBlockDeleteRoutes**. La designazione della migliore route viene regolata quando le route vengono eliminate, quindi la funzione Elimina tutte le route nel subset.

</dd> <dt>

*CriteriaRoute* \[ in\]
</dt> <dd>

Puntatore a una struttura di route specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)). I valori dei membri in questa struttura corrispondono ai flag specificati dal parametro *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito non è un \_ errore.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ Nessuna \_ Route**</dt> </dl>            | Non sono presenti route con i criteri specificati.<br/>                                           |
| <dl> <dt>**ERRORE \_ handle non valido \_**</dt> </dl>       | Il parametro *ClientHandle* non è valido.<br/>                                                      |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>    | Uno o più parametri di input non sono validi. ad esempio, i flag di enumerazione non sono validi.<br/> |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                    |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl>   | Memoria insufficiente per eseguire l'operazione.<br/>                                        |



 

## <a name="remarks"></a>Commenti

La funzione genera messaggi di notifica appropriati a tutti i client registrati, incluso il chiamante.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





