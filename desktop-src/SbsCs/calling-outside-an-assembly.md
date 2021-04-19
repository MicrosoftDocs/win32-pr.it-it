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
# <a name="calling-outside-an-assembly"></a>Chiamata all'esterno di un assembly

I componenti ospitati devono garantire che il contesto di attivazione corretto sia attivo quando si chiama all'esterno del componente. Chiama il codice esterno trovato chiamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) e quindi [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), deve essere chiamato con lo stesso contesto usato per trovarlo. Le chiamate al codice individuate all'esterno dei contesti di attivazione o richiamate nell'applicazione host devono essere chiamate con il contesto di attivazione predefinito dell'applicazione.

La compilazione con il supporto di isolamento \_ \_ abilitato definito può essere utile quando si chiama all'esterno dei componenti ospitati. Ciò significa tuttavia che solo le chiamate alle API di Windows sono isolate al contesto di attivazione del componente. Questa operazione è sufficiente per la maggior parte dei casi perché le chiamate a funzioni di terze parti non hanno un contesto attivato prima della chiamata. La compilazione con \_ \_ l'abilitazione dell'isolamento abilitato non è utile se il componente usa diversi contesti di attivazione con varie API della piattaforma.

Per implementare questo, usare un attivatore del contesto di attivazione come l'esempio presentato in [Isolating Components](isolating-components.md). Qui externals. manifest è il set di dipendenze al di fuori di quelle con cui è stato compilato il componente; potrebbe contenere un elenco estendibile di componenti che devono essere caricati e usati in fase di esecuzione. Internalcontext. manifest contiene il set di dipendenze che il componente è in grado di utilizzare durante la sua durata e che deve essere impostato in tutti i entryPoints dall'esterno. Si noti che questo contesto interno viene attivato in tutti entryPoints, mentre l'attivatore del contesto viene usato con ambito C++, in modo che venga impostato il contesto appropriato quando si richiama il codice esterno usato da questo componente.

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

 

 
