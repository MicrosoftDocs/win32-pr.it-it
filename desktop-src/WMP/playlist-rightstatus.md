---
title: PLAYLIST. rightStatus
description: L'attributo rightStatus specifica o Recupera il testo di stato visualizzato sul lato destro e sulla parte inferiore dell'elemento PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- PLAYLIST. rightStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326717"
---
# <a name="playlistrightstatus"></a><span data-ttu-id="d3f51-104">PLAYLIST. rightStatus</span><span class="sxs-lookup"><span data-stu-id="d3f51-104">PLAYLIST.rightStatus</span></span>

<span data-ttu-id="d3f51-105">L'attributo **rightStatus** specifica o Recupera il testo di stato visualizzato sul lato destro e sulla parte inferiore dell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="d3f51-105">The **rightStatus** attribute specifies or retrieves the status text that is displayed on the right side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a><span data-ttu-id="d3f51-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d3f51-106">Possible Values</span></span>

<span data-ttu-id="d3f51-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d3f51-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3f51-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3f51-108">Remarks</span></span>

<span data-ttu-id="d3f51-109">Questo attributo può combinare qualsiasi testo con parole chiave specifiche che visualizzeranno le informazioni desiderate, ad esempio la durata totale della playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="d3f51-110">Le parole chiave sono racchiuse tra simboli di percentuale (%) per mantenerli distinti dal testo normale.</span><span class="sxs-lookup"><span data-stu-id="d3f51-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="d3f51-111">È possibile utilizzare le parole chiave seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3f51-111">The following keywords can be used.</span></span>



| <span data-ttu-id="d3f51-112">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="d3f51-112">Keyword</span></span>               | <span data-ttu-id="d3f51-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3f51-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f51-114">count</span><span class="sxs-lookup"><span data-stu-id="d3f51-114">count</span></span>                 | <span data-ttu-id="d3f51-115">Numero di elementi nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="d3f51-116">size</span><span class="sxs-lookup"><span data-stu-id="d3f51-116">size</span></span>                  | <span data-ttu-id="d3f51-117">Dimensioni totali della playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="d3f51-118">duration</span><span class="sxs-lookup"><span data-stu-id="d3f51-118">duration</span></span>              | <span data-ttu-id="d3f51-119">Durata totale della playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="d3f51-120">*XXX*</span><span class="sxs-lookup"><span data-stu-id="d3f51-120">*XXX*</span></span>                 | <span data-ttu-id="d3f51-121">Esegue un **GetItemInfo** nella playlist con *xxx* che è l'elemento da ricevere.</span><span class="sxs-lookup"><span data-stu-id="d3f51-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="d3f51-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="d3f51-122">SelectedSize</span></span>          | <span data-ttu-id="d3f51-123">Dimensioni totali delle voci selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d3f51-124">SelectedCount</span><span class="sxs-lookup"><span data-stu-id="d3f51-124">SelectedCount</span></span>         | <span data-ttu-id="d3f51-125">Numero totale di voci selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="d3f51-126">SelectedDuration</span><span class="sxs-lookup"><span data-stu-id="d3f51-126">SelectedDuration</span></span>      | <span data-ttu-id="d3f51-127">Durata totale delle voci selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="d3f51-128">CheckedCount</span><span class="sxs-lookup"><span data-stu-id="d3f51-128">CheckedCount</span></span>          | <span data-ttu-id="d3f51-129">Numero totale di tracce selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d3f51-130">CheckedDuration</span><span class="sxs-lookup"><span data-stu-id="d3f51-130">CheckedDuration</span></span>       | <span data-ttu-id="d3f51-131">Durata totale delle tracce selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="d3f51-132">CheckedSize</span><span class="sxs-lookup"><span data-stu-id="d3f51-132">CheckedSize</span></span>           | <span data-ttu-id="d3f51-133">Dimensioni totali delle tracce selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d3f51-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="d3f51-134">DurationString</span><span class="sxs-lookup"><span data-stu-id="d3f51-134">DurationString</span></span>        | <span data-ttu-id="d3f51-135">Visualizza il testo che descrive la durata "tempo totale" o "tempo stimato", a seconda che i valori totali siano noti.</span><span class="sxs-lookup"><span data-stu-id="d3f51-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="d3f51-136">Il testo è seguito da "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="d3f51-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="d3f51-137">CheckedDurationString</span><span class="sxs-lookup"><span data-stu-id="d3f51-137">CheckedDurationString</span></span> | <span data-ttu-id="d3f51-138">Visualizza il testo che descrive la durata di tutti gli elementi selezionati nella playlist come "tempo totale" o "tempo stimato", a seconda che i valori totali siano noti o meno.</span><span class="sxs-lookup"><span data-stu-id="d3f51-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="d3f51-139">Il testo è seguito da "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="d3f51-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="d3f51-140">Il valore "tempo totale:% Duration%" per una playlist che contiene una durata totale di sette minuti visualizzerà "tempo totale: 07:00".</span><span class="sxs-lookup"><span data-stu-id="d3f51-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f51-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3f51-141">Requirements</span></span>



| <span data-ttu-id="d3f51-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f51-142">Requirement</span></span> | <span data-ttu-id="d3f51-143">Valore</span><span class="sxs-lookup"><span data-stu-id="d3f51-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d3f51-144">Versione</span><span class="sxs-lookup"><span data-stu-id="d3f51-144">Version</span></span><br/> | <span data-ttu-id="d3f51-145">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d3f51-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3f51-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3f51-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f51-147">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="d3f51-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





