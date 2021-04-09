---
title: Ordine di precedenza
description: Ordine di precedenza
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Metafile di Windows Media, ordine di precedenza
- Metafile di Windows Media, precedenza
- Metafile, ordine di precedenza
- Metafile, precedenza
- Windows Media, metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044367"
---
# <a name="order-of-precedence"></a><span data-ttu-id="e79c8-108">Ordine di precedenza</span><span class="sxs-lookup"><span data-stu-id="e79c8-108">Order of Precedence</span></span>

<span data-ttu-id="e79c8-109">Non tutti gli attributi dell'elemento metafile vengono creati uguali.</span><span class="sxs-lookup"><span data-stu-id="e79c8-109">Not all metafile element attributes are created equal.</span></span> <span data-ttu-id="e79c8-110">Alcuni attributi dell'elemento metafile eseguono l'override di altri attributi dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e79c8-110">Some metafile element attributes override other element attributes.</span></span> <span data-ttu-id="e79c8-111">Gli attributi degli elementi possono essere sottoposti a override da attributi di elementi simili a seconda della posizione e dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="e79c8-111">Element attributes can be overridden by similar element attributes depending on position and order.</span></span> <span data-ttu-id="e79c8-112">Tutti gli attributi di una playlist di metafile eseguono l'override di quelli contenuti in un file Windows Media a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="e79c8-112">Any attributes of a metafile playlist override those contained in a referenced Windows Media file.</span></span> <span data-ttu-id="e79c8-113">Un attributo che esegue l'override di un altro ha precedenza maggiore.</span><span class="sxs-lookup"><span data-stu-id="e79c8-113">An attribute that overrides another has higher precedence.</span></span>

<span data-ttu-id="e79c8-114">La gerarchia, con la precedenza più alta a quella più bassa, è illustrata nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e79c8-114">The hierarchy, highest precedence to lowest, is shown in the following table.</span></span> <span data-ttu-id="e79c8-115">L'elemento con precedenza più alta non viene mai sottoposto a override.</span><span class="sxs-lookup"><span data-stu-id="e79c8-115">The highest precedence item is never overridden.</span></span>



| <span data-ttu-id="e79c8-116">Ambito</span><span class="sxs-lookup"><span data-stu-id="e79c8-116">Scope</span></span>                    | <span data-ttu-id="e79c8-117">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="e79c8-117">Hierarchy</span></span>                                   |
|--------------------------|---------------------------------------------|
| <span data-ttu-id="e79c8-118">"Contenuto DRM firmato"</span><span class="sxs-lookup"><span data-stu-id="e79c8-118">"Signed DRM content"</span></span>     | <span data-ttu-id="e79c8-119">Mai sottoposto a override.</span><span class="sxs-lookup"><span data-stu-id="e79c8-119">Never overridden.</span></span>                           |
| <span data-ttu-id="e79c8-120">Ambito dell'elemento **ref**</span><span class="sxs-lookup"><span data-stu-id="e79c8-120">**REF** element scope</span></span>    | <span data-ttu-id="e79c8-121">Sottoposto a override solo dal contenuto DRM firmato.</span><span class="sxs-lookup"><span data-stu-id="e79c8-121">Only overridden by signed DRM content.</span></span>      |
| <span data-ttu-id="e79c8-122">Ambito elemento **voce**</span><span class="sxs-lookup"><span data-stu-id="e79c8-122">**ENTRY** element scope</span></span>  | <span data-ttu-id="e79c8-123">Esegue l'override degli elementi delle categorie seguenti.</span><span class="sxs-lookup"><span data-stu-id="e79c8-123">Overrides elements of the categories below.</span></span> |
| <span data-ttu-id="e79c8-124">Ambito **ASX**</span><span class="sxs-lookup"><span data-stu-id="e79c8-124">**ASX** scope</span></span>            | <span data-ttu-id="e79c8-125">Esegue l'override degli elementi del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="e79c8-125">Overrides media file elements.</span></span>              |
| <span data-ttu-id="e79c8-126">Ambito file Windows Media</span><span class="sxs-lookup"><span data-stu-id="e79c8-126">Windows Media file scope</span></span> | <span data-ttu-id="e79c8-127">Sottoposto a override da tutti i precedenti.</span><span class="sxs-lookup"><span data-stu-id="e79c8-127">Overridden by all of the above.</span></span>             |



 

-   <span data-ttu-id="e79c8-128">"Contenuto DRM firmato": oggetto firma digitale.</span><span class="sxs-lookup"><span data-stu-id="e79c8-128">"Signed DRM content" - Digital signature object.</span></span>

    <span data-ttu-id="e79c8-129">Gli attributi del contenuto DRM firmato eseguiranno l'override di tutti gli altri.</span><span class="sxs-lookup"><span data-stu-id="e79c8-129">Attributes of Signed DRM content will override all others.</span></span> <span data-ttu-id="e79c8-130">Le informazioni sul copyright di "contenuto DRM firmato", ad esempio, non verranno sostituite.</span><span class="sxs-lookup"><span data-stu-id="e79c8-130">For example, the Copyright information of "Signed DRM content" will not be overridden.</span></span> <span data-ttu-id="e79c8-131">Verrà sempre trasmesso e visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e79c8-131">It will always be streamed and presented.</span></span>

-   <span data-ttu-id="e79c8-132">Ambito dell'elemento **ref**</span><span class="sxs-lookup"><span data-stu-id="e79c8-132">**REF** element scope</span></span>

    <span data-ttu-id="e79c8-133">Gli attributi dell'elemento **ref** sostituiranno gli altri attributi degli elementi, ma non i contenuti DRM firmati.</span><span class="sxs-lookup"><span data-stu-id="e79c8-133">Attributes of the **REF** element will override other element attributes, but not signed DRM content.</span></span>

-   <span data-ttu-id="e79c8-134">Ambito **voce**</span><span class="sxs-lookup"><span data-stu-id="e79c8-134">**ENTRY** scope</span></span>

    <span data-ttu-id="e79c8-135">Gli attributi dell'elemento **entry** verranno sottoposti a override dall'attributo dell'elemento **ref** , ma eseguiranno l'override di altri attributi dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e79c8-135">Attributes of the **ENTRY** element will be overridden by the **REF** element attribute but will override other element attributes.</span></span> <span data-ttu-id="e79c8-136">Vengono visualizzati i metadati del **titolo** dall'elemento **entry** anziché le informazioni sul titolo del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="e79c8-136">**TITLE** metadata from the **ENTRY** element is displayed instead of the title information from the media file.</span></span>

-   <span data-ttu-id="e79c8-137">Ambito **ASX**</span><span class="sxs-lookup"><span data-stu-id="e79c8-137">**ASX** scope</span></span>

    <span data-ttu-id="e79c8-138">Tutte le proprietà immesse nel metafile eseguono l'override di quelle contenute nel file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e79c8-138">Any properties that are entered in the metafile override those contained in the Windows Media file.</span></span> <span data-ttu-id="e79c8-139">Attributi dell'elemento **entry** che eseguono l'override degli attributi degli elementi **ASX** .</span><span class="sxs-lookup"><span data-stu-id="e79c8-139">Attributes of the **ENTRY** element override **ASX** element attributes.</span></span> <span data-ttu-id="e79c8-140">Mentre viene riprodotto il clip multimediale a cui viene fatto riferimento nell'elemento **entry** , vengono visualizzati i metadati del **titolo** dall'elemento **entry** anziché le informazioni sul titolo dell'elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="e79c8-140">While the **ENTRY** element's referenced media clip is playing, **TITLE** metadata from the **ENTRY** element is displayed instead of title information from the **ASX** element.</span></span>

-   <span data-ttu-id="e79c8-141">Ambito file Windows Media</span><span class="sxs-lookup"><span data-stu-id="e79c8-141">Windows Media file scope</span></span>

    <span data-ttu-id="e79c8-142">Gli attributi del file Windows Media vengono sottoposti a override da qualsiasi attributo del metafile.</span><span class="sxs-lookup"><span data-stu-id="e79c8-142">Attributes of the Windows Media file are overridden by any metafile attributes.</span></span> <span data-ttu-id="e79c8-143">I metadati del file multimediale vengono visualizzati solo se non sono stati definiti metadati per tale elemento nel metafile.</span><span class="sxs-lookup"><span data-stu-id="e79c8-143">Media file metadata is displayed only if there is no metadata defined for that element in the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e79c8-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e79c8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e79c8-145">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="e79c8-145">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="e79c8-146">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="e79c8-146">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="e79c8-147">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e79c8-147">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e79c8-148">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e79c8-148">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




