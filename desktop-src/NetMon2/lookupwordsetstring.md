---
description: La funzione LookupWordSetString restituisce la stringa corrispondente al valore richiesto da un set con etichetta.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Funzione LookupWordSetString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 15b529076660eec093df370df47823fb21aa13e53cce61565fe82de7fbb7e017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364719"
---
# <a name="lookupwordsetstring-function"></a>Funzione LookupWordSetString

La **funzione LookupWordSetString** restituisce la stringa corrispondente al valore richiesto da un set con etichetta.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpSet* 
</dt> <dd>

Set con etichetta da cui si estrae l'etichetta del valore.

</dd> <dt>

*Valore* 
</dt> <dd>

Valore di un set con etichetta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è una stringa che corrisponde al valore richiesto.

Se la funzione ha esito negativo, il valore specificato non è presente nel set, il valore restituito è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




