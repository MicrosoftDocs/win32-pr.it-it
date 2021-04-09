---
description: La funzione MacTypeToAddressType converte un tipo MAC specificato in un tipo di indirizzo.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Funzione MacTypeToAddressType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879502"
---
# <a name="mactypetoaddresstype-function"></a>MacTypeToAddressType (funzione)

La funzione **MacTypeToAddressType** converte un tipo Mac specificato in un tipo di indirizzo.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MacType* \[ in\]
</dt> <dd>

Tipo MAC da convertire. Specificare uno dei valori seguenti:

tipo \_ Mac \_ Ethernet Mac \_ digitare \_ Tokenring Mac \_ tipo \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è uno dei seguenti tipi di indirizzo.

tipo di indirizzo Ethernet tipo indirizzo Tokenring tipo di indirizzo \_ \_ \_ \_ \_ \_ FDDI

Se la funzione ha esito negativo, il tipo MAC è sconosciuto, il valore restituito è-1.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **MacTypeToAddressType** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




