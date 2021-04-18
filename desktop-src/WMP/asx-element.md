---
title: Elemento ASX
description: L'elemento ASX definisce un file come metafile.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Windows elemento ASX Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331404"
---
# <a name="asx-element"></a><span data-ttu-id="6e6c7-104">Elemento ASX</span><span class="sxs-lookup"><span data-stu-id="6e6c7-104">ASX Element</span></span>

<span data-ttu-id="6e6c7-105">L'elemento **ASX** definisce un file come metafile.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-105">The **ASX** element defines a file as a metafile.</span></span>

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a><span data-ttu-id="6e6c7-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="6e6c7-106">Attributes</span></span>

<span data-ttu-id="6e6c7-107">`VERSION` (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="6e6c7-107">`VERSION` (required)</span></span>

<span data-ttu-id="6e6c7-108">Numero decimale che rappresenta il numero di versione della sintassi per il metafile.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-108">Decimal number representing the version number of the syntax for the metafile.</span></span> <span data-ttu-id="6e6c7-109">Impostare su 3 o 3,0.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-109">Set to 3 or 3.0.</span></span>

<span data-ttu-id="6e6c7-110">**PREVIEWMODE** (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6e6c7-110">**PREVIEWMODE** (optional)</span></span>

<span data-ttu-id="6e6c7-111">Valore che indica se Windows Media Player passa alla modalità di anteprima prima di riprodurre il primo clip.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-111">Value indicating whether Windows Media Player enters preview mode before playing the first clip.</span></span>

<span data-ttu-id="6e6c7-112">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-112">Must be one of the following values.</span></span>



| <span data-ttu-id="6e6c7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6c7-113">Value</span></span> | <span data-ttu-id="6e6c7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e6c7-114">Description</span></span>                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6c7-115">YES</span><span class="sxs-lookup"><span data-stu-id="6e6c7-115">YES</span></span>   | <span data-ttu-id="6e6c7-116">Windows Media Player passa alla modalità di anteprima prima di riprodurre il primo clip.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-116">Windows Media Player enters preview mode before playing the first clip.</span></span>                            |
| <span data-ttu-id="6e6c7-117">NO</span><span class="sxs-lookup"><span data-stu-id="6e6c7-117">NO</span></span>    | <span data-ttu-id="6e6c7-118">Il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-118">The default value.</span></span> <span data-ttu-id="6e6c7-119">Windows Media Player non entra in modalità di anteprima prima di riprodurre il primo clip.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-119">Windows Media Player does not enter preview mode before playing the first clip.</span></span> |



 

<span data-ttu-id="6e6c7-120">**BANNERBAR** (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6e6c7-120">**BANNERBAR** (optional)</span></span>

<span data-ttu-id="6e6c7-121">Valore che indica se Windows Media Player riserva spazio per una rappresentazione grafica del banner.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-121">Value indicating whether Windows Media Player reserves space for a banner graphic.</span></span>

<span data-ttu-id="6e6c7-122">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-122">Must be one of the following values.</span></span>



| <span data-ttu-id="6e6c7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6c7-123">Value</span></span> | <span data-ttu-id="6e6c7-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e6c7-124">Description</span></span>                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6c7-125">AUTO</span><span class="sxs-lookup"><span data-stu-id="6e6c7-125">AUTO</span></span>  | <span data-ttu-id="6e6c7-126">Il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-126">The default value.</span></span> <span data-ttu-id="6e6c7-127">Windows Media Player riserva spazio per la barra del banner solo quando una parte di contenuto ne include una.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-127">Windows Media Player reserves space for the banner bar only when a piece of content includes one.</span></span>                       |
| <span data-ttu-id="6e6c7-128">FIXED</span><span class="sxs-lookup"><span data-stu-id="6e6c7-128">FIXED</span></span> | <span data-ttu-id="6e6c7-129">Windows Media Player riserva uno spazio fisso per un grafico banner per ogni parte di contenuto riprodotta, a prescindere dal fatto che sia presente un banner associato.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-129">Windows Media Player reserves a fixed space for a banner graphic for every piece of content played, whether there is an associated banner.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6e6c7-130">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="6e6c7-130">Parent/Child Elements</span></span>



| <span data-ttu-id="6e6c7-131">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="6e6c7-131">Hierarchy</span></span>       | <span data-ttu-id="6e6c7-132">Elementi</span><span class="sxs-lookup"><span data-stu-id="6e6c7-132">Elements</span></span>                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6c7-133">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="6e6c7-133">Parent elements</span></span> | <span data-ttu-id="6e6c7-134">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-134">None.</span></span> <span data-ttu-id="6e6c7-135">L'elemento **ASX** deve essere il primo elemento di ogni metafile.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-135">The **ASX** element must be the first element in every metafile.</span></span>                                                                                                 |
| <span data-ttu-id="6e6c7-136">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6e6c7-136">Child elements</span></span>  | <span data-ttu-id="6e6c7-137">**abstract**, **Author**, **banner**, **base**, **Copyright**, **entry**, **ENTRYREF**, **Event**, **moreinfo**, **PREVIEWDURATION**, **param**, **Repeat**, **title**</span><span class="sxs-lookup"><span data-stu-id="6e6c7-137">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6e6c7-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e6c7-138">Remarks</span></span>

<span data-ttu-id="6e6c7-139">I primi quattro caratteri di una playlist di metafile devono essere "<ASX".</span><span class="sxs-lookup"><span data-stu-id="6e6c7-139">The first four characters of a metafile playlist must be "<ASX".</span></span> <span data-ttu-id="6e6c7-140">Gli altri elementi definiti nell'ambito dell'elemento **ASX** , ad esempio **titolo** e **autore**, sono associati alle informazioni di visualizzazione visualizzate da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-140">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the show information displayed by Windows Media Player.</span></span>

<span data-ttu-id="6e6c7-141">Per Windows Media Player, il numero di versione della sintassi è 3,0.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-141">For Windows Media Player, the syntax version number is 3.0.</span></span> <span data-ttu-id="6e6c7-142">Windows Media Player supporta tutte le versioni precedenti della sintassi del metafile.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-142">Windows Media Player supports all previous versions of metafile syntax.</span></span> <span data-ttu-id="6e6c7-143">I valori accettabili per l'attributo **Version** includono sia 3,0 che 3 (senza virgola decimale).</span><span class="sxs-lookup"><span data-stu-id="6e6c7-143">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="6e6c7-144">Se il valore dell'attributo **PREVIEWMODE** è sì, Windows Media Player passa immediatamente alla modalità di anteprima prima di riprodurre il primo clip.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-144">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player immediately enters preview mode before playing the first clip.</span></span> <span data-ttu-id="6e6c7-145">Quando Windows Media Player passa alla modalità di anteprima, Visualizza in anteprima ogni clip a cui viene fatto riferimento nel metafile.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-145">When Windows Media Player enters preview mode, it previews each clip referenced in the metafile.</span></span> <span data-ttu-id="6e6c7-146">L'elemento **PREVIEWDURATION** determina la durata di ogni anteprima.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-146">The **PREVIEWDURATION** element determines the duration of each preview.</span></span>

<span data-ttu-id="6e6c7-147">L'attributo **BANNERBAR** definisce se Windows Media Player riserva spazio per una rappresentazione grafica del banner.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-147">The **BANNERBAR** attribute defines whether Windows Media Player reserves space for a banner graphic.</span></span> <span data-ttu-id="6e6c7-148">Un banner è un grafico che viene visualizzato nell'area di visualizzazione del video mentre viene riprodotto il contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-148">A banner is a graphic that is displayed in the video display area while media content is playing.</span></span> <span data-ttu-id="6e6c7-149">(Usare l'elemento **banner** per aggiungere un banner al contenuto). Se il valore di **BANNERBAR** è fisso, Windows Media Player riserva lo spazio del banner per ogni contenuto multimediale, indipendentemente dal fatto che il contenuto multimediale includa un banner.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-149">(Use the **BANNER** element to add a banner to the content.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for every piece of media content, whether the media content has a banner.</span></span> <span data-ttu-id="6e6c7-150">Se a un contenuto multimediale non è associato alcun banner, lo spazio riservato per uno è nero.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-150">If a piece of media content does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="6e6c7-151">Se il valore dell'attributo **BANNERBAR** è auto, Windows Media Player riserva spazio per il banner solo quando il contenuto multimediale ne include uno.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-151">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the media content includes one.</span></span>

<span data-ttu-id="6e6c7-152">Se si crea un metafile con più clip (elementi **entry** o **ENTRYREF** ) e si imposta il valore dell'attributo **BANNERBAR** su auto, Windows Media Player potrebbe essere ridimensionato in modo da consentire lo spazio per un'immagine del banner per un clip e quindi ridimensionarlo nuovamente se il clip successivo non contiene una rappresentazione grafica del banner.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-152">If you create a metafile with multiple clips (**ENTRY** or **ENTRYREF** elements) and set the value of the **BANNERBAR** attribute to AUTO, Windows Media Player might resize to allow space for a banner graphic for one clip, and then resize again if the next clip does not contain a banner graphic.</span></span> <span data-ttu-id="6e6c7-153">Se si desidera che la dimensione della finestra resti invariata (tranne quando le dimensioni del video cambiano), utilizzare il valore fisso per l'attributo **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="6e6c7-153">If you want the size of the window to stay the same (except when the video size changes), use the FIXED value for the **BANNERBAR** attribute.</span></span>

<span data-ttu-id="6e6c7-154">Lo spazio riservato per una rappresentazione grafica del banner è 32 pixel di altezza di 194 pixel di larghezza.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-154">The space reserved for a banner graphic is 32 pixels high by 194 pixels wide.</span></span> <span data-ttu-id="6e6c7-155">Lo spazio riservato viene visualizzato al di sotto di qualsiasi contenuto video di cui è stato eseguito il rendering e 6 pixel sopra il bordo inferiore dell'area video, consentendo lo spazio per il bordo dell'area video a 6 pixel.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-155">The reserved space appears below any rendered video content and 6 pixels above the lower edge of the video area, allowing space for the 6-pixel video area border.</span></span> <span data-ttu-id="6e6c7-156">Lo spazio del banner riservato viene centrato orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-156">The reserved banner space is centered horizontally.</span></span>

<span data-ttu-id="6e6c7-157">Windows Media Player esegue il rendering dell'elemento grafico a partire dal pixel più a sinistra dello spazio del banner.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-157">Windows Media Player renders the graphic beginning in the leftmost pixel of the banner space.</span></span> <span data-ttu-id="6e6c7-158">Se il grafico riempie l'intero spazio, verrà visualizzato al centro orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-158">If the graphic fills the entire space, it will appear centered horizontally.</span></span> <span data-ttu-id="6e6c7-159">In caso contrario, sarà presente uno spazio finale.</span><span class="sxs-lookup"><span data-stu-id="6e6c7-159">Otherwise there will be trailing space.</span></span> <span data-ttu-id="6e6c7-160">Si noti che la larghezza minima di Windows Media Player è sempre più ampia della dimensione del clip video, indipendentemente dal valore dell'attributo **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="6e6c7-160">Note that the minimum width of Windows Media Player is always wider than the size of the video clip, regardless of the value of the **BANNERBAR** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6e6c7-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="6e6c7-161">Examples</span></span>


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="6e6c7-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e6c7-162">Requirements</span></span>



| <span data-ttu-id="6e6c7-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e6c7-163">Requirement</span></span> | <span data-ttu-id="6e6c7-164">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6c7-164">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="6e6c7-165">Versione</span><span class="sxs-lookup"><span data-stu-id="6e6c7-165">Version</span></span><br/> | <span data-ttu-id="6e6c7-166">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="6e6c7-166">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e6c7-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e6c7-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e6c7-168">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6e6c7-168">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6e6c7-169">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6e6c7-169">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





