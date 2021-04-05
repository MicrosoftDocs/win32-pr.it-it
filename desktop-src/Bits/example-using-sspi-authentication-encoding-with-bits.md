---
title: Esempio di utilizzo della codifica di autenticazione SSPI con BITS
description: È possibile utilizzare l'autenticazione SSPI (Security Support Provider Interface) e i metodi Servizio trasferimento intelligente in background (BITS) per ottenere le credenziali da un utente, codificare le credenziali e impostare le credenziali codificate in un processo di trasferimento BITS.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b86248c4782789010a817755d9bc27b3e5373b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730162"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>Esempio: uso della codifica di autenticazione SSPI con BITS

È possibile utilizzare l'autenticazione SSPI (Security Support Provider Interface) e i metodi Servizio trasferimento intelligente in background (BITS) per ottenere le credenziali da un utente, codificare le credenziali e impostare le credenziali codificate in un processo di trasferimento BITS. La codifica è necessaria per convertire la struttura di credenziali in stringhe che possono essere passate a un processo di trasferimento BITS.

Per ulteriori informazioni sull'autenticazione e sui metodi SSPI, vedere [SSPI](../secauthn/sspi.md).

Nella procedura seguente vengono richieste le credenziali dell'utente utilizzando il pacchetto di sicurezza Negotiate. Il programma crea una struttura di identità di autenticazione e popola la struttura con le stringhe codificate che rappresentano il nome utente, il dominio e la password dell'utente. Il programma crea quindi un processo di download BITS e imposta il nome utente e la password codificati come credenziali per il processo. Il programma libera la struttura di identità di autenticazione dopo che non è più necessaria.

Questo esempio usa l'intestazione e l'implementazione definite in [esempio: classi comuni](common-classes.md).

**Per utilizzare la codifica di autenticazione SSPI con processi di trasferimento BITS**

1.  Inizializzare i parametri COM chiamando la funzione CCoInitializer. Per ulteriori informazioni sulla funzione CCoInitializer, vedere [example: Common Classes](common-classes.md).
2.  Ottiene i puntatori per le interfacce [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)e [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) . In questo esempio viene utilizzata la [classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) per gestire i puntatori di interfaccia com.
3.  Creare una struttura di [ \_ informazioni CREDUI](/windows/win32/api/wincred/ns-wincred-credui_infoa) che contiene informazioni per personalizzare l'aspetto della finestra di dialogo per la [funzione SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa). Quindi richiedere le credenziali all'utente. Per ulteriori informazioni, vedere la [funzione SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).
4.  Codificare la struttura delle credenziali come stringhe che possono essere passate a un processo di trasferimento BITS tramite la funzione [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) .
5.  Preparare una struttura di [**\_ \_ credenziali di autenticazione BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) .
6.  Inizializzare la sicurezza del processo COM chiamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS richiede almeno il livello di rappresentazione della rappresentazione. BITS ha esito negativo con **E \_ AccessDenied** se il livello di rappresentazione corretto non è impostato.
7.  Ottenere il localizzatore iniziale sui bit chiamando la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
8.  Creare un processo di trasferimento BITS chiamando il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
9.  Ottenere l'identificatore per l'interfaccia [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) e chiamare il metodo **Metodo ibackgroundcopyjob:: QueryInterface** .
10. Popolare la struttura delle [**\_ \_ credenziali**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) di autenticazione di BG con le stringhe nome utente e password codificate e impostare lo schema di autenticazione su Negotiate (schema di autenticazione **BG \_ \_ \_ Negotiate**).
11. Usare il puntatore [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) per eseguire richieste a BITS. Questo programma usa il metodo [**IBackgroundCopyJob2:: Secredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per impostare le credenziali per il processo di trasferimento BITS.
12. Aggiungere file, modificare le proprietà o riprendere il processo di trasferimento BITS.
13. Al termine del processo di trasferimento BITS, rimuovere il processo dalla coda chiamando [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).
14. Infine, liberare la struttura di identità di autenticazione chiamando la funzione [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) .

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare la codifica di autenticazione SSPI con processi di trasferimento BITS.


```C++
#define SECURITY_WIN32
#define _SEC_WINNT_AUTH_TYPES

#include <windows.h>
#include <ntsecapi.h>
#include <bits.h>
#include <sspi.h>
#include <wincred.h>
#include <iostream>
#include <atlbase.h>
#include "CommonCode.h"

void PromptForCredentials(PWSTR pwTargetName)
{
    HRESULT hr;
    
    // If CoInitializeEx fails, the exception is unhandled and the program terminates
    CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    CComPtr<IBackgroundCopyManager> pQueueMgr;
    CComPtr<IBackgroundCopyJob> pJob;
    CComPtr<IBackgroundCopyJob2> pJob2;

    PSEC_WINNT_AUTH_IDENTITY_OPAQUE pAuthIdentityEx2 = NULL;
    DWORD dwFlags = 0;
    BOOL fSave = FALSE;
    BOOL bReturn = TRUE;

    CREDUI_INFO creduiInfo = { 0 };
    creduiInfo.cbSize = sizeof(creduiInfo);
    // Change the message text and caption to the actual text for your dialog.
    creduiInfo.pszMessageText = pwTargetName;
    creduiInfo.pszCaptionText = L"SSPIPFC title for the dialog box";

    try {
        // Prompt for credentials from user using Negotiate security package.
        DWORD dwRet = SspiPromptForCredentials(
            pwTargetName,
            &creduiInfo,
            0,
            L"Negotiate", 
            NULL,
            &pAuthIdentityEx2,
            &fSave,
            dwFlags
            );

        if (SEC_E_OK != dwRet) 
        {
            // Prompt for credentials failed.
            throw MyException(dwRet, L"SspiPromptForCredentials");
        }

        if (NULL != pAuthIdentityEx2) 
        {
            GUID guidJob;
            BG_AUTH_CREDENTIALS authCreds;

            PCWSTR pwUserName = NULL;
            PCWSTR pwDomainName = NULL;
            PCWSTR pwPassword = NULL;

            // Encode credential structure as strings that can
            // be passed to a BITS job.
            SECURITY_STATUS secStatus = SspiEncodeAuthIdentityAsStrings(
                pAuthIdentityEx2,
                &pwUserName,
                &pwDomainName,
                &pwPassword
                );

            if(SEC_E_OK != secStatus) 
            {
                // Encode authentication identity as strings.
                throw MyException(secStatus, L"SspiEncodeAuthIdentityAsStrings");   
            }

            // Show the encoded user name and domain name.
            wprintf(
                L"User Name: %s\nDomain Name: %s",
                pwUserName,
                pwDomainName
                );

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
            hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                CLSCTX_LOCAL_SERVER,
                __uuidof(IBackgroundCopyManager),
                (void**) &pQueueMgr);

            if (FAILED(hr))
            {
                // Failed to connect.
                throw MyException(hr, L"CoCreateInstance");
            }

            // Create a job.
            hr = pQueueMgr->CreateJob(
                L"EncodeSample", 
                BG_JOB_TYPE_DOWNLOAD, 
                &guidJob, 
                &pJob
                );

            if(FAILED(hr))
            {   
                // Failed to create a BITS job.
                throw MyException(hr, L"CreateJob");
            }

            // Get IBackgroundCopyJob2 interface.
            hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
            if (FAILED(hr)) 
            {
                // Failed to get a reference to the IBackgroundCopyJob2 interface.
                throw MyException(hr, L"QueryInterface(IBackgroundCopyJob2)");
            }

            // Create a BITS authentication structure from the encoded strings.
            authCreds.Target = BG_AUTH_TARGET_SERVER;
            authCreds.Scheme = BG_AUTH_SCHEME_NEGOTIATE;
            authCreds.Credentials.Basic.UserName = (LPWSTR)pwUserName;
            authCreds.Credentials.Basic.Password = (LPWSTR)pwPassword;

            // Set the credentials for the job.
            hr = pJob2->SetCredentials(&authCreds);
            if (FAILED(hr)) 
            {
                // Failed to set credentials.
                throw MyException(hr, L"SetCredentials");
            }

            // Modify the job's property values.
            // Add files to the job.
            // Activate (resume) the job in the transfer queue.

            // Remove the job from the transfer queue.
            hr = pJob->Complete();
            if (FAILED(hr)) 
            {
                // Failed to complete the job.
                throw MyException(hr, L"Complete");
            }
        }
    }
    catch(std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }
    catch(MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }

    // Free the auth identity structure.
    if (NULL != pAuthIdentityEx2)
    {
        SspiFreeAuthIdentity(pAuthIdentityEx2);
        pAuthIdentityEx2 = NULL;
    }

    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{
    PromptForCredentials(L"Target");
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SSPI](../secauthn/sspi.md)
</dt> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Esempio: classi comuni](common-classes.md)
</dt> </dl>

 

 