---
description: La funzione GetFrameSrcAddressOffset restituisce l'offset dell'indirizzo di origine dei frame.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Funzione GetFrameSrcAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232677"
---
# <a name="getframesrcaddressoffset-function"></a>GetFrameSrcAddressOffset (funzione)

La funzione **GetFrameSrcAddressOffset** restituisce l'offset dell'indirizzo di origine del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* 
</dt> <dd>

Handle per il frame.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo di indirizzo di origine. Il valore del parametro può essere uno dei seguenti:

-   tipo di indirizzo \_ \_ Ethernet
-   INDIRIZZO \_ \_ IP tipo
-   tipo di indirizzo \_ \_ IPX
-   tipo di indirizzo \_ \_ Tokenring
-   tipo di indirizzo \_ \_ FDDI
-   tipo di indirizzo \_ \_ XNS
-   tipo di indirizzo \_ \_ \_ IP viti
-   tipo di indirizzo \_ \_ ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

Puntatore a un **valore DWORD**, che, in restituzione, contiene la lunghezza dell'indirizzo, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'offset per l'indirizzo di origine.

Se la funzione ha esito negativo, il valore restituito è meno uno (-1).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




