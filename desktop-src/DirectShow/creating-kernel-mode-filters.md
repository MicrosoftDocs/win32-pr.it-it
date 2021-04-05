---
description: Creazione di filtri Kernel-Mode
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Creazione di filtri Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125415"
---
# <a name="creating-kernel-mode-filters"></a><span data-ttu-id="0a499-103">Creazione di filtri Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="0a499-103">Creating Kernel-Mode Filters</span></span>

<span data-ttu-id="0a499-104">Alcuni filtri in modalità kernel non possono essere creati tramite **CoCreateInstance** e pertanto non hanno CLSID.</span><span class="sxs-lookup"><span data-stu-id="0a499-104">Certain kernel-mode filters cannot be created through **CoCreateInstance**, and thus do not have CLSIDs.</span></span> <span data-ttu-id="0a499-105">Questi filtri includono il [convertitore Tee/Sink-to-sink](tee-sink-to-sink-converter.md), il filtro del [decodificatore CC](cc-decoder-filter.md) e il filtro [codec WST](wst-codec-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a499-105">These filters include the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md), the [CC Decoder](cc-decoder-filter.md) filter, and the [WST Codec](wst-codec-filter.md) filter.</span></span> <span data-ttu-id="0a499-106">Per creare uno di questi filtri, utilizzare l'oggetto [enumeratore dispositivo di sistema](system-device-enumerator.md) e cercare in base al nome del filtro.</span><span class="sxs-lookup"><span data-stu-id="0a499-106">To create one of these filters, use the [System Device Enumerator](system-device-enumerator.md) object and search by the filter's name.</span></span>

1.  <span data-ttu-id="0a499-107">Creare l'enumeratore di dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="0a499-107">Create the System Device Enumerator.</span></span>
2.  <span data-ttu-id="0a499-108">Chiamare il metodo [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il CLSID della categoria Filter per tale filtro.</span><span class="sxs-lookup"><span data-stu-id="0a499-108">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method with the CLSID of the filter category for that filter.</span></span> <span data-ttu-id="0a499-109">Questo metodo crea un enumeratore per la categoria Filter.</span><span class="sxs-lookup"><span data-stu-id="0a499-109">This method creates an enumerator for the filter category.</span></span> <span data-ttu-id="0a499-110">Un *enumeratore* è semplicemente un oggetto che restituisce un elenco di altri oggetti usando un'interfaccia com definita. L'enumeratore restituisce i puntatori **IMoniker** , che rappresentano i filtri in tale categoria.</span><span class="sxs-lookup"><span data-stu-id="0a499-110">(An *enumerator* is simply an object that returns a list of other objects, using a defined COM interface.) The enumerator returns **IMoniker** pointers, which represent the filters in that category.</span></span>
3.  <span data-ttu-id="0a499-111">Per ogni moniker, chiamare **IMoniker:: BindToStorage** per ottenere un'interfaccia **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="0a499-111">For each moniker, call **IMoniker::BindToStorage** to get an **IPropertyBag** interface.</span></span>
4.  <span data-ttu-id="0a499-112">Chiamare **IPropertyBag:: Read** per ottenere il nome del filtro.</span><span class="sxs-lookup"><span data-stu-id="0a499-112">Call **IPropertyBag::Read** to get the name of the filter.</span></span>
5.  <span data-ttu-id="0a499-113">Se il nome corrisponde, chiamare **IMoniker:: BindToObject** per creare il filtro.</span><span class="sxs-lookup"><span data-stu-id="0a499-113">If the name matches, call **IMoniker::BindToObject** to create the filter.</span></span>

<span data-ttu-id="0a499-114">Nel codice seguente viene illustrata una funzione che esegue questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="0a499-114">The following code shows a function that performs these steps:</span></span>


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



<span data-ttu-id="0a499-115">Nell'esempio di codice seguente viene usata questa funzione per creare il filtro del decodificatore CC e aggiungerlo al grafico del filtro:</span><span class="sxs-lookup"><span data-stu-id="0a499-115">The following code example uses this function to create the CC Decoder filter and add it to the filter graph:</span></span>


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="0a499-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a499-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a499-117">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="0a499-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="0a499-118">Uso di System Device Enumerator</span><span class="sxs-lookup"><span data-stu-id="0a499-118">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



