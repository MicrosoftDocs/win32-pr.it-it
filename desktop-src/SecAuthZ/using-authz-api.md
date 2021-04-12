---
description: L'API Authz consente alle applicazioni di eseguire controlli di accesso personalizzabili con prestazioni migliori e uno sviluppo più semplificato rispetto al controllo di accesso di basso livello.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Uso dell'API Authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349706"
---
# <a name="using-authz-api"></a><span data-ttu-id="af5e6-103">Uso dell'API Authz</span><span class="sxs-lookup"><span data-stu-id="af5e6-103">Using Authz API</span></span>

<span data-ttu-id="af5e6-104">L'API Authz consente alle applicazioni di eseguire controlli di accesso personalizzabili con prestazioni migliori e uno sviluppo più semplificato rispetto [al controllo di accesso di basso livello](low-level-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="af5e6-104">Authz API allows applications to perform customizable access checks with better performance and more simplified development than [Low-level Access Control](low-level-access-control.md).</span></span>

<span data-ttu-id="af5e6-105">L'API Authz consente alle applicazioni di memorizzare nella cache i controlli di accesso per migliorare le prestazioni, eseguire query e modificare i contesti dei client e definire regole business che possono essere usate per valutare in modo dinamico le autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="af5e6-105">Authz API allows applications to cache access checks for improved performance, to query and modify client contexts, and to define business rules that can be used to evaluate access permission dynamically.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af5e6-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="af5e6-106">In This Section</span></span>



| <span data-ttu-id="af5e6-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="af5e6-107">Topic</span></span>                                                                             | <span data-ttu-id="af5e6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af5e6-108">Description</span></span>                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af5e6-109">Inizializzazione di un contesto client</span><span class="sxs-lookup"><span data-stu-id="af5e6-109">Initializing a Client Context</span></span>](initializing-a-client-context.md)<br/>     | <span data-ttu-id="af5e6-110">Un'applicazione deve creare un contesto client prima di poter usare l'API Authz per eseguire verifiche di accesso o controllo.</span><span class="sxs-lookup"><span data-stu-id="af5e6-110">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="af5e6-111">Esecuzione di query su un contesto client</span><span class="sxs-lookup"><span data-stu-id="af5e6-111">Querying a Client Context</span></span>](querying-a-client-context.md)<br/>             | <span data-ttu-id="af5e6-112">Le applicazioni possono chiamare la funzione [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) per eseguire query sulle informazioni relative a un contesto client esistente.</span><span class="sxs-lookup"><span data-stu-id="af5e6-112">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="af5e6-113">Aggiunta di SID a un contesto client</span><span class="sxs-lookup"><span data-stu-id="af5e6-113">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)<br/> | <span data-ttu-id="af5e6-114">Un'applicazione può aggiungere [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) a un contesto client esistente chiamando la funzione [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="af5e6-114">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span><br/> |
| [<span data-ttu-id="af5e6-115">Verifica dell'accesso con l'API Authz</span><span class="sxs-lookup"><span data-stu-id="af5e6-115">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)<br/>   | <span data-ttu-id="af5e6-116">Le applicazioni determinano se concedere l'accesso agli oggetti a protezione diretta chiamando la funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="af5e6-116">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="af5e6-117">Memorizzazione nella cache di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="af5e6-117">Caching Access Checks</span></span>](caching-access-checks.md)<br/>                     | <span data-ttu-id="af5e6-118">Quando un'applicazione esegue un controllo di accesso chiamando la funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , i risultati del controllo di accesso possono essere memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="af5e6-118">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span><br/>                                                                                       |



 

 

