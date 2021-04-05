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
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>Esempio: aggiunta di un token Helper a un processo di trasferimento BITS

È possibile configurare un processo di trasferimento di Servizio trasferimento intelligente in background (BITS) con un token di sicurezza aggiuntivo. Il processo di trasferimento BITS usa questo token di supporto per l'autenticazione e per accedere alle risorse.

Per ulteriori informazioni, vedere [token helper per i processi di trasferimento BITS](helper-tokens-for-bits-transfer-jobs.md).

La procedura seguente consente di creare un processo di trasferimento BITS nel contesto dell'utente locale, di ottenere le credenziali di un secondo utente, di creare un token di supporto con queste credenziali, quindi di impostare il token helper nel processo di trasferimento BITS.

Questo esempio usa l'intestazione e l'implementazione definite in [esempio: classi comuni](common-classes.md).

**Per aggiungere un token Helper a un processo di trasferimento BITS**

1.  Inizializzare i parametri COM chiamando la funzione CCoInitializer. Per ulteriori informazioni sulla funzione CCoInitializer, vedere [example: Common Classes](common-classes.md).
2.  Ottenere un puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) . In questo esempio viene utilizzata la [classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) per gestire i puntatori di interfaccia com.
3.  Inizializzare la sicurezza del processo COM chiamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS richiede almeno il livello di rappresentazione della rappresentazione. BITS ha esito negativo con E \_ AccessDenied se il livello di rappresentazione corretto non è impostato.
4.  Ottenere un puntatore all'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e ottenere il localizzatore iniziale sui bit chiamando la funzione [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
5.  Creare un processo di trasferimento BITS chiamando il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
6.  Ottenere un puntatore all'interfaccia di callback CNotifyInterface e chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) per ricevere la notifica di eventi correlati al processo. Per ulteriori informazioni su CNotifyInterface, vedere [esempio: classi comuni](common-classes.md).
7.  Chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) per impostare i tipi di notifiche da ricevere. In questo esempio vengono impostati i flag di errore **BG \_ Notify \_ Job \_ trasferiti** e **BG \_ Notify \_ Job \_** .
8.  Ottenere un puntatore all'interfaccia [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) chiamando il metodo **Metodo ibackgroundcopyjob:: QueryInterface** con l'identificatore di interfaccia appropriato.
9.  Tentativo di accesso all'utente del token helper. Creare un handle di rappresentazione e chiamare la [funzione LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) per popolare l'handle di rappresentazione. In caso di esito positivo, chiamare la [funzione ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser). In caso di esito negativo, nell'esempio viene chiamata la [funzione RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) per terminare la rappresentazione dell'utente connesso, viene generato un errore e l'handle viene chiuso.
10. Chiamare il metodo [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) per rappresentare il token dell'utente che ha eseguito l'accesso. Se questo metodo ha esito negativo, nell'esempio viene chiamata la [funzione RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) per terminare la rappresentazione dell'utente connesso, viene generato un errore e l'handle viene chiuso.
    > [!Note]
    >
    > Nelle versioni supportate di Windows precedenti a Windows 10, versione 1607, il proprietario del processo deve disporre di credenziali amministrative per chiamare il metodo [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .
    >
    > A partire da Windows 10, versione 1607, i proprietari dei processi non amministrativi possono impostare token Helper non amministratori nei processi BITS di cui sono proprietari. Per impostare i token helper con privilegi di amministratore, i proprietari dei processi devono avere ancora credenziali amministrative.

     

11. Chiamare il metodo [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) per specificare le risorse a cui accedere usando il contesto di sicurezza del token di supporto.
12. Una volta completata la rappresentazione, nell'esempio viene chiamata la [funzione RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) per terminare la rappresentazione dell'utente connesso e l'handle viene chiuso.
13. Aggiungere i file al processo di trasferimento BITS chiamando [**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).
14. Una volta aggiunto il file, chiamare [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per riprendere il processo.
15. Configurare un ciclo while per attendere il messaggio QUIT dall'interfaccia di callback mentre è in corso il trasferimento del processo. Il ciclo while usa la funzione [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) per recuperare il numero di millisecondi trascorsi dall'avvio del processo di trasferimento.
16. Al termine del processo di trasferimento BITS, rimuovere il processo dalla coda chiamando [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

Nell'esempio di codice seguente viene aggiunto un token Helper a un processo di trasferimento BITS.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Token helper per i processi di trasferimento BITS](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[Esempio: classi comuni](common-classes.md)
</dt> </dl>

 

 