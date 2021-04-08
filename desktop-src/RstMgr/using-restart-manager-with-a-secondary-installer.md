---
title: Uso di gestione riavvio con un programma di installazione secondario
description: Nella procedura riportata di seguito viene descritto l'utilizzo di gestione riavvio con i programmi di installazione primari e secondari.
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb44105d9f3d391bb2ed793aca8a6da2c330b30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855730"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a><span data-ttu-id="aad90-103">Uso di gestione riavvio con un programma di installazione secondario</span><span class="sxs-lookup"><span data-stu-id="aad90-103">Using Restart Manager with a Secondary Installer</span></span>

<span data-ttu-id="aad90-104">Nella procedura riportata di seguito viene descritto l'utilizzo di gestione riavvio con i programmi di installazione primari e secondari.</span><span class="sxs-lookup"><span data-stu-id="aad90-104">The following procedure describes the use of the Restart Manager with primary and secondary installers.</span></span>

<span data-ttu-id="aad90-105">Quando si usano programmi di installazione primari e secondari, il programma di installazione principale controlla l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="aad90-105">When using primary and secondary installers, the primary installer controls the user interface.</span></span>

<span data-ttu-id="aad90-106">**Per usare Gestione riavvio con i programmi di installazione primari e secondari**</span><span class="sxs-lookup"><span data-stu-id="aad90-106">**To use Restart Manager with primary and secondary installers**</span></span>

1.  <span data-ttu-id="aad90-107">Il programma di installazione principale chiama la funzione [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) per avviare la sessione di gestione riavvio e ottenere un handle di sessione e una chiave.</span><span class="sxs-lookup"><span data-stu-id="aad90-107">The primary installer calls the [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) function to start the Restart Manager session and obtain a session handle and key.</span></span>
2.  <span data-ttu-id="aad90-108">Il programma di installazione primario avvia o Contatta il programma di installazione secondario e lo fornisce alla chiave di sessione ottenuta nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="aad90-108">The primary installer starts or contacts the secondary installer and provides it with the session key obtained in the previous step.</span></span>
3.  <span data-ttu-id="aad90-109">Il programma di installazione secondario chiama la funzione [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) con la chiave della sessione per partecipare alla sessione di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="aad90-109">The secondary installer calls the [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) function with the session key to join the Restart Manager session.</span></span> <span data-ttu-id="aad90-110">Un programma di installazione secondario può partecipare a una sessione avviata dal programma di installazione primario solo quando entrambi i programmi di installazione vengono eseguiti nello stesso contesto utente.</span><span class="sxs-lookup"><span data-stu-id="aad90-110">A secondary installer can join a session that is started by the primary installer only when both installers run in the same user context.</span></span>
4.  <span data-ttu-id="aad90-111">I programmi di installazione primari e secondari chiamano la funzione [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) per registrare le risorse.</span><span class="sxs-lookup"><span data-stu-id="aad90-111">The primary and secondary installers call the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function to register resources.</span></span> <span data-ttu-id="aad90-112">Gestione riavvio può utilizzare solo le risorse registrate per determinare quali applicazioni e servizi devono essere arrestati e riavviati.</span><span class="sxs-lookup"><span data-stu-id="aad90-112">The Restart Manager can use only registered resources to determine which applications and services must be shut down and restarted.</span></span> <span data-ttu-id="aad90-113">Tutte le risorse che possono essere interessate dall'installazione devono essere registrate con la sessione.</span><span class="sxs-lookup"><span data-stu-id="aad90-113">All resources that can be affected by the installation should be registered with the session.</span></span> <span data-ttu-id="aad90-114">Le risorse possono essere identificate in base al nome file, al nome breve del servizio o a una struttura di [**\_ \_ processo univoca RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) .</span><span class="sxs-lookup"><span data-stu-id="aad90-114">Resources can be identified by filename, service short name, or an [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structure.</span></span>
5.  <span data-ttu-id="aad90-115">Il programma di installazione principale chiama la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) per ottenere una matrice di strutture di [**\_ \_ informazioni del processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) che elenca tutte le applicazioni e i servizi che devono essere arrestati e riavviati.</span><span class="sxs-lookup"><span data-stu-id="aad90-115">The primary installer calls the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to obtain an array of [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structures that lists all applications and services that must be shut down and restarted.</span></span>

    <span data-ttu-id="aad90-116">Se il valore del parametro *lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è diverso da zero, gestione riavvio non è in grado di liberare una risorsa registrata dalla chiusura di un'applicazione o di un servizio.</span><span class="sxs-lookup"><span data-stu-id="aad90-116">If the value of the *lpdwRebootReason* parameter that is returned by the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function is nonzero, the Restart Manager is unable to free a registered resource by the shutdown of an application or service.</span></span> <span data-ttu-id="aad90-117">In questo caso, è necessario arrestare e riavviare il sistema per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="aad90-117">In this case, a system shutdown and restart is required to continue the installation.</span></span> <span data-ttu-id="aad90-118">Il programma di installazione principale deve richiedere all'utente un'azione, arrestare programmi o servizi oppure pianificare un arresto e un riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="aad90-118">The primary installer should prompt the user for an action, stop programs or services, or schedule a system shutdown and restart.</span></span>

    <span data-ttu-id="aad90-119">Se il valore del parametro *lpdwRebootReason* restituito dalla funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) è zero, il programma di installazione deve chiamare la funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) .</span><span class="sxs-lookup"><span data-stu-id="aad90-119">If the value of the *lpdwRebootReason* parameter that is returned by the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function is zero, the installer should call the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function.</span></span> <span data-ttu-id="aad90-120">Questa operazione arresta i servizi e le applicazioni che usano risorse registrate.</span><span class="sxs-lookup"><span data-stu-id="aad90-120">This shuts down the services and applications that are using registered resources.</span></span> <span data-ttu-id="aad90-121">I programmi di installazione primari e secondari devono quindi eseguire le modifiche di sistema necessarie per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="aad90-121">The primary and secondary installers should then perform system modifications that are required to complete the installation.</span></span> <span data-ttu-id="aad90-122">Infine, il programma di installazione principale deve chiamare la funzione [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) in modo che la gestione riavvio possa riavviare le applicazioni arrestate e registrate per il riavvio.</span><span class="sxs-lookup"><span data-stu-id="aad90-122">Finally, the primary installer should call the [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function so that the Restart Manager can restart the applications it has shut down and that have been registered for a restart.</span></span>

6.  <span data-ttu-id="aad90-123">Il programma di installazione primario e secondario chiama la funzione [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) per chiudere la sessione di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="aad90-123">The primary and secondary installer call the [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) function to close the Restart Manager session.</span></span>

<span data-ttu-id="aad90-124">Il frammento di codice seguente mostra un esempio di un programma di installazione primario che inizia e usa una sessione di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="aad90-124">The following code snippet shows an example of a primary installer starting and using a Restart Manager session.</span></span> <span data-ttu-id="aad90-125">L'esempio richiede Windows 7 o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="aad90-125">The example requires Windows 7 or Windows Server 2008 R2.</span></span> <span data-ttu-id="aad90-126">In Windows Vista o Windows Server 2008, l'applicazione del calcolatore viene arrestata ma non viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="aad90-126">On Windows Vista or Windows Server 2008, the Calculator application shuts down but does not restart.</span></span> <span data-ttu-id="aad90-127">Questo esempio Mostra come un programma di installazione primario può usare Gestione riavvio per arrestare e riavviare un processo.</span><span class="sxs-lookup"><span data-stu-id="aad90-127">This example shows how a primary installer can use Restart Manager to shutdown and restart a process.</span></span> <span data-ttu-id="aad90-128">Nell'esempio si presuppone che il calcolatore sia già in esecuzione prima di avviare la sessione di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="aad90-128">The example assumes that Calculator is already running before starting the Restart Manager session.</span></span>


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



<span data-ttu-id="aad90-129">Il frammento di codice seguente mostra un esempio di aggiunta di un programma di installazione secondario alla sessione di gestione riavvio esistente.</span><span class="sxs-lookup"><span data-stu-id="aad90-129">The following code snippet shows an example of joining a secondary installer to the existing Restart Manager session.</span></span> <span data-ttu-id="aad90-130">L'esempio richiede Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="aad90-130">The example requires Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="aad90-131">Il programma di installazione secondario ottiene la chiave della sessione dal programma di installazione principale e la usa per partecipare alla sessione.</span><span class="sxs-lookup"><span data-stu-id="aad90-131">The secondary installer obtains the session key from the primary installer and uses this to join the session.</span></span>


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



 

 




