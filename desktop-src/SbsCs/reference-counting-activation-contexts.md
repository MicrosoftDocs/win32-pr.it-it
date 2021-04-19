---
description: I contesti di attivazione sono oggetti conteggiati come riferimento. Per usarlo, l'applicazione deve avere un riferimento a un contesto di attivazione.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Conteggio dei riferimenti dei contesti di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff00afa0dd3a347e14ff9723c06d54af4520ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317095"
---
# <a name="reference-counting-activation-contexts"></a>Conteggio dei riferimenti dei contesti di attivazione

I contesti di attivazione sono oggetti conteggiati come riferimento. Per usarlo, l'applicazione deve avere un riferimento a un contesto di attivazione. Le funzioni dell'API del contesto di attivazione che accettano un contesto di attivazione possono eseguire il proprio conteggio dei riferimenti. Ad esempio, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aumenta e [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) riduce il conteggio dei riferimenti. Se tuttavia l'applicazione passa un contesto di attivazione senza usare queste funzioni, l'applicazione deve fornire il proprio metodo di conteggio dei riferimenti.

Quando un'applicazione chiama [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), l'handle restituito avrà un conteggio dei riferimenti di uno. Al termine dell'applicazione con il contesto di attivazione, è necessario rilasciare l'handle e ridurre il numero di riferimenti chiamando [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx). Non tentare di usare [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)o altre funzioni di gestione della memoria nell'handle del contesto di attivazione.

Nell'esempio seguente viene illustrato un metodo per gestire il conteggio dei riferimenti per la durata di un contesto di attivazione. La funzione Funct crea un contesto di attivazione, che passa quindi alla destinazione dell'oggetto, che incrementa il conteggio dei riferimenti a 2. Funct rilascia quindi il riferimento al contesto di attivazione e diminuisce di nuovo il conteggio dei riferimenti a 1. La destinazione possiede quindi il rilascio del proprio riferimento quando SetActCtx viene chiamato di nuovo o quando l'oggetto viene eliminato definitivamente.


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



 

 
