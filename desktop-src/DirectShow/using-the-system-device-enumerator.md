---
description: Uso di System Device Enumerator
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Uso di System Device Enumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564174"
---
# <a name="using-the-system-device-enumerator"></a><span data-ttu-id="51856-103">Uso di System Device Enumerator</span><span class="sxs-lookup"><span data-stu-id="51856-103">Using the System Device Enumerator</span></span>

<span data-ttu-id="51856-104">L'enumeratore di dispositivo System fornisce un modo uniforme per enumerare, per categoria, i filtri registrati nel sistema di un utente.</span><span class="sxs-lookup"><span data-stu-id="51856-104">The System Device Enumerator provides a uniform way to enumerate, by category, the filters registered on a user's system.</span></span> <span data-ttu-id="51856-105">Inoltre, distingue tra i singoli dispositivi hardware, anche se lo stesso filtro li supporta.</span><span class="sxs-lookup"><span data-stu-id="51856-105">Moreover, it differentiates between individual hardware devices, even if the same filter supports them.</span></span> <span data-ttu-id="51856-106">Questa operazione è particolarmente utile per i dispositivi che usano il Windows Driver Model (WDM) e il filtro KSProxy.</span><span class="sxs-lookup"><span data-stu-id="51856-106">This is particularly useful for devices that use the Windows Driver Model (WDM) and the KSProxy filter.</span></span> <span data-ttu-id="51856-107">Ad esempio, l'utente potrebbe avere diversi dispositivi di acquisizione video WDM, tutti supportati dallo stesso filtro.</span><span class="sxs-lookup"><span data-stu-id="51856-107">For example, the user might have several WDM video capture devices, all supported by the same filter.</span></span> <span data-ttu-id="51856-108">L'enumeratore di dispositivi di sistema li considera come istanze di dispositivo separate.</span><span class="sxs-lookup"><span data-stu-id="51856-108">The System Device Enumerator treats them as separate device instances.</span></span>

<span data-ttu-id="51856-109">L'enumeratore di dispositivi di sistema funziona creando un enumeratore per una categoria specifica, ad esempio l'acquisizione audio o la compressione video.</span><span class="sxs-lookup"><span data-stu-id="51856-109">The System Device Enumerator works by creating an enumerator for a specific category, such as audio capture or video compression.</span></span> <span data-ttu-id="51856-110">L'enumeratore Category restituisce un moniker univoco per ogni dispositivo nella categoria.</span><span class="sxs-lookup"><span data-stu-id="51856-110">The category enumerator returns a unique moniker for each device in the category.</span></span> <span data-ttu-id="51856-111">L'enumeratore Category include automaticamente eventuali dispositivi Plug and Play rilevanti nella categoria.</span><span class="sxs-lookup"><span data-stu-id="51856-111">The category enumerator automatically includes any relevant Plug and Play devices in the category.</span></span> <span data-ttu-id="51856-112">Per un elenco di categorie, vedere [filtrare le categorie](filter-categories.md).</span><span class="sxs-lookup"><span data-stu-id="51856-112">For a list of categories, see [Filter Categories](filter-categories.md).</span></span>

<span data-ttu-id="51856-113">Per usare l'enumeratore di dispositivo di sistema, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="51856-113">To use the System Device Enumerator, do the following:</span></span>

1.  <span data-ttu-id="51856-114">Creare l'enumeratore di dispositivo di sistema chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="51856-114">Create the system device enumerator by calling **CoCreateInstance**.</span></span> <span data-ttu-id="51856-115">L'identificatore di classe (CLSID) è CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="51856-115">The class identifier (CLSID) is CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="51856-116">Ottenere un enumeratore Category chiamando [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il CLSID della categoria desiderata.</span><span class="sxs-lookup"><span data-stu-id="51856-116">Obtain a category enumerator by calling [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the CLSID of the desired category.</span></span> <span data-ttu-id="51856-117">Questo metodo restituisce un puntatore all'interfaccia **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="51856-117">This method returns an **IEnumMoniker** interface pointer.</span></span> <span data-ttu-id="51856-118">Se la categoria è vuota (o non esiste), il metodo restituisce \_ false anziché un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="51856-118">If the category is empty (or does not exist), the method returns S\_FALSE rather than an error code.</span></span> <span data-ttu-id="51856-119">In caso affermativo, il puntatore **IEnumMoniker** restituito è **null** e la dereferenziazione provocherà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="51856-119">If so, the returned **IEnumMoniker** pointer is **NULL** and dereferencing it will cause an exception.</span></span> <span data-ttu-id="51856-120">Pertanto, testare in modo esplicito for S \_ OK quando si chiama **CreateClassEnumerator**, invece di chiamare la normale macro **succeeded** .</span><span class="sxs-lookup"><span data-stu-id="51856-120">Therefore, explicitly test for S\_OK when you call **CreateClassEnumerator**, instead of calling the usual **SUCCEEDED** macro.</span></span>
3.  <span data-ttu-id="51856-121">Usare il metodo **IEnumMoniker:: Next** per enumerare ogni moniker.</span><span class="sxs-lookup"><span data-stu-id="51856-121">Use the **IEnumMoniker::Next** method to enumerate each moniker.</span></span> <span data-ttu-id="51856-122">Questo metodo restituisce un puntatore a interfaccia **IMoniker** .</span><span class="sxs-lookup"><span data-stu-id="51856-122">This method returns an **IMoniker** interface pointer.</span></span> <span data-ttu-id="51856-123">Quando il metodo **successivo** raggiunge la fine dell'enumerazione, restituisce anche s \_ false, quindi controlla di nuovo la presenza di s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="51856-123">When the **Next** method reaches the end of the enumeration, it also returns S\_FALSE, so again check for S\_OK.</span></span>
4.  <span data-ttu-id="51856-124">Per recuperare il nome descrittivo del dispositivo (ad esempio, per visualizzarlo nell'interfaccia utente), chiamare il metodo **IMoniker:: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="51856-124">To retrieve the friendly name of the device (for example, to display in the user interface), call the **IMoniker::BindToStorage** method.</span></span>
5.  <span data-ttu-id="51856-125">Per creare e inizializzare il filtro DirectShow che gestisce il dispositivo, chiamare **IMoniker:: BindToObject** nel moniker.</span><span class="sxs-lookup"><span data-stu-id="51856-125">To create and initialize the DirectShow filter that manages the device, call **IMoniker::BindToObject** on the moniker.</span></span> <span data-ttu-id="51856-126">Chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafo.</span><span class="sxs-lookup"><span data-stu-id="51856-126">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span>

<span data-ttu-id="51856-127">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="51856-127">The following diagram illustrates this process.</span></span>

![Enumerazione dei dispositivi](images/sysdevenum.png)

<span data-ttu-id="51856-129">Nell'esempio seguente viene illustrato come enumerare i compressioni video installati nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="51856-129">The following example shows how to enumerate the video compressors installed on the user's system.</span></span> <span data-ttu-id="51856-130">Per brevità, nell'esempio viene eseguito il controllo minimo degli errori.</span><span class="sxs-lookup"><span data-stu-id="51856-130">For brevity, the example performs minimal error checking.</span></span>


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



<span data-ttu-id="51856-131">**Moniker del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="51856-131">**Device Monikers**</span></span>

<span data-ttu-id="51856-132">Per i moniker del dispositivo, è possibile passare il moniker al metodo [**IFilterGraph2:: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) per creare un filtro di acquisizione per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51856-132">For device monikers, you can pass the moniker to the [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) method to create a capture filter for the device.</span></span> <span data-ttu-id="51856-133">Per un esempio di codice, vedere la documentazione relativa a tale metodo.</span><span class="sxs-lookup"><span data-stu-id="51856-133">For example code, see the documentation for that method.</span></span>

<span data-ttu-id="51856-134">Il metodo **IMoniker:: GetDisplayName** restituisce il nome visualizzato del moniker.</span><span class="sxs-lookup"><span data-stu-id="51856-134">The **IMoniker::GetDisplayName** method returns the display name of the moniker.</span></span> <span data-ttu-id="51856-135">Sebbene il nome visualizzato sia leggibile, in genere non viene visualizzato a un utente finale.</span><span class="sxs-lookup"><span data-stu-id="51856-135">Although the display name is readable, you would not typically display it to an end-user.</span></span> <span data-ttu-id="51856-136">Ottenere invece il nome descrittivo dall'elenco delle proprietà, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="51856-136">Get the friendly name from the property bag instead, as described previously.</span></span>

<span data-ttu-id="51856-137">Il metodo **IMoniker::P arsedisplayname** o la funzione **MkParseDisplayName** può essere usato per creare un moniker di dispositivo predefinito per una categoria di filtro specificata.</span><span class="sxs-lookup"><span data-stu-id="51856-137">The **IMoniker::ParseDisplayName** method or the **MkParseDisplayName** function can be used to create a default device moniker for a given filter category.</span></span> <span data-ttu-id="51856-138">Usare un nome visualizzato con il formato `@device:*:{category-clsid}` , dove `category-clsid` è la rappresentazione di stringa del GUID di categoria.</span><span class="sxs-lookup"><span data-stu-id="51856-138">Use a display name with the form `@device:*:{category-clsid}`, where `category-clsid` is the string representation of the category GUID.</span></span> <span data-ttu-id="51856-139">Il moniker predefinito è il primo moniker restituito dall'enumeratore del dispositivo per tale categoria.</span><span class="sxs-lookup"><span data-stu-id="51856-139">The default moniker is the first moniker returned by the device enumerator for that category.</span></span>

 

 



