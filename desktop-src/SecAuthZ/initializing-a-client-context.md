---
description: Un'applicazione deve creare un contesto client prima di poter usare l'API Authz per eseguire verifiche di accesso o controllo.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inizializzazione di un contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317045"
---
# <a name="initializing-a-client-context"></a><span data-ttu-id="a004d-103">Inizializzazione di un contesto client</span><span class="sxs-lookup"><span data-stu-id="a004d-103">Initializing a Client Context</span></span>

<span data-ttu-id="a004d-104">Un'applicazione deve creare un contesto client prima di poter usare l'API Authz per eseguire verifiche di accesso o controllo.</span><span class="sxs-lookup"><span data-stu-id="a004d-104">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span>

<span data-ttu-id="a004d-105">Per inizializzare Resource Manager, un'applicazione deve chiamare la funzione [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="a004d-105">An application must call the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function to initialize the resource manager.</span></span> <span data-ttu-id="a004d-106">L'applicazione può quindi chiamare una delle diverse funzioni per creare un contesto client.</span><span class="sxs-lookup"><span data-stu-id="a004d-106">The application can then call one of several functions to create a client context.</span></span> <span data-ttu-id="a004d-107">Inoltre, se si eseguono controlli di accesso o di controllo in modalità remota, è necessario utilizzare la funzione [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="a004d-107">Additionally, if you are performing access checks or auditing remotely, you must use the [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) function.</span></span>

<span data-ttu-id="a004d-108">Per creare un contesto client basato su un contesto client esistente, chiamare la funzione [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .</span><span class="sxs-lookup"><span data-stu-id="a004d-108">To create a client context based on an existing client context, call the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) function.</span></span>

<span data-ttu-id="a004d-109">La funzione [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crea un nuovo contesto client usando le informazioni contenute in un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="a004d-109">The [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function creates a new client context by using information in a logon token.</span></span> <span data-ttu-id="a004d-110">La funzione [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crea un nuovo contesto client usando il [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)specificato.</span><span class="sxs-lookup"><span data-stu-id="a004d-110">The [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) function creates a new client context by using the specified [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid).</span></span>

<span data-ttu-id="a004d-111">Se possibile, chiamare la funzione [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) anziché [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span><span class="sxs-lookup"><span data-stu-id="a004d-111">If possible, call the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function instead of [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span></span> <span data-ttu-id="a004d-112">**AuthzInitializeContextFromSid** tenta di recuperare le informazioni disponibili in un token di accesso se il client ha effettivamente effettuato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="a004d-112">**AuthzInitializeContextFromSid** attempts to retrieve the information available in a logon token had the client actually logged on.</span></span> <span data-ttu-id="a004d-113">Un token di accesso effettivo fornisce ulteriori informazioni, ad esempio il tipo di accesso e le proprietà di accesso, e riflette il comportamento del pacchetto di autenticazione utilizzato per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="a004d-113">An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon.</span></span> <span data-ttu-id="a004d-114">Il contesto client creato da **AuthzInitializeContextFromToken** utilizza un token di accesso e il contesto client risultante è più completo e accurato rispetto a un contesto client creato da **AuthzInitializeContextFromSid**.</span><span class="sxs-lookup"><span data-stu-id="a004d-114">The client context created by **AuthzInitializeContextFromToken** uses a logon token, and the resulting client context is more complete and accurate than a client context created by **AuthzInitializeContextFromSid**.</span></span>

> [!Note]  
> <span data-ttu-id="a004d-115">Le variabili degli attributi di sicurezza devono essere presenti nel contesto client se si fa riferimento a in un'espressione condizionale. in caso contrario, il termine dell'espressione condizionale che vi fa riferimento verrà valutato come sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a004d-115">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="a004d-116">Per altre informazioni sulle espressioni condizionali, vedere il [linguaggio di definizione del descrittore di sicurezza per le voci ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="a004d-116">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

 

## <a name="example"></a><span data-ttu-id="a004d-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a004d-117">Example</span></span>

<span data-ttu-id="a004d-118">Nell'esempio seguente viene inizializzato il gestore di risorse Authz e viene chiamata la funzione [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) per creare un contesto client dal token di accesso associato al processo corrente.</span><span class="sxs-lookup"><span data-stu-id="a004d-118">The following example initializes the Authz resource manager and calls the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function to create a client context from the logon token associated with the current process.</span></span>


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="a004d-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a004d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a004d-120">Aggiunta di SID a un contesto client</span><span class="sxs-lookup"><span data-stu-id="a004d-120">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="a004d-121">Memorizzazione nella cache di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="a004d-121">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="a004d-122">Verifica dell'accesso con l'API Authz</span><span class="sxs-lookup"><span data-stu-id="a004d-122">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="a004d-123">Funzionamento di AccessCheck</span><span class="sxs-lookup"><span data-stu-id="a004d-123">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="a004d-124">Esecuzione di query su un contesto client</span><span class="sxs-lookup"><span data-stu-id="a004d-124">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="a004d-125">Linguaggio di definizione del descrittore di sicurezza per le voci</span><span class="sxs-lookup"><span data-stu-id="a004d-125">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="a004d-126">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="a004d-126">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="a004d-127">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="a004d-127">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



