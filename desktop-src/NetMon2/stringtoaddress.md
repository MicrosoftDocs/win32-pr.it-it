---
description: La funzione StringToAddress converte una stringa in un indirizzo.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Funzione StringToAddress (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbac01f5df9d32a65fe5afb1c1437064f6dd0d4480c95dacd0fe8f7d58e2fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676691"
---
# <a name="stringtoaddress-function"></a>Funzione StringToAddress

La **funzione StringToAddress** converte una stringa in un indirizzo.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpAddress* \[ Cambio\]
</dt> <dd>

Puntatore all'indirizzo in cui viene convertita la stringa.

</dd> <dt>

*string* \[ Pollici\]
</dt> <dd>

Stringa convertita in un indirizzo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un puntatore alla stringa convertita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




