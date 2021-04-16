---
description: L'esempio seguente può essere usato come punto di ingresso per un programma di servizio che supporta un singolo servizio.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Scrittura di una funzione principale di un programma di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525807"
---
# <a name="writing-a-service-programs-main-function"></a>Scrittura della funzione principale di un programma del servizio

La funzione **principale** di un [programma del servizio](service-programs.md) chiama la funzione [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) per connettersi a [Gestione controllo servizi](service-control-manager.md) (SCM) e avviare il thread del dispatcher del controllo. Il thread del dispatcher esegue il ciclo in attesa delle richieste di controllo in ingresso per i servizi specificati nella tabella dispatch. Questo thread restituisce quando si verifica un errore o quando tutti i servizi nel processo sono stati terminati. Quando tutti i servizi del processo sono stati interrotti, il gestore SCM invia una richiesta di controllo al thread del dispatcher che indica di uscire. Questo thread restituisce quindi dalla chiamata **Impossibile eseguire StartServiceCtrlDispatcher** e il processo può terminare.

In questo esempio vengono utilizzate le seguenti definizioni globali.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



L'esempio seguente può essere usato come punto di ingresso per un programma di servizio che supporta un singolo servizio. Se il programma del servizio supporta più servizi, aggiungere i nomi dei servizi aggiuntivi alla tabella dispatch in modo che possano essere monitorati dal thread del dispatcher.

La \_ funzione tmain è il punto di ingresso. La funzione SvcReportEvent scrive messaggi informativi ed errori nel registro eventi. Per informazioni sulla scrittura della funzione SvcMain, vedere [scrittura di una funzione ServiceMain](writing-a-servicemain-function.md). Per ulteriori informazioni sulla funzione SvcInstall, vedere [installazione di un servizio](installing-a-service.md). Per informazioni sulla scrittura della funzione SvcCtrlHandler, vedere [scrittura di una funzione di gestione del controllo](writing-a-control-handler-function.md). Per il servizio di esempio completo, inclusa l'origine per la funzione SvcReportEvent, vedere [svc. cpp](svc-cpp.md).


```C++
//
// Purpose: 
//   Entry point for the process
//
// Parameters:
//   None
// 
// Return value:
//   None, defaults to 0 (zero)
//
int __cdecl _tmain(int argc, TCHAR *argv[])
{ 
    // If command-line parameter is "install", install the service. 
    // Otherwise, the service is probably being started by the SCM.

    if( lstrcmpi( argv[1], TEXT("install")) == 0 )
    {
        SvcInstall();
        return;
    }

    // TO_DO: Add any additional services for the process to this table.
    SERVICE_TABLE_ENTRY DispatchTable[] = 
    { 
        { SVCNAME, (LPSERVICE_MAIN_FUNCTION) SvcMain }, 
        { NULL, NULL } 
    }; 
 
    // This call returns when the service has stopped. 
    // The process should simply terminate when the call returns.

    if (!StartServiceCtrlDispatcher( DispatchTable )) 
    { 
        SvcReportEvent(TEXT("StartServiceCtrlDispatcher")); 
    } 
} 

```



Di seguito è riportato un esempio di esempio. h generato dal compilatore di messaggi. Per ulteriori informazioni, vedere [Sample.MC](sample-mc.md).

``` syntax
 // The following are message definitions.
//
//  Values are 32 bit values layed out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: SVC_ERROR
//
// MessageText:
//
//  An error has occurred (%2).
//  
//
#define SVC_ERROR                        ((DWORD)0xC0020001L)
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Punto di ingresso del servizio](service-entry-point.md)
</dt> <dt>

[Esempio di servizio completo](the-complete-service-sample.md)
</dt> </dl>

 

 



