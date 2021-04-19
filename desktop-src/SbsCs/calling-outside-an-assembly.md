---
description: Chiamata all'esterno di un assembly
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Chiamata all'esterno di un assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313757"
---
# <a name="calling-outside-an-assembly"></a><span data-ttu-id="a29a8-103">Chiamata all'esterno di un assembly</span><span class="sxs-lookup"><span data-stu-id="a29a8-103">Calling Outside An Assembly</span></span>

<span data-ttu-id="a29a8-104">I componenti ospitati devono garantire che il contesto di attivazione corretto sia attivo quando si chiama all'esterno del componente.</span><span class="sxs-lookup"><span data-stu-id="a29a8-104">Hosted components should ensure that the correct activation context is active when calling outside the component.</span></span> <span data-ttu-id="a29a8-105">Chiama il codice esterno trovato chiamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) e quindi [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), deve essere chiamato con lo stesso contesto usato per trovarlo.</span><span class="sxs-lookup"><span data-stu-id="a29a8-105">Calls into outside code that was found by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) and then [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), should be called with the same context that was used to find it.</span></span> <span data-ttu-id="a29a8-106">Le chiamate al codice individuate all'esterno dei contesti di attivazione o richiamate nell'applicazione host devono essere chiamate con il contesto di attivazione predefinito dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a29a8-106">Calls into code that was found outside of activation contexts, or calls back into the hosting application should be called with the application default activation context.</span></span>

<span data-ttu-id="a29a8-107">La compilazione con il supporto di isolamento \_ \_ abilitato definito può essere utile quando si chiama all'esterno dei componenti ospitati.</span><span class="sxs-lookup"><span data-stu-id="a29a8-107">Compiling with ISOLATION\_AWARE\_ENABLED defined may be useful when calling outside of hosted components.</span></span> <span data-ttu-id="a29a8-108">Ciò significa tuttavia che solo le chiamate alle API di Windows sono isolate al contesto di attivazione del componente.</span><span class="sxs-lookup"><span data-stu-id="a29a8-108">However this means that only calls to Windows APIs are isolated to the component's activation context.</span></span> <span data-ttu-id="a29a8-109">Questa operazione è sufficiente per la maggior parte dei casi perché le chiamate a funzioni di terze parti non hanno un contesto attivato prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="a29a8-109">This is sufficient for most cases because calls to third-party functions do not have a context activated before being called.</span></span> <span data-ttu-id="a29a8-110">La compilazione con \_ \_ l'abilitazione dell'isolamento abilitato non è utile se il componente usa diversi contesti di attivazione con varie API della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a29a8-110">Compiling with ISOLATION\_AWARE\_ENABLED defined does not help if your component uses several activation contexts with various platform APIs.</span></span>

<span data-ttu-id="a29a8-111">Per implementare questo, usare un attivatore del contesto di attivazione come l'esempio presentato in [Isolating Components](isolating-components.md).</span><span class="sxs-lookup"><span data-stu-id="a29a8-111">To implement this, use an activation context activator like the example presented in [Isolating Components](isolating-components.md).</span></span> <span data-ttu-id="a29a8-112">Qui externals. manifest è il set di dipendenze al di fuori di quelle con cui è stato compilato il componente; potrebbe contenere un elenco estendibile di componenti che devono essere caricati e usati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a29a8-112">Here externals.manifest is the set of dependencies outside those the component was built with; perhaps it contains some extendable list of components that are to be loaded and used during runtime.</span></span> <span data-ttu-id="a29a8-113">Internalcontext. manifest contiene il set di dipendenze che il componente è in grado di utilizzare durante la sua durata e che deve essere impostato in tutti i entryPoints dall'esterno.</span><span class="sxs-lookup"><span data-stu-id="a29a8-113">The internalcontext.manifest contains the set of dependencies that the component is sure to use during its lifetime, and which should be set in all entrypoints from the outside.</span></span> <span data-ttu-id="a29a8-114">Si noti che questo contesto interno viene attivato in tutti entryPoints, mentre l'attivatore del contesto viene usato con ambito C++, in modo che venga impostato il contesto appropriato quando si richiama il codice esterno usato da questo componente.</span><span class="sxs-lookup"><span data-stu-id="a29a8-114">Notice that this internal context is activated in all entrypoints, while the context activator is used with C++ scoping so that the proper context is set when calling out to the various outside code that this component uses.</span></span>

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
