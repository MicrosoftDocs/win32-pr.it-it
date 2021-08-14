---
description: La funzione CCHeapFree rilascia la memoria allocata dalla funzione CCHeapAlloc.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Funzione CCHeapFree (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b29d57c3d56136103fb1948340472343f56727c2df0268a5036dc148fdd0493a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796341"
---
# <a name="ccheapfree-function"></a>Funzione CCHeapFree

La **funzione CCHeapFree** rilascia la memoria allocata dalla **funzione CCHeapAlloc.**

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpMem* 
</dt> <dd>

Puntatore alla memoria rilasciata da questa funzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la **funzione CCHeapFree** ha esito positivo, il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

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

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




