---
description: La funzione GetFrameDstAddressOffset restituisce l'offset all'indirizzo di destinazione di un frame specificato.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Funzione GetFrameDstAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305909"
---
# <a name="getframedstaddressoffset-function"></a>GetFrameDstAddressOffset (funzione)

La funzione **GetFrameDstAddressOffset** restituisce l'offset all'indirizzo di destinazione di un frame specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame.

</dd> <dt>

*AddressType* \[ in\]
</dt> <dd>

Tipo di indirizzo di destinazione. Specificare uno dei valori seguenti:

tipo di indirizzo IP indirizzo IP tipo indirizzo IP tipo di indirizzo IPX tipo di indirizzo Tokenring tipo di indirizzo FDDI tipo di indirizzo XNS tipo di indirizzo di tipo indirizzo \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ IP viti \_ \_ ATM.

</dd> <dt>

*AddressLength* \[ in\]
</dt> <dd>

Lunghezza, in byte, dell'indirizzo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'offset, espresso in byte, al tipo di indirizzo richiesto.

Se la funzione ha esito negativo, il valore restituito è meno uno (-1).

## <a name="remarks"></a>Commenti

Se il parametro *addressType* è impostato sul tipo di indirizzo \_ \_ Ethernet, il valore restituito della funzione **GetFrameDstAddressOffset** è sempre zero. L'offset di un indirizzo Ethernet è sempre zero.

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameDstAddressOffset** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




