---
description: La funzione LoadIPXAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi IPX tratto da una variabile di stringa di configurazione HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Funzione LoadIPXAddresses (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ed8bb6948102e8d28150edf102fa261c9c7f7adfcf105e377352054304b352df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677311"
---
# <a name="loadipxaddresses-function"></a>Funzione LoadIPXAddresses

La **funzione LoadIPXAddresses viene** chiamata dal monitoraggio per compilare un elenco di indirizzi IPX tratto da una variabile di stringa di configurazione HTML.

## <a name="syntax"></a>Sintassi


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConfig* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio dal [metodo IMonitor::D oConfigure.](imonitor-doconfigure.md)

</dd> <dt>

*pVarName* \[ Pollici\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*ppAddresses* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una matrice di indirizzi. Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza non zero, viene allocato spazio sufficiente (tramite **HeapAllocMemory)** e tutti gli indirizzi IPX vengono archiviati come matrice.

</dd> <dt>

*pNumAddresses* \[ Cambio\]
</dt> <dd>

Puntatore alla **variabile DWORD** impostata sul numero di indirizzi IPX prelevati dalla stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (il nome della variabile è stato trovato ed è presente una stringa di lunghezza non zero che rappresenta gli indirizzi IPX), il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




