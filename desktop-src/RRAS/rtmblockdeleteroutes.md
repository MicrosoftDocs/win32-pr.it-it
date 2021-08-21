---
title: Funzione RtmBlockDeleteRoutes (Rtm.h)
description: La funzione RtmBlockDeleteRoutes elimina tutte le route nel subset specificato di route nella tabella.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- Funzione RtmBlockDeleteRoutes RAS
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
ms.openlocfilehash: f830603bba4bcdf07bd7bc8c631ac17028301a795fc14ebbce6483ef72f81361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073881"
---
# <a name="rtmblockdeleteroutes-function"></a>Funzione RtmBlockDeleteRoutes

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **funzione RtmBlockDeleteRoutes** elimina tutte le route nel subset specificato di route nella tabella.

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

*ClientHandle* \[ Pollici\]
</dt> <dd>

Handle che identifica il client e quindi il protocollo di routing delle route da eliminare.

</dd> <dt>

*EnumerationFlags* \[ Pollici\]
</dt> <dd>

Specifica le route da enumerare. Questo parametro limita il set di route eliminate a un subset definito dai flag seguenti e i valori nei membri corrispondenti della struttura a cui punta *il parametro CriteriaRoute.* I flag sono uguali a quelli usati in [**RtmCreateEnumerationHandle,**](rtmcreateenumerationhandle.md) ad eccezione del fatto che RTM ONLY BEST ROUTES è \_ ridondante per \_ \_ **RtmBlockDeleteRoutes.** La designazione di route migliore viene modificata quando vengono eliminate le route, quindi la funzione elimina tutte le route nel subset.

</dd> <dt>

*CriteriaRoute* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura di route specifica della famiglia di protocolli ( [**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**RTM \_ IPX \_ ROUTE).**](rtm-ipx-route.md) I valori dei membri in questa struttura corrispondono ai flag specificati dal *parametro EnumerationFlags.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ - NESSUNA \_ ROUTE**</dt> </dl>            | Non sono presenti route con i criteri specificati.<br/>                                           |
| <dl> <dt>**ERRORE \_ HANDLE NON \_ VALIDO**</dt> </dl>       | Il *parametro ClientHandle* non è valido.<br/>                                                      |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>    | Uno o più parametri di input non sono validi, ad esempio i flag di enumerazione non sono validi.<br/> |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>                                    |
| <dl> <dt>**ERRORE \_ MEMORIA \_ \_ INSUFFICIENTE**</dt> </dl>   | Memoria insufficiente per eseguire l'operazione.<br/>                                        |



 

## <a name="remarks"></a>Commenti

La funzione genera messaggi di notifica appropriati per tutti i client registrati, incluso il chiamante.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





