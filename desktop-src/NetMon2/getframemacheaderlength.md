---
description: La funzione GetFrameMacHeaderLength restituisce la lunghezza, in byte, dell'intestazione MAC del frame.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Funzione GetFrameMacHeaderLength (Netmon.h)
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
ms.openlocfilehash: 0e6c4abe859cd4c307d8ade586b9371b69b5c171681006cf4aa1634ef815d794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743901"
---
# <a name="getframemacheaderlength-function"></a>Funzione GetFrameMacHeaderLength

La **funzione GetFrameMacHeaderLength** restituisce la lunghezza, in byte, dell'intestazione MAC del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è la lunghezza in byte dell'intestazione MAC.

Se la funzione non ha esito positivo o viene rilevato un tipo MAC sconosciuto, il valore restituito è zero.

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione GetFrameMacHeaderLength.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




