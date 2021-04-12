---
description: La funzione LoadIPXAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi IPX tratto da una variabile di stringa di configurazione HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Funzione LoadIPXAddresses (Netmon. h)
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
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233302"
---
# <a name="loadipxaddresses-function"></a>LoadIPXAddresses (funzione)

La funzione **LoadIPXAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi IPX tratto da una variabile di stringa di configurazione HTML.

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

*pConfig* \[ in\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .

</dd> <dt>

*pVarName* \[ in\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*ppAddresses* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una matrice di indirizzi. Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza diversa da zero, viene allocato spazio sufficiente (usando **HeapAllocMemory**) e tutti gli indirizzi IPX vengono archiviati come matrice.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Puntatore alla variabile **DWORD** impostata sul numero di indirizzi IPX ricavati dalla stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (il nome della variabile è stato trovato e ha una stringa di lunghezza non zero che rappresentava gli indirizzi IPX), il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




