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
# <a name="reference-counting-activation-contexts"></a><span data-ttu-id="8e4b5-104">Conteggio dei riferimenti dei contesti di attivazione</span><span class="sxs-lookup"><span data-stu-id="8e4b5-104">Reference Counting Activation Contexts</span></span>

<span data-ttu-id="8e4b5-105">I contesti di attivazione sono oggetti conteggiati come riferimento.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-105">Activation contexts are reference-counted objects.</span></span> <span data-ttu-id="8e4b5-106">Per usarlo, l'applicazione deve avere un riferimento a un contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-106">Your application must have a reference on an activation context in order to use it.</span></span> <span data-ttu-id="8e4b5-107">Le funzioni dell'API del contesto di attivazione che accettano un contesto di attivazione possono eseguire il proprio conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-107">The functions of the Activation Context API that take an activation context can perform their own reference counting.</span></span> <span data-ttu-id="8e4b5-108">Ad esempio, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aumenta e [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-108">For example, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) increases and [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) decreases the reference count.</span></span> <span data-ttu-id="8e4b5-109">Se tuttavia l'applicazione passa un contesto di attivazione senza usare queste funzioni, l'applicazione deve fornire il proprio metodo di conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-109">If however your application passes an activation context without using these functions, the application should provide its own method of reference counting.</span></span>

<span data-ttu-id="8e4b5-110">Quando un'applicazione chiama [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), l'handle restituito avrà un conteggio dei riferimenti di uno.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-110">When an application calls [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), the handle returned will have a reference count of one.</span></span> <span data-ttu-id="8e4b5-111">Al termine dell'applicazione con il contesto di attivazione, è necessario rilasciare l'handle e ridurre il numero di riferimenti chiamando [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span><span class="sxs-lookup"><span data-stu-id="8e4b5-111">After the application finishes with the activation context, the handle should be released and the reference count decreased by calling [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span></span> <span data-ttu-id="8e4b5-112">Non tentare di usare [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)o altre funzioni di gestione della memoria nell'handle del contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-112">Do not attempt to use [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree), or any other memory-management functions on the activation context handle.</span></span>

<span data-ttu-id="8e4b5-113">Nell'esempio seguente viene illustrato un metodo per gestire il conteggio dei riferimenti per la durata di un contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-113">The following example shows a method for handling reference counting over the lifetime of an activation context.</span></span> <span data-ttu-id="8e4b5-114">La funzione Funct crea un contesto di attivazione, che passa quindi alla destinazione dell'oggetto, che incrementa il conteggio dei riferimenti a 2.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-114">The function Funct creates an activation context, which it then passes to the object Target, which increments the reference count to 2.</span></span> <span data-ttu-id="8e4b5-115">Funct rilascia quindi il riferimento al contesto di attivazione e diminuisce di nuovo il conteggio dei riferimenti a 1.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-115">Funct then releases its reference on the activation context and decreases the reference count back to 1.</span></span> <span data-ttu-id="8e4b5-116">La destinazione possiede quindi il rilascio del proprio riferimento quando SetActCtx viene chiamato di nuovo o quando l'oggetto viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="8e4b5-116">Target then owns releasing its own reference when SetActCtx is called again or when the object is destroyed.</span></span>


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



 

 
