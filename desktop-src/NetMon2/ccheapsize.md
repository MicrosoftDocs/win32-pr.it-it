---
description: La funzione CCHeapSize restituisce le dimensioni della memoria allocata dalla funzione CCHeapAlloc.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Funzione CCHeapSize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314183"
---
# <a name="ccheapsize-function"></a>CCHeapSize (funzione)

La funzione **CCHeapSize** restituisce le dimensioni della memoria allocata dalla funzione **CCHeapAlloc** .

## <a name="syntax"></a>Sintassi


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpMem* 
</dt> <dd>

Puntatore alla memoria allocata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito corrisponde alla dimensione del blocco di memoria richiesto misurato in byte.

Se la funzione ha esito negativo, il valore restituito è **null**.

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

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> </dl>

 

 




