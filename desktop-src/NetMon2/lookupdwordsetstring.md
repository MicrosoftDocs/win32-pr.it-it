---
description: La funzione LookupDwordSetString restituisce la stringa corrispondente al valore specificato di un set con etichetta.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Funzione LookupDwordSetString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b72f21d47001e2060c3b27daa80a584dcad77b55fd1df289a5bdb5476549cf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677231"
---
# <a name="lookupdwordsetstring-function"></a>Funzione LookupDwordSetString

La **funzione LookupDwordSetString** restituisce la stringa corrispondente al valore specificato di un set con etichetta.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpSet* 
</dt> <dd>

Set con etichetta, da cui è possibile estrarre l'etichetta del valore.

</dd> <dt>

*Valore* 
</dt> <dd>

Valore di un set con etichetta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è la stringa corrispondente al valore specificato.

Se la funzione ha esito negativo, il valore specificato non è presente nel set, il valore restituito è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




