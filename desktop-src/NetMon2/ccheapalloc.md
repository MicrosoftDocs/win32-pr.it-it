---
description: La funzione CCHeapAlloc alloca memoria in base a un'acquisizione.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Funzione CCHeapAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881442"
---
# <a name="ccheapalloc-function"></a>CCHeapAlloc (funzione)

La funzione **CCHeapAlloc** alloca memoria in base a un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwBytes* 
</dt> <dd>

Lunghezza della memoria richiesta allocata.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indica se la memoria allocata è stata inizializzata. Se il valore del parametro è **true**, la memoria allocata viene inizializzata su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata. Al termine dell'utilizzo della memoria allocata, liberare la memoria chiamando la funzione [**CCHeapFree**](ccheapfree.md) .

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

[**SetCCInstPtr**](setccinstptr.md)
</dt> <dt>

[**GetCCInstPtr**](getccinstptr.md)
</dt> <dt>

[**CCHeapFree**](ccheapfree.md)
</dt> <dt>

[**CCHeapReAlloc**](ccheaprealloc.md)
</dt> <dt>

[**CCHeapSize**](ccheapsize.md)
</dt> </dl>

 

 




