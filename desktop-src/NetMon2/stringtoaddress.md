---
description: La funzione StringToAddress converte una stringa in un indirizzo.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Funzione StringToAddress (Netmon. h)
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
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310478"
---
# <a name="stringtoaddress-function"></a>StringToAddress (funzione)

La funzione **StringToAddress** converte una stringa in un indirizzo.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpAddress* \[ out\]
</dt> <dd>

Puntatore all'indirizzo in cui la stringa viene convertita.

</dd> <dt>

*stringa* \[ di in\]
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
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




