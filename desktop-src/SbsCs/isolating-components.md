---
description: I componenti ben creati non turbano l'ambiente dell'applicazione host, né i contesti di attivazione.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolamento dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878982"
---
# <a name="isolating-components"></a><span data-ttu-id="efaae-103">Isolamento dei componenti</span><span class="sxs-lookup"><span data-stu-id="efaae-103">Isolating Components</span></span>

<span data-ttu-id="efaae-104">I componenti ben creati non turbano l'ambiente dell'applicazione host, né i contesti di attivazione.</span><span class="sxs-lookup"><span data-stu-id="efaae-104">Well-authored components do not perturb the environment of the hosting application, nor do they leak activation contexts.</span></span> <span data-ttu-id="efaae-105">I componenti creati correttamente eseguono la gestione del contesto anziché basarsi sull'ambiente dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="efaae-105">Well-authored components perform their own context management rather than relying on the hosting application's environment.</span></span>

<span data-ttu-id="efaae-106">L'autore del componente ospitato si trova nella posizione migliore per capire esattamente quali altri assembly richiede il componente.</span><span class="sxs-lookup"><span data-stu-id="efaae-106">The author of the hosted component is in the best position to know exactly which other assemblies the component requires.</span></span> <span data-ttu-id="efaae-107">Basarsi sull'applicazione host per fornire l'ambiente corretto per il componente ospitato è una probabile fonte di errori.</span><span class="sxs-lookup"><span data-stu-id="efaae-107">Relying on the host application to provide the correct environment for your hosted component is a probable source of errors.</span></span> <span data-ttu-id="efaae-108">In alternativa, creare un manifesto per il componente ospitato che specifichi tutte le relative dipendenze e quindi eseguire la compilazione utilizzando il supporto di isolamento \_ \_ abilitato.</span><span class="sxs-lookup"><span data-stu-id="efaae-108">Instead, create a manifest for your hosted component that specifies all its dependencies, and then compile using ISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="efaae-109">Ciò garantisce che le chiamate all'esterno effettuate dal componente siano isolate e usino le versioni corrette.</span><span class="sxs-lookup"><span data-stu-id="efaae-109">This ensures that outside calls made by your component are isolated and use the correct versions.</span></span> <span data-ttu-id="efaae-110">Poiché il contesto di attivazione utilizzato da compatibile con l'isolamento \_ \_ è per ogni dll, è possibile utilizzarlo in più dll, ognuna con il proprio manifesto che chiama le dipendenze.</span><span class="sxs-lookup"><span data-stu-id="efaae-110">Because the activation context that ISOLATION\_AWARE\_ENABLED uses is per-DLL, it is safe to use in multiple DLLs, each with their own manifest calling out dependencies.</span></span>

<span data-ttu-id="efaae-111">Se non è possibile eseguire la compilazione con \_ \_ l'abilitazione dell'isolamento, usare una soluzione simile a quella illustrata nell' [uso di callback da componenti ospitati](using-callbacks-from-hosted-components.md).</span><span class="sxs-lookup"><span data-stu-id="efaae-111">If it is not possible to compile with ISOLATION\_AWARE\_ENABLED, then use a solution like the one presented in [Using Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).</span></span>

<span data-ttu-id="efaae-112">È necessario attivare il proprio contesto di attivazione in tutti i punti di ingresso che l'applicazione host può chiamare per assicurarsi che il componente ospitato venga eseguito interamente con il contesto di attivazione corretto.</span><span class="sxs-lookup"><span data-stu-id="efaae-112">You should activate your own activation context in all the entry points that the hosting application can call to ensure that your hosted component runs entirely with the correct activation context.</span></span> <span data-ttu-id="efaae-113">È possibile usare un oggetto Helper C++ per facilitare la modifica di tutti i entryPoints.</span><span class="sxs-lookup"><span data-stu-id="efaae-113">You can use a C++ helper object to facilitate changing all the entrypoints.</span></span> <span data-ttu-id="efaae-114">Ad esempio, è possibile usare una classe C++ come la seguente:</span><span class="sxs-lookup"><span data-stu-id="efaae-114">For example, you could use a C++ class such as the following:</span></span>


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



<span data-ttu-id="efaae-115">Questa operazione può quindi essere usata nel componente, usando una variabile globale per archiviare il contesto di attivazione che deve essere attivato in ogni punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="efaae-115">This can then be used in your component, using a global variable to store the activation context that should be activated on each entry point.</span></span> <span data-ttu-id="efaae-116">In questo modo, è possibile isolare il componente dall'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="efaae-116">In this way, you can isolate your component from your hosting application.</span></span>


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



