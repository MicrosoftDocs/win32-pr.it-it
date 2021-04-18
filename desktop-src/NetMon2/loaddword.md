---
description: La funzione LoadDWORD viene chiamata dal monitoraggio per impostare una variabile DWORD con un valore tratto da una variabile di stringa di configurazione HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Funzione LoadDWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318971"
---
# <a name="loaddword-function"></a>LoadDWORD (funzione)

La funzione **LoadDWORD** viene chiamata dal monitoraggio per impostare una variabile **DWORD** con un valore tratto da una variabile di stringa di configurazione HTML.

## <a name="syntax"></a>Sintassi


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
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

*pValue* \[ in\]
</dt> <dd>

Puntatore alla variabile **DWORD** impostata sul valore della variabile della stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (se il nome della variabile è stato trovato e ha una stringa di lunghezza diversa da zero), viene inserito il valore **DWORD** e il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




