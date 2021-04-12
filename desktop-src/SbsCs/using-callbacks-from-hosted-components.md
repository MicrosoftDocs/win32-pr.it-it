---
description: I callback dai componenti ospitati sono elementi che rendono possibile l'hosting. Tuttavia, è possibile che il componente che si sta ospitando abbia attivato un altro contesto di attivazione che usa per accedere ai plug-in o ai componenti propri.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Utilizzo di callback da componenti ospitati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128814"
---
# <a name="using-callbacks-from-hosted-components"></a><span data-ttu-id="84c60-104">Utilizzo di callback da componenti ospitati</span><span class="sxs-lookup"><span data-stu-id="84c60-104">Using Callbacks From Hosted Components</span></span>

<span data-ttu-id="84c60-105">I callback dai componenti ospitati sono elementi che rendono possibile l'hosting.</span><span class="sxs-lookup"><span data-stu-id="84c60-105">Callbacks from hosted components are what make hosting possible.</span></span> <span data-ttu-id="84c60-106">Tuttavia, è possibile che il componente che si sta ospitando abbia attivato un altro contesto di attivazione che usa per accedere ai plug-in o ai componenti propri.</span><span class="sxs-lookup"><span data-stu-id="84c60-106">However, it is possible that the component you are hosting has activated another activation context that it uses to access plug-ins or components of its own.</span></span> <span data-ttu-id="84c60-107">In questo caso, se il componente hosted lascia un contesto di attivazione nello stack che fa riferimento al relativo oggetto COM, l'applicazione host potrebbe chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto che si prevede sia la propria implementazione e ricevere invece l'oggetto del componente ospitato.</span><span class="sxs-lookup"><span data-stu-id="84c60-107">In this case, if the hosted component leaves an activation context on the stack that refers to its own COM object, the hosting application might call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get an object that it expects to be its own implementation and instead receive the hosted component's object.</span></span> <span data-ttu-id="84c60-108">Per evitare questa ereditarietà dei contesti di attivazione, è consigliabile che una buona applicazione host attivi il proprio contesto di attivazione noto prima durante un callback.</span><span class="sxs-lookup"><span data-stu-id="84c60-108">To prevent this inheritance of activation contexts, a good hosting applications should activate its own well-known activation context first during a callback.</span></span>

<span data-ttu-id="84c60-109">Si consideri l'esempio seguente che protegge il codice dell'applicazione host:</span><span class="sxs-lookup"><span data-stu-id="84c60-109">Consider the following example that protects the hosting application's code:</span></span>

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

<span data-ttu-id="84c60-110">In questo modo si garantisce che venga impostato un contesto di attivazione appropriato prima di passare la richiesta a un'implementazione interna di **Funct**.</span><span class="sxs-lookup"><span data-stu-id="84c60-110">This ensures that a proper activation context is set before passing the request on to some inner implementation of **Funct**.</span></span> <span data-ttu-id="84c60-111">La tua implementazione può avere l'implementazione effettiva inline, ma il metodo precedente garantisce una maggiore interoperabilità semplicemente creando wrapper delegati.</span><span class="sxs-lookup"><span data-stu-id="84c60-111">Your own implementation can have the actual implementation inline, but the preceding method ensures easier interoperability by just creating delegated wrappers.</span></span> <span data-ttu-id="84c60-112">È consigliabile usare un metodo simile quando si espongono callback normali (non COM).</span><span class="sxs-lookup"><span data-stu-id="84c60-112">It is recommended to use a similar method when exposing normal (non-COM) callbacks.</span></span>

 

 
