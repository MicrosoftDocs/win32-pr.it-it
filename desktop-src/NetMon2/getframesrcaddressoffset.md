---
description: La funzione GetFrameSrcAddressOffset restituisce l'offset dell'indirizzo di origine dei frame.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Funzione GetFrameSrcAddressOffset (Netmon.h)
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
ms.openlocfilehash: 5c8c2315b53d336a06a73e63019daee842439f65aa53e3fb7d34d4944dcab9cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366095"
---
# <a name="getframesrcaddressoffset-function"></a>Funzione GetFrameSrcAddressOffset

La **funzione GetFrameSrcAddressOffset** restituisce l'offset dell'indirizzo di origine del frame.

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

-   TIPO \_ DI \_ INDIRIZZO ETHERNET
-   TIPO \_ DI \_ INDIRIZZO IP
-   TIPO \_ DI \_ INDIRIZZO IPX
-   TIPO \_ DI INDIRIZZO \_ TOKENRING
-   TIPO \_ DI INDIRIZZO \_ FDDI
-   TIPO \_ DI INDIRIZZO \_ XNS
-   TIPO \_ DI INDIRIZZO IP \_ VINES \_
-   TIPO \_ DI \_ INDIRIZZO ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

Puntatore a **un valore DWORD**, che in caso di restituzione contiene la lunghezza dell'indirizzo, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'offset dell'indirizzo di origine.

Se la funzione ha esito negativo, il valore restituito è meno uno (-1).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




