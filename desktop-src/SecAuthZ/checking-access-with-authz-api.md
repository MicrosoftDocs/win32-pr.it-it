---
description: Le applicazioni determinano se concedere l'accesso agli oggetti a protezione diretta chiamando la funzione AuthzAccessCheck.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Verifica dell'accesso con l'API Authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879494"
---
# <a name="checking-access-with-authz-api"></a>Verifica dell'accesso con l'API Authz

Le applicazioni determinano se concedere l'accesso agli oggetti a protezione diretta chiamando la funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

La funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) accetta sia le strutture di [**\_ \_ richiesta di accesso AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) che di [**\_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) come parametri. La struttura della **\_ \_ richiesta di accesso AUTHZ** specifica un livello di accesso richiesto. La funzione **AuthzAccessCheck** valuta l'accesso richiesto rispetto al **\_ descrittore di sicurezza** specificato per un contesto client specificato. Per informazioni sul modo in cui un descrittore di sicurezza controlla l'accesso a un oggetto, vedere [come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).

Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.

## <a name="callback-function"></a>Funzione di callback

Se l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) [**del \_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) dell'oggetto da controllare contiene le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) di callback, [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) chiama la funzione [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) per ogni ACE di callback contenuto nell'elenco DACL. Una voce ACE di callback è qualsiasi struttura ACE il cui tipo ACE contiene la parola "callback". La funzione **AuthzAccessCheckCallback** è una funzione definita dall'applicazione che deve essere registrata quando il gestore di risorse viene inizializzato chiamando la funzione [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .

Una funzione di callback consente a un'applicazione di definire la logica di business da valutare in fase di esecuzione. Quando viene chiamata la funzione [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) , l'ACE di callback che ha causato la chiamata viene passata alla funzione di callback per la valutazione. Se la logica definita dall'applicazione restituisce **true**, la voce ACE di callback viene inclusa nel controllo di accesso. In caso contrario, viene ignorata.

## <a name="caching-access-results"></a>Memorizzazione nella cache dei risultati di accesso

I risultati di un controllo di accesso possono essere memorizzati nella cache e usati in chiamate future alla funzione [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . Per ulteriori informazioni sulla memorizzazione nella cache dei controlli di accesso, incluso un esempio, vedere [caching Access Checks](caching-access-checks.md).

## <a name="example"></a>Esempio

Nell'esempio seguente viene creato [**un \_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) che consente l'accesso al **\_ controllo di lettura** agli amministratori predefiniti. USA tale descrittore di sicurezza per controllare l'accesso per il client specificato dal contesto client creato nell'esempio nell' [inizializzazione di un contesto client](initializing-a-client-context.md).


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

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

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di SID a un contesto client](adding-sids-to-a-client-context.md)
</dt> <dt>

[Memorizzazione nella cache di controlli di accesso](caching-access-checks.md)
</dt> <dt>

[Inizializzazione di un contesto client](initializing-a-client-context.md)
</dt> <dt>

[Esecuzione di query su un contesto client](querying-a-client-context.md)
</dt> </dl>

 

 
