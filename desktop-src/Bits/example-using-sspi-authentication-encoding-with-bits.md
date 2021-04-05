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
# <a name="example-using-sspi-authentication-encoding-with-bits"></a><span data-ttu-id="d56ed-103">Esempio: uso della codifica di autenticazione SSPI con BITS</span><span class="sxs-lookup"><span data-stu-id="d56ed-103">Example: Using SSPI Authentication Encoding with BITS</span></span>

<span data-ttu-id="d56ed-104">È possibile utilizzare l'autenticazione SSPI (Security Support Provider Interface) e i metodi Servizio trasferimento intelligente in background (BITS) per ottenere le credenziali da un utente, codificare le credenziali e impostare le credenziali codificate in un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="d56ed-104">You can use Security Support Provider Interface (SSPI) Authentication and Background Intelligent Transfer Service (BITS) methods to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span> <span data-ttu-id="d56ed-105">La codifica è necessaria per convertire la struttura di credenziali in stringhe che possono essere passate a un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="d56ed-105">Encoding is required to convert credentials structure into strings that can be passed to a BITS transfer job.</span></span>

<span data-ttu-id="d56ed-106">Per ulteriori informazioni sull'autenticazione e sui metodi SSPI, vedere [SSPI](../secauthn/sspi.md).</span><span class="sxs-lookup"><span data-stu-id="d56ed-106">For more information about SSPI authentication and methods, see [SSPI](../secauthn/sspi.md).</span></span>

<span data-ttu-id="d56ed-107">Nella procedura seguente vengono richieste le credenziali dell'utente utilizzando il pacchetto di sicurezza Negotiate.</span><span class="sxs-lookup"><span data-stu-id="d56ed-107">The following procedure prompts for credentials from the user by using the Negotiate security package.</span></span> <span data-ttu-id="d56ed-108">Il programma crea una struttura di identità di autenticazione e popola la struttura con le stringhe codificate che rappresentano il nome utente, il dominio e la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d56ed-108">The program creates an authentication identity structure and populates the structure with the encoded strings that represent the user name, domain, and password of the user.</span></span> <span data-ttu-id="d56ed-109">Il programma crea quindi un processo di download BITS e imposta il nome utente e la password codificati come credenziali per il processo.</span><span class="sxs-lookup"><span data-stu-id="d56ed-109">Then the program creates a BITS download job and sets the encoded user name and password as the credentials for the job.</span></span> <span data-ttu-id="d56ed-110">Il programma libera la struttura di identità di autenticazione dopo che non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="d56ed-110">The program frees the authentication identity structure after it is no longer needed.</span></span>

<span data-ttu-id="d56ed-111">Questo esempio usa l'intestazione e l'implementazione definite in [esempio: classi comuni](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d56ed-111">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="d56ed-112">**Per utilizzare la codifica di autenticazione SSPI con processi di trasferimento BITS**</span><span class="sxs-lookup"><span data-stu-id="d56ed-112">**To use SSPI authentication encoding with BITS transfer jobs**</span></span>

1.  <span data-ttu-id="d56ed-113">Inizializzare i parametri COM chiamando la funzione CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="d56ed-113">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="d56ed-114">Per ulteriori informazioni sulla funzione CCoInitializer, vedere [example: Common Classes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d56ed-114">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="d56ed-115">Ottiene i puntatori per le interfacce [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)e [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="d56ed-115">Get pointers for the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interfaces.</span></span> <span data-ttu-id="d56ed-116">In questo esempio viene utilizzata la [classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) per gestire i puntatori di interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="d56ed-116">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="d56ed-117">Creare una struttura di [ \_ informazioni CREDUI](/windows/win32/api/wincred/ns-wincred-credui_infoa) che contiene informazioni per personalizzare l'aspetto della finestra di dialogo per la [funzione SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="d56ed-117">Create a [CREDUI\_INFO](/windows/win32/api/wincred/ns-wincred-credui_infoa) structure that contains information for customizing the appearance of the dialog box for the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span> <span data-ttu-id="d56ed-118">Quindi richiedere le credenziali all'utente.</span><span class="sxs-lookup"><span data-stu-id="d56ed-118">Then prompt for credentials from the user.</span></span> <span data-ttu-id="d56ed-119">Per ulteriori informazioni, vedere la [funzione SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="d56ed-119">For more information, see the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span>
4.  <span data-ttu-id="d56ed-120">Codificare la struttura delle credenziali come stringhe che possono essere passate a un processo di trasferimento BITS tramite la funzione [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) .</span><span class="sxs-lookup"><span data-stu-id="d56ed-120">Encode credential structure as strings that can be passed to a BITS transfer job by using the [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) function.</span></span>
5.  <span data-ttu-id="d56ed-121">Preparare una struttura di [**\_ \_ credenziali di autenticazione BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="d56ed-121">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span>
6.  <span data-ttu-id="d56ed-122">Inizializzare la sicurezza del processo COM chiamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="d56ed-122">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="d56ed-123">BITS richiede almeno il livello di rappresentazione della rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="d56ed-123">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="d56ed-124">BITS ha esito negativo con **E \_ AccessDenied** se il livello di rappresentazione corretto non è impostato.</span><span class="sxs-lookup"><span data-stu-id="d56ed-124">BITS fails with **E\_ACCESSDENIED** if the correct impersonation level is not set.</span></span>
7.  <span data-ttu-id="d56ed-125">Ottenere il localizzatore iniziale sui bit chiamando la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="d56ed-125">Obtain the initial locator to BITS by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
8.  <span data-ttu-id="d56ed-126">Creare un processo di trasferimento BITS chiamando il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="d56ed-126">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
9.  <span data-ttu-id="d56ed-127">Ottenere l'identificatore per l'interfaccia [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) e chiamare il metodo **Metodo ibackgroundcopyjob:: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="d56ed-127">Get the identifier for the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface, and call the **IBackgroundCopyJob::QueryInterface** method.</span></span>
10. <span data-ttu-id="d56ed-128">Popolare la struttura delle [**\_ \_ credenziali**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) di autenticazione di BG con le stringhe nome utente e password codificate e impostare lo schema di autenticazione su Negotiate (schema di autenticazione **BG \_ \_ \_ Negotiate**).</span><span class="sxs-lookup"><span data-stu-id="d56ed-128">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure with the encoded user name and password strings, and set the authentication scheme to Negotiate (**BG\_AUTH\_SCHEME\_NEGOTIATE**).</span></span>
11. <span data-ttu-id="d56ed-129">Usare il puntatore [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) per eseguire richieste a BITS.</span><span class="sxs-lookup"><span data-stu-id="d56ed-129">Use the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) pointer to make requests to BITS.</span></span> <span data-ttu-id="d56ed-130">Questo programma usa il metodo [**IBackgroundCopyJob2:: Secredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per impostare le credenziali per il processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="d56ed-130">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
12. <span data-ttu-id="d56ed-131">Aggiungere file, modificare le proprietà o riprendere il processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="d56ed-131">Add files, modify properties, or resume the BITS transfer job.</span></span>
13. <span data-ttu-id="d56ed-132">Al termine del processo di trasferimento BITS, rimuovere il processo dalla coda chiamando [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="d56ed-132">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>
14. <span data-ttu-id="d56ed-133">Infine, liberare la struttura di identità di autenticazione chiamando la funzione [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) .</span><span class="sxs-lookup"><span data-stu-id="d56ed-133">Finally, free the authentication identity structure by calling the [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) function.</span></span>

<span data-ttu-id="d56ed-134">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare la codifica di autenticazione SSPI con processi di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="d56ed-134">The following code example demonstrates how to use SSPI Authentication Encoding with BITS transfer jobs.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d56ed-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d56ed-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d56ed-136">SSPI</span><span class="sxs-lookup"><span data-stu-id="d56ed-136">SSPI</span></span>](../secauthn/sspi.md)
</dt> <dt>

[<span data-ttu-id="d56ed-137">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="d56ed-137">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="d56ed-138">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="d56ed-138">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="d56ed-139">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="d56ed-139">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="d56ed-140">Esempio: classi comuni</span><span class="sxs-lookup"><span data-stu-id="d56ed-140">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 