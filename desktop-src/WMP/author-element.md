---
title: Elemento AUTHOR
description: L'elemento AUTHOR contiene il nome dell'autore di un metafile di Windows Media o di un clip multimediale.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Elemento AUTHOR Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325267"
---
# <a name="author-element"></a><span data-ttu-id="a374f-104">Elemento AUTHOR</span><span class="sxs-lookup"><span data-stu-id="a374f-104">AUTHOR Element</span></span>

<span data-ttu-id="a374f-105">L'elemento **Author** contiene il nome dell'autore di un metafile di Windows Media o di un clip multimediale.</span><span class="sxs-lookup"><span data-stu-id="a374f-105">The **AUTHOR** element contains the name of the author of a Windows Media metafile or media clip.</span></span>

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a><span data-ttu-id="a374f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="a374f-106">Attributes</span></span>

<span data-ttu-id="a374f-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="a374f-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="a374f-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="a374f-108">Parent/Child Elements</span></span>



| <span data-ttu-id="a374f-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="a374f-109">Hierarchy</span></span>       | <span data-ttu-id="a374f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a374f-110">Element</span></span>            |
|-----------------|--------------------|
| <span data-ttu-id="a374f-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a374f-111">Parent elements</span></span> | <span data-ttu-id="a374f-112">**ASX**, **voce**</span><span class="sxs-lookup"><span data-stu-id="a374f-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="a374f-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a374f-113">Child elements</span></span>  | <span data-ttu-id="a374f-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="a374f-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="a374f-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a374f-115">Remarks</span></span>

<span data-ttu-id="a374f-116">Questo elemento contiene una stringa di testo che rappresenta il nome dell'autore di un metafile Windows Media o di un clip multimediale.</span><span class="sxs-lookup"><span data-stu-id="a374f-116">This element contains a text string representing the name of the author of a Windows Media metafile or media clip.</span></span> <span data-ttu-id="a374f-117">È possibile utilizzare l'elemento **Author** all'interno dell'elemento **ASX** e negli elementi **entry** .</span><span class="sxs-lookup"><span data-stu-id="a374f-117">You can use the **AUTHOR** element within the **ASX** element and within **ENTRY** elements.</span></span>

<span data-ttu-id="a374f-118">Se questo elemento viene visualizzato nell'elemento **ASX** , il testo viene visualizzato come **Mostra** informazioni.</span><span class="sxs-lookup"><span data-stu-id="a374f-118">If this element appears in the **ASX** element, the text is displayed as **Show** information.</span></span>

<span data-ttu-id="a374f-119">Se questo elemento viene visualizzato in un elemento **entry** , il testo viene visualizzato come autore della clip.</span><span class="sxs-lookup"><span data-stu-id="a374f-119">If this element appears in an **ENTRY** element, the text is displayed as the clip author.</span></span>

<span data-ttu-id="a374f-120">Ogni elemento **ASX** e **entry** padre deve contenere al massimo un elemento **autore** figlio.</span><span class="sxs-lookup"><span data-stu-id="a374f-120">Each parent **ASX** and **ENTRY** element should contain at most one child **AUTHOR** element.</span></span> <span data-ttu-id="a374f-121">Più elementi **Author** dopo il primo verranno ignorati e non verranno visualizzati.</span><span class="sxs-lookup"><span data-stu-id="a374f-121">Multiple **AUTHOR** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="a374f-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="a374f-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="a374f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a374f-123">Requirements</span></span>



| <span data-ttu-id="a374f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a374f-124">Requirement</span></span> | <span data-ttu-id="a374f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a374f-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="a374f-126">Versione</span><span class="sxs-lookup"><span data-stu-id="a374f-126">Version</span></span><br/> | <span data-ttu-id="a374f-127">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="a374f-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a374f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a374f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a374f-129">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a374f-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a374f-130">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a374f-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





