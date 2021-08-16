---
description: Quando un'applicazione esegue un controllo di accesso chiamando la funzione AuthzAccessCheck, i risultati di tale controllo di accesso possono essere memorizzati nella cache.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Caching Controlli di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83659c35fb9334e55bd7dfcd2368275dc16eb0d4836b8d6fa69a6ed8d713d953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783556"
---
# <a name="caching-access-checks"></a>Caching Controlli di accesso

Quando un'applicazione esegue un controllo di accesso chiamando la funzione [**AuthzAccessCheck,**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) i risultati di tale controllo di accesso possono essere memorizzati nella cache. Quando il *parametro pAuthzHandle* della funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) non è **NULL,** la [**funzione \_**](access-mask.md) esegue un controllo di accesso separato, con una maschera di accesso richiesta di **MAXIMUM \_ ALLOWED,** e memorizza nella cache i risultati di tale controllo. Un handle per i risultati di tale controllo può quindi essere passato come parametro *AuthzHandle* alla [**funzione AuthzCachedAccessCheck.**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) Ciò consente un controllo di accesso più rapido per un determinato client e [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly).

Solo la parte statica di un controllo di accesso può essere memorizzata nella cache. Per ogni [*controllo di*](/windows/desktop/SecGloss/a-gly) accesso è necessario valutare tutte le voci di controllo di accesso di callback (ACE) o le voci ACE contenenti il SID **\_ SELF** principale.

Le variabili di attributo devono essere nel formato di un'espressione se usate con operatori logici. in caso contrario, vengono valutati come sconosciuti.

## <a name="example"></a>Esempio

Nell'esempio seguente viene controllato l'accesso rispetto a un risultato memorizzato nella cache da un controllo di accesso precedente. Il controllo di accesso precedente è stato eseguito nell'esempio in [Verifica dell'accesso con Authz API](checking-access-with-authz-api.md).


```C++
BOOL CheckCachedAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR                pSecurityDescriptor = NULL;
    ULONG                                cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST                Request;
    CHAR                                ReplyBuffer[MY_MAX];
    CHAR                                CachedReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY                    pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    PAUTHZ_ACCESS_REPLY                    pCachedReply = (PAUTHZ_ACCESS_REPLY)CachedReplyBuffer;
    DWORD                                AuthzError =0;
    AUTHZ_ACCESS_CHECK_RESULTS_HANDLE    hCached;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the initial access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Allocate memory for the cached access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the cached access reply structure.
    pCachedReply->ResultListLength = 1;
    pCachedReply->Error = (PDWORD) ((PCHAR) pCachedReply + sizeof(AUTHZ_ACCESS_REPLY));
    pCachedReply->GrantedAccessMask = (PACCESS_MASK) (pCachedReply->Error + pCachedReply->ResultListLength);
    pCachedReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck and cache results.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        &hCached))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
        
        return FALSE;
    }

    //Call AuthzCachedAccessCheck with the cached result from the previous call.
    if(!AuthzCachedAccessCheck(
        0,
        hCached,
        &Request,
        NULL,
        pCachedReply))
    {
        printf_s("AuthzCachedAccessCheck failed with %d\n", GetLastError());
        
        LocalFree(pSecurityDescriptor);
    AuthzFreeHandle(hCached);
    
        return FALSE;
    }

    //Print results.
    if(*pCachedReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }


  LocalFree(pSecurityDescriptor);
  AuthzFreeHandle(hCached);
    return TRUE;

}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di SID a un contesto client](adding-sids-to-a-client-context.md)
</dt> <dt>

[Controllo dell'accesso con Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Inizializzazione di un contesto client](initializing-a-client-context.md)
</dt> <dt>

[Esecuzione di query su un contesto client](querying-a-client-context.md)
</dt> </dl>

 

 
