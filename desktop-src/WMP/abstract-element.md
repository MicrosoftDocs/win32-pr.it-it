---
title: ABSTRACT (elemento)
description: L'elemento astratto contiene testo che descrive l'elemento ASX, BANNER o ENTRY associato.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Media Player di Windows elemento astratto
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330903"
---
# <a name="abstract-element"></a><span data-ttu-id="a504c-104">ABSTRACT (elemento)</span><span class="sxs-lookup"><span data-stu-id="a504c-104">ABSTRACT Element</span></span>

<span data-ttu-id="a504c-105">L'elemento **astratto** contiene testo che descrive l'elemento **ASX**, **banner** o **entry** associato.</span><span class="sxs-lookup"><span data-stu-id="a504c-105">The **ABSTRACT** element contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a><span data-ttu-id="a504c-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="a504c-106">Attributes</span></span>

<span data-ttu-id="a504c-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="a504c-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="a504c-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="a504c-108">Parent/Child Elements</span></span>



| <span data-ttu-id="a504c-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="a504c-109">Hierarchy</span></span> | <span data-ttu-id="a504c-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="a504c-110">Elements</span></span>                       |
|-----------|--------------------------------|
| <span data-ttu-id="a504c-111">Padre</span><span class="sxs-lookup"><span data-stu-id="a504c-111">Parent</span></span>    | <span data-ttu-id="a504c-112">**ASX**, **voce**, **banner**</span><span class="sxs-lookup"><span data-stu-id="a504c-112">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="a504c-113">Figlio</span><span class="sxs-lookup"><span data-stu-id="a504c-113">Child</span></span>     | <span data-ttu-id="a504c-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="a504c-114">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="a504c-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a504c-115">Remarks</span></span>

<span data-ttu-id="a504c-116">Se questo elemento viene visualizzato all'interno di un elemento **ASX** , il testo viene visualizzato come descrizione comando quando il mouse viene posizionato sul titolo della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a504c-116">If this element appears within an **ASX** element, the text displays as a ToolTip when the mouse hovers over the show title.</span></span>

<span data-ttu-id="a504c-117">Se questo elemento viene visualizzato all'interno di un elemento **entry** , il testo viene visualizzato come descrizione comando quando il mouse viene posizionato sul titolo della clip.</span><span class="sxs-lookup"><span data-stu-id="a504c-117">If this element appears within an **ENTRY** element, the text displays as a ToolTip when the mouse hovers over the clip title.</span></span>

<span data-ttu-id="a504c-118">Se questo elemento viene visualizzato all'interno di un elemento **banner** , il testo viene visualizzato come descrizione comando per l'icona del banner.</span><span class="sxs-lookup"><span data-stu-id="a504c-118">If this element appears within a **BANNER** element, the text displays as a ToolTip for the banner graphic.</span></span>

<span data-ttu-id="a504c-119">Usare un solo elemento **astratto** per ambito.</span><span class="sxs-lookup"><span data-stu-id="a504c-119">Use only one **ABSTRACT** element per scope.</span></span> <span data-ttu-id="a504c-120">Quando viene elaborato un file Metafile, viene utilizzato solo il primo elemento **astratto** nell'ambito di un altro elemento.</span><span class="sxs-lookup"><span data-stu-id="a504c-120">Only the first **ABSTRACT** element within the scope of another element is used when a metafile file is processed.</span></span> <span data-ttu-id="a504c-121">Tutti gli elementi **astratti** successivi in tale ambito vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="a504c-121">Any subsequent **ABSTRACT** elements in that scope are ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="a504c-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="a504c-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="a504c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a504c-123">Requirements</span></span>



| <span data-ttu-id="a504c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a504c-124">Requirement</span></span> | <span data-ttu-id="a504c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a504c-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="a504c-126">Versione</span><span class="sxs-lookup"><span data-stu-id="a504c-126">Version</span></span><br/> | <span data-ttu-id="a504c-127">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="a504c-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a504c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a504c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a504c-129">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a504c-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a504c-130">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a504c-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





