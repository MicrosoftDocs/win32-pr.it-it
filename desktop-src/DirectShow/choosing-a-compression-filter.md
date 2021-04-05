---
description: Scelta di un filtro di compressione
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Scelta di un filtro di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125511"
---
# <a name="choosing-a-compression-filter"></a><span data-ttu-id="545bc-103">Scelta di un filtro di compressione</span><span class="sxs-lookup"><span data-stu-id="545bc-103">Choosing a Compression Filter</span></span>

<span data-ttu-id="545bc-104">Diversi tipi di componenti software possono eseguire la compressione video o audio, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="545bc-104">Several types of software components can perform video or audio compression, such as:</span></span>

-   <span data-ttu-id="545bc-105">Filtri DirectShow nativi</span><span class="sxs-lookup"><span data-stu-id="545bc-105">Native DirectShow filters</span></span>
-   <span data-ttu-id="545bc-106">Codec di Gestione compressione video (VCM)</span><span class="sxs-lookup"><span data-stu-id="545bc-106">Video Compression Manager (VCM) codecs</span></span>
-   <span data-ttu-id="545bc-107">Codec di Gestione compressione audio (ACM)</span><span class="sxs-lookup"><span data-stu-id="545bc-107">Audio Compression Manager (ACM) codecs</span></span>
-   <span data-ttu-id="545bc-108">Oggetti multimediali DirectX (DMOs)</span><span class="sxs-lookup"><span data-stu-id="545bc-108">DirectX Media Objects (DMOs)</span></span>

<span data-ttu-id="545bc-109">In DirectShow, i codec VCM sono inclusi nel [filtro del compressore AVI](avi-compressor-filter.md)e i codec ACM sono inclusi nel [filtro del wrapper ACM](acm-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="545bc-109">In DirectShow, VCM codecs are wrapped by the [AVI Compressor Filter](avi-compressor-filter.md), and ACM codecs are wrapped by the [ACM Wrapper Filter](acm-wrapper-filter.md).</span></span> <span data-ttu-id="545bc-110">DMOs è incluso nel [filtro del wrapper DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="545bc-110">DMOs are wrapped by the [DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="545bc-111">System Device Enumerator fornisce un modo coerente per enumerare e creare uno di questi tipi di compensatori, senza preoccuparsi del modello sottostante.</span><span class="sxs-lookup"><span data-stu-id="545bc-111">The system device enumerator provides a consistent way to enumerate and create any of these compressor types, without worrying about the underlying model.</span></span>

<span data-ttu-id="545bc-112">Per informazioni dettagliate sull'enumeratore di dispositivo di sistema, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="545bc-112">For details about the system device enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="545bc-113">In breve, tutti i filtri DirectShow sono classificati in base alla categoria e ogni categoria viene identificata da un GUID.</span><span class="sxs-lookup"><span data-stu-id="545bc-113">Briefly, all DirectShow filters are classified by category, and each category is identified by a GUID.</span></span> <span data-ttu-id="545bc-114">Per i commediatori video, il GUID categoria è CLSID \_ VideoCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="545bc-114">For video compressors, the category GUID is CLSID\_VideoCompressorCategory.</span></span> <span data-ttu-id="545bc-115">Per i commediatori audio, è CLSID \_ AudioCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="545bc-115">For audio compressors, it is CLSID\_AudioCompressorCategory.</span></span> <span data-ttu-id="545bc-116">Per enumerare una particolare categoria, l'enumeratore di dispositivo di sistema crea un oggetto *enumeratore* che supporta l'interfaccia [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="545bc-116">To enumerate a particular category, the system device enumerator creates an *enumerator* object that supports the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="545bc-117">L'applicazione usa questa interfaccia per recuperare i moniker del dispositivo, dove ogni moniker del dispositivo rappresenta un'istanza di un filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="545bc-117">The application uses this interface to retrieve device monikers, where each device moniker represents an instance of a DirectShow filter.</span></span> <span data-ttu-id="545bc-118">È possibile usare il moniker per creare il filtro o per ottenere il nome descrittivo del dispositivo senza creare il filtro.</span><span class="sxs-lookup"><span data-stu-id="545bc-118">You can use the moniker to create the filter, or to get the device's friendly name without creating the filter.</span></span>

<span data-ttu-id="545bc-119">Per enumerare i compressori video o audio disponibili nel sistema dell'utente, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="545bc-119">To enumerate the video or audio compressors available on the user's system, do the following:</span></span>

1.  <span data-ttu-id="545bc-120">Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'enumeratore di dispositivo di sistema, che ha un ID di classe CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="545bc-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the system device enumerator, which has a class ID of CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="545bc-121">Chiamare [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il GUID della categoria di filtro.</span><span class="sxs-lookup"><span data-stu-id="545bc-121">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the filter category GUID.</span></span> <span data-ttu-id="545bc-122">Il metodo restituisce un puntatore di interfaccia **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="545bc-122">The method returns an **IEnumMoniker** interface pointer.</span></span>
3.  <span data-ttu-id="545bc-123">Usare il Metodo IEnumMoniker:: Next per enumerare i moniker del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="545bc-123">Use the IEnumMoniker::Next method to enumerate the device monikers.</span></span> <span data-ttu-id="545bc-124">Questo metodo restituisce un'interfaccia [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , che rappresenta il moniker.</span><span class="sxs-lookup"><span data-stu-id="545bc-124">This method returns an [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) interface, which represents the moniker.</span></span>

<span data-ttu-id="545bc-125">Per ottenere il nome descrittivo da un moniker, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="545bc-125">To get the friendly name from a moniker, do the following:</span></span>

1.  <span data-ttu-id="545bc-126">Chiamare il metodo **IMoniker:: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="545bc-126">Call the **IMoniker::BindToStorage** method.</span></span> <span data-ttu-id="545bc-127">Questo metodo restituisce un puntatore all'interfaccia **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="545bc-127">This method returns an **IPropertyBag** interface pointer.</span></span>
2.  <span data-ttu-id="545bc-128">Usare il metodo **IPropertyBag:: Read** per leggere la proprietà **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="545bc-128">Use the **IPropertyBag::Read** method to read the **FriendlyName** property.</span></span>

<span data-ttu-id="545bc-129">In genere, in un'applicazione viene visualizzato un elenco di compressatori, in modo che l'utente possa sceglierne uno.</span><span class="sxs-lookup"><span data-stu-id="545bc-129">Typically, an application would display a list of compressors, so that the user could choose one.</span></span> <span data-ttu-id="545bc-130">Il codice seguente, ad esempio, popola una casella di riepilogo con i nomi dei commediatori video disponibili.</span><span class="sxs-lookup"><span data-stu-id="545bc-130">For example, the following code populates a list box with the names of the available video compressors.</span></span>


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



<span data-ttu-id="545bc-131">Per creare un'istanza di filtro dal moniker, chiamare il metodo **IMoniker:: BindToObject** .</span><span class="sxs-lookup"><span data-stu-id="545bc-131">To create a filter instance from the moniker, call the **IMoniker::BindToObject** method.</span></span> <span data-ttu-id="545bc-132">Il metodo restituisce un puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="545bc-132">The method returns an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



<span data-ttu-id="545bc-133">Per i codec VCM, ogni moniker rappresenta un codec particolare, anche se tutti i codec sono racchiusi dallo stesso filtro di compressione AVI.</span><span class="sxs-lookup"><span data-stu-id="545bc-133">For VCM codecs, each moniker represents one particular codec, even though all of the codecs are wrapped by the same AVI Compression filter.</span></span> <span data-ttu-id="545bc-134">La chiamata a **BindToObject** crea un'istanza di questo filtro, inizializzata per il codec.</span><span class="sxs-lookup"><span data-stu-id="545bc-134">Calling **BindToObject** creates an instance of this filter, initialized for that codec.</span></span> <span data-ttu-id="545bc-135">Per questo motivo, non è possibile chiamare **CoCreateInstance** direttamente nel filtro di compressione AVI.</span><span class="sxs-lookup"><span data-stu-id="545bc-135">For this reason, you cannot call **CoCreateInstance** directly on the AVI Compression filter.</span></span> <span data-ttu-id="545bc-136">È necessario esaminare l'enumeratore di dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="545bc-136">You must go through the system device enumerator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="545bc-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="545bc-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="545bc-138">Ricompressione di un file AVI</span><span class="sxs-lookup"><span data-stu-id="545bc-138">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 
