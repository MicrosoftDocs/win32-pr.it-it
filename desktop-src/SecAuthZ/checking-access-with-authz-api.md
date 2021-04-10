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
# <a name="checking-access-with-authz-api"></a><span data-ttu-id="34d8b-103">Verifica dell'accesso con l'API Authz</span><span class="sxs-lookup"><span data-stu-id="34d8b-103">Checking Access with Authz API</span></span>

<span data-ttu-id="34d8b-104">Le applicazioni determinano se concedere l'accesso agli oggetti a protezione diretta chiamando la funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="34d8b-104">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

<span data-ttu-id="34d8b-105">La funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) accetta sia le strutture di [**\_ \_ richiesta di accesso AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) che di [**\_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) come parametri.</span><span class="sxs-lookup"><span data-stu-id="34d8b-105">The [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function takes both [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) and [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structures as parameters.</span></span> <span data-ttu-id="34d8b-106">La struttura della **\_ \_ richiesta di accesso AUTHZ** specifica un livello di accesso richiesto.</span><span class="sxs-lookup"><span data-stu-id="34d8b-106">The **AUTHZ\_ACCESS\_REQUEST** structure specifies a level of access requested.</span></span> <span data-ttu-id="34d8b-107">La funzione **AuthzAccessCheck** valuta l'accesso richiesto rispetto al **\_ descrittore di sicurezza** specificato per un contesto client specificato.</span><span class="sxs-lookup"><span data-stu-id="34d8b-107">The **AuthzAccessCheck** function evaluates the requested access against the specified **SECURITY\_DESCRIPTOR** for a specified client context.</span></span> <span data-ttu-id="34d8b-108">Per informazioni sul modo in cui un descrittore di sicurezza controlla l'accesso a un oggetto, vedere [come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="34d8b-108">For information about how a security descriptor controls access to an object, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="34d8b-109">Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="34d8b-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="callback-function"></a><span data-ttu-id="34d8b-110">Funzione di callback</span><span class="sxs-lookup"><span data-stu-id="34d8b-110">Callback Function</span></span>

<span data-ttu-id="34d8b-111">Se l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) [**del \_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) dell'oggetto da controllare contiene le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) di callback, [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) chiama la funzione [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) per ogni ACE di callback contenuto nell'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="34d8b-111">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) of the object to be checked contains any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) calls the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function for each callback ACE contained in the DACL.</span></span> <span data-ttu-id="34d8b-112">Una voce ACE di callback è qualsiasi struttura ACE il cui tipo ACE contiene la parola "callback".</span><span class="sxs-lookup"><span data-stu-id="34d8b-112">A callback ACE is any ACE structure whose ACE type contains the word "callback."</span></span> <span data-ttu-id="34d8b-113">La funzione **AuthzAccessCheckCallback** è una funzione definita dall'applicazione che deve essere registrata quando il gestore di risorse viene inizializzato chiamando la funzione [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="34d8b-113">The **AuthzAccessCheckCallback** function is an application-defined function that must be registered when the resource manager is initialized by calling the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function.</span></span>

<span data-ttu-id="34d8b-114">Una funzione di callback consente a un'applicazione di definire la logica di business da valutare in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="34d8b-114">A callback function allows an application to define business logic to be evaluated at runtime.</span></span> <span data-ttu-id="34d8b-115">Quando viene chiamata la funzione [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) , l'ACE di callback che ha causato la chiamata viene passata alla funzione di callback per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="34d8b-115">When the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function is called, the callback ACE that caused the call is passed to the callback function for evaluation.</span></span> <span data-ttu-id="34d8b-116">Se la logica definita dall'applicazione restituisce **true**, la voce ACE di callback viene inclusa nel controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="34d8b-116">If the application-defined logic evaluates as **TRUE**, then the callback ACE is included in the access check.</span></span> <span data-ttu-id="34d8b-117">In caso contrario, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="34d8b-117">Otherwise, it is ignored.</span></span>

## <a name="caching-access-results"></a><span data-ttu-id="34d8b-118">Memorizzazione nella cache dei risultati di accesso</span><span class="sxs-lookup"><span data-stu-id="34d8b-118">Caching Access Results</span></span>

<span data-ttu-id="34d8b-119">I risultati di un controllo di accesso possono essere memorizzati nella cache e usati in chiamate future alla funzione [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="34d8b-119">The results of an access check can be cached and used in future calls to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="34d8b-120">Per ulteriori informazioni sulla memorizzazione nella cache dei controlli di accesso, incluso un esempio, vedere [caching Access Checks](caching-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="34d8b-120">For more information about caching access checks, including an example, see [Caching Access Checks](caching-access-checks.md).</span></span>

## <a name="example"></a><span data-ttu-id="34d8b-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="34d8b-121">Example</span></span>

<span data-ttu-id="34d8b-122">Nell'esempio seguente viene creato [**un \_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) che consente l'accesso al **\_ controllo di lettura** agli amministratori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="34d8b-122">The following example creates a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) that allows **READ\_CONTROL** access to built-in administrators.</span></span> <span data-ttu-id="34d8b-123">USA tale descrittore di sicurezza per controllare l'accesso per il client specificato dal contesto client creato nell'esempio nell' [inizializzazione di un contesto client](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="34d8b-123">It uses that security descriptor to check access for the client specified by the client context created in the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="34d8b-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34d8b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34d8b-125">Aggiunta di SID a un contesto client</span><span class="sxs-lookup"><span data-stu-id="34d8b-125">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="34d8b-126">Memorizzazione nella cache di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="34d8b-126">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="34d8b-127">Inizializzazione di un contesto client</span><span class="sxs-lookup"><span data-stu-id="34d8b-127">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="34d8b-128">Esecuzione di query su un contesto client</span><span class="sxs-lookup"><span data-stu-id="34d8b-128">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
