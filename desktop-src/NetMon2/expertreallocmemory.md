---
description: La funzione ExpertReallocMemory consente di aumentare o diminuire la quantità di memoria allocata dal Network Monitor.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Funzione ExpertReallocMemory (Netmon. h)
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
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305946"
---
# <a name="expertreallocmemory-function"></a>ExpertReallocMemory (funzione)

La funzione **ExpertReallocMemory** consente di aumentare o diminuire la quantità di memoria allocata dal Network Monitor.

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

*hExpertKey* \[ in\]
</dt> <dd>

Identificatore univoco passato all'esperto in fase di [**esecuzione**](run.md) o [**configurazione**](configure.md).

</dd> <dt>

*pOriginalMemory* \[ in\]
</dt> <dd>

Puntatore alla memoria allocata dal Network Monitor. Il puntatore *pOriginalMemory* può essere restituito da una precedente chiamata a [**ExpertAllocMemory**](expertallocmemory.md) o **ExpertReallocMemory**.

</dd> <dt>

*nBytes* \[ in\]
</dt> <dd>

Dimensione della memoria riallocata.

</dd> <dt>

*perror* \[ out\]
</dt> <dd>

Al ritorno, un codice di errore se la funzione ha esito negativo. Se il codice di errore è NMERR \_ Expert \_ Terminate, l'esperto deve effettuare la pulizia e restituire immediatamente un risultato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata.

Se la funzione ha esito negativo, il valore restituito è **null** e *perror* (se è un valore non **null** ) indica il motivo dell'errore.

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



 

 




