---
description: La funzione ExpertFreeMemory libera la memoria acquisita dalle chiamate alle funzioni ExpertAllocMemory ed ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Funzione ExpertFreeMemory (Netmon.h)
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
ms.openlocfilehash: edc4d1a9e33139372d0f397053d233a28c9e2445ba270a47e7dbfe97090eb6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890830"
---
# <a name="expertfreememory-function"></a>Funzione ExpertFreeMemory

La **funzione ExpertFreeMemory** libera la memoria acquisita dalle chiamate alle [**funzioni ExpertAllocMemory**](expertallocmemory.md) [**ed ExpertReallocMemory.**](expertreallocmemory.md)

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

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la [funzione](run.md) Run.

</dd> <dt>

*pMemory* \[ Pollici\]
</dt> <dd>

Puntatore alla memoria allocata Network Monitor memoria. Il *puntatore pMemory* può essere restituito da una chiamata precedente a [**ExpertAllocMemory**](expertallocmemory.md) o [**ExpertReallocMemory**](expertreallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo. il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore. Se il valore restituito è NMERR \_ EXPERT \_ TERMINATE, l'esperto pulisce e restituisce immediatamente .

## <a name="remarks"></a>Commenti

È importante notare che un esperto deve usare le Network Monitor di allocazione della memoria per la gestione della memoria. Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor liberare la memoria allocata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




