---
description: Un'applicazione può aggiungere identificatori di sicurezza (SID) a un contesto client esistente chiamando la funzione AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Aggiunta di SID a un contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529730"
---
# <a name="adding-sids-to-a-client-context"></a><span data-ttu-id="00897-103">Aggiunta di SID a un contesto client</span><span class="sxs-lookup"><span data-stu-id="00897-103">Adding SIDs to a Client Context</span></span>

<span data-ttu-id="00897-104">Un'applicazione può aggiungere [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) a un contesto client esistente chiamando la funzione [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="00897-104">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span> <span data-ttu-id="00897-105">La funzione [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) consente a un'applicazione di specificare sia un elenco di SID che un elenco di SID di restrizione al contesto client specificato.</span><span class="sxs-lookup"><span data-stu-id="00897-105">The [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function allows an application to specify both a list of SIDs and a list of restricting SIDs to the specified client context.</span></span>

<span data-ttu-id="00897-106">Il sistema utilizza l'elenco dei SID di restrizione quando controlla l'accesso del token a un oggetto a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="00897-106">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="00897-107">Quando un processo o un thread con restrizioni tenta di accedere a un oggetto a protezione diretta, il sistema esegue due controlli di accesso: uno usando i SID abilitati del token e un altro usando l'elenco dei SID di restrizione.</span><span class="sxs-lookup"><span data-stu-id="00897-107">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="00897-108">L'accesso viene concesso solo se entrambi i controlli di accesso consentono i diritti di accesso richiesti.</span><span class="sxs-lookup"><span data-stu-id="00897-108">Access is granted only if both access checks allow the requested access rights.</span></span>

<span data-ttu-id="00897-109">Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="00897-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="00897-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="00897-110">Example</span></span>

<span data-ttu-id="00897-111">Nell'esempio seguente vengono aggiunti un SID e un SID restrittivo al contesto client creato dall'esempio nell' [inizializzazione di un contesto client](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="00897-111">The following example adds a SID and a restricting SID to the client context created by the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="00897-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00897-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00897-113">Memorizzazione nella cache di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="00897-113">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="00897-114">Verifica dell'accesso con l'API Authz</span><span class="sxs-lookup"><span data-stu-id="00897-114">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="00897-115">Inizializzazione di un contesto client</span><span class="sxs-lookup"><span data-stu-id="00897-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="00897-116">Esecuzione di query su un contesto client</span><span class="sxs-lookup"><span data-stu-id="00897-116">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
