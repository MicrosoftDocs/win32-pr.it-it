---
description: La funzione ExpertReallocMemory aumenta o riduce la quantità di memoria allocata Network Monitor.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Funzione ExpertReallocMemory (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be43fa99021ec5612a148ba42db1b11e1fd6d885fa64fa003c0dfa672688d555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012259"
---
# <a name="expertreallocmemory-function"></a>Funzione ExpertReallocMemory

La **funzione ExpertReallocMemory** aumenta o riduce la quantità di memoria allocata Network Monitor.

## <a name="syntax"></a>Sintassi


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ Pollici\]
</dt> <dd>

Identificatore univoco passato all'esperto in [**Eseguire**](run.md) o [**configurare**](configure.md).

</dd> <dt>

*pOriginalMemory* \[ Pollici\]
</dt> <dd>

Puntatore alla memoria allocata da Network Monitor. Il *puntatore pOriginalMemory* può essere restituito da una chiamata precedente a [**ExpertAllocMemory**](expertallocmemory.md) **o ExpertReallocMemory.**

</dd> <dt>

*nBytes* \[ Pollici\]
</dt> <dd>

Dimensione della memoria riallocata.

</dd> <dt>

*pError* \[ Cambio\]
</dt> <dd>

Al ritorno, un codice di errore se la funzione ha esito negativo. Se il codice di errore è NMERR \_ EXPERT \_ TERMINATE, l'esperto deve eseguire la pulizia e restituire immediatamente un messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata.

Se la funzione ha esito negativo, il valore restituito è **NULL** e *pError* (se è un valore diverso da **NULL)** indica il motivo dell'errore.

## <a name="remarks"></a>Commenti

È importante notare che un esperto deve usare le funzioni di Network Monitor di allocazione della memoria per la gestione della memoria. Se l'esperto non riesce in fase di esecuzione, l'uso di queste funzioni consentirà Network Monitor liberare la memoria allocata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




