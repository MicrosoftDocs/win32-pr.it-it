---
description: La funzione ExpertAllocMemory alloca memoria per l'esperto.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Funzione ExpertAllocMemory (Netmon.h)
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
ms.openlocfilehash: fd932a5330baf687d5578bac4e4bfac77ad4f5bad0560263ab7f1e8832e61fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890851"
---
# <a name="expertallocmemory-function"></a>Funzione ExpertAllocMemory

La **funzione ExpertAllocMemory** alloca memoria per l'esperto.

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

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la [funzione Run.](run.md)

</dd> <dt>

*nBytes* \[ Pollici\]
</dt> <dd>

Memoria allocata, misurata in byte.

</dd> <dt>

*pError* \[ Cambio\]
</dt> <dd>

Indicatore di errore. Se la funzione ha esito negativo, *il parametro nBytes* contiene il codice di errore. Se il codice di errore è NMERR \_ EXPERT \_ TERMINATE, l'esperto deve eseguire la pulizia e restituire immediatamente un messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata.

Se la funzione ha esito negativo, il valore restituito è **NULL** e *pError* fornisce un codice di errore che indica il motivo dell'errore.

## <a name="remarks"></a>Commenti

È importante notare che un esperto deve usare le funzioni Network Monitor di allocazione della memoria [(incluso ExpertReallocMemory)](expertreallocmemory.md)per la gestione della memoria. Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor liberare la memoria allocata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




