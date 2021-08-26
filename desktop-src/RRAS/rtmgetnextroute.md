---
title: Funzione RtmGetNextRoute (Rtm.h)
description: La funzione RtmGetNextRoute restituisce la route successiva dal subset specificato di route nella tabella.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- Funzione RtmGetNextRoute RAS
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
ms.openlocfilehash: ec33ff5932d40a146811056d74ca3b91f0bdbfdd772a04a2d7392390d63209e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073821"
---
# <a name="rtmgetnextroute-function"></a>Funzione RtmGetNextRoute

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **funzione RtmGetNextRoute** restituisce la route successiva dal subset specificato di route nella tabella.

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

*ProtocolFamily* \[ Pollici\]
</dt> <dd>

Specifica la famiglia di protocolli di route da recuperare, ad esempio IP o IPX.

</dd> <dt>

*EnumerationFlags* \[ Pollici\]
</dt> <dd>

Specifica le route da enumerare. Questo parametro limita il set di route eliminate a un subset definito dai flag seguenti e i valori nei membri corrispondenti della struttura a cui punta *il parametro CriteriaRoute.* I flag sono gli stessi usati in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Route* \[ in, out\]
</dt> <dd>

In input, *Route* punta a una struttura specifica della famiglia di protocolli ( [**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)).

La funzione chiamante fornisce i valori dei membri per questa struttura. Questi valori, insieme al *parametro EnumerationFlags,* specificano il set da cui restituire le route.

In caso di output, *Route* punta a una struttura che riceve la prima route corrispondente ai criteri specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **NO \_ ERROR**.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>    | Uno dei parametri non è valido.<br/>                            |
| <dl> <dt>**ERRORE \_ NESSUNA \_ ROUTE**</dt> </dl>            | Non sono presenti route che corrispondono ai criteri specificati.<br/>       |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le route vengono restituite nell'ordine seguente:

1.  Numero di rete
2.  Protocollo di routing
3.  Identificatore di interfaccia
4.  Indirizzo dell'hop successivo

Questa funzione è meno efficiente delle funzioni di handle di enumerazione corrispondenti.

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

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





