---
description: La funzione GetCCInstPtr restituisce il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Funzione GetCCInstPtr (Netmon. h)
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
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750090"
---
# <a name="getccinstptr-function"></a>GetCCInstPtr (funzione)

La funzione **GetCCInstPtr** restituisce il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.

## <a name="syntax"></a>Sintassi


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore ai dati dell'istanza di un'acquisizione specifica.

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

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




