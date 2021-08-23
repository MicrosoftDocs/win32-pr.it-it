---
description: La funzione GetPreviousProtocolOffsetByName restituisce l'istanza precedente di un protocollo specificato.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Funzione GetPreviousProtocolOffsetByName (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 17b472bbdead74612ccc6d76f1059443ce6f62dd122f7933ae31c99fb82900a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743761"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>Funzione GetPreviousProtocolOffsetByName

La **funzione GetPreviousProtocolOffsetByName** restituisce l'istanza precedente di un protocollo specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame.

</dd> <dt>

*dwStartOffset* \[ Pollici\]
</dt> <dd>

Offset nel frame.

</dd> <dt>

*szProtocolName* \[ Pollici\]
</dt> <dd>

Nome del protocollo da cercare.

</dd> <dt>

*pdwPreviousOffset* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore DWORD** che contiene l'offset al protocollo precedente (se la funzione ha esito positivo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è NMERR \_ PROTOCOL \_ NOT \_ FOUND.

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare **GetPreviousProtocolOffsetByName.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




