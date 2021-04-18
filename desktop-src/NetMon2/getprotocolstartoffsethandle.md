---
description: La funzione GetProtocolStartOffsetHandle restituisce l'offset del frame di un protocollo specificato.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Funzione GetProtocolStartOffsetHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305894"
---
# <a name="getprotocolstartoffsethandle-function"></a>GetProtocolStartOffsetHandle (funzione)

La funzione **GetProtocolStartOffsetHandle** restituisce l'offset del frame di un protocollo specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per un frame.

</dd> <dt>

*hProtocol* \[ in\]
</dt> <dd>

Handle per un protocollo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'offset del frame misurato in byte.

Se la funzione ha esito negativo, il valore restituito è uno (1).

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetProtocolStartOffsetHandle** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




