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
# <a name="using-one-time-initialization"></a><span data-ttu-id="3eac7-103">Utilizzo dell'inizializzazione One-Time</span><span class="sxs-lookup"><span data-stu-id="3eac7-103">Using One-Time Initialization</span></span>

<span data-ttu-id="3eac7-104">Negli esempi seguenti viene illustrato l'utilizzo delle funzioni di inizializzazione una sola volta.</span><span class="sxs-lookup"><span data-stu-id="3eac7-104">The following examples demonstrate the use of the one-time initialization functions.</span></span>

## <a name="synchronous-example"></a><span data-ttu-id="3eac7-105">Esempio sincrono</span><span class="sxs-lookup"><span data-stu-id="3eac7-105">Synchronous Example</span></span>

<span data-ttu-id="3eac7-106">In questo esempio la `g_InitOnce` variabile globale è la struttura di inizializzazione unica.</span><span class="sxs-lookup"><span data-stu-id="3eac7-106">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="3eac7-107">Viene inizializzata in modo statico usando **init \_ una volta \_ static \_ init**.</span><span class="sxs-lookup"><span data-stu-id="3eac7-107">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="3eac7-108">La `OpenEventHandleSync` funzione restituisce un handle a un evento che viene creato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="3eac7-108">The `OpenEventHandleSync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="3eac7-109">Chiama la funzione [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) per eseguire il codice di inizializzazione contenuto nella `InitHandleFunction` funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="3eac7-109">It calls the [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) function to execute the initialization code contained in the `InitHandleFunction` callback function.</span></span> <span data-ttu-id="3eac7-110">Se la funzione di callback ha esito positivo, `OpenEventHandleSync` restituisce l'handle di evento restituito in *lpContext*; in caso contrario, restituisce un **\_ \_ valore di handle non valido**.</span><span class="sxs-lookup"><span data-stu-id="3eac7-110">If the callback function succeeds, `OpenEventHandleSync` returns the event handle returned in *lpContext*; otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="3eac7-111">La `InitHandleFunction` funzione è la [funzione di callback di inizializzazione unica](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span><span class="sxs-lookup"><span data-stu-id="3eac7-111">The `InitHandleFunction` function is the [one-time initialization callback function](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span></span> <span data-ttu-id="3eac7-112">`InitHandleFunction` chiama la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) per creare l'evento e restituisce l'handle dell'evento nel parametro *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="3eac7-112">`InitHandleFunction` calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and returns the event handle in the *lpContext* parameter.</span></span>


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



## <a name="asynchronous-example"></a><span data-ttu-id="3eac7-113">Esempio asincrono</span><span class="sxs-lookup"><span data-stu-id="3eac7-113">Asynchronous Example</span></span>

<span data-ttu-id="3eac7-114">In questo esempio la `g_InitOnce` variabile globale è la struttura di inizializzazione unica.</span><span class="sxs-lookup"><span data-stu-id="3eac7-114">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="3eac7-115">Viene inizializzata in modo statico usando **init \_ una volta \_ static \_ init**.</span><span class="sxs-lookup"><span data-stu-id="3eac7-115">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="3eac7-116">La `OpenEventHandleAsync` funzione restituisce un handle a un evento che viene creato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="3eac7-116">The `OpenEventHandleAsync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="3eac7-117">`OpenEventHandleAsync` chiama la funzione [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) per immettere lo stato di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="3eac7-117">`OpenEventHandleAsync` calls the [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) function to enter the initializing state.</span></span>

<span data-ttu-id="3eac7-118">Se la chiamata ha esito positivo, il codice controlla il valore del parametro *fPending* per determinare se creare l'evento o semplicemente restituire un handle all'evento creato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="3eac7-118">If the call succeeds, the code checks the value of the *fPending* parameter to determine whether to create the event or simply return a handle to the event created by another thread.</span></span> <span data-ttu-id="3eac7-119">Se *fPending* è **false**, l'inizializzazione è già stata completata, quindi `OpenEventHandleAsync` restituisce l'handle di evento restituito nel parametro *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="3eac7-119">If *fPending* is **FALSE**, initialization has already completed so `OpenEventHandleAsync` returns the event handle returned in the *lpContext* parameter.</span></span> <span data-ttu-id="3eac7-120">In caso contrario, chiama la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) per creare l'evento e la funzione [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) per completare l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="3eac7-120">Otherwise, it calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and the [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) function to complete the initialization.</span></span>

<span data-ttu-id="3eac7-121">Se la chiamata a [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) ha esito positivo, `OpenEventHandleAsync` restituisce il nuovo handle di evento.</span><span class="sxs-lookup"><span data-stu-id="3eac7-121">If the call to [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) succeeds, `OpenEventHandleAsync` returns the new event handle.</span></span> <span data-ttu-id="3eac7-122">In caso contrario, chiude l'handle di evento e chiama [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una sola volta \_ Check \_ solo** per determinare se l'inizializzazione non è riuscita o è stata completata da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="3eac7-122">Otherwise, it closes the event handle and calls [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) with **INIT\_ONCE\_CHECK\_ONLY** to determine whether initialization failed or was completed by another thread.</span></span>

<span data-ttu-id="3eac7-123">Se l'inizializzazione è stata completata da un altro thread, `OpenEventHandleAsync` restituisce l'handle di evento restituito in *lpContext*.</span><span class="sxs-lookup"><span data-stu-id="3eac7-123">If the initialization was completed by another thread, `OpenEventHandleAsync` returns the event handle returned in *lpContext*.</span></span> <span data-ttu-id="3eac7-124">In caso contrario, restituisce un **\_ \_ valore di handle non valido**.</span><span class="sxs-lookup"><span data-stu-id="3eac7-124">Otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3eac7-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3eac7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eac7-126">Inizializzazione unica</span><span class="sxs-lookup"><span data-stu-id="3eac7-126">One-Time Initialization</span></span>](one-time-initialization.md)
</dt> </dl>

 

 
