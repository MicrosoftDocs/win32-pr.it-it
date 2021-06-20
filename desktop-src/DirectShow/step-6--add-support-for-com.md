---
description: Aggiunta del supporto per COM come parte della scrittura di un filtro di trasformazione. Questo è il passaggio finale di questa esercitazione.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Passaggio 6. Aggiunta del supporto per COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d51fa440812311edde9ce448916c66721a507
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406774"
---
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="d1e14-105">Passaggio 6.</span><span class="sxs-lookup"><span data-stu-id="d1e14-105">Step 6.</span></span> <span data-ttu-id="d1e14-106">Aggiunta del supporto per COM</span><span class="sxs-lookup"><span data-stu-id="d1e14-106">Add Support for COM</span></span>

<span data-ttu-id="d1e14-107">Questo è il passaggio 6 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="d1e14-107">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="d1e14-108">Il passaggio finale consiste nell'aggiungere il supporto per COM.</span><span class="sxs-lookup"><span data-stu-id="d1e14-108">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="d1e14-109">Conteggio dei riferimenti</span><span class="sxs-lookup"><span data-stu-id="d1e14-109">Reference Counting</span></span>

<span data-ttu-id="d1e14-110">Non è necessario implementare [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) o [**IUnknown::Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="d1e14-110">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d1e14-111">Tutte le classi di filtro e pin derivano da [**CUnknown,**](cunknown.md)che gestisce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="d1e14-111">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="d1e14-112">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="d1e14-112">QueryInterface</span></span>

<span data-ttu-id="d1e14-113">Tutte le classi di filtro e pin implementano [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per tutte le interfacce COM che ereditano.</span><span class="sxs-lookup"><span data-stu-id="d1e14-113">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="d1e14-114">Ad esempio, [**CTransformFilter**](ctransformfilter.md) eredita [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (tramite [**CBaseFilter).**](cbasefilter.md)</span><span class="sxs-lookup"><span data-stu-id="d1e14-114">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="d1e14-115">Se il filtro non espone interfacce aggiuntive, non è necessario eseguire altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="d1e14-115">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="d1e14-116">Per esporre interfacce aggiuntive, eseguire l'override [**del metodo CUnknown::NonDelegatingQueryInterface.**](cunknown-nondelegatingqueryinterface.md)</span><span class="sxs-lookup"><span data-stu-id="d1e14-116">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="d1e14-117">Si supponga, ad esempio, che il filtro implementi un'interfaccia personalizzata denominata IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="d1e14-117">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="d1e14-118">Per esporre questa interfaccia ai client, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1e14-118">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="d1e14-119">Derivare la classe di filtro da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d1e14-119">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="d1e14-120">Inserire la macro [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) nella sezione della dichiarazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="d1e14-120">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="d1e14-121">Eseguire [**l'override di NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per verificare l'IID dell'interfaccia e restituire un puntatore al filtro.</span><span class="sxs-lookup"><span data-stu-id="d1e14-121">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="d1e14-122">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="d1e14-122">The following code shows these steps:</span></span>


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



<span data-ttu-id="d1e14-123">Per altre informazioni, vedere [Come implementare IUnknown.](how-to-implement-iunknown.md)</span><span class="sxs-lookup"><span data-stu-id="d1e14-123">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="d1e14-124">Creazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="d1e14-124">Object Creation</span></span>

<span data-ttu-id="d1e14-125">Se si prevede di creare un pacchetto del filtro in una DLL e renderlo disponibile ad altri client, è necessario supportare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e altre funzioni COM correlate.</span><span class="sxs-lookup"><span data-stu-id="d1e14-125">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="d1e14-126">La libreria di classi di base implementa la maggior parte di questo; È sufficiente fornire alcune informazioni sul filtro.</span><span class="sxs-lookup"><span data-stu-id="d1e14-126">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="d1e14-127">Questa sezione offre una breve panoramica delle attività da eseguire.</span><span class="sxs-lookup"><span data-stu-id="d1e14-127">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="d1e14-128">Per informazioni dettagliate, [vedere How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d1e14-128">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="d1e14-129">Prima di tutto, scrivere un metodo di classe statico che restituisce una nuova istanza del filtro.</span><span class="sxs-lookup"><span data-stu-id="d1e14-129">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="d1e14-130">È possibile assegnare a questo metodo un nome qualsiasi, ma la firma deve corrispondere a quella illustrata nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d1e14-130">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



<span data-ttu-id="d1e14-131">Dichiarare quindi una matrice globale di istanze [**della classe CFactoryTemplate,**](cfactorytemplate.md) denominata *g \_ Templates.*</span><span class="sxs-lookup"><span data-stu-id="d1e14-131">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="d1e14-132">Ogni **classe CFactoryTemplate contiene** informazioni del Registro di sistema per un filtro.</span><span class="sxs-lookup"><span data-stu-id="d1e14-132">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="d1e14-133">Diversi filtri possono risiedere in una singola DLL. includere semplicemente voci **CFactoryTemplate** aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="d1e14-133">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="d1e14-134">È anche possibile dichiarare altri oggetti COM, ad esempio le pagine delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d1e14-134">You can also declare other COM objects, such as property pages.</span></span>


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



<span data-ttu-id="d1e14-135">Definire un intero globale denominato *g \_ cTemplates* il cui valore è uguale alla lunghezza della *matrice \_ templates g:*</span><span class="sxs-lookup"><span data-stu-id="d1e14-135">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="d1e14-136">Infine, implementare le funzioni di registrazione dll.</span><span class="sxs-lookup"><span data-stu-id="d1e14-136">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="d1e14-137">L'esempio seguente illustra l'implementazione minima per queste funzioni:</span><span class="sxs-lookup"><span data-stu-id="d1e14-137">The following example shows the minimal implementation for these functions:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a><span data-ttu-id="d1e14-138">Filtrare le voci del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d1e14-138">Filter Registry Entries</span></span>

<span data-ttu-id="d1e14-139">Negli esempi precedenti viene illustrato come registrare il CLSID di un filtro per COM.</span><span class="sxs-lookup"><span data-stu-id="d1e14-139">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="d1e14-140">Per molti filtri, questa operazione è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="d1e14-140">For many filters, this is sufficient.</span></span> <span data-ttu-id="d1e14-141">Il client deve quindi creare il filtro usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e aggiungerlo al grafico dei filtri chiamando [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="d1e14-141">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="d1e14-142">In alcuni casi, tuttavia, potrebbe essere necessario fornire informazioni aggiuntive sul filtro nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d1e14-142">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="d1e14-143">Questa informazione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1e14-143">This information does the following:</span></span>

-   <span data-ttu-id="d1e14-144">Consente ai client di individuare il filtro usando [l'enumeratore Filter Mapper](filter-mapper.md) o [System Device Enumerator.](system-device-enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="d1e14-144">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="d1e14-145">Consente a Filter Graph Manager di individuare il filtro durante la compilazione automatica del grafo.</span><span class="sxs-lookup"><span data-stu-id="d1e14-145">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="d1e14-146">Nell'esempio seguente viene registrato il filtro del codificatore RLE nella categoria video.</span><span class="sxs-lookup"><span data-stu-id="d1e14-146">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="d1e14-147">Per informazioni dettagliate, [vedere How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d1e14-147">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="d1e14-148">Leggere la sezione Linee guida [per la registrazione dei filtri,](guidelines-for-registering-filters.md)che descrive le procedure consigliate per la registrazione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="d1e14-148">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



<span data-ttu-id="d1e14-149">Inoltre, i filtri non devono essere in pacchetto all'interno delle DLL.</span><span class="sxs-lookup"><span data-stu-id="d1e14-149">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="d1e14-150">In alcuni casi, è possibile scrivere un filtro specializzato progettato solo per un'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="d1e14-150">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="d1e14-151">In tal caso, è possibile compilare la classe di filtro direttamente nell'applicazione e crearla con l'operatore , come `new` illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d1e14-151">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d1e14-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1e14-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e14-153">Intelligent Connect</span><span class="sxs-lookup"><span data-stu-id="d1e14-153">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="d1e14-154">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1e14-154">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d1e14-155">Scrittura di filtri di trasformazione</span><span class="sxs-lookup"><span data-stu-id="d1e14-155">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
