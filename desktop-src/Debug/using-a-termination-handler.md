---
description: Nell'esempio seguente viene illustrato come viene utilizzato un gestore di terminazione per garantire che le risorse vengano rilasciate quando viene terminata l'esecuzione di un corpo sorvegliato di codice.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Uso di un gestore di terminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966125"
---
# <a name="using-a-termination-handler"></a>Uso di un gestore di terminazione

Nell'esempio seguente viene illustrato come viene utilizzato un gestore di terminazione per garantire che le risorse vengano rilasciate quando viene terminata l'esecuzione di un corpo sorvegliato di codice. In questo caso, un thread utilizza la funzione [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) per attendere la proprietà di un oggetto della sezione critica. Al termine dell'esecuzione del codice protetto dalla sezione critica, il thread deve chiamare la funzione [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) per rendere disponibile l'oggetto sezione critica ad altri thread. L'utilizzo di un gestore di terminazione garantisce che questa operazione verrà eseguita. Per ulteriori informazioni, vedere [oggetti sezione critica](../sync/critical-section-objects.md).


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



 

 
