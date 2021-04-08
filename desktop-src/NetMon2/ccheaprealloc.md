---
description: La funzione CCHeapReAlloc consente di riallocare la memoria allocata dalla funzione CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Funzione CCHeapReAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756452"
---
# <a name="ccheaprealloc-function"></a>CCHeapReAlloc (funzione)

La funzione **CCHeapReAlloc** consente di riallocare la memoria allocata dalla funzione **CCHeapAlloc** .

## <a name="syntax"></a>Sintassi


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpMem* 
</dt> <dd>

Puntatore alla memoria allocata originale.

</dd> <dt>

*dwBytes* 
</dt> <dd>

Dimensione della memoria riallocata, misurata in byte.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indica se la memoria riallocata è stata inizializzata. Se il valore del parametro è **true**, la nuova memoria riallocata viene inizializzata su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria riallocata.

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

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




