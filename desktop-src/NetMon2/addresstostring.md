---
description: La funzione AddressToString converte un indirizzo in una stringa.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Funzione AddressToString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131995"
---
# <a name="addresstostring-function"></a>AddressToString (funzione)

La funzione **AddressToString** converte un indirizzo in una stringa.

## <a name="syntax"></a>Sintassi


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*stringa* \[ di out\]
</dt> <dd>

Stringa in cui viene convertito l'indirizzo.

</dd> <dt>

*lpAddress* \[ in\]
</dt> <dd>

Indirizzo stampato.

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



 

 




