---
description: La funzione CCHeapFree rilascia la memoria allocata dalla funzione CCHeapAlloc.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Funzione CCHeapFree (Netmon. h)
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
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131859"
---
# <a name="ccheapfree-function"></a>CCHeapFree (funzione)

La funzione **CCHeapFree** rilascia la memoria allocata dalla funzione **CCHeapAlloc** .

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

Se la funzione **CCHeapFree** ha esito positivo, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
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

 

 




