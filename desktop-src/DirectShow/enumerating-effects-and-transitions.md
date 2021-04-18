---
description: Enumerazione degli effetti e delle transizioni
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Enumerazione degli effetti e delle transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303969"
---
# <a name="enumerating-effects-and-transitions"></a><span data-ttu-id="67a8d-103">Enumerazione degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="67a8d-103">Enumerating Effects and Transitions</span></span>

<span data-ttu-id="67a8d-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="67a8d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="67a8d-105">DirectShow fornisce un oggetto [enumeratore dispositivo di sistema](system-device-enumerator.md) per l'enumerazione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="67a8d-105">DirectShow provides a [System Device Enumerator](system-device-enumerator.md) object for enumerating devices.</span></span> <span data-ttu-id="67a8d-106">È possibile usarlo per recuperare i moniker per gli effetti o le transizioni installate nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="67a8d-106">You can use it to retrieve monikers for effects or transitions installed on the user's system.</span></span>

<span data-ttu-id="67a8d-107">System Device Enumerator espone l'interfaccia [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="67a8d-107">The system device enumerator exposes the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span> <span data-ttu-id="67a8d-108">Restituisce gli enumeratori di categoria per le categorie di dispositivi specificate.</span><span class="sxs-lookup"><span data-stu-id="67a8d-108">It returns category enumerators for specified device categories.</span></span> <span data-ttu-id="67a8d-109">Un enumeratore Category, a sua volta, espone l'interfaccia [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) e restituisce moniker per ogni dispositivo nella categoria.</span><span class="sxs-lookup"><span data-stu-id="67a8d-109">A category enumerator, in turn, exposes the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface and returns monikers for each device in the category.</span></span> <span data-ttu-id="67a8d-110">Per una descrizione dettagliata dell'uso di **ICreateDevEnum**, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="67a8d-110">For a detailed discussion of using **ICreateDevEnum**, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span> <span data-ttu-id="67a8d-111">Di seguito è riportato un breve riepilogo, specifico per i servizi di modifica DirectShow.</span><span class="sxs-lookup"><span data-stu-id="67a8d-111">The following is a brief summary, specific to DirectShow Editing Services.</span></span>

<span data-ttu-id="67a8d-112">Per enumerare gli effetti o le transizioni, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="67a8d-112">To enumerate effects or transitions, perform the following steps.</span></span>

1.  <span data-ttu-id="67a8d-113">Creare un'istanza dell'enumeratore di dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="67a8d-113">Create an instance of the system device enumerator.</span></span>
2.  <span data-ttu-id="67a8d-114">Chiamare il metodo [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) per recuperare un enumeratore Category.</span><span class="sxs-lookup"><span data-stu-id="67a8d-114">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method to retrieve a category enumerator.</span></span> <span data-ttu-id="67a8d-115">Le categorie sono definite dagli identificatori di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="67a8d-115">Categories are defined by class identifiers (CLSIDs).</span></span> <span data-ttu-id="67a8d-116">Usare CLSID \_ VideoEffects1Category per Effects o CLSID \_ VideoEffects2Category per le transizioni.</span><span class="sxs-lookup"><span data-stu-id="67a8d-116">Use CLSID\_VideoEffects1Category for effects or CLSID\_VideoEffects2Category for transitions.</span></span>
3.  <span data-ttu-id="67a8d-117">Chiamare **IEnumMoniker:: Next** per recuperare ogni moniker nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="67a8d-117">Call **IEnumMoniker::Next** to retrieve each moniker in the enumeration.</span></span>
4.  <span data-ttu-id="67a8d-118">Per ogni moniker, chiamare **IMoniker:: BindToStorage** per recuperare il contenitore delle proprietà associato.</span><span class="sxs-lookup"><span data-stu-id="67a8d-118">For each moniker, call **IMoniker::BindToStorage** to retrieve its associated property bag.</span></span>

<span data-ttu-id="67a8d-119">Il contenitore delle proprietà contiene il nome descrittivo e l'identificatore univoco globale (GUID) per l'effetto o la transizione.</span><span class="sxs-lookup"><span data-stu-id="67a8d-119">The property bag contains the friendly name and the globally unique identifier (GUID) for the effect or transition.</span></span> <span data-ttu-id="67a8d-120">Un'applicazione può visualizzare un elenco di nomi descrittivi e quindi ottenere il GUID corrispondente.</span><span class="sxs-lookup"><span data-stu-id="67a8d-120">An application can display a list of friendly names and then obtain the corresponding GUID.</span></span>

<span data-ttu-id="67a8d-121">Nell'esempio di codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="67a8d-121">The following code example illustrates these steps.</span></span>


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a><span data-ttu-id="67a8d-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67a8d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a8d-123">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="67a8d-123">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
