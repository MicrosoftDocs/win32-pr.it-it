---
description: Selezione di un dispositivo di acquisizione
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Selezione di un dispositivo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303908"
---
# <a name="selecting-a-capture-device"></a><span data-ttu-id="ac14a-103">Selezione di un dispositivo di acquisizione</span><span class="sxs-lookup"><span data-stu-id="ac14a-103">Selecting a Capture Device</span></span>

<span data-ttu-id="ac14a-104">Per selezionare un dispositivo di acquisizione audio o video, usare l' [enumeratore](system-device-enumerator.md)del dispositivo di sistema, descritto nell'argomento [uso di System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="ac14a-104">To select an audio or video capture device, use the [System Device Enumerator](system-device-enumerator.md), described in the topic [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="ac14a-105">L'enumeratore del dispositivo di sistema restituisce una raccolta di moniker di dispositivo, selezionati per categoria del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-105">The System Device Enumerator returns a collection of device monikers, selected by device category.</span></span> <span data-ttu-id="ac14a-106">Un *moniker* è un oggetto com che contiene informazioni su un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac14a-106">A *moniker* is a COM object that contains information about another object.</span></span> <span data-ttu-id="ac14a-107">I moniker consentono all'applicazione di ottenere informazioni su un oggetto senza creare effettivamente l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac14a-107">Monikers enable the application to get information about an object without actually creating the object.</span></span> <span data-ttu-id="ac14a-108">Successivamente, l'applicazione può utilizzare il moniker per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac14a-108">Later, the application can use the moniker to create the object.</span></span> <span data-ttu-id="ac14a-109">Per ulteriori informazioni sui moniker, vedere la documentazione relativa a [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span><span class="sxs-lookup"><span data-stu-id="ac14a-109">For more information about monikers, see the documentation for [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span></span>

<span data-ttu-id="ac14a-110">Per usare l'enumeratore di dispositivo di sistema, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="ac14a-110">To use the System Device Enumerator, perform the following steps.</span></span>

1.  <span data-ttu-id="ac14a-111">Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'enumeratore di dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="ac14a-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an instance of the System Device Enumerator.</span></span>
2.  <span data-ttu-id="ac14a-112">Chiamare [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) e specificare la categoria del dispositivo come GUID.</span><span class="sxs-lookup"><span data-stu-id="ac14a-112">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) and specify the device category as a GUID.</span></span> <span data-ttu-id="ac14a-113">Per i dispositivi di acquisizione, le seguenti categorie sono rilevanti.</span><span class="sxs-lookup"><span data-stu-id="ac14a-113">For capture devices, the following categories are relevant.</span></span> 

    | <span data-ttu-id="ac14a-114">GUID categoria</span><span class="sxs-lookup"><span data-stu-id="ac14a-114">Category GUID</span></span>                       | <span data-ttu-id="ac14a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac14a-115">Description</span></span>           |
    |-------------------------------------|-----------------------|
    | <span data-ttu-id="ac14a-116">**\_AUDIOINPUTDEVICECATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="ac14a-116">**CLSID\_AudioInputDeviceCategory**</span></span> | <span data-ttu-id="ac14a-117">Dispositivi di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="ac14a-117">Audio capture devices</span></span> |
    | <span data-ttu-id="ac14a-118">**\_VIDEOINPUTDEVICECATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="ac14a-118">**CLSID\_VideoInputDeviceCategory**</span></span> | <span data-ttu-id="ac14a-119">Dispositivi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="ac14a-119">Video capture devices</span></span> |

    

     

    <span data-ttu-id="ac14a-120">Se una videocamera ha un microfono integrato, viene visualizzata in entrambe le categorie.</span><span class="sxs-lookup"><span data-stu-id="ac14a-120">If a video camera has an integrated microphone, it appears in both categories.</span></span> <span data-ttu-id="ac14a-121">Tuttavia, la fotocamera e il microfono vengono considerati dispositivi distinti dal sistema, ai fini dell'enumerazione, della creazione del dispositivo e del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="ac14a-121">However, the camera and microphone are treated as separate devices by the system, for purposes of enumeration, device creation, and data streaming.</span></span>

3.  <span data-ttu-id="ac14a-122">Il metodo [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) restituisce un puntatore all'interfaccia [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="ac14a-122">The [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method returns a pointer to the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="ac14a-123">Per enumerare i moniker, chiamare [**IEnumMoniker:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span><span class="sxs-lookup"><span data-stu-id="ac14a-123">To enumerate the monikers, call [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span></span>

<span data-ttu-id="ac14a-124">Il codice seguente crea un enumeratore per una categoria di dispositivi specificata.</span><span class="sxs-lookup"><span data-stu-id="ac14a-124">The following code creates an enumerator for a specified device category.</span></span>


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



<span data-ttu-id="ac14a-125">L'interfaccia [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) enumera un elenco di interfacce [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , ognuna delle quali rappresenta un moniker di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-125">The [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface enumerates a list of [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interfaces, each of which represents a device moniker.</span></span> <span data-ttu-id="ac14a-126">L'applicazione può leggere le proprietà dal moniker oppure usare il moniker per creare un filtro di acquisizione DirectShow per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-126">The application can read properties from the moniker, or use the moniker to create a DirectShow capture filter for the device.</span></span> <span data-ttu-id="ac14a-127">Le proprietà del moniker vengono restituite come valori **Variant** .</span><span class="sxs-lookup"><span data-stu-id="ac14a-127">Moniker properties are returned as **VARIANT** values.</span></span> <span data-ttu-id="ac14a-128">Le proprietà seguenti sono supportate dai moniker del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-128">The following properties are supported by device monikers.</span></span>



| <span data-ttu-id="ac14a-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac14a-129">Property</span></span>       | <span data-ttu-id="ac14a-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac14a-130">Description</span></span>                                                               | <span data-ttu-id="ac14a-131">Tipo VARIANT</span><span class="sxs-lookup"><span data-stu-id="ac14a-131">VARIANT Type</span></span> |
|----------------|---------------------------------------------------------------------------|--------------|
| <span data-ttu-id="ac14a-132">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ac14a-132">"FriendlyName"</span></span> | <span data-ttu-id="ac14a-133">Nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-133">The name of the device.</span></span>                                                   | <span data-ttu-id="ac14a-134">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="ac14a-134">**VT\_BSTR**</span></span> |
| <span data-ttu-id="ac14a-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac14a-135">"Description"</span></span>  | <span data-ttu-id="ac14a-136">Descrizione del modello.</span><span class="sxs-lookup"><span data-stu-id="ac14a-136">A description of the device.</span></span>                                              | <span data-ttu-id="ac14a-137">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="ac14a-137">**VT\_BSTR**</span></span> |
| <span data-ttu-id="ac14a-138">DevicePath</span><span class="sxs-lookup"><span data-stu-id="ac14a-138">"DevicePath"</span></span>   | <span data-ttu-id="ac14a-139">Stringa univoca che identifica il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-139">A unique string that identifies the device.</span></span> <span data-ttu-id="ac14a-140">(Solo per dispositivi di acquisizione video).</span><span class="sxs-lookup"><span data-stu-id="ac14a-140">(Video capture devices only.)</span></span> | <span data-ttu-id="ac14a-141">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="ac14a-141">**VT\_BSTR**</span></span> |
| <span data-ttu-id="ac14a-142">"WaveInID"</span><span class="sxs-lookup"><span data-stu-id="ac14a-142">"WaveInID"</span></span>     | <span data-ttu-id="ac14a-143">Identificatore di un dispositivo di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="ac14a-143">The identifier for an audio capture device.</span></span> <span data-ttu-id="ac14a-144">(Solo dispositivi di acquisizione audio.)</span><span class="sxs-lookup"><span data-stu-id="ac14a-144">(Audio capture devices only.)</span></span> | <span data-ttu-id="ac14a-145">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="ac14a-145">**VT\_I4**</span></span>   |



 

<span data-ttu-id="ac14a-146">Le proprietà "FriendlyName" e "Description" sono adatte per la visualizzazione in un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ac14a-146">The "FriendlyName" and "Description" properties are suitable for displaying in a UI.</span></span>

-   <span data-ttu-id="ac14a-147">La proprietà "FriendlyName" è disponibile per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-147">The "FriendlyName" property is available for every device.</span></span> <span data-ttu-id="ac14a-148">Contiene un nome leggibile per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-148">It contains a human-readable name for the device.</span></span>
-   <span data-ttu-id="ac14a-149">La proprietà "Description" è disponibile solo per i dispositivi DV e D-VHS/MPEG.</span><span class="sxs-lookup"><span data-stu-id="ac14a-149">The "Description" property is available only for DV and D-VHS/MPEG camcorder devices.</span></span> <span data-ttu-id="ac14a-150">Per ulteriori informazioni, vedere [driver Msdv](msdv-driver.md) e [driver MSTape](mstape-driver.md).</span><span class="sxs-lookup"><span data-stu-id="ac14a-150">For more information, see [MSDV Driver](msdv-driver.md) and [MSTape Driver](mstape-driver.md).</span></span> <span data-ttu-id="ac14a-151">Se disponibile, contiene una descrizione del dispositivo più specifica della proprietà "FriendlyName".</span><span class="sxs-lookup"><span data-stu-id="ac14a-151">If available, it contains a description of the device which is more specific than the "FriendlyName" property.</span></span> <span data-ttu-id="ac14a-152">In genere include il nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="ac14a-152">Typically it includes the vendor name.</span></span>
-   <span data-ttu-id="ac14a-153">La proprietà "DevicePath" non è una stringa leggibile, ma è sicuramente univoca per ogni dispositivo di acquisizione video nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ac14a-153">The "DevicePath" property is not a human-readable string, but is guaranteed to be unique for each video capture device on the system.</span></span> <span data-ttu-id="ac14a-154">È possibile usare questa proprietà per distinguere tra due o più istanze dello stesso modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-154">You can use this property to distinguish between two or more instances of the same model of device.</span></span>
-   <span data-ttu-id="ac14a-155">Se è presente la proprietà "WaveInID", significa che il filtro di acquisizione DirectShow usa le API [audio della forma d'onda](../multimedia/waveform-audio.md) internamente per comunicare con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac14a-155">If the "WaveInID" property is present, it means the DirectShow capture filter uses the [Waveform Audio](../multimedia/waveform-audio.md) APIs internally to communicate with the device.</span></span> <span data-ttu-id="ac14a-156">Il valore della proprietà "WaveInID" corrisponde all'identificatore usato dalle funzioni \**WaveIn \** _, ad esempio [_ *waveInOpen* \*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span><span class="sxs-lookup"><span data-stu-id="ac14a-156">The value of the "WaveInID" property corresponds to the identifier used by the \**waveIn\** _ functions, such as [_ *waveInOpen*\*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span></span>

<span data-ttu-id="ac14a-157">Per leggere le proprietà dal moniker, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="ac14a-157">To read properties from the moniker, perform the following steps.</span></span>

1.  <span data-ttu-id="ac14a-158">Chiamare [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) per ottenere un puntatore all'interfaccia [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) .</span><span class="sxs-lookup"><span data-stu-id="ac14a-158">Call [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) to get a pointer to the [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) interface.</span></span>
2.  <span data-ttu-id="ac14a-159">Chiamare **IPropertyBag:: Read** per leggere la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ac14a-159">Call **IPropertyBag::Read** to read the property.</span></span>

<span data-ttu-id="ac14a-160">Nell'esempio di codice riportato di seguito viene illustrato come enumerare un elenco di moniker di dispositivo e recuperare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="ac14a-160">The following code example shows how to enumerate a list of device monikers and get the properties.</span></span>


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



<span data-ttu-id="ac14a-161">Per creare un filtro di acquisizione DirectShow per il dispositivo, chiamare il metodo [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) per ottenere un puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="ac14a-161">To create a DirectShow capture filter for the device, call the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to get an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="ac14a-162">Quindi, chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafo del filtro:</span><span class="sxs-lookup"><span data-stu-id="ac14a-162">Then call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph:</span></span>


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a><span data-ttu-id="ac14a-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac14a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac14a-164">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="ac14a-164">Audio Capture</span></span>](audio-capture.md)
</dt> <dt>

[<span data-ttu-id="ac14a-165">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="ac14a-165">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
