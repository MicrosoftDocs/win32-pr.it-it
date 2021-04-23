---
description: Impostare la proprietà Pin
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Impostare la proprietà Pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909619"
---
# <a name="pin-property-set"></a><span data-ttu-id="187e7-103">Impostare la proprietà Pin</span><span class="sxs-lookup"><span data-stu-id="187e7-103">Pin Property Set</span></span>

<span data-ttu-id="187e7-104">Il set di proprietà pin restituisce la categoria pin per un segnaposto in un filtro.</span><span class="sxs-lookup"><span data-stu-id="187e7-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="187e7-105">La categoria viene impostata dal filtro quando crea il segnaposto. la categoria indica il tipo di dati recapitati o ricevuti dal pin.</span><span class="sxs-lookup"><span data-stu-id="187e7-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



| <span data-ttu-id="187e7-106">Label</span><span class="sxs-lookup"><span data-stu-id="187e7-106">Label</span></span> | <span data-ttu-id="187e7-107">Valore</span><span class="sxs-lookup"><span data-stu-id="187e7-107">Value</span></span> |
|-------------------|----------------------|
| <span data-ttu-id="187e7-108">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="187e7-108">Property Set GUID</span></span> | <span data-ttu-id="187e7-109">**AMPROPSETID \_ Pin**</span><span class="sxs-lookup"><span data-stu-id="187e7-109">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="187e7-110">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="187e7-110">Property ID</span></span>                   | <span data-ttu-id="187e7-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="187e7-111">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="187e7-112">**CATEGORIA PIN AMPROPERTY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="187e7-112">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="187e7-113">Specifica la categoria di un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="187e7-113">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="187e7-114">DirectShow definisce le categorie di pin seguenti nel file di intestazione Uuids.h.</span><span class="sxs-lookup"><span data-stu-id="187e7-114">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="187e7-115">GUID della categoria</span><span class="sxs-lookup"><span data-stu-id="187e7-115">Category GUID</span></span>                     | <span data-ttu-id="187e7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="187e7-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="187e7-117">**CATEGORIA \_ PIN \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="187e7-117">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="187e7-118">Segnaposto di input del filtro di acquisizione che accetta l'analogia e lo digitalizza.</span><span class="sxs-lookup"><span data-stu-id="187e7-118">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="187e7-119">**ACQUISIZIONE \_ DI CATEGORIE DI \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="187e7-119">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="187e7-120">Pin di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="187e7-120">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="187e7-121">**CATEGORIA \_ \_ DI PIN CC**</span><span class="sxs-lookup"><span data-stu-id="187e7-121">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="187e7-122">Aggiungere i dati di sottotitoli codificati dalla riga 21.</span><span class="sxs-lookup"><span data-stu-id="187e7-122">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="187e7-123">**CATEGORIA \_ \_ DI PIN EDS**</span><span class="sxs-lookup"><span data-stu-id="187e7-123">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="187e7-124">Aggiungere l'extended data services (riga 21, campi pari).</span><span class="sxs-lookup"><span data-stu-id="187e7-124">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="187e7-125">**PIN \_ CATEGORY \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="187e7-125">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="187e7-126">Aggiungere i dati videotext standard dell'America del Nord.</span><span class="sxs-lookup"><span data-stu-id="187e7-126">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="187e7-127">**ANTEPRIMA \_ CATEGORIA \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="187e7-127">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="187e7-128">Pin di anteprima.</span><span class="sxs-lookup"><span data-stu-id="187e7-128">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="187e7-129">**CATEGORIA \_ PIN \_ ANCORA**</span><span class="sxs-lookup"><span data-stu-id="187e7-129">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="187e7-130">Segnaposto che fornisce un'immagine fissa.</span><span class="sxs-lookup"><span data-stu-id="187e7-130">Pin that provides a still image.</span></span> <span data-ttu-id="187e7-131">Il pin di acquisizione del filtro deve essere connesso prima che il pin dell'immagine fissa sia connesso.</span><span class="sxs-lookup"><span data-stu-id="187e7-131">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="187e7-132">**TELETEXT \_ CATEGORIA \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="187e7-132">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="187e7-133">Pin che fornisce teletext (una variante di sottotitoli codificati).</span><span class="sxs-lookup"><span data-stu-id="187e7-133">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="187e7-134">**PIN \_ CATEGORY \_ TIMECODE**</span><span class="sxs-lookup"><span data-stu-id="187e7-134">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="187e7-135">Pin che fornisce i dati del timecode.</span><span class="sxs-lookup"><span data-stu-id="187e7-135">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="187e7-136">**CATEGORIA \_ DI PIN \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="187e7-136">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="187e7-137">Aggiungere i dati dell'intervallo di blanking verticale.</span><span class="sxs-lookup"><span data-stu-id="187e7-137">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="187e7-138">**PIN \_ CATEGORY \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="187e7-138">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="187e7-139">Pin di output video da collegare al pin di input zero nel [mixer di sovrimpressione.](overlay-mixer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="187e7-139">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="187e7-140">**CATEGORIA \_ PIN \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="187e7-140">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="187e7-141">Pin da collegare all'allocatore di superficie [VBI,](vbi-surface-allocator.md)il filtro dell'allocatore di superficie VBI necessario per allocare la memoria video corretta per elementi come le sovrimpressione di sottotitoli codificati negli scenari in cui viene usata una porta video.</span><span class="sxs-lookup"><span data-stu-id="187e7-141">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="187e7-142">Gli scenari PCI, IEEE 1394 e USB non usano questo filtro.</span><span class="sxs-lookup"><span data-stu-id="187e7-142">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="187e7-143">**PINNAME \_ VIDEO \_ CC \_ CAPTURE**</span><span class="sxs-lookup"><span data-stu-id="187e7-143">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="187e7-144">Pin di sezione hardware per sottotitoli codificati</span><span class="sxs-lookup"><span data-stu-id="187e7-144">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="187e7-145">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="187e7-145">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="187e7-146">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="187e7-146">Example Code</span></span>

<span data-ttu-id="187e7-147">Il codice seguente illustra come verificare se un pin supporta questo set di proprietà e, in tal caso, come ottenere la categoria del pin:</span><span class="sxs-lookup"><span data-stu-id="187e7-147">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="187e7-148">Questo esempio usa la [funzione SafeRelease](../medfound/saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="187e7-148">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="187e7-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="187e7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="187e7-150">Requisiti di aggiunta per i filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="187e7-150">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="187e7-151">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="187e7-151">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="187e7-152">Uso delle categorie di aggiunta</span><span class="sxs-lookup"><span data-stu-id="187e7-152">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
