---
description: Negli esempi seguenti viene illustrato l'utilizzo delle funzioni di inizializzazione una sola volta.
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: Utilizzo dell'inizializzazione One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f89cbe0e2d3e7c45d4f18863533c8c161037ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529767"
---
# <a name="using-one-time-initialization"></a>Utilizzo dell'inizializzazione One-Time

Negli esempi seguenti viene illustrato l'utilizzo delle funzioni di inizializzazione una sola volta.

## <a name="synchronous-example"></a>Esempio sincrono

In questo esempio la `g_InitOnce` variabile globale è la struttura di inizializzazione unica. Viene inizializzata in modo statico usando **init \_ una volta \_ static \_ init**.

La `OpenEventHandleSync` funzione restituisce un handle a un evento che viene creato una sola volta. Chiama la funzione [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) per eseguire il codice di inizializzazione contenuto nella `InitHandleFunction` funzione di callback. Se la funzione di callback ha esito positivo, `OpenEventHandleSync` restituisce l'handle di evento restituito in *lpContext*; in caso contrario, restituisce un **\_ \_ valore di handle non valido**.

La `InitHandleFunction` funzione è la [funzione di callback di inizializzazione unica](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn). `InitHandleFunction` chiama la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) per creare l'evento e restituisce l'handle dell'evento nel parametro *lpContext* .


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Initialization callback function 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        
    PVOID Parameter,            
    PVOID *lpContext);           

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleSync()
{
  PVOID lpContext;
  BOOL  bStatus;
  
  // Execute the initialization callback function 
  bStatus = InitOnceExecuteOnce(&g_InitOnce,          // One-time initialization structure
                                InitHandleFunction,   // Pointer to initialization callback function
                                NULL,                 // Optional parameter to callback function (not used)
                                &lpContext);          // Receives pointer to event object stored in g_InitOnce

  // InitOnceExecuteOnce function succeeded. Return event object.
  if (bStatus)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return (INVALID_HANDLE_VALUE);
  }
}

// Initialization callback function that creates the event object 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        // Pointer to one-time initialization structure        
    PVOID Parameter,            // Optional parameter passed by InitOnceExecuteOnce            
    PVOID *lpContext)           // Receives pointer to event object           
{
  HANDLE hEvent;

  // Create event object
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return FALSE;
  }
  // Event object creation succeeded.
  else
  {
    *lpContext = hEvent;
    return TRUE;
  }
}
```



## <a name="asynchronous-example"></a>Esempio asincrono

In questo esempio la `g_InitOnce` variabile globale è la struttura di inizializzazione unica. Viene inizializzata in modo statico usando **init \_ una volta \_ static \_ init**.

La `OpenEventHandleAsync` funzione restituisce un handle a un evento che viene creato una sola volta. `OpenEventHandleAsync` chiama la funzione [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) per immettere lo stato di inizializzazione.

Se la chiamata ha esito positivo, il codice controlla il valore del parametro *fPending* per determinare se creare l'evento o semplicemente restituire un handle all'evento creato da un altro thread. Se *fPending* è **false**, l'inizializzazione è già stata completata, quindi `OpenEventHandleAsync` restituisce l'handle di evento restituito nel parametro *lpContext* . In caso contrario, chiama la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) per creare l'evento e la funzione [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) per completare l'inizializzazione.

Se la chiamata a [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) ha esito positivo, `OpenEventHandleAsync` restituisce il nuovo handle di evento. In caso contrario, chiude l'handle di evento e chiama [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una sola volta \_ Check \_ solo** per determinare se l'inizializzazione non è riuscita o è stata completata da un altro thread.

Se l'inizializzazione è stata completata da un altro thread, `OpenEventHandleAsync` restituisce l'handle di evento restituito in *lpContext*. In caso contrario, restituisce un **\_ \_ valore di handle non valido**.


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleAsync()
{
  PVOID  lpContext;
  BOOL   fStatus;
  BOOL   fPending;
  HANDLE hEvent;
  
  // Begin one-time initialization
  fStatus = InitOnceBeginInitialize(&g_InitOnce,       // Pointer to one-time initialization structure
                                    INIT_ONCE_ASYNC,   // Asynchronous one-time initialization
                                    &fPending,         // Receives initialization status
                                    &lpContext);       // Receives pointer to data in g_InitOnce  

  // InitOnceBeginInitialize function failed.
  if (!fStatus)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Initialization has already completed and lpContext contains event object.
  if (!fPending)
  {
    return (HANDLE)lpContext;
  }

  // Create event object for one-time initialization.
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Complete one-time initialization.
  fStatus = InitOnceComplete(&g_InitOnce,             // Pointer to one-time initialization structure
                             INIT_ONCE_ASYNC,         // Asynchronous initialization
                             (PVOID)hEvent);          // Pointer to event object to be stored in g_InitOnce

  // InitOnceComplete function succeeded. Return event object.
  if (fStatus)
  {
    return hEvent;
  }
  
  // Initialization has already completed. Free the local event.
  CloseHandle(hEvent);


  // Retrieve the final context data.
  fStatus = InitOnceBeginInitialize(&g_InitOnce,            // Pointer to one-time initialization structure
                                    INIT_ONCE_CHECK_ONLY,   // Check whether initialization is complete
                                    &fPending,              // Receives initialization status
                                    &lpContext);            // Receives pointer to event object in g_InitOnce
  
  // Initialization is complete. Return handle.
  if (fStatus && !fPending)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return INVALID_HANDLE_VALUE;
  }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione unica](one-time-initialization.md)
</dt> </dl>

 

 
