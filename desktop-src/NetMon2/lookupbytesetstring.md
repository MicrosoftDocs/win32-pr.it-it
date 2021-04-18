---
description: La funzione LookupByteSetString restituisce la stringa corrispondente al valore specificato di un set con etichetta.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Funzione LookupByteSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307716"
---
# <a name="lookupbytesetstring-function"></a>LookupByteSetString (funzione)

La funzione **LookupByteSetString** restituisce la stringa corrispondente al valore specificato di un set con etichetta.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpSet* 
</dt> <dd>

Puntatore a un set con etichetta, da cui è possibile estrarre l'etichetta del valore.

</dd> <dt>

*Valore* 
</dt> <dd>

Valore di un set con etichetta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è una stringa che corrisponde al valore specificato.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




