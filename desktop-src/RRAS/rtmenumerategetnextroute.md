---
title: Funzione RtmEnumerateGetNextRoute (Rtm.h)
description: La funzione RtmEnumerateGetNextRoute restituisce la voce di route successiva nell'enumerazione avviata da una chiamata a RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- Funzione RtmEnumerateGetNextRoute RAS
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
ms.openlocfilehash: 6105340003c6240b49acec4699fa7b229d11963116367ab0fa0c069211b6fd1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035871"
---
# <a name="rtmenumerategetnextroute-function"></a>Funzione RtmEnumerateGetNextRoute

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **funzione RtmEnumerateGetNextRoute** restituisce la voce di route successiva nell'enumerazione avviata da una chiamata a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

## <a name="syntax"></a>Sintassi


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnumerationHandle* \[ Pollici\]
</dt> <dd>

Handle che identifica l'enumerazione e ne specifica l'ambito. Ottenere questo handle chiamando [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Route* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura di route specifica della famiglia di protocolli ( [**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)). Questa struttura riceverà la route successiva nell'enumerazione .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ HANDLE NON \_ VALIDO**</dt> </dl>       | Il *parametro EnumerationHandle* non è valido.<br/>              |
| <dl> <dt>**ERRORE \_ NON \_ PIÙ \_ ROUTE**</dt> </dl>      | Nell'enumerazione non sono presenti altre route.<br/>                 |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Anche se le route non vengono restituite in un ordine specifico, ogni route nell'enumerazione viene restituita una sola volta.

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

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





