---
description: Definire un meccanismo per l'impostazione della proprietà come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Passaggio 1. Definire un meccanismo per l'impostazione della proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410074"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="c753b-104">Passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="c753b-104">Step 1.</span></span> <span data-ttu-id="c753b-105">Definire un meccanismo per l'impostazione della proprietà</span><span class="sxs-lookup"><span data-stu-id="c753b-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="c753b-106">Il filtro deve supportare una modalità di comunicazione tra la pagina delle proprietà, in modo che la pagina delle proprietà possa impostare e recuperare le proprietà nel filtro.</span><span class="sxs-lookup"><span data-stu-id="c753b-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="c753b-107">Di seguito sono riportati i possibili meccanismi:</span><span class="sxs-lookup"><span data-stu-id="c753b-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="c753b-108">Esporre un'interfaccia COM personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c753b-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="c753b-109">Supporto delle proprietà di automazione tramite **IDispatch.**</span><span class="sxs-lookup"><span data-stu-id="c753b-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="c753b-110">Esporre **l'interfaccia IPropertyBag** e definire un set di proprietà denominate.</span><span class="sxs-lookup"><span data-stu-id="c753b-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="c753b-111">In questo esempio viene utilizzata un'interfaccia COM personalizzata, denominata ISaturation.</span><span class="sxs-lookup"><span data-stu-id="c753b-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="c753b-112">Non si tratta di un'interfaccia DirectShow effettiva. è definito solo per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="c753b-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="c753b-113">Per iniziare, dichiarare l'interfaccia in un file di intestazione, insieme all'identificatore di interfaccia (IID):</span><span class="sxs-lookup"><span data-stu-id="c753b-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



<span data-ttu-id="c753b-114">È anche possibile definire l'interfaccia con IDL e usare il compilatore MIDL per creare il file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="c753b-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="c753b-115">Implementare quindi l'interfaccia personalizzata nel filtro.</span><span class="sxs-lookup"><span data-stu-id="c753b-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="c753b-116">Questo esempio usa i metodi "Get" e "Set" per il valore di saturazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="c753b-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="c753b-117">Si noti che entrambi i metodi proteggono il membro \_ m lSaturation con una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="c753b-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



<span data-ttu-id="c753b-118">Naturalmente, i dettagli della propria implementazione differiranno dall'esempio illustrato qui.</span><span class="sxs-lookup"><span data-stu-id="c753b-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="c753b-119">Passaggio [2. Implementare ISpecifyPropertyPages.](step-2--implement-ispecifypropertypages.md)</span><span class="sxs-lookup"><span data-stu-id="c753b-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c753b-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c753b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c753b-121">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="c753b-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="c753b-122">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="c753b-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



