---
description: Le applicazioni possono chiamare la funzione AuthzGetInformationFromContext per eseguire query sulle informazioni relative a un contesto client esistente.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Esecuzione di query su un contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308145"
---
# <a name="querying-a-client-context"></a><span data-ttu-id="7aae1-103">Esecuzione di query su un contesto client</span><span class="sxs-lookup"><span data-stu-id="7aae1-103">Querying a Client Context</span></span>

<span data-ttu-id="7aae1-104">Le applicazioni possono chiamare la funzione [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) per eseguire query sulle informazioni relative a un contesto client esistente.</span><span class="sxs-lookup"><span data-stu-id="7aae1-104">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span>

<span data-ttu-id="7aae1-105">Il parametro *InfoClass* della funzione [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) accetta un valore dall'enumerazione della [**\_ \_ \_ classe di informazioni sul contesto AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) che specifica il tipo di informazioni che la funzione esegue query.</span><span class="sxs-lookup"><span data-stu-id="7aae1-105">The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) enumeration that specifies what type of information the function queries.</span></span>

<span data-ttu-id="7aae1-106">Le variabili degli attributi di sicurezza devono essere presenti nel contesto client se si fa riferimento a in un'espressione condizionale. in caso contrario, il termine dell'espressione condizionale che vi fa riferimento verrà valutato come sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7aae1-106">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="7aae1-107">Per altre informazioni sulle espressioni condizionali, vedere il [linguaggio di definizione del descrittore di sicurezza per le voci ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="7aae1-107">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

## <a name="example"></a><span data-ttu-id="7aae1-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="7aae1-108">Example</span></span>

<span data-ttu-id="7aae1-109">Nell'esempio seguente viene eseguita una query sul contesto client creato nell'esempio dall' [inizializzazione di un contesto client](initializing-a-client-context.md) per recuperare l'elenco dei [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) dei gruppi associati a tale contesto client.</span><span class="sxs-lookup"><span data-stu-id="7aae1-109">The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) of groups associated with that client context.</span></span>


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="7aae1-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7aae1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7aae1-111">Aggiunta di SID a un contesto client</span><span class="sxs-lookup"><span data-stu-id="7aae1-111">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="7aae1-112">Memorizzazione nella cache di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="7aae1-112">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="7aae1-113">Verifica dell'accesso con l'API Authz</span><span class="sxs-lookup"><span data-stu-id="7aae1-113">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="7aae1-114">Funzionamento di AccessCheck</span><span class="sxs-lookup"><span data-stu-id="7aae1-114">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="7aae1-115">Inizializzazione di un contesto client</span><span class="sxs-lookup"><span data-stu-id="7aae1-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="7aae1-116">Linguaggio di definizione del descrittore di sicurezza per le voci</span><span class="sxs-lookup"><span data-stu-id="7aae1-116">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



