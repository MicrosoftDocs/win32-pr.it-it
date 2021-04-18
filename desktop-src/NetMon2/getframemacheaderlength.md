---
description: La funzione GetFrameMacHeaderLength restituisce la lunghezza, in byte, dell'intestazione MAC del frame.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Funzione GetFrameMacHeaderLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305905"
---
# <a name="getframemacheaderlength-function"></a>GetFrameMacHeaderLength (funzione)

La funzione **GetFrameMacHeaderLength** restituisce la lunghezza, in byte, dell'intestazione MAC del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è la lunghezza in byte dell'intestazione MAC.

Se la funzione ha esito negativo o viene rilevato un tipo MAC sconosciuto, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameMacHeaderLength** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




