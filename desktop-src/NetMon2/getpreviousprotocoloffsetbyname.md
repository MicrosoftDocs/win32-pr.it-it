---
description: La funzione GetPreviousProtocolOffsetByName restituisce l'istanza precedente di un protocollo specificato.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Funzione GetPreviousProtocolOffsetByName (Netmon. h)
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
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305900"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>GetPreviousProtocolOffsetByName (funzione)

La funzione **GetPreviousProtocolOffsetByName** restituisce l'istanza precedente di un protocollo specificato.

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

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame.

</dd> <dt>

*dwStartOffset* \[ in\]
</dt> <dd>

Offset nel frame.

</dd> <dt>

*szProtocolName* \[ in\]
</dt> <dd>

Nome del protocollo che si desidera cercare.

</dd> <dt>

*pdwPreviousOffset* \[ out\]
</dt> <dd>

Puntatore a un **valore DWORD** che contiene l'offset al protocollo precedente (se la funzione ha esito positivo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è il \_ protocollo NMERR \_ non \_ trovato.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare **GetPreviousProtocolOffsetByName**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




