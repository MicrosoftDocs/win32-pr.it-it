---
description: La funzione LoadMACAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi MAC con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Funzione LoadMACAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526767"
---
# <a name="loadmacaddresses-function"></a>LoadMACAddresses (funzione)

La funzione **LoadMACAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi Mac con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.

## <a name="syntax"></a>Sintassi


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
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

Puntatore a un puntatore a una matrice di indirizzi. Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza diversa da zero, la funzione alloca spazio sufficiente (usando **HeapAllocMemory**) e archivia tutti gli indirizzi Mac come matrice.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Puntatore alla variabile **DWORD** impostata sul numero di indirizzi Mac ricavati dalla stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, (il nome della variabile è stato trovato e presenta una stringa di lunghezza diversa da zero che rappresenta gli indirizzi MAC), il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




