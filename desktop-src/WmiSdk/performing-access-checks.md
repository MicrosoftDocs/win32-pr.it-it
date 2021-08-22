---
description: Un controllo di accesso determina se un descrittore di sicurezza concede un set specificato di diritti di accesso al client o al thread identificato da un token di accesso.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Esecuzione dei controlli di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e06f2bccab886b38b53ecc3592371555b8c93a0ed12cdad0a4f039b62d62752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050509"
---
# <a name="performing-access-checks"></a>Esecuzione dei controlli di accesso

Un controllo di accesso determina se un descrittore di sicurezza concede un set specificato di diritti di accesso al client o al thread identificato da un token di accesso. È possibile chiamare la funzione di sicurezza [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) da applicazioni client WMI o provider scritti in C++ o C#. Gli script e Visual Basic applicazioni non possono eseguire controlli di accesso usando il metodo descritto qui.

Le applicazioni client devono eseguire un controllo di accesso per determinare l'identità del callback quando restituiscono i risultati al sink fornito dalla chiamata asincrona del client.

Quando i provider non possono rappresentare l'applicazione client o lo script che richiede i dati, devono eseguire controlli di accesso nelle situazioni seguenti:

-   Quando si accede a risorse non protette da elenchi di controllo di accesso (ACL).
-   Quando il client si è connesso al livello di rappresentazione **RPC \_ C LEVEL \_ \_ IDENTIFY.**

> [!Note]  
> Le applicazioni C++ e C# possono controllare se i controlli di accesso vengono eseguiti da un processo separato. Gli script e Visual Basic applicazioni possono leggere o modificare una chiave del Registro di sistema per assicurarsi che WMI esegua i controlli di accesso. Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)

 

L'esempio di codice in questo argomento richiede i riferimenti seguenti e \# le istruzioni include per la compilazione corretta.


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



Nell'esempio di codice seguente viene illustrato come verificare che il token di sicurezza di un thread dell'applicazione client contenga le autorizzazioni appropriate per un descrittore di sicurezza specificato. La funzione accetta la stringa "domain \\ user" e restituisce il SID. Se la chiamata ha esito negativo, la funzione restituisce **NULL,** in caso contrario il chiamante deve liberare il puntatore restituito.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta della registrazione corretta](choosing-correct-registration.md)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
