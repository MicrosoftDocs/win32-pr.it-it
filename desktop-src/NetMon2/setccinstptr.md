---
description: La funzione SetCCInstPtr acquisisce un puntatore all'istanza del contesto.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Funzione SetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526754"
---
# <a name="setccinstptr-function"></a>SetCCInstPtr (funzione)

La funzione **SetCCInstPtr** acquisisce un puntatore all'istanza del contesto.

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpCurCaptureInst* 
</dt> <dd>

Puntatore ai dati dell'istanza aggiunti all'acquisizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

Utilizzare questa funzione per archiviare un puntatore a un blocco allocato con la funzione **CCHeapAlloc** . Ogni parser può impostare una singola istanza di dati in un'acquisizione.

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

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




