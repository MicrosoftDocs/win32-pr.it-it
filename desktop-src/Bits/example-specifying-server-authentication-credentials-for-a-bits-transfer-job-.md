---
title: Specificare le credenziali di autenticazione server per un processo di trasferimento BITS
description: È possibile specificare schemi di autenticazione diversi per un processo di trasferimento Servizio trasferimento intelligente in background (BITS).
ms.assetid: 31db38f6-3639-4042-97f2-4f9d78942e15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4373cdf0c8b4c8afe7dff367fda9387eec0b54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047344"
---
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a><span data-ttu-id="f86a1-103">Specificare le credenziali di autenticazione server per un processo di trasferimento BITS</span><span class="sxs-lookup"><span data-stu-id="f86a1-103">Specify server authentication credentials for a BITS transfer job</span></span>

<span data-ttu-id="f86a1-104">È possibile specificare schemi di autenticazione diversi per un processo di trasferimento Servizio trasferimento intelligente in background (BITS).</span><span class="sxs-lookup"><span data-stu-id="f86a1-104">You can specify different authentication schemes for a Background Intelligent Transfer Service (BITS) transfer job.</span></span>

<span data-ttu-id="f86a1-105">La procedura seguente consente di ottenere uno schema di autenticazione e di creare una struttura di identità di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f86a1-105">The following procedure gets an authentication scheme and creates an authentication identity structure.</span></span> <span data-ttu-id="f86a1-106">Quindi, l'applicazione crea un processo di download BITS e imposta le credenziali per il processo.</span><span class="sxs-lookup"><span data-stu-id="f86a1-106">Then the application creates a BITS download job and sets the credentials for the job.</span></span> <span data-ttu-id="f86a1-107">Dopo la creazione del processo, l'applicazione ottiene un puntatore a un'interfaccia di callback e esegue il polling dello stato del processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="f86a1-107">After the job is created, the application gets a pointer to a callback interface and polls for the status of the BITS transfer job.</span></span> <span data-ttu-id="f86a1-108">Una volta completato il processo, questo viene rimosso dalla coda.</span><span class="sxs-lookup"><span data-stu-id="f86a1-108">After the job is complete, it is removed from the queue.</span></span>

<span data-ttu-id="f86a1-109">Questo esempio usa l'intestazione e l'implementazione definite in [esempio: classi comuni](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f86a1-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="f86a1-110">**Per specificare le credenziali di autenticazione server per un processo di trasferimento BITS**</span><span class="sxs-lookup"><span data-stu-id="f86a1-110">**To specify server authentication credentials for a BITS transfer job**</span></span>

1.  <span data-ttu-id="f86a1-111">Creare una struttura di contenitori che esegue il mapping dei valori dello [**\_ \_ schema di autenticazione BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) ai nomi degli schemi.</span><span class="sxs-lookup"><span data-stu-id="f86a1-111">Create a container structure that maps [**BG\_AUTH\_SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) values to scheme names.</span></span>

    ```C++
    struct
    {
        LPCWSTR        Name;
        BG_AUTH_SCHEME Scheme;
    }
    SchemeNames[] =
    {
        { L"basic",      BG_AUTH_SCHEME_BASIC },
        { L"digest",     BG_AUTH_SCHEME_DIGEST },
        { L"ntlm",       BG_AUTH_SCHEME_NTLM },
        { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
        { L"passport",   BG_AUTH_SCHEME_PASSPORT },

        { NULL,         BG_AUTH_SCHEME_BASIC }
    };
    ```

    

2.  <span data-ttu-id="f86a1-112">Inizializzare i parametri COM chiamando la funzione CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="f86a1-112">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="f86a1-113">Per ulteriori informazioni sulla funzione CCoInitializer, vedere [example: Common Classes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f86a1-113">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
3.  <span data-ttu-id="f86a1-114">Preparare una struttura di [**\_ \_ credenziali di autenticazione BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="f86a1-114">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span> <span data-ttu-id="f86a1-115">Nell'esempio viene utilizzata la funzione [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) per cancellare le posizioni di memoria associate alle informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="f86a1-115">The example uses the [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function to clear the memory locations associated with the sensitive information.</span></span> <span data-ttu-id="f86a1-116">La funzione [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) è definita in winbase. h.</span><span class="sxs-lookup"><span data-stu-id="f86a1-116">The [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function is defined in WinBase.h.</span></span>
4.  <span data-ttu-id="f86a1-117">Utilizzare la funzione getScheme per ottenere lo schema di autenticazione da utilizzare per la connessione al server.</span><span class="sxs-lookup"><span data-stu-id="f86a1-117">Use the GetScheme function to get the authentication scheme to use to connect to the server.</span></span>

    ```C++
    bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
    {
        int i;

        i = 0;
        while (SchemeNames[i].Name != NULL)
        {
            if (0 == _wcsicmp( s, SchemeNames[i].Name ))
            {

                *scheme = SchemeNames[i].Scheme;
                return true;
            }

            ++i;
        }

        return false;
    }
    ```

    

5.  <span data-ttu-id="f86a1-118">Popolare la struttura delle [**\_ \_ credenziali**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) di autenticazione di BG con lo schema di autenticazione restituito dalla funzione getScheme e il nome utente e la password passati nella funzione ServerAuthentication.</span><span class="sxs-lookup"><span data-stu-id="f86a1-118">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure with the authentication scheme returned by the GetScheme function and the user name and password that were passed into the ServerAuthentication function.</span></span>
6.  <span data-ttu-id="f86a1-119">Ottenere un puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).</span><span class="sxs-lookup"><span data-stu-id="f86a1-119">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface (pJob).</span></span>
7.  <span data-ttu-id="f86a1-120">Inizializzare la sicurezza del processo COM chiamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="f86a1-120">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f86a1-121">BITS richiede almeno il livello di rappresentazione della rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="f86a1-121">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="f86a1-122">BITS ha esito negativo con E \_ AccessDenied se il livello di rappresentazione corretto non è impostato.</span><span class="sxs-lookup"><span data-stu-id="f86a1-122">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
8.  <span data-ttu-id="f86a1-123">Ottenere un puntatore all'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e ottenere il localizzatore iniziale sui bit chiamando la funzione [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="f86a1-123">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
9.  <span data-ttu-id="f86a1-124">Creare un processo di trasferimento BITS chiamando il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="f86a1-124">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
10. <span data-ttu-id="f86a1-125">Ottenere un puntatore all'interfaccia di callback CNotifyInterface e chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) per ricevere la notifica di eventi correlati al processo.</span><span class="sxs-lookup"><span data-stu-id="f86a1-125">Get a pointer to the CNotifyInterface callback interface and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="f86a1-126">Per ulteriori informazioni su CNotifyInterface, vedere [esempio: classi comuni](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f86a1-126">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
11. <span data-ttu-id="f86a1-127">Chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) per impostare i tipi di notifiche da ricevere.</span><span class="sxs-lookup"><span data-stu-id="f86a1-127">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="f86a1-128">In questo esempio vengono impostati i flag di errore **BG \_ Notify \_ Job \_ trasferiti** e **BG \_ Notify \_ Job \_** .</span><span class="sxs-lookup"><span data-stu-id="f86a1-128">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
12. <span data-ttu-id="f86a1-129">Ottenere un puntatore all'interfaccia [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="f86a1-129">Get a pointer to the [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface.</span></span> <span data-ttu-id="f86a1-130">Usare il puntatore **IBackgroundCopyJob2** per impostare proprietà aggiuntive nel processo.</span><span class="sxs-lookup"><span data-stu-id="f86a1-130">Use the **IBackgroundCopyJob2** pointer to set additional properties on the job.</span></span> <span data-ttu-id="f86a1-131">Questo programma usa il metodo [**IBackgroundCopyJob2:: Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per impostare le credenziali per il processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="f86a1-131">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
13. <span data-ttu-id="f86a1-132">Aggiungere i file al processo di trasferimento BITS chiamando [**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="f86a1-132">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span> <span data-ttu-id="f86a1-133">In questo esempio, il metodo **Metodo ibackgroundcopyjob:: AddFile** usa le variabili fileremoto e LocalFile passate nella funzione ServerAuthentication.</span><span class="sxs-lookup"><span data-stu-id="f86a1-133">In this example, the **IBackgroundCopyJob::AddFile** method uses the remoteFile and localFile variables that were passed into the ServerAuthentication function.</span></span>
14. <span data-ttu-id="f86a1-134">Una volta aggiunto il file, chiamare [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per riprendere il processo.</span><span class="sxs-lookup"><span data-stu-id="f86a1-134">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="f86a1-135">Configurare un ciclo while per attendere il messaggio QUIT dall'interfaccia di callback mentre è in corso il trasferimento del processo.</span><span class="sxs-lookup"><span data-stu-id="f86a1-135">Set up a while loop to wait for Quit Message from the callback interface while the job is transferring.</span></span>

    > [!Note]  
    > <span data-ttu-id="f86a1-136">Questo passaggio è necessario solo se l'Apartment COM è un Apartment a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="f86a1-136">This step is necessary only if the COM apartment is a single-threaded apartment.</span></span> <span data-ttu-id="f86a1-137">Per altre informazioni, vedere [Apartment a thread singolo](../com/single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="f86a1-137">For more information, see [Single-Threaded Apartments](../com/single-threaded-apartments.md).</span></span>

     

    ```C++
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
    ```

    

    <span data-ttu-id="f86a1-138">Il ciclo precedente usa la funzione [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) per recuperare il numero di millisecondi trascorsi dall'avvio del processo di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="f86a1-138">The preceding loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>

16. <span data-ttu-id="f86a1-139">Al termine del processo di trasferimento BITS, rimuovere il processo dalla coda chiamando [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="f86a1-139">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="f86a1-140">Nell'esempio di codice seguente vengono specificate le credenziali di autenticazione server per un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="f86a1-140">The following code example specifies server authentication credentials for a BITS transfer job.</span></span>


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

//
// Retrieve BG_AUTH_SCHEME from scheme name.
//
//
struct
{
    LPCWSTR        Name;
    BG_AUTH_SCHEME Scheme;
}
SchemeNames[] =
{
    { L"basic",      BG_AUTH_SCHEME_BASIC },
    { L"digest",     BG_AUTH_SCHEME_DIGEST },
    { L"ntlm",       BG_AUTH_SCHEME_NTLM },
    { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
    { L"passport",   BG_AUTH_SCHEME_PASSPORT },

    { NULL,         BG_AUTH_SCHEME_BASIC }
};

bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
{
    int i;

    i = 0;
    while (SchemeNames[i].Name != NULL)
    {
        if (0 == _wcsicmp( s, SchemeNames[i].Name ))
        {

            *scheme = SchemeNames[i].Scheme;
            return true;
        }

        ++i;
    }

    return false;
}

void ServerAuthentication(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &scheme, const LPWSTR &username, const LPWSTR &password)
{

 // If CoInitializeEx fails, the exception is unhandled and the program terminates  
 CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    // Prepare the credentials structure.
    BG_AUTH_CREDENTIALS cred;
    ZeroMemory(&cred, sizeof(cred));
    if (!GetScheme(scheme,&cred.Scheme))
    {
        wprintf(L"Invalid authentication scheme specified\n");
        return;
    }

    cred.Target = BG_AUTH_TARGET_SERVER;
    cred.Credentials.Basic.UserName = username;
    if (0 == _wcsicmp(cred.Credentials.Basic.UserName, L"NULL"))
    {
        cred.Credentials.Basic.UserName = NULL;
    }

    cred.Credentials.Basic.Password = password;
    if (0 == _wcsicmp(cred.Credentials.Basic.Password, L"NULL"))
    {
        cred.Credentials.Basic.Password = NULL;
    }

    CComPtr<IBackgroundCopyJob> pJob;
    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(NULL, 
            -1, 
            NULL, 
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL, 
            EOAC_DYNAMIC_CLOAKING, 
            0);
        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void**)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"BitsAuthSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyFlags");
        }

        // Set credentials.
        CComPtr<IBackgroundCopyJob2> job2;
        hr = pJob.QueryInterface(&job2);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"QueryInterface");
        }

        hr = job2->SetCredentials(&cred);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetCredentials");
        }

        // Add a file.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile, localFile);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Failed to connect.
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
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack.
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
        wprintf(L"%s", argv[0]);
        wprintf(L" [remote name] [local name] [server authentication scheme =\"NTLM\"|\"NEGOTIATE\"|\"BASIC\"|\"DIGEST\"] [username] [password]\n");
        return;
    }

    ServerAuthentication(argv[1], argv[2], argv[3], argv[4], argv[5]); 

}
```



## <a name="related-topics"></a><span data-ttu-id="f86a1-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f86a1-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f86a1-142">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="f86a1-142">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="f86a1-143">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="f86a1-143">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="f86a1-144">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="f86a1-144">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="f86a1-145">Esempio: classi comuni</span><span class="sxs-lookup"><span data-stu-id="f86a1-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 