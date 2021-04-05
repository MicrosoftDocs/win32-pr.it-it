---
description: Questo esempio crea un pool di thread personalizzato, crea un elemento di lavoro e un timer del pool di thread e li associa a un gruppo di pulitura. Il pool è costituito da un thread permanente.
ms.assetid: 3d349c83-8b1a-4a5b-9625-be905d613b92
title: Uso delle funzioni del pool di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4492913af54241c3480f6550af7e943e31495a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131662"
---
# <a name="using-the-thread-pool-functions"></a><span data-ttu-id="0422b-104">Uso delle funzioni del pool di thread</span><span class="sxs-lookup"><span data-stu-id="0422b-104">Using the Thread Pool Functions</span></span>

<span data-ttu-id="0422b-105">Questo esempio crea un pool di thread personalizzato, crea un elemento di lavoro e un timer del pool di thread e li associa a un gruppo di pulitura.</span><span class="sxs-lookup"><span data-stu-id="0422b-105">This example creates a custom thread pool, creates a work item and a thread pool timer, and associates them with a cleanup group.</span></span> <span data-ttu-id="0422b-106">Il pool è costituito da un thread permanente.</span><span class="sxs-lookup"><span data-stu-id="0422b-106">The pool consists of one persistent thread.</span></span> <span data-ttu-id="0422b-107">Viene illustrato l'utilizzo delle funzioni del pool di thread seguenti:</span><span class="sxs-lookup"><span data-stu-id="0422b-107">It demonstrates the use of the following thread pool functions:</span></span>

-   [<span data-ttu-id="0422b-108">**CloseThreadpool**</span><span class="sxs-lookup"><span data-stu-id="0422b-108">**CloseThreadpool**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)
-   [<span data-ttu-id="0422b-109">**CloseThreadpoolCleanupGroup**</span><span class="sxs-lookup"><span data-stu-id="0422b-109">**CloseThreadpoolCleanupGroup**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)
-   [<span data-ttu-id="0422b-110">**CloseThreadpoolCleanupGroupMembers**</span><span class="sxs-lookup"><span data-stu-id="0422b-110">**CloseThreadpoolCleanupGroupMembers**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)
-   [<span data-ttu-id="0422b-111">**CloseThreadpoolWait**</span><span class="sxs-lookup"><span data-stu-id="0422b-111">**CloseThreadpoolWait**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)
-   [<span data-ttu-id="0422b-112">**CreateThreadpool**</span><span class="sxs-lookup"><span data-stu-id="0422b-112">**CreateThreadpool**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)
-   [<span data-ttu-id="0422b-113">**CreateThreadpoolCleanupGroup**</span><span class="sxs-lookup"><span data-stu-id="0422b-113">**CreateThreadpoolCleanupGroup**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)
-   [<span data-ttu-id="0422b-114">**CreateThreadpoolTimer**</span><span class="sxs-lookup"><span data-stu-id="0422b-114">**CreateThreadpoolTimer**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)
-   [<span data-ttu-id="0422b-115">**CreateThreadpoolWait**</span><span class="sxs-lookup"><span data-stu-id="0422b-115">**CreateThreadpoolWait**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)
-   [<span data-ttu-id="0422b-116">**CreateThreadpoolWork**</span><span class="sxs-lookup"><span data-stu-id="0422b-116">**CreateThreadpoolWork**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)
-   [<span data-ttu-id="0422b-117">**InitializeThreadpoolEnvironment**</span><span class="sxs-lookup"><span data-stu-id="0422b-117">**InitializeThreadpoolEnvironment**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)
-   [<span data-ttu-id="0422b-118">**SetThreadpoolCallbackCleanupGroup**</span><span class="sxs-lookup"><span data-stu-id="0422b-118">**SetThreadpoolCallbackCleanupGroup**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)
-   [<span data-ttu-id="0422b-119">**SetThreadpoolCallbackPool**</span><span class="sxs-lookup"><span data-stu-id="0422b-119">**SetThreadpoolCallbackPool**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)
-   [<span data-ttu-id="0422b-120">**SetThreadpoolThreadMaximum**</span><span class="sxs-lookup"><span data-stu-id="0422b-120">**SetThreadpoolThreadMaximum**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)
-   [<span data-ttu-id="0422b-121">**SetThreadpoolThreadMinimum**</span><span class="sxs-lookup"><span data-stu-id="0422b-121">**SetThreadpoolThreadMinimum**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)
-   [<span data-ttu-id="0422b-122">**SetThreadpoolTimer**</span><span class="sxs-lookup"><span data-stu-id="0422b-122">**SetThreadpoolTimer**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)
-   [<span data-ttu-id="0422b-123">**SetThreadpoolWait**</span><span class="sxs-lookup"><span data-stu-id="0422b-123">**SetThreadpoolWait**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)
-   [<span data-ttu-id="0422b-124">**SubmitThreadpoolWork**</span><span class="sxs-lookup"><span data-stu-id="0422b-124">**SubmitThreadpoolWork**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)
-   [<span data-ttu-id="0422b-125">**WaitForThreadpoolWaitCallbacks**</span><span class="sxs-lookup"><span data-stu-id="0422b-125">**WaitForThreadpoolWaitCallbacks**</span></span>](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

//
// Thread pool wait callback function template
//
VOID
CALLBACK
MyWaitCallback(
    PTP_CALLBACK_INSTANCE Instance,
    PVOID                 Parameter,
    PTP_WAIT              Wait,
    TP_WAIT_RESULT        WaitResult
    )
{
    // Instance, Parameter, Wait, and WaitResult not used in this example.
    UNREFERENCED_PARAMETER(Instance);
    UNREFERENCED_PARAMETER(Parameter);
    UNREFERENCED_PARAMETER(Wait);
    UNREFERENCED_PARAMETER(WaitResult);

    //
    // Do something when the wait is over.
    //
    _tprintf(_T("MyWaitCallback: wait is over.\n"));
}


//
// Thread pool timer callback function template
//
VOID
CALLBACK
MyTimerCallback(
    PTP_CALLBACK_INSTANCE Instance,
    PVOID                 Parameter,
    PTP_TIMER             Timer
    )
{
    // Instance, Parameter, and Timer not used in this example.
    UNREFERENCED_PARAMETER(Instance);
    UNREFERENCED_PARAMETER(Parameter);
    UNREFERENCED_PARAMETER(Timer);

    //
    // Do something when the timer fires.
    //
    _tprintf(_T("MyTimerCallback: timer has fired.\n"));

}


//
// This is the thread pool work callback function.
//
VOID
CALLBACK
MyWorkCallback(
    PTP_CALLBACK_INSTANCE Instance,
    PVOID                 Parameter,
    PTP_WORK              Work
    )
{
    // Instance, Parameter, and Work not used in this example.
    UNREFERENCED_PARAMETER(Instance);
    UNREFERENCED_PARAMETER(Parameter);
    UNREFERENCED_PARAMETER(Work);

    BOOL bRet = FALSE;
 
    //
    // Do something when the work callback is invoked.
    //
     {
         _tprintf(_T("MyWorkCallback: Task performed.\n"));
     }

    return;
}

VOID
DemoCleanupPersistentWorkTimer()
{
    BOOL bRet = FALSE;
    PTP_WORK work = NULL;
    PTP_TIMER timer = NULL;
    PTP_POOL pool = NULL;
    PTP_WORK_CALLBACK workcallback = MyWorkCallback;
    PTP_TIMER_CALLBACK timercallback = MyTimerCallback;
    TP_CALLBACK_ENVIRON CallBackEnviron;
    PTP_CLEANUP_GROUP cleanupgroup = NULL;
    FILETIME FileDueTime;
    ULARGE_INTEGER ulDueTime;
    UINT rollback = 0;

    InitializeThreadpoolEnvironment(&CallBackEnviron);

    //
    // Create a custom, dedicated thread pool.
    //
    pool = CreateThreadpool(NULL);

    if (NULL == pool) {
        _tprintf(_T("CreateThreadpool failed. LastError: %u\n"),
                     GetLastError());
        goto main_cleanup;
    }

    rollback = 1; // pool creation succeeded

    //
    // The thread pool is made persistent simply by setting
    // both the minimum and maximum threads to 1.
    //
    SetThreadpoolThreadMaximum(pool, 1);

    bRet = SetThreadpoolThreadMinimum(pool, 1);

    if (FALSE == bRet) {
        _tprintf(_T("SetThreadpoolThreadMinimum failed. LastError: %u\n"),
                     GetLastError());
        goto main_cleanup;
    }

    //
    // Create a cleanup group for this thread pool.
    //
    cleanupgroup = CreateThreadpoolCleanupGroup();

    if (NULL == cleanupgroup) {
        _tprintf(_T("CreateThreadpoolCleanupGroup failed. LastError: %u\n"), 
                     GetLastError());
        goto main_cleanup; 
    }

    rollback = 2;  // Cleanup group creation succeeded

    //
    // Associate the callback environment with our thread pool.
    //
    SetThreadpoolCallbackPool(&CallBackEnviron, pool);

    //
    // Associate the cleanup group with our thread pool.
    // Objects created with the same callback environment
    // as the cleanup group become members of the cleanup group.
    //
    SetThreadpoolCallbackCleanupGroup(&CallBackEnviron,
                                      cleanupgroup,
                                      NULL);

    //
    // Create work with the callback environment.
    //
    work = CreateThreadpoolWork(workcallback,
                                NULL, 
                                &CallBackEnviron);

    if (NULL == work) {
        _tprintf(_T("CreateThreadpoolWork failed. LastError: %u\n"),
                     GetLastError());
        goto main_cleanup;
    }

    rollback = 3;  // Creation of work succeeded

    //
    // Submit the work to the pool. Because this was a pre-allocated
    // work item (using CreateThreadpoolWork), it is guaranteed to execute.
    //
    SubmitThreadpoolWork(work);


    //
    // Create a timer with the same callback environment.
    //
    timer = CreateThreadpoolTimer(timercallback,
                                  NULL,
                                  &CallBackEnviron);


    if (NULL == timer) {
        _tprintf(_T("CreateThreadpoolTimer failed. LastError: %u\n"),
                     GetLastError());
        goto main_cleanup;
    }

    rollback = 4;  // Timer creation succeeded

    //
    // Set the timer to fire in one second.
    //
    ulDueTime.QuadPart = (ULONGLONG) -(1 * 10 * 1000 * 1000);
    FileDueTime.dwHighDateTime = ulDueTime.HighPart;
    FileDueTime.dwLowDateTime  = ulDueTime.LowPart;

    SetThreadpoolTimer(timer,
                       &FileDueTime,
                       0,
                       0);

    //
    // Delay for the timer to be fired
    //
    Sleep(1500);

    //
    // Wait for all callbacks to finish.
    // CloseThreadpoolCleanupGroupMembers also releases objects
    // that are members of the cleanup group, so it is not necessary 
    // to call close functions on individual objects 
    // after calling CloseThreadpoolCleanupGroupMembers.
    //
    CloseThreadpoolCleanupGroupMembers(cleanupgroup,
                                       FALSE,
                                       NULL);

    //
    // Already cleaned up the work item with the
    // CloseThreadpoolCleanupGroupMembers, so set rollback to 2.
    //
    rollback = 2;
    goto main_cleanup;

main_cleanup:
    //
    // Clean up any individual pieces manually
    // Notice the fall-through structure of the switch.
    // Clean up in reverse order.
    //

    switch (rollback) {
        case 4:
        case 3:
            // Clean up the cleanup group members.
            CloseThreadpoolCleanupGroupMembers(cleanupgroup,
                FALSE, NULL);
        case 2:
            // Clean up the cleanup group.
            CloseThreadpoolCleanupGroup(cleanupgroup);

        case 1:
            // Clean up the pool.
            CloseThreadpool(pool);

        default:
            break;
    }

    return;
}

VOID
DemoNewRegisterWait()
{
    PTP_WAIT Wait = NULL;
    PTP_WAIT_CALLBACK waitcallback = MyWaitCallback;
    HANDLE hEvent = NULL;
    UINT i = 0;
    UINT rollback = 0;

    //
    // Create an auto-reset event.
    //
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (NULL == hEvent) {
        // Error Handling
        return;
    }

    rollback = 1; // CreateEvent succeeded

    Wait = CreateThreadpoolWait(waitcallback,
                                NULL,
                                NULL);

    if(NULL == Wait) {
        _tprintf(_T("CreateThreadpoolWait failed. LastError: %u\n"),
                     GetLastError());
        goto new_wait_cleanup;
    }

    rollback = 2; // CreateThreadpoolWait succeeded

    //
    // Need to re-register the event with the wait object
    // each time before signaling the event to trigger the wait callback.
    //
    for (i = 0; i < 5; i ++) {
        SetThreadpoolWait(Wait,
                          hEvent,
                          NULL);

        SetEvent(hEvent);

        //
        // Delay for the waiter thread to act if necessary.
        //
        Sleep(500);

        //
        // Block here until the callback function is done executing.
        //

        WaitForThreadpoolWaitCallbacks(Wait, FALSE);
    }

new_wait_cleanup:
    switch (rollback) {
        case 2:
            // Unregister the wait by setting the event to NULL.
            SetThreadpoolWait(Wait, NULL, NULL);

            // Close the wait.
            CloseThreadpoolWait(Wait);

        case 1:
            // Close the event.
            CloseHandle(hEvent);

        default:
            break;
    }
    return;
}

int main( void)
{
    DemoNewRegisterWait();
    DemoCleanupPersistentWorkTimer();
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="0422b-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0422b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0422b-127">Pool di thread</span><span class="sxs-lookup"><span data-stu-id="0422b-127">Thread Pools</span></span>](thread-pools.md)
</dt> </dl>

 

 
