---
description: I contesti di attivazione sono oggetti con conteggio dei riferimenti. Per poter essere utilizzata, l'applicazione deve avere un riferimento a un contesto di attivazione.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Contesti di attivazione del conteggio dei riferimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f7806a452dc8b98f824069be0cd584c39f45ad9807a97a11f6f3d7c4929f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141934"
---
# <a name="reference-counting-activation-contexts"></a>Contesti di attivazione del conteggio dei riferimenti

I contesti di attivazione sono oggetti con conteggio dei riferimenti. Per poter essere utilizzata, l'applicazione deve avere un riferimento a un contesto di attivazione. Le funzioni dell'API del contesto di attivazione che accettano un contesto di attivazione possono eseguire il proprio conteggio dei riferimenti. Ad esempio, [**ActivateActCtx aumenta**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) e [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) riduce il conteggio dei riferimenti. Se tuttavia l'applicazione passa un contesto di attivazione senza usare queste funzioni, l'applicazione deve fornire il proprio metodo di conteggio dei riferimenti.

Quando un'applicazione chiama [**CreateActCtx,**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)l'handle restituito avrà un conteggio dei riferimenti di uno. Al termine dell'applicazione con il contesto di attivazione, l'handle deve essere rilasciato e il conteggio dei riferimenti diminuisce chiamando [**ReleaseActCtx.**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx) Non tentare di usare [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)o altre funzioni di gestione della memoria nell'handle del contesto di attivazione.

L'esempio seguente illustra un metodo per la gestione del conteggio dei riferimenti per la durata di un contesto di attivazione. La funzione Funct crea un contesto di attivazione, che quindi passa all'oggetto Target, che incrementa il conteggio dei riferimenti a 2. Funct rilascia quindi il riferimento nel contesto di attivazione e riduce il conteggio dei riferimenti a 1. La destinazione è quindi proprietaria del rilascio del proprio riferimento quando SetActCtx viene chiamato nuovamente o quando l'oggetto viene eliminato.


```C++
#include <windows.h>

class CMyObject 
{
private:
    HANDLE m_hActCtx;
public:
    CMyObject() : m_hActCtx(INVALID_HANDLE_VALUE) { }
    ~CMyObject() 
    { 
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
            m_hActCtx = INVALID_HANDLE_VALUE;
        }
    }
    void SetActCtx(HANDLE hActCtx) 
    {
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
        }
        m_hActCtx = hActCtx;
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            AddRefActCtx(m_hActCtx);
        }
    }
    void DoWorkWithActCtx();
};

void Funct(CMyObject &Target) 
{
    HANDLE hActCtx;
    ACTCTX actctx = { sizeof(ACTCTX) };
    hActCtx = CreateActCtx(&actctx);  //create activation context  
    Target.SetActCtx(hActCtx);    //pass activation context to Target; 
    // actctx now has 1 more reference
    ReleaseActCtx(hActCtx);
}
```



 

 
