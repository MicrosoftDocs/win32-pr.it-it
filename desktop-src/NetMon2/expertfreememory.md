---
description: La funzione ExpertFreeMemory libera la memoria acquisita dalle chiamate alle funzioni ExpertAllocMemory e ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Funzione ExpertFreeMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305950"
---
# <a name="expertfreememory-function"></a>ExpertFreeMemory (funzione)

La funzione **ExpertFreeMemory** libera la memoria acquisita dalle chiamate alle funzioni [**ExpertAllocMemory**](expertallocmemory.md) e [**ExpertReallocMemory**](expertreallocmemory.md) .

## <a name="syntax"></a>Sintassi


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .

</dd> <dt>

*pMemory* \[ in\]
</dt> <dd>

Puntatore alla memoria allocata da Network Monitor. Il puntatore *pMemory* può essere restituito da una precedente chiamata a [**ExpertAllocMemory**](expertallocmemory.md) o [**ExpertReallocMemory**](expertreallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo. il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore. Se il valore restituito è NMERR \_ Expert \_ Terminate, l'esperto viene immediatamente ripulito e restituito.

## <a name="remarks"></a>Commenti

È importante notare che un esperto deve usare le funzioni di allocazione della memoria Network Monitor per la gestione della memoria. Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor di liberare la memoria allocata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




