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
# <a name="isolating-components"></a>Isolamento dei componenti

I componenti ben creati non turbano l'ambiente dell'applicazione host, né i contesti di attivazione. I componenti creati correttamente eseguono la gestione del contesto anziché basarsi sull'ambiente dell'applicazione host.

L'autore del componente ospitato si trova nella posizione migliore per capire esattamente quali altri assembly richiede il componente. Basarsi sull'applicazione host per fornire l'ambiente corretto per il componente ospitato è una probabile fonte di errori. In alternativa, creare un manifesto per il componente ospitato che specifichi tutte le relative dipendenze e quindi eseguire la compilazione utilizzando il supporto di isolamento \_ \_ abilitato. Ciò garantisce che le chiamate all'esterno effettuate dal componente siano isolate e usino le versioni corrette. Poiché il contesto di attivazione utilizzato da compatibile con l'isolamento \_ \_ è per ogni dll, è possibile utilizzarlo in più dll, ognuna con il proprio manifesto che chiama le dipendenze.

Se non è possibile eseguire la compilazione con \_ \_ l'abilitazione dell'isolamento, usare una soluzione simile a quella illustrata nell' [uso di callback da componenti ospitati](using-callbacks-from-hosted-components.md).

È necessario attivare il proprio contesto di attivazione in tutti i punti di ingresso che l'applicazione host può chiamare per assicurarsi che il componente ospitato venga eseguito interamente con il contesto di attivazione corretto. È possibile usare un oggetto Helper C++ per facilitare la modifica di tutti i entryPoints. Ad esempio, è possibile usare una classe C++ come la seguente:


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



Questa operazione può quindi essere usata nel componente, usando una variabile globale per archiviare il contesto di attivazione che deve essere attivato in ogni punto di ingresso. In questo modo, è possibile isolare il componente dall'applicazione host.


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



 

 



