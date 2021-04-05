---
title: Esempio di aggiunta di un token Helper a un processo di trasferimento BITS
description: È possibile configurare un processo di trasferimento di Servizio trasferimento intelligente in background (BITS) con un token di sicurezza aggiuntivo. Il processo di trasferimento BITS usa questo token di supporto per l'autenticazione e per accedere alle risorse.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab12fe93ae54d91d02bef5e59e99d267571413e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047292"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a><span data-ttu-id="574cb-104">Esempio: aggiunta di un token Helper a un processo di trasferimento BITS</span><span class="sxs-lookup"><span data-stu-id="574cb-104">Example: Adding a Helper Token to a BITS Transfer Job</span></span>

<span data-ttu-id="574cb-105">È possibile configurare un processo di trasferimento di Servizio trasferimento intelligente in background (BITS) con un token di sicurezza aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="574cb-105">You can configure a Background Intelligent Transfer Service (BITS) transfer job with an additional security token.</span></span> <span data-ttu-id="574cb-106">Il processo di trasferimento BITS usa questo token di supporto per l'autenticazione e per accedere alle risorse.</span><span class="sxs-lookup"><span data-stu-id="574cb-106">The BITS transfer job uses this helper token for authentication and to access resources.</span></span>

<span data-ttu-id="574cb-107">Per ulteriori informazioni, vedere [token helper per i processi di trasferimento BITS](helper-tokens-for-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="574cb-107">For more information, see [Helper tokens for BITS transfer jobs](helper-tokens-for-bits-transfer-jobs.md).</span></span>

<span data-ttu-id="574cb-108">La procedura seguente consente di creare un processo di trasferimento BITS nel contesto dell'utente locale, di ottenere le credenziali di un secondo utente, di creare un token di supporto con queste credenziali, quindi di impostare il token helper nel processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="574cb-108">The following procedure creates a BITS transfer job in the context of the local user, gets credentials of a second user, creates a helper token with these credentials, and then sets the helper token on the BITS transfer job.</span></span>

<span data-ttu-id="574cb-109">Questo esempio usa l'intestazione e l'implementazione definite in [esempio: classi comuni](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="574cb-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="574cb-110">**Per aggiungere un token Helper a un processo di trasferimento BITS**</span><span class="sxs-lookup"><span data-stu-id="574cb-110">**To add a helper token to a BITS transfer job**</span></span>

1.  <span data-ttu-id="574cb-111">Inizializzare i parametri COM chiamando la funzione CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="574cb-111">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="574cb-112">Per ulteriori informazioni sulla funzione CCoInitializer, vedere [example: Common Classes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="574cb-112">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="574cb-113">Ottenere un puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .</span><span class="sxs-lookup"><span data-stu-id="574cb-113">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface.</span></span> <span data-ttu-id="574cb-114">In questo esempio viene utilizzata la [classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) per gestire i puntatori di interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="574cb-114">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="574cb-115">Inizializzare la sicurezza del processo COM chiamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="574cb-115">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="574cb-116">BITS richiede almeno il livello di rappresentazione della rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="574cb-116">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="574cb-117">BITS ha esito negativo con E \_ AccessDenied se il livello di rappresentazione corretto non è impostato.</span><span class="sxs-lookup"><span data-stu-id="574cb-117">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
4.  <span data-ttu-id="574cb-118">Ottenere un puntatore all'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e ottenere il localizzatore iniziale sui bit chiamando la funzione [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="574cb-118">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
5.  <span data-ttu-id="574cb-119">Creare un processo di trasferimento BITS chiamando il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="574cb-119">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
6.  <span data-ttu-id="574cb-120">Ottenere un puntatore all'interfaccia di callback CNotifyInterface e chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) per ricevere la notifica di eventi correlati al processo.</span><span class="sxs-lookup"><span data-stu-id="574cb-120">Get a pointer to the CNotifyInterface callback interface, and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="574cb-121">Per ulteriori informazioni su CNotifyInterface, vedere [esempio: classi comuni](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="574cb-121">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
7.  <span data-ttu-id="574cb-122">Chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) per impostare i tipi di notifiche da ricevere.</span><span class="sxs-lookup"><span data-stu-id="574cb-122">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="574cb-123">In questo esempio vengono impostati i flag di errore **BG \_ Notify \_ Job \_ trasferiti** e **BG \_ Notify \_ Job \_** .</span><span class="sxs-lookup"><span data-stu-id="574cb-123">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
8.  <span data-ttu-id="574cb-124">Ottenere un puntatore all'interfaccia [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) chiamando il metodo **Metodo ibackgroundcopyjob:: QueryInterface** con l'identificatore di interfaccia appropriato.</span><span class="sxs-lookup"><span data-stu-id="574cb-124">Get a pointer to the [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) interface by calling the **IBackgroundCopyJob::QueryInterface** method with the proper interface identifier.</span></span>
9.  <span data-ttu-id="574cb-125">Tentativo di accesso all'utente del token helper.</span><span class="sxs-lookup"><span data-stu-id="574cb-125">Attempt to log on the user of the helper token.</span></span> <span data-ttu-id="574cb-126">Creare un handle di rappresentazione e chiamare la [funzione LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) per popolare l'handle di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="574cb-126">Create an impersonation handle, and call the [LogonUser Function]( /windows/win32/api/winbase/nf-winbase-logonusera) to populate the impersonation handle.</span></span> <span data-ttu-id="574cb-127">In caso di esito positivo, chiamare la [funzione ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span><span class="sxs-lookup"><span data-stu-id="574cb-127">If successful, call the [ImpersonateLoggedOnUser Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span></span> <span data-ttu-id="574cb-128">In caso di esito negativo, nell'esempio viene chiamata la [funzione RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) per terminare la rappresentazione dell'utente connesso, viene generato un errore e l'handle viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="574cb-128">If unsuccessful, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
10. <span data-ttu-id="574cb-129">Chiamare il metodo [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) per rappresentare il token dell'utente che ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="574cb-129">Call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method to impersonate the token of the logged-on user.</span></span> <span data-ttu-id="574cb-130">Se questo metodo ha esito negativo, nell'esempio viene chiamata la [funzione RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) per terminare la rappresentazione dell'utente connesso, viene generato un errore e l'handle viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="574cb-130">If this method fails, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
    > [!Note]
    >
    > <span data-ttu-id="574cb-131">Nelle versioni supportate di Windows precedenti a Windows 10, versione 1607, il proprietario del processo deve disporre di credenziali amministrative per chiamare il metodo [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .</span><span class="sxs-lookup"><span data-stu-id="574cb-131">In supported versions of Windows before Windows 10, version 1607, the job owner must have administrative credentials to call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method.</span></span>
    >
    > <span data-ttu-id="574cb-132">A partire da Windows 10, versione 1607, i proprietari dei processi non amministrativi possono impostare token Helper non amministratori nei processi BITS di cui sono proprietari.</span><span class="sxs-lookup"><span data-stu-id="574cb-132">Starting with Windows 10, version 1607, non-administrator job owners can set non-administrator helper tokens on BITS jobs they own.</span></span> <span data-ttu-id="574cb-133">Per impostare i token helper con privilegi di amministratore, i proprietari dei processi devono avere ancora credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="574cb-133">Job owners must still have administrative credentials to set helper tokens with administrator privileges.</span></span>

     

11. <span data-ttu-id="574cb-134">Chiamare il metodo [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) per specificare le risorse a cui accedere usando il contesto di sicurezza del token di supporto.</span><span class="sxs-lookup"><span data-stu-id="574cb-134">Call the [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) method to specify which resources to access using the helper token's security context.</span></span>
12. <span data-ttu-id="574cb-135">Una volta completata la rappresentazione, nell'esempio viene chiamata la [funzione RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) per terminare la rappresentazione dell'utente connesso e l'handle viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="574cb-135">After the impersonation is complete, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of logged on user, and the handle is closed.</span></span>
13. <span data-ttu-id="574cb-136">Aggiungere i file al processo di trasferimento BITS chiamando [**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="574cb-136">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span>
14. <span data-ttu-id="574cb-137">Una volta aggiunto il file, chiamare [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per riprendere il processo.</span><span class="sxs-lookup"><span data-stu-id="574cb-137">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="574cb-138">Configurare un ciclo while per attendere il messaggio QUIT dall'interfaccia di callback mentre è in corso il trasferimento del processo.</span><span class="sxs-lookup"><span data-stu-id="574cb-138">Set up a while loop to wait for the quit message from the callback interface while the job is transferring.</span></span> <span data-ttu-id="574cb-139">Il ciclo while usa la funzione [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) per recuperare il numero di millisecondi trascorsi dall'avvio del processo di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="574cb-139">The while loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>
16. <span data-ttu-id="574cb-140">Al termine del processo di trasferimento BITS, rimuovere il processo dalla coda chiamando [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="574cb-140">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="574cb-141">Nell'esempio di codice seguente viene aggiunto un token Helper a un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="574cb-141">The following code example adds a helper token to a BITS transfer job.</span></span>


```C++
#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"


void HelperToken(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &domain, const LPWSTR &username, const LPWSTR &password)
{
// If CoInitializeEx fails, the exception is unhandled and the program terminates   
CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);

CComPtr<IBackgroundCopyJob> pJob; 

    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(
            NULL,
            -1,
            NULL,
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL,
            EOAC_DYNAMIC_CLOAKING,
            0
            );

        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void **)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"HelperTokenSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);


        if(FAILED(hr))
        {   
            // Failed to create job.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;    
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to SetNotifyInterface.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to SetNotifyFlags.
            throw MyException(hr, L"SetNotifyFlags");
        }

        //Retrieve the IBitsTokenOptions interface pointer from the BITS transfer job.
        CComPtr<IBitsTokenOptions> pTokenOptions;
        hr = pJob->QueryInterface(__uuidof(IBitsTokenOptions), (void** ) &pTokenOptions);

        if (FAILED(hr))
        {
            // Failed to QueryInterface.
            throw MyException(hr, L"QueryInterface");
        }

        // Log on user of the helper token.
        wprintf(L"Credentials for helper token %s\\%s %s\n", domain, username, password);

        HANDLE hImpersonation = INVALID_HANDLE_VALUE;
        if(LogonUser(username, domain, password, LOGON32_LOGON_INTERACTIVE, LOGON32_PROVIDER_DEFAULT, &hImpersonation))
        {
            // Impersonate the logged-on user.
            if(ImpersonateLoggedOnUser(hImpersonation))
            {
                // Configure the impersonated logged-on user's token as the helper token.
                hr = pTokenOptions->SetHelperToken();        
                if (FAILED(hr))
                {
                    //Failed to set helper token.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperToken");
                }

                hr = pTokenOptions->SetHelperTokenFlags(BG_TOKEN_LOCAL_FILE);
                if (FAILED(hr))
                {
                    //Failed to set helper token flags.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperTokenFlags");
                }

                RevertToSelf();
            }               
            CloseHandle(hImpersonation);
        }

        // Add a file.
        // Replace parameters with variables that contain valid paths.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile,localFile);

        if(FAILED(hr))
        {   
            //Failed to add file to job.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Resume failed.                   
            throw MyException(hr, L"Resume");
        }    
    }
    catch(const std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }
    catch(const MyException &ex)
    {
        wprintf(L"Error 0x%x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack
    DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
    while (dwLimit > GetTickCount())
    {
        MSG msg;

        while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
        { 
            // If it is a quit message, exit.
            if (msg.message == WM_QUIT) 
            {
                return;
            }

            // Otherwise, dispatch the message.
            DispatchMessage(&msg); 
        } // End of PeekMessage while loop
    }

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s ", argv[0]);
        wprintf(L"[remote name] [local name] [helpertoken domain] [helpertoken userrname] [helpertoken password]\n");
        return;
    }

    HelperToken(argv[1],argv[2],argv[3],argv[4],argv[5]);

}
```



## <a name="related-topics"></a><span data-ttu-id="574cb-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="574cb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="574cb-143">Token helper per i processi di trasferimento BITS</span><span class="sxs-lookup"><span data-stu-id="574cb-143">Helper tokens for BITS transfer jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[<span data-ttu-id="574cb-144">**IBitsTokenOptions**</span><span class="sxs-lookup"><span data-stu-id="574cb-144">**IBitsTokenOptions**</span></span>](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[<span data-ttu-id="574cb-145">Esempio: classi comuni</span><span class="sxs-lookup"><span data-stu-id="574cb-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 