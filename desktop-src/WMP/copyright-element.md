---
title: Elemento COPYRIGHT (msfeeds. h)
description: L'elemento COPYRIGHT definisce una stringa di testo che specifica le informazioni sul copyright per un elemento ASX o ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento COPYRIGHT Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330117"
---
# <a name="copyright-element"></a><span data-ttu-id="87b3b-104">COPYRIGHT (elemento)</span><span class="sxs-lookup"><span data-stu-id="87b3b-104">COPYRIGHT Element</span></span>

<span data-ttu-id="87b3b-105">L'elemento **Copyright** definisce una stringa di testo che specifica le informazioni sul copyright per un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="87b3b-105">The **COPYRIGHT** element defines a text string specifying the copyright information for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a><span data-ttu-id="87b3b-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="87b3b-106">Attributes</span></span>

<span data-ttu-id="87b3b-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="87b3b-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="87b3b-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="87b3b-108">Parent/Child Elements</span></span>



| <span data-ttu-id="87b3b-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="87b3b-109">Hierarchy</span></span>       | <span data-ttu-id="87b3b-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="87b3b-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="87b3b-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="87b3b-111">Parent elements</span></span> | <span data-ttu-id="87b3b-112">**ASX**, **voce**</span><span class="sxs-lookup"><span data-stu-id="87b3b-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="87b3b-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="87b3b-113">Child elements</span></span>  | <span data-ttu-id="87b3b-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="87b3b-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="87b3b-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="87b3b-115">Remarks</span></span>

<span data-ttu-id="87b3b-116">Questo elemento definisce una stringa di testo che specifica le informazioni sul copyright per un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="87b3b-116">This element defines a text string that specifies the copyright information for an **ASX** or **ENTRY** element.</span></span>

<span data-ttu-id="87b3b-117">Quando questo elemento viene visualizzato all'interno di un elemento **ASX** , la stringa di copyright viene visualizzata solo come **Mostra** informazioni.</span><span class="sxs-lookup"><span data-stu-id="87b3b-117">When this element appears within an **ASX** element, the copyright string is displayed only as **Show** information.</span></span> <span data-ttu-id="87b3b-118">Quando questo elemento viene visualizzato all'interno di un elemento **entry** , il testo viene visualizzato come informazioni di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="87b3b-118">When this element appears within an **ENTRY** element, the text is displayed as clip information.</span></span> <span data-ttu-id="87b3b-119">Ogni elemento **ASX** e **entry** padre deve contenere al massimo un elemento **Copyright** figlio.</span><span class="sxs-lookup"><span data-stu-id="87b3b-119">Each parent **ASX** and **ENTRY** element should contain at most one child **COPYRIGHT** element.</span></span> <span data-ttu-id="87b3b-120">Più elementi di **Copyright** dopo il primo verranno ignorati e non verranno visualizzati.</span><span class="sxs-lookup"><span data-stu-id="87b3b-120">Multiple **COPYRIGHT** elements after the first will be ignored and will not be displayed.</span></span>

<span data-ttu-id="87b3b-121">I caratteri per il copyright e i simboli di registrazione dei marchi (o) potrebbero non essere visualizzati correttamente se il metafile non è codificato con lo schema di codifica UTF-8.</span><span class="sxs-lookup"><span data-stu-id="87b3b-121">The characters for copyright and trademark registration symbols (   or   ) may not display properly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="87b3b-122">In questo caso, per visualizzare correttamente uno di questi simboli per tutti gli utenti, è invece possibile usare gli equivalenti ASCII (c) e (R).</span><span class="sxs-lookup"><span data-stu-id="87b3b-122">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (R) instead.</span></span>

<span data-ttu-id="87b3b-123">Se il metafile è codificato con UTF-8, i simboli del copyright e dei marchi vengono visualizzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="87b3b-123">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="87b3b-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="87b3b-124">Examples</span></span>


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a><span data-ttu-id="87b3b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87b3b-125">Requirements</span></span>



| <span data-ttu-id="87b3b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="87b3b-126">Requirement</span></span> | <span data-ttu-id="87b3b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="87b3b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87b3b-128">Versione</span><span class="sxs-lookup"><span data-stu-id="87b3b-128">Version</span></span><br/> | <span data-ttu-id="87b3b-129">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="87b3b-129">Windows Media Player version 7.0 or later</span></span><br/>                                 |
| <span data-ttu-id="87b3b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87b3b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="87b3b-131"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="87b3b-131"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87b3b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87b3b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b3b-133">**Aggiunta di caratteri di copyright a metafile**</span><span class="sxs-lookup"><span data-stu-id="87b3b-133">**Adding Copyright Characters to Metafiles**</span></span>](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[<span data-ttu-id="87b3b-134">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="87b3b-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="87b3b-135">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="87b3b-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





