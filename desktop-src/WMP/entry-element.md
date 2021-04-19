---
title: Elemento ENTRY
description: L'elemento ENTRY specifica un file di Windows Media da visualizzare come clip.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Elemento ENTRY Media Player Windows
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333245"
---
# <a name="entry-element"></a><span data-ttu-id="d3b19-104">Elemento ENTRY</span><span class="sxs-lookup"><span data-stu-id="d3b19-104">ENTRY Element</span></span>

<span data-ttu-id="d3b19-105">L'elemento **entry** specifica un file di Windows Media da visualizzare come clip.</span><span class="sxs-lookup"><span data-stu-id="d3b19-105">The **ENTRY** element specifies a Windows Media file to render as a clip.</span></span>

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a><span data-ttu-id="d3b19-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="d3b19-106">Attributes</span></span>

<span data-ttu-id="d3b19-107">**CLIENTSKIP**</span><span class="sxs-lookup"><span data-stu-id="d3b19-107">**CLIENTSKIP**</span></span>

<span data-ttu-id="d3b19-108">Valore che indica se l'utente può andare avanti oltre il clip.</span><span class="sxs-lookup"><span data-stu-id="d3b19-108">Value indicating whether the user can skip forward past the clip.</span></span>

<span data-ttu-id="d3b19-109">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="d3b19-109">Possible values include the following.</span></span>



| <span data-ttu-id="d3b19-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d3b19-110">Value</span></span> | <span data-ttu-id="d3b19-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3b19-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="d3b19-112">YES</span><span class="sxs-lookup"><span data-stu-id="d3b19-112">YES</span></span>   | <span data-ttu-id="d3b19-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d3b19-113">Default.</span></span> <span data-ttu-id="d3b19-114">L'utente può andare avanti oltre il clip.</span><span class="sxs-lookup"><span data-stu-id="d3b19-114">User can skip forward past the clip.</span></span> |
| <span data-ttu-id="d3b19-115">NO</span><span class="sxs-lookup"><span data-stu-id="d3b19-115">NO</span></span>    | <span data-ttu-id="d3b19-116">L'utente non può andare avanti oltre il clip.</span><span class="sxs-lookup"><span data-stu-id="d3b19-116">User cannot skip forward past the clip.</span></span>       |



 

<span data-ttu-id="d3b19-117">**SKIPIFREF**</span><span class="sxs-lookup"><span data-stu-id="d3b19-117">**SKIPIFREF**</span></span>

<span data-ttu-id="d3b19-118">Valore che indica se Windows Media Player deve ignorare questa clip quando l'elemento **entry** viene incluso in un secondo metafile mediante l'utilizzo di un elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="d3b19-118">Value indicating whether Windows Media Player should skip this clip when the **ENTRY** element is included in a second metafile through the use of an **ENTRYREF** element.</span></span>

<span data-ttu-id="d3b19-119">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="d3b19-119">Possible values include the following.</span></span>



| <span data-ttu-id="d3b19-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d3b19-120">Value</span></span> | <span data-ttu-id="d3b19-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3b19-121">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b19-122">YES</span><span class="sxs-lookup"><span data-stu-id="d3b19-122">YES</span></span>   | <span data-ttu-id="d3b19-123">Windows Media Player ignorerà questa voce, se vi viene fatto riferimento tramite un elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="d3b19-123">Windows Media Player will ignore this entry, if referenced through an **ENTRYREF** element.</span></span> |
| <span data-ttu-id="d3b19-124">NO</span><span class="sxs-lookup"><span data-stu-id="d3b19-124">NO</span></span>    | <span data-ttu-id="d3b19-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d3b19-125">Default.</span></span> <span data-ttu-id="d3b19-126">Questa voce non verrà ignorata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d3b19-126">Windows Media Player will not ignore this entry.</span></span>                                   |



 

## <a name="parentchild-elements"></a><span data-ttu-id="d3b19-127">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="d3b19-127">Parent/Child Elements</span></span>



| <span data-ttu-id="d3b19-128">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="d3b19-128">Hierarchy</span></span>       | <span data-ttu-id="d3b19-129">Elementi</span><span class="sxs-lookup"><span data-stu-id="d3b19-129">Elements</span></span>                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b19-130">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d3b19-130">Parent elements</span></span> | <span data-ttu-id="d3b19-131">**ASX**, **evento**, **ripetizione**</span><span class="sxs-lookup"><span data-stu-id="d3b19-131">**ASX**, **EVENT**, **REPEAT**</span></span>                                                                                                                                                               |
| <span data-ttu-id="d3b19-132">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d3b19-132">Child elements</span></span>  | <span data-ttu-id="d3b19-133">**abstract**, **Author**, **banner**, **base**, **Copyright**, **Duration**, **ENDMARKER**, **moreinfo**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **StartTime**, **title**</span><span class="sxs-lookup"><span data-stu-id="d3b19-133">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d3b19-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3b19-134">Remarks</span></span>

<span data-ttu-id="d3b19-135">Questo elemento è il costrutto fondamentale in un metafile di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d3b19-135">This element is the fundamental construct in a Windows Media metafile.</span></span> <span data-ttu-id="d3b19-136">L'elemento **entry** e gli attributi associati definiscono le metainformazioni per una singola parte logica di contenuto, denominata clip.</span><span class="sxs-lookup"><span data-stu-id="d3b19-136">The **ENTRY** element and its associated attributes define meta-information for a single, logical piece of content, called a clip.</span></span> <span data-ttu-id="d3b19-137">Gli elementi figlio all'interno dell'ambito di un elemento **entry** definiscono il contenuto multimediale per Windows Media Player per aprire (**ref**), informazioni sul clip che Windows Media Player visualizzerà come testo (**autore**, **Copyright**, **titolo**) e altre impostazioni correlate alla clip.</span><span class="sxs-lookup"><span data-stu-id="d3b19-137">Child elements within the scope of an **ENTRY** element define media content for Windows Media Player to open (**REF**), information about the clip that Windows Media Player will display as text (**AUTHOR**, **COPYRIGHT**, **TITLE**), and other settings related to the clip.</span></span> <span data-ttu-id="d3b19-138">L'elemento figlio **ref** collega il contenuto da trasmettere per l'elemento **entry** padre.</span><span class="sxs-lookup"><span data-stu-id="d3b19-138">The **REF** child element links the content to be streamed for the parent **ENTRY** element.</span></span> <span data-ttu-id="d3b19-139">Sebbene lo script non venga interrotta, la **voce** non è significativa senza un elemento figlio **ref** .</span><span class="sxs-lookup"><span data-stu-id="d3b19-139">Though the script will not break, the **ENTRY** is meaningless without a **REF** child.</span></span>

<span data-ttu-id="d3b19-140">Se il valore dell'attributo **CLIENTSKIP** è No, l'utente non può andare avanti oltre il contenuto definito dall'elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="d3b19-140">If the value of the **CLIENTSKIP** attribute is NO, the user cannot skip forward past the piece of content defined by the **ENTRY** element.</span></span> <span data-ttu-id="d3b19-141">Questa operazione non funziona se l'elemento **ref** figlio fa riferimento a un altro metafile.</span><span class="sxs-lookup"><span data-stu-id="d3b19-141">This does not work if the child **REF** element references another metafile.</span></span> <span data-ttu-id="d3b19-142">È necessario fare riferimento ai metafile annidati usando l'elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="d3b19-142">Nested metafiles should be referenced using the **ENTRYREF** element.</span></span>

<span data-ttu-id="d3b19-143">L'attributo **SKIPIFREF** riguarda solo gli elementi **entry** inclusi in un secondo metafile tramite l'uso di un elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="d3b19-143">The **SKIPIFREF** attribute pertains only to **ENTRY** elements that are included in a second metafile through the use of an **ENTRYREF** element.</span></span> <span data-ttu-id="d3b19-144">L'elemento **ENTRYREF** fa riferimento a un altro metafile per l'inclusione logica nel file corrente.</span><span class="sxs-lookup"><span data-stu-id="d3b19-144">The **ENTRYREF** element references another metafile for logical inclusion in the current file.</span></span> <span data-ttu-id="d3b19-145">Se il valore dell'attributo **SKIPIFREF** per un elemento **entry** dal file Metafile a cui si fa riferimento è Yes, Windows Media Player ignora questa voce di cui è stato eseguito il pull e passa all'elemento **entry** successivo, se presente.</span><span class="sxs-lookup"><span data-stu-id="d3b19-145">If the value of the **SKIPIFREF** attribute for an **ENTRY** element from the referenced metafile file is YES, Windows Media Player ignores this pulled-in entry, and moves on to the next **ENTRY** element, if any.</span></span> <span data-ttu-id="d3b19-146">L'elemento **entry** successivo può essere la voce successiva nel file originale o la voce successiva nel metafile a cui si fa riferimento nell'elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="d3b19-146">The next **ENTRY** element can be the next entry in the original file, or the next entry in the metafile referenced in the **ENTRYREF** element.</span></span>

## <a name="examples"></a><span data-ttu-id="d3b19-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3b19-147">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="d3b19-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3b19-148">Requirements</span></span>



| <span data-ttu-id="d3b19-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b19-149">Requirement</span></span> | <span data-ttu-id="d3b19-150">Valore</span><span class="sxs-lookup"><span data-stu-id="d3b19-150">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="d3b19-151">Versione</span><span class="sxs-lookup"><span data-stu-id="d3b19-151">Version</span></span><br/> | <span data-ttu-id="d3b19-152">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="d3b19-152">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3b19-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3b19-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b19-154">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d3b19-154">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d3b19-155">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d3b19-155">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





