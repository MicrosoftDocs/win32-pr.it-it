---
description: La funzione ExpertAllocMemory alloca memoria per l'esperto.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Funzione ExpertAllocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750106"
---
# <a name="expertallocmemory-function"></a>ExpertAllocMemory (funzione)

La funzione **ExpertAllocMemory** alloca memoria per l'esperto.

## <a name="syntax"></a>Sintassi


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .

</dd> <dt>

*nBytes* \[ in\]
</dt> <dd>

Memoria allocata, misurata in byte.

</dd> <dt>

*perror* \[ out\]
</dt> <dd>

Indicatore di errore. Se la funzione ha esito negativo, il parametro *nBytes* contiene il codice di errore. Se il codice di errore è NMERR \_ Expert \_ Terminate, l'esperto deve effettuare la pulizia e restituire immediatamente un risultato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata.

Se la funzione ha esito negativo, il valore restituito è **null** e *perror* fornisce un codice di errore che indica il motivo dell'errore.

## <a name="remarks"></a>Commenti

È importante notare che un esperto deve usare le funzioni di allocazione della memoria Network Monitor (incluso [ExpertReallocMemory](expertreallocmemory.md)) per la gestione della memoria. Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor di liberare la memoria allocata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




