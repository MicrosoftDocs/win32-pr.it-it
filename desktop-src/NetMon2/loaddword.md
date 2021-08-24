---
description: La funzione LoadDWORD viene chiamata dal monitoraggio per impostare una variabile DWORD con un valore derivato da una variabile di stringa di configurazione HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Funzione LoadDWORD (Netmon.h)
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
ms.openlocfilehash: 8fa0477122548dad30911948a3581d269b22d8d6eb866273f32aa40a9b427545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778761"
---
# <a name="loaddword-function"></a>Funzione LoadDWORD

La **funzione LoadDWORD** viene chiamata dal monitoraggio per impostare una **variabile DWORD** con un valore derivato da una variabile di stringa di configurazione HTML.

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

*pConfig* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio dal metodo [IMonitor::D oConfigure.](imonitor-doconfigure.md)

</dd> <dt>

*pVarName* \[ Pollici\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*pValue* \[ Pollici\]
</dt> <dd>

Puntatore alla **variabile DWORD** impostata sul valore della variabile della stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (se il nome della variabile è stato trovato e ha una stringa di lunghezza non zero), viene inserito **il valore DWORD** e il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




