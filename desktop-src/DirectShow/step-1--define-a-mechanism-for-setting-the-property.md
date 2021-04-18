---
description: Passaggio 1.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Passaggio 1. Definire un meccanismo per l'impostazione della proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314407"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="86922-104">Passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="86922-104">Step 1.</span></span> <span data-ttu-id="86922-105">Definire un meccanismo per l'impostazione della proprietà</span><span class="sxs-lookup"><span data-stu-id="86922-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="86922-106">Il filtro deve supportare una modalità di comunicazione della pagina delle proprietà, in modo che la pagina delle proprietà possa impostare e recuperare le proprietà sul filtro.</span><span class="sxs-lookup"><span data-stu-id="86922-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="86922-107">I meccanismi possibili includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="86922-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="86922-108">Esporre un'interfaccia COM personalizzata.</span><span class="sxs-lookup"><span data-stu-id="86922-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="86922-109">Supportare le proprietà di automazione tramite **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="86922-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="86922-110">Esporre l'interfaccia **IPropertyBag** e definire un set di proprietà denominate.</span><span class="sxs-lookup"><span data-stu-id="86922-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="86922-111">In questo esempio viene utilizzata un'interfaccia COM personalizzata, denominata ISaturation.</span><span class="sxs-lookup"><span data-stu-id="86922-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="86922-112">Non si tratta di un'interfaccia DirectShow effettiva; viene definito solo per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="86922-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="86922-113">Iniziare dichiarando l'interfaccia in un file di intestazione, insieme all'identificatore di interfaccia (IID):</span><span class="sxs-lookup"><span data-stu-id="86922-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


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



<span data-ttu-id="86922-114">È anche possibile definire l'interfaccia con IDL e usare il compilatore MIDL per creare il file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="86922-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="86922-115">Implementare quindi l'interfaccia personalizzata nel filtro.</span><span class="sxs-lookup"><span data-stu-id="86922-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="86922-116">In questo esempio vengono usati i metodi "Get" e "set" per il valore di saturazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="86922-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="86922-117">Si noti che entrambi i metodi proteggono il \_ membro lSaturation m con una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="86922-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


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



<span data-ttu-id="86922-118">Naturalmente, i dettagli dell'implementazione si differenziano dall'esempio illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="86922-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="86922-119">Successivo: [passaggio 2. Implementare ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span><span class="sxs-lookup"><span data-stu-id="86922-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86922-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86922-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86922-121">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="86922-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="86922-122">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="86922-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



