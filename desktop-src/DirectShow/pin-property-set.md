---
description: Imposta la proprietà pin
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Imposta la proprietà pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401151"
---
# <a name="pin-property-set"></a><span data-ttu-id="81fef-103">Imposta la proprietà pin</span><span class="sxs-lookup"><span data-stu-id="81fef-103">Pin Property Set</span></span>

<span data-ttu-id="81fef-104">Il set di proprietà pin restituisce la categoria pin per un pin in un filtro.</span><span class="sxs-lookup"><span data-stu-id="81fef-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="81fef-105">La categoria viene impostata dal filtro durante la creazione del PIN. la categoria indica il tipo di dati che il PIN viene recapitato o riceve da questo pin.</span><span class="sxs-lookup"><span data-stu-id="81fef-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



|                   |                      |
|-------------------|----------------------|
| <span data-ttu-id="81fef-106">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="81fef-106">Property Set GUID</span></span> | <span data-ttu-id="81fef-107">**\_Pin AMPROPSETID**</span><span class="sxs-lookup"><span data-stu-id="81fef-107">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="81fef-108">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="81fef-108">Property ID</span></span>                   | <span data-ttu-id="81fef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81fef-109">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="81fef-110">**\_categoria pin \_ AMPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="81fef-110">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="81fef-111">Specifica la categoria di un PIN.</span><span class="sxs-lookup"><span data-stu-id="81fef-111">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="81fef-112">DirectShow definisce le categorie di pin seguenti nel file di intestazione UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="81fef-112">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="81fef-113">GUID categoria</span><span class="sxs-lookup"><span data-stu-id="81fef-113">Category GUID</span></span>                     | <span data-ttu-id="81fef-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81fef-114">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fef-115">**PIN \_ categoria \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="81fef-115">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="81fef-116">Pin di input del filtro di acquisizione che accetta analogie e lo Digitalizza.</span><span class="sxs-lookup"><span data-stu-id="81fef-116">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="81fef-117">**\_ \_ blocca acquisizione categoria**</span><span class="sxs-lookup"><span data-stu-id="81fef-117">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="81fef-118">Pin di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="81fef-118">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="81fef-119">**\_categoria pin \_ CC**</span><span class="sxs-lookup"><span data-stu-id="81fef-119">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="81fef-120">Pin che fornisce dati di didascalia chiusi dalla riga 21.</span><span class="sxs-lookup"><span data-stu-id="81fef-120">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="81fef-121">**PIN \_ categoria \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="81fef-121">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="81fef-122">Pin che fornisce servizi dati estesi (riga 21, anche campi).</span><span class="sxs-lookup"><span data-stu-id="81fef-122">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="81fef-123">**PIN \_ categoria \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="81fef-123">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="81fef-124">Pin che fornisce dati standard Videotext nord-americani.</span><span class="sxs-lookup"><span data-stu-id="81fef-124">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="81fef-125">**\_anteprima categoria \_ pin**</span><span class="sxs-lookup"><span data-stu-id="81fef-125">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="81fef-126">Pin di anteprima.</span><span class="sxs-lookup"><span data-stu-id="81fef-126">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="81fef-127">**BLOCCA \_ categoria \_ ancora**</span><span class="sxs-lookup"><span data-stu-id="81fef-127">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="81fef-128">Pin che fornisce un'immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="81fef-128">Pin that provides a still image.</span></span> <span data-ttu-id="81fef-129">Il pin di acquisizione del filtro deve essere connesso prima della connessione del Pin Still-Image.</span><span class="sxs-lookup"><span data-stu-id="81fef-129">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="81fef-130">**\_televideo categoria \_ pin**</span><span class="sxs-lookup"><span data-stu-id="81fef-130">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="81fef-131">Pin che fornisce il televideo (una variante di didascalia chiusa).</span><span class="sxs-lookup"><span data-stu-id="81fef-131">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="81fef-132">**Aggiungi \_ \_ timecode categoria**</span><span class="sxs-lookup"><span data-stu-id="81fef-132">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="81fef-133">Pin che fornisce i dati del timecode.</span><span class="sxs-lookup"><span data-stu-id="81fef-133">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="81fef-134">**PIN \_ categoria \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="81fef-134">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="81fef-135">Pin che fornisce dati dell'intervallo di spazi vuoti verticali.</span><span class="sxs-lookup"><span data-stu-id="81fef-135">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="81fef-136">**PIN \_ categoria \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="81fef-136">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="81fef-137">Pin di output del video da connettere al pin di input zero nel [mixer della sovrimpressione](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="81fef-137">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="81fef-138">**PIN \_ categoria \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="81fef-138">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="81fef-139">Pin da connettere a [VBI Surface allocator](vbi-surface-allocator.md), il filtro VBI Surface allocator, necessario per allocare la memoria video corretta per elementi come le sovrimpressioni dei sottotitoli codificati negli scenari in cui viene usata una porta video.</span><span class="sxs-lookup"><span data-stu-id="81fef-139">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="81fef-140">Gli scenari PCI, IEEE 1394 e USB non utilizzano questo filtro.</span><span class="sxs-lookup"><span data-stu-id="81fef-140">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="81fef-141">**\_acquisizione PINNAME video \_ CC \_**</span><span class="sxs-lookup"><span data-stu-id="81fef-141">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="81fef-142">Codice PIN per la didascalia di hardware chiuso</span><span class="sxs-lookup"><span data-stu-id="81fef-142">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="81fef-143">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="81fef-143">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="81fef-144">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="81fef-144">Example Code</span></span>

<span data-ttu-id="81fef-145">Il codice seguente illustra come verificare se un pin supporta questo set di proprietà e, in tal caso, come ottenere la categoria di pin:</span><span class="sxs-lookup"><span data-stu-id="81fef-145">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


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
> <span data-ttu-id="81fef-146">Questo esempio usa la funzione [SafeRelease](../medfound/saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="81fef-146">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="81fef-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81fef-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81fef-148">Requisiti PIN per i filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="81fef-148">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="81fef-149">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="81fef-149">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="81fef-150">Utilizzo delle categorie pin</span><span class="sxs-lookup"><span data-stu-id="81fef-150">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
