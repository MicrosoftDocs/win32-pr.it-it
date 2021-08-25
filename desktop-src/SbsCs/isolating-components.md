---
description: I componenti ben creati non perturbano l'ambiente dell'applicazione host, né perdono i contesti di attivazione.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolamento dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411d5e90114b7509dff2e5e48a4770841774df52fce804895155d2bd4d43e514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885191"
---
# <a name="isolating-components"></a>Isolamento dei componenti

I componenti ben creati non perturbano l'ambiente dell'applicazione host, né perdono i contesti di attivazione. I componenti ben creati eseguono la gestione del contesto anziché basarsi sull'ambiente dell'applicazione host.

L'autore del componente ospitato è nella posizione migliore per sapere esattamente quali altri assembly sono necessari al componente. L'uso dell'applicazione host per fornire l'ambiente corretto per il componente ospitato è una probabile origine di errori. Creare invece un manifesto per il componente ospitato che specifichi tutte le relative dipendenze e quindi eseguire la compilazione usando ISOLATION \_ AWARE \_ ENABLED. Ciò garantisce che le chiamate esterne effettuate dal componente siano isolate e usino le versioni corrette. Poiché il contesto di attivazione utilizzato da ISOLATION AWARE ENABLED è per DLL, è possibile usarlo in più DLL, ognuna con il proprio manifesto che chiama \_ \_ le dipendenze.

Se non è possibile eseguire la compilazione con ISOLATION AWARE ENABLED, usare una soluzione simile a quella presentata \_ \_ in Using [Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).

È necessario attivare il proprio contesto di attivazione in tutti i punti di ingresso che l'applicazione host può chiamare per assicurarsi che il componente ospitato venga eseguito interamente con il contesto di attivazione corretto. È possibile usare un oggetto helper C++ per facilitare la modifica di tutti i punti di ingresso. Ad esempio, è possibile usare una classe C++ come la seguente:


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



Può quindi essere usato nel componente, usando una variabile globale per archiviare il contesto di attivazione che deve essere attivato in ogni punto di ingresso. In questo modo, è possibile isolare il componente dall'applicazione host.


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



 

 



