---
title: PLAYLIST. leftStatus
description: L'attributo leftStatus specifica o Recupera il testo di stato visualizzato sul lato sinistro e inferiore dell'elemento PLAYLIST.
ms.assetid: c83f4fd1-d0e6-4822-9208-8e968c409a78
keywords:
- PLAYLIST. leftStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.leftStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33d4c3d235a7bba67219378063cb9811601e68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327621"
---
# <a name="playlistleftstatus"></a><span data-ttu-id="3a938-104">PLAYLIST. leftStatus</span><span class="sxs-lookup"><span data-stu-id="3a938-104">PLAYLIST.leftStatus</span></span>

<span data-ttu-id="3a938-105">L'attributo **leftStatus** specifica o Recupera il testo di stato visualizzato sul lato sinistro e inferiore dell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="3a938-105">The **leftStatus** attribute specifies or retrieves the status text that is displayed on the left side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.leftStatus
```

## <a name="possible-values"></a><span data-ttu-id="3a938-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3a938-106">Possible Values</span></span>

<span data-ttu-id="3a938-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3a938-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a938-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a938-108">Remarks</span></span>

<span data-ttu-id="3a938-109">Questo attributo può combinare qualsiasi testo con parole chiave specifiche che visualizzeranno le informazioni desiderate, ad esempio la durata totale della playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="3a938-110">Le parole chiave sono racchiuse tra simboli di percentuale (%) per mantenerli distinti dal testo normale.</span><span class="sxs-lookup"><span data-stu-id="3a938-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="3a938-111">È possibile utilizzare le parole chiave seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a938-111">The following keywords can be used.</span></span>



| <span data-ttu-id="3a938-112">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="3a938-112">Keyword</span></span>               | <span data-ttu-id="3a938-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a938-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a938-114">count</span><span class="sxs-lookup"><span data-stu-id="3a938-114">count</span></span>                 | <span data-ttu-id="3a938-115">Numero di elementi nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="3a938-116">size</span><span class="sxs-lookup"><span data-stu-id="3a938-116">size</span></span>                  | <span data-ttu-id="3a938-117">Dimensioni totali della playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="3a938-118">duration</span><span class="sxs-lookup"><span data-stu-id="3a938-118">duration</span></span>              | <span data-ttu-id="3a938-119">Durata totale della playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="3a938-120">*XXX*</span><span class="sxs-lookup"><span data-stu-id="3a938-120">*XXX*</span></span>                 | <span data-ttu-id="3a938-121">Esegue un **GetItemInfo** nella playlist con *xxx* che è l'elemento da ricevere.</span><span class="sxs-lookup"><span data-stu-id="3a938-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="3a938-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="3a938-122">SelectedSize</span></span>          | <span data-ttu-id="3a938-123">Dimensioni totali delle voci selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="3a938-124">SelectedCount</span><span class="sxs-lookup"><span data-stu-id="3a938-124">SelectedCount</span></span>         | <span data-ttu-id="3a938-125">Numero totale di voci selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="3a938-126">SelectedDuration</span><span class="sxs-lookup"><span data-stu-id="3a938-126">SelectedDuration</span></span>      | <span data-ttu-id="3a938-127">Durata totale delle voci selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="3a938-128">CheckedCount</span><span class="sxs-lookup"><span data-stu-id="3a938-128">CheckedCount</span></span>          | <span data-ttu-id="3a938-129">Numero totale di tracce selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="3a938-130">CheckedDuration</span><span class="sxs-lookup"><span data-stu-id="3a938-130">CheckedDuration</span></span>       | <span data-ttu-id="3a938-131">Durata totale delle tracce selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="3a938-132">CheckedSize</span><span class="sxs-lookup"><span data-stu-id="3a938-132">CheckedSize</span></span>           | <span data-ttu-id="3a938-133">Dimensioni totali delle tracce selezionate nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3a938-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="3a938-134">DurationString</span><span class="sxs-lookup"><span data-stu-id="3a938-134">DurationString</span></span>        | <span data-ttu-id="3a938-135">Visualizza il testo che descrive la durata "tempo totale" o "tempo stimato", a seconda che i valori totali siano noti.</span><span class="sxs-lookup"><span data-stu-id="3a938-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="3a938-136">Il testo è seguito da "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="3a938-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="3a938-137">CheckedDurationString</span><span class="sxs-lookup"><span data-stu-id="3a938-137">CheckedDurationString</span></span> | <span data-ttu-id="3a938-138">Visualizza il testo che descrive la durata di tutti gli elementi selezionati nella playlist come "tempo totale" o "tempo stimato", a seconda che i valori totali siano noti o meno.</span><span class="sxs-lookup"><span data-stu-id="3a938-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="3a938-139">Il testo è seguito da "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="3a938-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="3a938-140">Il valore "tempo totale:% Duration%" per una playlist che contiene una durata totale di sette minuti visualizzerà "tempo totale: 07:00".</span><span class="sxs-lookup"><span data-stu-id="3a938-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="3a938-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a938-141">Requirements</span></span>



| <span data-ttu-id="3a938-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a938-142">Requirement</span></span> | <span data-ttu-id="3a938-143">Valore</span><span class="sxs-lookup"><span data-stu-id="3a938-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3a938-144">Versione</span><span class="sxs-lookup"><span data-stu-id="3a938-144">Version</span></span><br/> | <span data-ttu-id="3a938-145">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3a938-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a938-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a938-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a938-147">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="3a938-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





