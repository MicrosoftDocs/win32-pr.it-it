---
description: Recupera il numero del processore su cui era in esecuzione il thread corrente durante la chiamata a questa funzione.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Funzione NtGetCurrentProcessorNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: f45ee39e9599e2d77d77131eb64c2a9037de1f4ba31f907ac5c9ea562a706c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032191"
---
# <a name="ntgetcurrentprocessornumber-function"></a>Funzione NtGetCurrentProcessorNumber

\[**NtGetCurrentProcessorNumber** può essere modificato o non disponibile nelle versioni future di Windows. Le applicazioni devono invece [**usare la funzione GetCurrentProcessorNumber.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)\]

Recupera il numero del processore su cui era in esecuzione il thread corrente durante la chiamata a questa funzione.

## <a name="syntax"></a>Sintassi


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

La funzione restituisce il numero del processore corrente.

## <a name="remarks"></a>Commenti

Questa funzione viene usata per fornire informazioni per stimare le prestazioni del processo.

A questa funzione non è associata alcuna libreria di importazione. È necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori multipli](multiple-processors.md)
</dt> <dt>

[Funzioni di processi e thread](process-and-thread-functions.md)
</dt> <dt>

[Processi](child-processes.md)
</dt> </dl>

 

 
