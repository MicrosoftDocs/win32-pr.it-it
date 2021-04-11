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
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a>Specificare le credenziali di autenticazione server per un processo di trasferimento BITS

È possibile specificare schemi di autenticazione diversi per un processo di trasferimento Servizio trasferimento intelligente in background (BITS).

La procedura seguente consente di ottenere uno schema di autenticazione e di creare una struttura di identità di autenticazione. Quindi, l'applicazione crea un processo di download BITS e imposta le credenziali per il processo. Dopo la creazione del processo, l'applicazione ottiene un puntatore a un'interfaccia di callback e esegue il polling dello stato del processo di trasferimento BITS. Una volta completato il processo, questo viene rimosso dalla coda.

Questo esempio usa l'intestazione e l'implementazione definite in [esempio: classi comuni](common-classes.md).

**Per specificare le credenziali di autenticazione server per un processo di trasferimento BITS**

1.  Creare una struttura di contenitori che esegue il mapping dei valori dello [**\_ \_ schema di autenticazione BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) ai nomi degli schemi.

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

    

2.  Inizializzare i parametri COM chiamando la funzione CCoInitializer. Per ulteriori informazioni sulla funzione CCoInitializer, vedere [example: Common Classes](common-classes.md).
3.  Preparare una struttura di [**\_ \_ credenziali di autenticazione BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) . Nell'esempio viene utilizzata la funzione [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) per cancellare le posizioni di memoria associate alle informazioni riservate. La funzione [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) è definita in winbase. h.
4.  Utilizzare la funzione getScheme per ottenere lo schema di autenticazione da utilizzare per la connessione al server.

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

    

5.  Popolare la struttura delle [**\_ \_ credenziali**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) di autenticazione di BG con lo schema di autenticazione restituito dalla funzione getScheme e il nome utente e la password passati nella funzione ServerAuthentication.
6.  Ottenere un puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).
7.  Inizializzare la sicurezza del processo COM chiamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS richiede almeno il livello di rappresentazione della rappresentazione. BITS ha esito negativo con E \_ AccessDenied se il livello di rappresentazione corretto non è impostato.
8.  Ottenere un puntatore all'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e ottenere il localizzatore iniziale sui bit chiamando la funzione [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
9.  Creare un processo di trasferimento BITS chiamando il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
10. Ottenere un puntatore all'interfaccia di callback CNotifyInterface e chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) per ricevere la notifica di eventi correlati al processo. Per ulteriori informazioni su CNotifyInterface, vedere [esempio: classi comuni](common-classes.md).
11. Chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) per impostare i tipi di notifiche da ricevere. In questo esempio vengono impostati i flag di errore **BG \_ Notify \_ Job \_ trasferiti** e **BG \_ Notify \_ Job \_** .
12. Ottenere un puntatore all'interfaccia [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Usare il puntatore **IBackgroundCopyJob2** per impostare proprietà aggiuntive nel processo. Questo programma usa il metodo [**IBackgroundCopyJob2:: Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per impostare le credenziali per il processo di trasferimento BITS.
13. Aggiungere i file al processo di trasferimento BITS chiamando [**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile). In questo esempio, il metodo **Metodo ibackgroundcopyjob:: AddFile** usa le variabili fileremoto e LocalFile passate nella funzione ServerAuthentication.
14. Una volta aggiunto il file, chiamare [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per riprendere il processo.
15. Configurare un ciclo while per attendere il messaggio QUIT dall'interfaccia di callback mentre è in corso il trasferimento del processo.

    > [!Note]  
    > Questo passaggio è necessario solo se l'Apartment COM è un Apartment a thread singolo. Per altre informazioni, vedere [Apartment a thread singolo](../com/single-threaded-apartments.md).

     

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

    

    Il ciclo precedente usa la funzione [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) per recuperare il numero di millisecondi trascorsi dall'avvio del processo di trasferimento.

16. Al termine del processo di trasferimento BITS, rimuovere il processo dalla coda chiamando [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

Nell'esempio di codice seguente vengono specificate le credenziali di autenticazione server per un processo di trasferimento BITS.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Esempio: classi comuni](common-classes.md)
</dt> </dl>

 

 