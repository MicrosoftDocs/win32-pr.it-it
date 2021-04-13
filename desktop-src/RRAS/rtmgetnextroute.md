---
title: Funzione RtmGetNextRoute (RTM. h)
description: La funzione RtmGetNextRoute restituisce la route successiva dal subset specificato di route nella tabella.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RAS funzione RtmGetNextRoute
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518088"
---
# <a name="rtmgetnextroute-function"></a>RtmGetNextRoute (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmGetNextRoute** restituisce la route successiva dal subset specificato di route nella tabella.

## <a name="syntax"></a>Sintassi


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Specifica la famiglia di protocolli di route da recuperare, ad esempio IP o IPX.

</dd> <dt>

*EnumerationFlags* \[ in\]
</dt> <dd>

Specifica le route da enumerare. Questo parametro limita il set di route eliminate a un subset definito dai seguenti flag e i valori dei membri corrispondenti della struttura a cui punta il parametro *CriteriaRoute* . I flag sono identici a quelli usati in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Route* \[ in uscita\]
</dt> <dd>

In input, la *Route* punta a una struttura specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)).

La funzione chiamante fornisce i valori dei membri per questa struttura. Questi valori, insieme al parametro *EnumerationFlags* , specificano il set dal quale restituire le route.

Nell'output, la *Route* punta a una struttura che riceve la prima route corrispondente ai criteri specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito **non è un \_ errore**.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>    | Uno dei parametri non è valido.<br/>                            |
| <dl> <dt>**ERRORE \_ Nessuna \_ Route**</dt> </dl>            | Nessuna route corrispondente ai criteri specificati.<br/>       |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le route vengono restituite nell'ordine seguente:

1.  Numero di rete
2.  Protocollo di routing
3.  Identificatore di interfaccia
4.  Indirizzo hop successivo

Questa funzione è meno efficiente delle funzioni di handle di enumerazione corrispondenti.

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

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





