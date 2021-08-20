---
description: La funzione GetCCInstPtr restituisce il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Funzione GetCCInstPtr (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 08904de629260c82ef6f9cbc2b0a44724f3ca31d2b74ca7212356359f2563289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982379"
---
# <a name="getccinstptr-function"></a>Funzione GetCCInstPtr

La **funzione GetCCInstPtr** restituisce il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.

## <a name="syntax"></a>Sintassi


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore ai dati dell'istanza di un'acquisizione specifica.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




