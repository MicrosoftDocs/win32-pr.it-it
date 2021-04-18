---
description: Un controllo di accesso determina se un descrittore di sicurezza concede un set specificato di diritti di accesso al client o al thread identificato da un token di accesso.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Esecuzione di controlli di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9af65605b6e96a5ad8b820de876d553f8d19202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315195"
---
# <a name="performing-access-checks"></a><span data-ttu-id="d1238-103">Esecuzione di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="d1238-103">Performing Access Checks</span></span>

<span data-ttu-id="d1238-104">Un controllo di accesso determina se un descrittore di sicurezza concede un set specificato di diritti di accesso al client o al thread identificato da un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="d1238-104">An access check determines whether a security descriptor grants a specified set of access rights to the client or thread identified by an access token.</span></span> <span data-ttu-id="d1238-105">È possibile chiamare la funzione di sicurezza [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) da applicazioni client WMI o da provider scritti in C++ o C#.</span><span class="sxs-lookup"><span data-stu-id="d1238-105">You can call the security function [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) from WMI client applications or providers written in C++ or C#.</span></span> <span data-ttu-id="d1238-106">Gli script e le applicazioni Visual Basic non possono eseguire controlli di accesso usando il metodo descritto qui.</span><span class="sxs-lookup"><span data-stu-id="d1238-106">Scripts and Visual Basic applications cannot perform access checks using the method described here.</span></span>

<span data-ttu-id="d1238-107">Le applicazioni client devono eseguire un controllo di accesso per determinare l'identità del callback quando restituiscono risultati al sink fornito dalla chiamata asincrona del client.</span><span class="sxs-lookup"><span data-stu-id="d1238-107">Client applications should do an access check to determine the identity of the callback when returning results to the sink provided by the client asynchronous call.</span></span>

<span data-ttu-id="d1238-108">Quando i provider non possono rappresentare l'applicazione client o lo script che richiede i dati, devono eseguire verifiche di accesso per le situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1238-108">When providers cannot impersonate the client application or script that is requesting data, they should perform access checks for the following situations:</span></span>

-   <span data-ttu-id="d1238-109">Quando si accede a risorse non protette da elenchi di controllo di accesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="d1238-109">When accessing resources that are not protected by access control lists (ACL).</span></span>
-   <span data-ttu-id="d1238-110">Quando il client si è connesso a **\_ livello C RPC, \_ \_ identificare** il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="d1238-110">When the client has connected at the **RPC\_C\_LEVEL\_IDENTIFY** impersonation level.</span></span>

> [!Note]  
> <span data-ttu-id="d1238-111">Le applicazioni C++ e C# possono controllare se i controlli di accesso vengono eseguiti da un processo separato.</span><span class="sxs-lookup"><span data-stu-id="d1238-111">C++ and C# applications can control whether access checks are performed by a separate process.</span></span> <span data-ttu-id="d1238-112">Gli script e le applicazioni Visual Basic possono leggere o modificare una chiave del registro di sistema per garantire che WMI esegua i controlli di accesso.</span><span class="sxs-lookup"><span data-stu-id="d1238-112">Scripts and Visual Basic applications can read or change a registry key to ensure that WMI performs access checks.</span></span> <span data-ttu-id="d1238-113">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="d1238-113">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

 

<span data-ttu-id="d1238-114">Nell'esempio di codice in questo argomento sono necessari i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="d1238-114">The code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#include <lmcons.h>
#define _WIN32_DCOM
#define SECURITY_WIN32
#include <wbemidl.h>
#include <security.h>
#include <safestr.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "Secur32.lib")
```



<span data-ttu-id="d1238-115">Nell'esempio di codice riportato di seguito viene illustrato come verificare che il token di sicurezza di un thread dell'applicazione client contenga le autorizzazioni appropriate per un descrittore di sicurezza specificato.</span><span class="sxs-lookup"><span data-stu-id="d1238-115">The following code example shows how to check that the security token of a client application thread contains permissions appropriate to a specified security descriptor.</span></span> <span data-ttu-id="d1238-116">La funzione accetta la stringa "domain \\ User" e restituisce il SID.</span><span class="sxs-lookup"><span data-stu-id="d1238-116">The function takes the string "domain\\user" and returns the SID.</span></span> <span data-ttu-id="d1238-117">Se la chiamata ha esito negativo, la funzione restituisce **null**; in caso contrario, il chiamante deve liberare il puntatore restituito.</span><span class="sxs-lookup"><span data-stu-id="d1238-117">If the call fails, the function returns **NULL**, otherwise the caller must free the returned pointer.</span></span>


```C++
BYTE * GetSid(LPWSTR pwcUserName)
{
    DWORD dwSidSize = 0, dwDomainSize = 0;
    SID_NAME_USE use;

    // first call is to get the size
    BOOL bRet = LookupAccountNameW(

      NULL,            // system name
      pwcUserName,     // account name
      NULL,            // security identifier
      &dwSidSize,      // size of security identifier
      NULL,            // domain name
      &dwDomainSize,   // size of domain name
      &use             // SID-type indicator
      );    

    if(bRet == FALSE && ERROR_INSUFFICIENT_BUFFER 
        != GetLastError())\
        return NULL;

    BYTE * buff = new BYTE[dwSidSize];

    if(buff == NULL)
        return NULL;

    WCHAR * pwcDomain = new WCHAR[dwDomainSize];

    if(pwcDomain == NULL)

    {
        delete [] buff;
        return FALSE;
    }

    // Call to LookupAccountNameW actually gets the SID
    bRet = LookupAccountNameW(

      NULL,           // system name
      pwcUserName,    // account name
      buff,           // security identifier
      &dwSidSize,     // size of security identifier
      pwcDomain,      // domain name
      &dwDomainSize,  // size of domain name
      &use            // SID-type indicator
      );    

    delete [] pwcDomain;

    if(bRet == FALSE)
    {
        delete [] buff;
        return NULL;
    }

    return buff;
}

// This returns true if the caller is coming 
//   from the expected computer in the expected domain.

BOOL IsAllowed(LPWSTR pwsExpectedDomain, 
   LPWSTR pwsExpectedMachine)
{

    WCHAR wCallerName[UNLEN + 1];
    DWORD nSize = UNLEN + 1;

// Impersonate the caller and get its name

    HRESULT hr = CoImpersonateClient();
    if(FAILED(hr))

        return FALSE;

    BOOL bRet = GetUserNameExW(NameSamCompatible, 
       wCallerName, &nSize);

    CoRevertToSelf();

    if(bRet == FALSE)

        return FALSE;


    // take the expected domain and lan manager 
    //   style name and create a SID.  In actual
    // production code, it would be more efficient 
    //   to do this only when necessary

    WCHAR wExpectedName[UNLEN + 1];

    HRESULT hrCopyCat;
    hrCopyCat = StringCchCopy(wExpectedName,
        sizeof(pwsExpectedDomain)*sizeof(WCHAR)+1, 
        pwsExpectedDomain);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = 
        StringCchCat(wExpectedName,sizeof(wExpectedName)
        + 2*sizeof(WCHAR)+1, L"\\");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(pwsExpectedMachine)*sizeof(WCHAR)+1, 
        pwsExpectedMachine);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(WCHAR)+1, L"$");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
  

    // convert the two names to SIDs and compare.  
    // Note that SIDs are used since 
    //   the format of the names might vary.  

    BYTE * pCaller = GetSid(wCallerName);

    if(pCaller == NULL)

        return FALSE;

    BYTE * pExpected = GetSid(wExpectedName);

    if(pExpected == NULL)
    {
        delete [] pCaller;

        return FALSE;
    }

    bRet = EqualSid((PSID)pCaller, (PSID)pExpected);

    delete [] pCaller;
    delete [] pExpected;

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="d1238-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1238-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1238-119">Scelta della registrazione corretta</span><span class="sxs-lookup"><span data-stu-id="d1238-119">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="d1238-120">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="d1238-120">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="d1238-121">Sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="d1238-121">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="d1238-122">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="d1238-122">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
