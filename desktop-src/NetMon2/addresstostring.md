---
description: La funzione AddressToString converte un indirizzo in una stringa.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Funzione AddressToString (Netmon.h)
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
ms.openlocfilehash: 58c105fb8fa646fbffcc7d7d4a3f1dad3a9cd86e7bb6ef8cc426dc982873f720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796371"
---
# <a name="addresstostring-function"></a>Funzione AddressToString

La **funzione AddressToString** converte un indirizzo in una stringa.

## <a name="syntax"></a>Sintassi


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*string* \[ Cambio\]
</dt> <dd>

Stringa in cui viene convertito l'indirizzo.

</dd> <dt>

*lpAddress* \[ Pollici\]
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
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




