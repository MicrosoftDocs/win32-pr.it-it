---
description: La funzione SvcMain nell'esempio seguente è la funzione ServiceMain per il servizio di esempio.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Scrittura di una funzione ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca28b09efdc228457ae85d8a3343f334a26f246b6e48e49208d7416551e7f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887974"
---
# <a name="writing-a-servicemain-function"></a>Scrittura di una funzione ServiceMain

La funzione SvcMain nell'esempio seguente è la [**funzione ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) per il servizio di esempio. SvcMain ha accesso agli argomenti della riga di comando per il servizio come la **funzione** principale di un'applicazione console. Il primo parametro contiene il numero di argomenti passati al servizio nel secondo parametro. Sarà sempre presente almeno un argomento. Il secondo parametro è un puntatore a una matrice di puntatori di stringa. Il primo elemento nella matrice è sempre il nome del servizio.

La funzione SvcMain chiama prima di tutto la funzione [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) per registrare la funzione SvcCtrlHandler come funzione [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) del servizio e avviare l'inizializzazione. **RegisterServiceCtrlHandler** deve essere la prima funzione non funzionante in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) in modo che il servizio possa usare l'handle di stato restituito da questa funzione per chiamare [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con lo stato SERVICE STOPPED se si verifica un \_ errore.

Successivamente, la funzione SvcMain chiama la funzione ReportSvcStatus per indicare che lo stato iniziale è SERVICE \_ START \_ PENDING. Mentre il servizio si trova in questo stato, non viene accettato alcun controllo. Per semplificare la logica del servizio, è consigliabile che il servizio non accetti alcun controllo durante l'inizializzazione.

Infine, la funzione SvcMain chiama la funzione SvcInit per eseguire l'inizializzazione specifica del servizio e iniziare il lavoro che deve essere eseguito dal servizio.

La funzione di inizializzazione di esempio, SvcInit, è un esempio molto semplice. non esegue attività di inizializzazione più complesse, ad esempio la creazione di thread aggiuntivi. Crea un evento che il gestore del controllo del servizio può segnalare per indicare che il servizio deve arrestarsi, quindi chiama ReportSvcStatus per indicare che il servizio è nello stato SERVICE \_ RUNNING. A questo punto, il servizio ha completato l'inizializzazione ed è pronto ad accettare i controlli. Per ottenere prestazioni di sistema ottimali, l'applicazione deve entrare nello stato di esecuzione entro 25-100 millisecondi.

Poiché questo servizio di esempio non completa alcuna attività reale, SvcInit attende semplicemente che l'evento di arresto del servizio sia segnalato chiamando la funzione [**WaitForSingleObject,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) chiama ReportSvcStatus per indicare che il servizio è nello stato SERVICE STOPPED e restituisce \_ . Si noti che è importante che la funzione restituirà anziché chiamare la funzione [**ExitThread,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) perché la restituzione di consente la pulizia della memoria allocata per gli argomenti. È possibile eseguire attività di pulizia aggiuntive usando la [**funzione RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) anziché **WaitForSingleObject**. Il thread che esegue la [**funzione ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) termina, ma l'esecuzione del servizio stesso continua. Quando il gestore del controllo del servizio segnala l'evento, un thread del pool di thread esegue il callback per eseguire la pulizia aggiuntiva, inclusa l'impostazione dello stato su SERVICE \_ STOPPED.

Si noti che in questo esempio viene utilizzato SvcReportEvent per scrivere gli eventi di errore nel registro eventi. Per il codice sorgente per SvcReportEvent, vedere [Svc.cpp.](svc-cpp.md) Per una funzione del gestore di controllo di esempio, vedere [Scrittura di una funzione del gestore del controllo](writing-a-control-handler-function.md).

In questo esempio vengono usate le definizioni globali seguenti.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



Il frammento di esempio seguente è tratto dall'esempio di servizio completo.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzione ServiceMain del servizio](service-servicemain-function.md)
</dt> <dt>

[Esempio di servizio completo](the-complete-service-sample.md)
</dt> </dl>

 

 
