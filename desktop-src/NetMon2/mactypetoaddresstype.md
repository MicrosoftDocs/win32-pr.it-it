---
description: La funzione MacTypeToAddressType converte un determinato tipo MAC in un tipo di indirizzo.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Funzione MacTypeToAddressType (Netmon.h)
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
ms.openlocfilehash: fe02cb6f0bec62a3bda35eabe288eafc2d5c3c15e422b7d68dc0b488546b83b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742321"
---
# <a name="mactypetoaddresstype-function"></a>Funzione MacTypeToAddressType

La **funzione MacTypeToAddressType** converte un determinato tipo MAC in un tipo di indirizzo.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MacType* \[ Pollici\]
</dt> <dd>

Tipo MAC da convertire. Specificare uno dei valori seguenti:

TIPO MAC \_ \_ ETHERNET MAC \_ TYPE \_ TOKENRING MAC \_ TYPE \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è uno dei tipi di indirizzo seguenti.

TIPO \_ DI \_ INDIRIZZO ETHERNET TIPO \_ \_ TOKENRING ADDRESS TYPE \_ \_ FDDI

Se la funzione ha esito negativo, il tipo MAC è sconosciuto, il valore restituito è -1.

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione MacTypeToAddressType.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




