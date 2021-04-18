---
description: 'Passaggio 2:'
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 'Passaggio 2: Implementare ISpecifyPropertyPages'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315532"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="08c70-104">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="08c70-104">Step 2.</span></span> <span data-ttu-id="08c70-105">Implementare ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="08c70-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="08c70-106">Implementare quindi l'interfaccia **ISpecifyPropertyPages** nel filtro.</span><span class="sxs-lookup"><span data-stu-id="08c70-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="08c70-107">Questa interfaccia dispone di un singolo metodo, **GetPages**, che restituisce una matrice di CLSID per le pagine delle proprietà supportate dal filtro.</span><span class="sxs-lookup"><span data-stu-id="08c70-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="08c70-108">In questo esempio, il filtro ha una singola pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="08c70-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="08c70-109">Per iniziare, generare il CLSID e dichiararlo nel file di intestazione:</span><span class="sxs-lookup"><span data-stu-id="08c70-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="08c70-110">Implementare ora il metodo **GetPages** :</span><span class="sxs-lookup"><span data-stu-id="08c70-110">Now implement the **GetPages** method:</span></span>


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



<span data-ttu-id="08c70-111">Allocare memoria per la matrice utilizzando **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="08c70-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="08c70-112">Il chiamante rilascerà la memoria.</span><span class="sxs-lookup"><span data-stu-id="08c70-112">The caller will release the memory.</span></span>

<span data-ttu-id="08c70-113">Successivo: [passaggio 3. Supporta QueryInterface](step-3--support-queryinterface.md).</span><span class="sxs-lookup"><span data-stu-id="08c70-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08c70-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08c70-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08c70-115">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="08c70-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



