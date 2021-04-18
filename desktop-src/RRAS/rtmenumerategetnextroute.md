---
title: Funzione RtmEnumerateGetNextRoute (RTM. h)
description: La funzione RtmEnumerateGetNextRoute restituisce la voce di route successiva nell'enumerazione avviata da una chiamata a RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RAS funzione RtmEnumerateGetNextRoute
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301914"
---
# <a name="rtmenumerategetnextroute-function"></a>RtmEnumerateGetNextRoute (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmEnumerateGetNextRoute** restituisce la voce di route successiva nell'enumerazione avviata da una chiamata a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

## <a name="syntax"></a>Sintassi


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnumerationHandle* \[ in\]
</dt> <dd>

Handle che identifica l'enumerazione e ne specifica l'ambito. Ottenere questo handle chiamando [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Route* \[ out\]
</dt> <dd>

Puntatore a una struttura di route specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)). Questa struttura riceverà la route successiva nell'enumerazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito non è un \_ errore.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ handle non valido \_**</dt> </dl>       | Il parametro *EnumerationHandle* non è valido.<br/>              |
| <dl> <dt>**ERRORE \_ \_ altre \_ Route**</dt> </dl>      | Nell'enumerazione non sono presenti altre route.<br/>                 |
| <dl> <dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Sebbene le route non vengano restituite in un ordine particolare, ogni route nell'enumerazione viene restituita una sola volta.

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

[**\_route IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_Route IPX \_ RTM**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





