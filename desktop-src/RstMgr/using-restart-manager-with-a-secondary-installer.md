---
title: Uso di Gestione riavvio con un programma di installazione secondario
description: La procedura seguente descrive l'uso di Gestione riavvio con i programmi di installazione primari e secondari.
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aefb1f9658752677e7850e939fcb6a3c4c6047c5efc2dc0ceb06ec0f51900ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009989"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a>Uso di Gestione riavvio con un programma di installazione secondario

La procedura seguente descrive l'uso di Gestione riavvio con i programmi di installazione primari e secondari.

Quando si usano programmi di installazione primari e secondari, il programma di installazione primario controlla l'interfaccia utente.

**Per usare Gestione riavvio con programmi di installazione primari e secondari**

1.  Il programma di installazione primario chiama la [**funzione RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) per avviare la sessione di Gestione riavvio e ottenere un handle di sessione e una chiave.
2.  Il programma di installazione primario avvia o contatta il programma di installazione secondario e lo fornisce con la chiave di sessione ottenuta nel passaggio precedente.
3.  Il programma di installazione secondario chiama la [**funzione RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) con la chiave di sessione per partecipare alla sessione di Gestione riavvio. Un programma di installazione secondario può partecipare a una sessione avviata dal programma di installazione primario solo quando entrambi i programmi di installazione vengono eseguiti nello stesso contesto utente.
4.  I programmi di installazione primario e secondario chiamano la [**funzione RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) per registrare le risorse. Gestione riavvio può usare solo le risorse registrate per determinare quali applicazioni e servizi devono essere arrestati e riavviati. Tutte le risorse che possono essere interessate dall'installazione devono essere registrate con la sessione. Le risorse possono essere identificate in base al nome file, al nome breve del servizio o a [**una struttura RM \_ UNIQUE \_ PROCESS.**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process)
5.  Il programma di installazione primario chiama la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) per ottenere una matrice di [**strutture RM \_ PROCESS \_ INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) che elenca tutte le applicazioni e i servizi che devono essere arrestati e riavviati.

    Se il valore del parametro *lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è diverso da zero, Gestione riavvio non è in grado di liberare una risorsa registrata dall'arresto di un'applicazione o di un servizio. In questo caso, è necessario un arresto e un riavvio del sistema per continuare l'installazione. Il programma di installazione primario deve richiedere un'azione all'utente, arrestare programmi o servizi o pianificare l'arresto e il riavvio del sistema.

    Se il valore del *parametro lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è zero, il programma di installazione deve chiamare la funzione [**RmShutdown.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) In questo modo vengono arrestati i servizi e le applicazioni che usano risorse registrate. I programmi di installazione primario e secondario devono quindi eseguire le modifiche di sistema necessarie per completare l'installazione. Infine, il programma di installazione primario deve chiamare la funzione [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) in modo che Gestione riavvii possa riavviare le applicazioni arrestate e registrate per un riavvio.

6.  Il programma di installazione primario e secondario chiamano la [**funzione RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) per chiudere la sessione di Gestione riavvio.

Il frammento di codice seguente illustra un esempio di programma di installazione primario che avvia e usa una sessione di Gestione riavvio. L'esempio richiede Windows 7 o Windows Server 2008 R2. In Windows Vista o Windows Server 2008, l'applicazione Calculator viene arrestata ma non riavviata. Questo esempio illustra come un programma di installazione primario può usare Gestione riavvio per arrestare e riavviare un processo. Nell'esempio si presuppone che calculator sia già in esecuzione prima di avviare la sessione di Gestione riavvio.


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the  
    // Text-Encoded session key,defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of calc files to be registered.
    DWORD dwFiles           = 2;   

    //
    // NOTE:We register two calc executable files. 
    // The second one is for the redirection of 32 bit calc on 
    // 64 bit machines. Even if you are using a 32 bit machine,  
    // you don't need to comment out the second line. 
    //
    LPCWSTR rgsFiles[]      = 
     {L"C:\\Windows\\System32\\calc.exe",
      L"C:\\Windows\\SysWow64\\calc.exe"};

    UINT nRetry             = 0; 
    UINT nAffectedApps      = 0;
    UINT nProcInfoNeeded    = 0;
    RM_REBOOT_REASON dwRebootReasons    = RmRebootReasonNone;
    RM_PROCESS_INFO *rgAffectedApps     = NULL;
    
    //
    // Start a Restart Manager Session
    //
    dwErrCode = RmStartSession(&dwSessionHandle, 0, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: we only register two calc executable files 
    // in this sample. You can register files, processes 
    // (in the form of process ID), and services (in the   
    // form of service short names) with Restart Manager.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,       // Files
                                    0,  
                                    NULL,           // Processes
                                    0, 
                                    NULL);          // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Obtain the list of affected applications/services.
    //
    // NOTE: Restart Manager returns the results into the  
    // buffer allocated by the caller. The first call to 
    // RmGetList() will return the size of the buffer  
    // (i.e. nProcInfoNeeded) the caller needs to allocate. 
    // The caller then needs to allocate the buffer  
    // (i.e. rgAffectedApps) and make another RmGetList() 
    // call to ask Restart Manager to write the results 
    // into the buffer. However, since Restart Manager 
    // refreshes the list every time RmGetList()is called, 
    // it is possible that the size returned by the first 
    // RmGetList()call is not sufficient to hold the results  
    // discovered by the second RmGetList() call. Therefore, 
    // it is recommended that the caller follows the 
    // following practice to handle this race condition:
    //   
    //    Use a loop to call RmGetList() in case the buffer 
    //    allocated according to the size returned in previous 
    //    call is not enough.      
    // 
    // In this example, we use a do-while loop trying to make 
    // 3 RmGetList() calls (including the first attempt to get 
    // buffer size) and if we still cannot succeed, we give up. 
    //
    do
    {
        dwErrCode = RmGetList(dwSessionHandle,
                              &nProcInfoNeeded,
                              &nAffectedApps, 
                              rgAffectedApps, 
                              (LPDWORD) &dwRebootReasons);
        if (ERROR_SUCCESS == dwErrCode)
        {
            //
            // RmGetList() succeeded
            //
            break;
        }

        if (ERROR_MORE_DATA != dwErrCode)
        {
            //
            // RmGetList() failed, with errors 
            // other than ERROR_MORE_DATA
            //
            goto RM_CLEANUP;
        }

        //
        // RmGetList() is asking for more data
        //
        nAffectedApps = nProcInfoNeeded;
        
        if (NULL != rgAffectedApps)
        {
            delete []rgAffectedApps;
            rgAffectedApps = NULL;
        }

        rgAffectedApps = new RM_PROCESS_INFO[nAffectedApps];
    } while ((ERROR_MORE_DATA == dwErrCode) && (nRetry ++ < 3));

    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    if (RmRebootReasonNone != dwRebootReasons)
    {
        //
        // Restart Manager cannot mitigate a reboot. 
        // We goes to the clean up. The caller may want   
        // to add additional code to handle this scenario.
        //
        goto RM_CLEANUP;
    }
    
    //
    // Now rgAffectedApps contains the affected applications 
    // and services. The number of applications and services
    // returned is nAffectedApps. The result of RmGetList can 
    // be interpreted by the user to determine subsequent  
    // action (e.g. ask user's permission to shutdown).
    //
    // CALLER CODE GOES HERE...
     
    //
    // Shut down all running instances of affected 
    // applications and services.
    //
    dwErrCode = RmShutdown(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // An installer can now replace or update
    // the calc executable file.
    //
    // CALLER CODE GOES HERE...


    //
    // Restart applications and services, after the 
    // files have been replaced or updated.
    //
    dwErrCode = RmRestart(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:
    
    if (NULL != rgAffectedApps)
    {
        delete [] rgAffectedApps;
        rgAffectedApps = NULL;
    }

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // Clean up the Restart Manager session.
        //
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}
```



Il frammento di codice seguente illustra un esempio di aggiunta di un programma di installazione secondario alla sessione di Gestione riavvio esistente. L'esempio richiede Windows Vista o Windows Server 2008. Il programma di installazione secondario ottiene la chiave di sessione dal programma di installazione primario e la usa per partecipare alla sessione.


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the 
    // Text-Encoded session key, defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of files to be registered.
    DWORD dwFiles           = 1;   
    //
    // We register oleaut32.dll with Restart Manager.
    //
    LPCWSTR rgsFiles[]      = 
        {L"C:\\Windows\\System32\\oleaut32.dll"};

    //    
    // Secondary installer needs to obtain the session key from  
    // the primary installer and uses it to join the session.
    //
    // CALLER CODE GOES HERE ...
    //

    // We assume the session key obtained is stored in sessKey
    dwErrCode = RmJoinSession(&dwSessionHandle, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: In Vista, the subordinate is only allowed to 
    // register resources and cannot perform any other 
    // getlist, shutdown, restart or filter operations.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,     // Files
                                    0,  
                                    NULL,         // Processes
                                    0, 
                                    NULL);        // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // The subordinate leaves the conductor's session 
        // by calling RmEndSession(). The session itself 
        // won't be destroyed until the primary installer 
        // calls RmEndSession()
        //          
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}

```



 

 




