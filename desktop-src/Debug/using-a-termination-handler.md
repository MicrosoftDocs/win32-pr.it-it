---
description: L'esempio seguente illustra come viene usato un gestore di terminazione per garantire che le risorse siano rilasciate quando termina l'esecuzione di un corpo di codice sorvegliato.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Uso di un gestore di terminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6fe2d2ba8a7b8443eb164571a42347ce6cfb7e99c44f90da25c6fd57863e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655081"
---
# <a name="using-a-termination-handler"></a>Uso di un gestore di terminazione

L'esempio seguente illustra come viene usato un gestore di terminazione per garantire che le risorse siano rilasciate quando termina l'esecuzione di un corpo di codice sorvegliato. In questo caso, un thread usa la [**funzione EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) per attendere la proprietà di un oggetto sezione critica. Al termine dell'esecuzione del codice protetto dalla sezione critica, il thread deve chiamare la funzione [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) per rendere disponibile l'oggetto sezione critica ad altri thread. L'uso di un gestore di terminazione garantisce che ciò si verifica. Per altre informazioni, vedere [oggetti sezione critica](../sync/critical-section-objects.md).


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
