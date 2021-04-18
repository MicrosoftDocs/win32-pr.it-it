---
description: La funzione SvcMain nell'esempio seguente è la funzione ServiceMain per il servizio di esempio.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Scrittura di una funzione ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3e947c356bad6c6d54395a671aa192c93de1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306524"
---
# <a name="writing-a-servicemain-function"></a><span data-ttu-id="4e616-103">Scrittura di una funzione ServiceMain</span><span class="sxs-lookup"><span data-stu-id="4e616-103">Writing a ServiceMain Function</span></span>

<span data-ttu-id="4e616-104">La funzione SvcMain nell'esempio seguente è la funzione [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) per il servizio di esempio.</span><span class="sxs-lookup"><span data-stu-id="4e616-104">The SvcMain function in the following example is the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function for the example service.</span></span> <span data-ttu-id="4e616-105">SvcMain ha accesso agli argomenti della riga di comando per il servizio nel modo in cui viene eseguita la funzione **principale** di un'applicazione console.</span><span class="sxs-lookup"><span data-stu-id="4e616-105">SvcMain has access to the command-line arguments for the service in the way that the **main** function of a console application does.</span></span> <span data-ttu-id="4e616-106">Il primo parametro contiene il numero di argomenti passati al servizio nel secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="4e616-106">The first parameter contains the number of arguments being passed to the service in the second parameter.</span></span> <span data-ttu-id="4e616-107">Sarà sempre presente almeno un argomento.</span><span class="sxs-lookup"><span data-stu-id="4e616-107">There will always be at least one argument.</span></span> <span data-ttu-id="4e616-108">Il secondo parametro è un puntatore a una matrice di puntatori di stringa.</span><span class="sxs-lookup"><span data-stu-id="4e616-108">The second parameter is a pointer to an array of string pointers.</span></span> <span data-ttu-id="4e616-109">Il primo elemento nella matrice è sempre il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e616-109">The first item in the array is always the service name.</span></span>

<span data-ttu-id="4e616-110">La funzione SvcMain chiama prima la funzione [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) per registrare la funzione SvcCtrlHandler come funzione del [**gestore**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) del servizio e iniziare l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="4e616-110">The SvcMain function first calls the [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) function to register the SvcCtrlHandler function as the service's [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function and begin initialization.</span></span> <span data-ttu-id="4e616-111">**RegisterServiceCtrlHandler** deve essere la prima funzione non di errore in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , in modo che il servizio possa usare l'handle di stato restituito da questa funzione per chiamare [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con lo \_ stato arrestato del servizio se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4e616-111">**RegisterServiceCtrlHandler** should be the first nonfailing function in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) so the service can use the status handle returned by this function to call [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) with the SERVICE\_STOPPED state if an error occurs.</span></span>

<span data-ttu-id="4e616-112">Successivamente, la funzione SvcMain chiama la funzione ReportSvcStatus per indicare che lo stato iniziale è servizio \_ avviato \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="4e616-112">Next, the SvcMain function calls the ReportSvcStatus function to indicate that its initial status is SERVICE\_START\_PENDING.</span></span> <span data-ttu-id="4e616-113">Mentre il servizio è in questo stato, non viene accettato alcun controllo.</span><span class="sxs-lookup"><span data-stu-id="4e616-113">While the service is in this state, no controls are accepted.</span></span> <span data-ttu-id="4e616-114">Per semplificare la logica del servizio, è consigliabile che il servizio non accetti alcun controllo mentre esegue l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="4e616-114">To simplify the logic of the service, it is recommended that the service not accept any controls while it is performing its initialization.</span></span>

<span data-ttu-id="4e616-115">Infine, la funzione SvcMain chiama la funzione SvcInit per eseguire l'inizializzazione specifica del servizio e iniziare il lavoro per l'esecuzione da parte del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e616-115">Finally, the SvcMain function calls the SvcInit function to perform the service-specific initialization and begin the work to be performed by the service.</span></span>

<span data-ttu-id="4e616-116">La funzione di inizializzazione di esempio, SvcInit, è un esempio molto semplice. non esegue attività di inizializzazione più complesse, ad esempio la creazione di thread aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="4e616-116">The sample initialization function, SvcInit, is a very simple example; it does not perform more complex initialization tasks such as creating additional threads.</span></span> <span data-ttu-id="4e616-117">Viene creato un evento che il gestore di controllo del servizio può segnalare per indicare che il servizio deve essere arrestato, quindi chiama ReportSvcStatus per indicare che il servizio è entrato nello stato di esecuzione del servizio \_ .</span><span class="sxs-lookup"><span data-stu-id="4e616-117">It creates an event that the service control handler can signal to indicate that the service should stop, then calls ReportSvcStatus to indicate that the service has entered the SERVICE\_RUNNING state.</span></span> <span data-ttu-id="4e616-118">A questo punto, il servizio ha completato l'inizializzazione ed è pronto ad accettare i controlli.</span><span class="sxs-lookup"><span data-stu-id="4e616-118">At this point, the service has completed its initialization and is ready to accept controls.</span></span> <span data-ttu-id="4e616-119">Per ottimizzare le prestazioni del sistema, l'applicazione deve immettere lo stato di esecuzione entro 25-100 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="4e616-119">For best system performance, your application should enter the running state within 25-100 milliseconds.</span></span>

<span data-ttu-id="4e616-120">Poiché questo servizio di esempio non completa attività reali, SvcInit semplicemente attende che l'evento di arresto del servizio venga segnalato chiamando la funzione [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) , chiama ReportSvcStatus per indicare che il servizio è \_ stato arrestato e restituisce.</span><span class="sxs-lookup"><span data-stu-id="4e616-120">Because this sample service does not complete any real tasks, SvcInit simply waits for the service stop event to be signaled by calling the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function, calls ReportSvcStatus to indicate that the service has entered the SERVICE\_STOPPED state, and returns.</span></span> <span data-ttu-id="4e616-121">Si noti che è importante che la funzione restituisca, anziché chiamare la funzione [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) , perché la restituzione consente la pulizia della memoria allocata per gli argomenti. È possibile eseguire attività di pulizia aggiuntive usando la funzione [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) anziché **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="4e616-121">(Note that it is important for the function to return, rather than call the [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) function, because returning allows for cleanup of the memory allocated for the arguments.) You can perform additional cleanup tasks by using the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) function instead of **WaitForSingleObject**.</span></span> <span data-ttu-id="4e616-122">Il thread che esegue la funzione [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) termina, ma il servizio stesso continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e616-122">The thread that is running the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function terminates, but the service itself continues to run.</span></span> <span data-ttu-id="4e616-123">Quando il gestore di controllo del servizio segnala l'evento, un thread del pool di thread esegue il callback per eseguire la pulizia aggiuntiva, inclusa l'impostazione dello stato su servizio \_ arrestato.</span><span class="sxs-lookup"><span data-stu-id="4e616-123">When the service control handler signals the event, a thread from the thread pool executes your callback to perform the additional cleanup, including setting the status to SERVICE\_STOPPED.</span></span>

<span data-ttu-id="4e616-124">Si noti che in questo esempio viene usato SvcReportEvent per scrivere eventi di errore nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="4e616-124">Note that this example uses SvcReportEvent to write error events to the event log.</span></span> <span data-ttu-id="4e616-125">Per il codice sorgente per SvcReportEvent, vedere [svc. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="4e616-125">For the source code for SvcReportEvent, see [Svc.cpp](svc-cpp.md).</span></span> <span data-ttu-id="4e616-126">Per una funzione di gestione del controllo di esempio, vedere [scrittura di una funzione](writing-a-control-handler-function.md)di gestione del controllo.</span><span class="sxs-lookup"><span data-stu-id="4e616-126">For an example control handler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span>

<span data-ttu-id="4e616-127">In questo esempio vengono utilizzate le seguenti definizioni globali.</span><span class="sxs-lookup"><span data-stu-id="4e616-127">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="4e616-128">Il frammento di esempio seguente viene tratto dall'esempio di servizio completo.</span><span class="sxs-lookup"><span data-stu-id="4e616-128">The following sample fragment is taken from the complete service sample.</span></span>


```C++
//
// Purpose: 
//   Entry point for the service
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None.
//
VOID WINAPI SvcMain( DWORD dwArgc, LPTSTR *lpszArgv )
{
    // Register the handler function for the service

    gSvcStatusHandle = RegisterServiceCtrlHandler( 
        SVCNAME, 
        SvcCtrlHandler);

    if( !gSvcStatusHandle )
    { 
        SvcReportEvent(TEXT("RegisterServiceCtrlHandler")); 
        return; 
    } 

    // These SERVICE_STATUS members remain as set here

    gSvcStatus.dwServiceType = SERVICE_WIN32_OWN_PROCESS; 
    gSvcStatus.dwServiceSpecificExitCode = 0;    

    // Report initial status to the SCM

    ReportSvcStatus( SERVICE_START_PENDING, NO_ERROR, 3000 );

    // Perform service-specific initialization and work.

    SvcInit( dwArgc, lpszArgv );
}

//
// Purpose: 
//   The service code
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None
//
VOID SvcInit( DWORD dwArgc, LPTSTR *lpszArgv)
{
    // TO_DO: Declare and set any required variables.
    //   Be sure to periodically call ReportSvcStatus() with 
    //   SERVICE_START_PENDING. If initialization fails, call
    //   ReportSvcStatus with SERVICE_STOPPED.

    // Create an event. The control handler function, SvcCtrlHandler,
    // signals this event when it receives the stop control code.

    ghSvcStopEvent = CreateEvent(
                         NULL,    // default security attributes
                         TRUE,    // manual reset event
                         FALSE,   // not signaled
                         NULL);   // no name

    if ( ghSvcStopEvent == NULL)
    {
        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }

    // Report running status when initialization is complete.

    ReportSvcStatus( SERVICE_RUNNING, NO_ERROR, 0 );

    // TO_DO: Perform work until service stops.

    while(1)
    {
        // Check whether to stop the service.

        WaitForSingleObject(ghSvcStopEvent, INFINITE);

        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }
}

//
// Purpose: 
//   Sets the current service status and reports it to the SCM.
//
// Parameters:
//   dwCurrentState - The current state (see SERVICE_STATUS)
//   dwWin32ExitCode - The system error code
//   dwWaitHint - Estimated time for pending operation, 
//     in milliseconds
// 
// Return value:
//   None
//
VOID ReportSvcStatus( DWORD dwCurrentState,
                      DWORD dwWin32ExitCode,
                      DWORD dwWaitHint)
{
    static DWORD dwCheckPoint = 1;

    // Fill in the SERVICE_STATUS structure.

    gSvcStatus.dwCurrentState = dwCurrentState;
    gSvcStatus.dwWin32ExitCode = dwWin32ExitCode;
    gSvcStatus.dwWaitHint = dwWaitHint;

    if (dwCurrentState == SERVICE_START_PENDING)
        gSvcStatus.dwControlsAccepted = 0;
    else gSvcStatus.dwControlsAccepted = SERVICE_ACCEPT_STOP;

    if ( (dwCurrentState == SERVICE_RUNNING) ||
           (dwCurrentState == SERVICE_STOPPED) )
        gSvcStatus.dwCheckPoint = 0;
    else gSvcStatus.dwCheckPoint = dwCheckPoint++;

    // Report the status of the service to the SCM.
    SetServiceStatus( gSvcStatusHandle, &gSvcStatus );
}

```



## <a name="related-topics"></a><span data-ttu-id="4e616-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e616-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e616-130">Funzione ServiceMain del servizio</span><span class="sxs-lookup"><span data-stu-id="4e616-130">Service ServiceMain Function</span></span>](service-servicemain-function.md)
</dt> <dt>

[<span data-ttu-id="4e616-131">Esempio di servizio completo</span><span class="sxs-lookup"><span data-stu-id="4e616-131">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
