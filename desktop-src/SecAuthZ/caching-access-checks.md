---
description: Quando un'applicazione esegue un controllo di accesso chiamando la funzione AuthzAccessCheck, i risultati del controllo di accesso possono essere memorizzati nella cache.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Memorizzazione nella cache di controlli di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967e0a5398d93c1715d7d08e5c7c75695e4120ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350586"
---
# <a name="caching-access-checks"></a><span data-ttu-id="a8ab6-103">Memorizzazione nella cache di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="a8ab6-103">Caching Access Checks</span></span>

<span data-ttu-id="a8ab6-104">Quando un'applicazione esegue un controllo di accesso chiamando la funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , i risultati del controllo di accesso possono essere memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="a8ab6-104">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span> <span data-ttu-id="a8ab6-105">Quando il parametro *pAuthzHandle* della funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) non è **null**, la funzione esegue un controllo di accesso separato con una maschera di [**accesso \_**](access-mask.md) richiesta **massima \_ consentita** e memorizza nella cache i risultati di tale controllo.</span><span class="sxs-lookup"><span data-stu-id="a8ab6-105">When the *pAuthzHandle* parameter of the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function is not **NULL**, the function performs a separate access check, with a requested [**ACCESS\_MASK**](access-mask.md) of **MAXIMUM\_ALLOWED**, and caches the results of that check.</span></span> <span data-ttu-id="a8ab6-106">Un handle per i risultati di tale controllo può quindi essere passato come parametro *AuthzHandle* alla funzione [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="a8ab6-106">A handle to the results of that check can then be passed as the *AuthzHandle* parameter to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="a8ab6-107">In questo modo è possibile controllare più rapidamente gli accessi per un determinato client e [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="a8ab6-107">This allows faster access checking for a given client and [*security descriptors*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="a8ab6-108">Solo la parte statica di un controllo di accesso può essere memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="a8ab6-108">Only the static portion of an access check can be cached.</span></span> <span data-ttu-id="a8ab6-109">Tutte le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) o ACE che contengono il SID **principale self- \_ Service** devono essere valutate per ogni controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="a8ab6-109">Any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) or ACEs that contain the **PRINCIPAL\_SELF** SID must be evaluated for each access check.</span></span>

<span data-ttu-id="a8ab6-110">Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="a8ab6-110">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="a8ab6-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8ab6-111">Example</span></span>

<span data-ttu-id="a8ab6-112">Nell'esempio seguente viene controllato l'accesso in base a un risultato memorizzato nella cache da un controllo di accesso precedente.</span><span class="sxs-lookup"><span data-stu-id="a8ab6-112">The following example checks access against a cached result from a previous access check.</span></span> <span data-ttu-id="a8ab6-113">Il controllo di accesso precedente è stato eseguito nell'esempio di [Verifica dell'accesso con l'API Authz](checking-access-with-authz-api.md).</span><span class="sxs-lookup"><span data-stu-id="a8ab6-113">The previous access check was performed in the example in [Checking Access with Authz API](checking-access-with-authz-api.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a8ab6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8ab6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ab6-115">Aggiunta di SID a un contesto client</span><span class="sxs-lookup"><span data-stu-id="a8ab6-115">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="a8ab6-116">Verifica dell'accesso con l'API Authz</span><span class="sxs-lookup"><span data-stu-id="a8ab6-116">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="a8ab6-117">Inizializzazione di un contesto client</span><span class="sxs-lookup"><span data-stu-id="a8ab6-117">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="a8ab6-118">Esecuzione di query su un contesto client</span><span class="sxs-lookup"><span data-stu-id="a8ab6-118">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
