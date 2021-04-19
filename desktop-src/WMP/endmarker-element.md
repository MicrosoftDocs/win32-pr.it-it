---
title: Elemento ENDMARKER
description: L'elemento ENDMARKER specifica un marcatore in corrispondenza del quale Windows Media Player arresterà il rendering del flusso.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Finestra elementi ENDMARKER Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333247"
---
# <a name="endmarker-element"></a><span data-ttu-id="14d24-104">Elemento ENDMARKER</span><span class="sxs-lookup"><span data-stu-id="14d24-104">ENDMARKER Element</span></span>

<span data-ttu-id="14d24-105">L'elemento **ENDMARKER** specifica un marcatore in corrispondenza del quale Windows Media Player arresterà il rendering del flusso.</span><span class="sxs-lookup"><span data-stu-id="14d24-105">The **ENDMARKER** element specifies a marker at which Windows Media Player will stop rendering the stream.</span></span>

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="14d24-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="14d24-106">Attributes</span></span>

<span data-ttu-id="14d24-107">**NUMERO**</span><span class="sxs-lookup"><span data-stu-id="14d24-107">**NUMBER**</span></span>

<span data-ttu-id="14d24-108">Numero di un marcatore numerico nell'indice.</span><span class="sxs-lookup"><span data-stu-id="14d24-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="14d24-109">Il valore predefinito è la fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="14d24-109">The default value is the end of the content.</span></span>

<span data-ttu-id="14d24-110">**NOME**</span><span class="sxs-lookup"><span data-stu-id="14d24-110">**NAME**</span></span>

<span data-ttu-id="14d24-111">Nome di un marcatore denominato nell'indice.</span><span class="sxs-lookup"><span data-stu-id="14d24-111">The name of a named marker in the index.</span></span> <span data-ttu-id="14d24-112">Il valore predefinito è la fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="14d24-112">The default value is the end of the content.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="14d24-113">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="14d24-113">Parent/Child Elements</span></span>



| <span data-ttu-id="14d24-114">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="14d24-114">Hierarchy</span></span>       | <span data-ttu-id="14d24-115">Elementi</span><span class="sxs-lookup"><span data-stu-id="14d24-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="14d24-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="14d24-116">Parent elements</span></span> | <span data-ttu-id="14d24-117">**voce**, **ref**</span><span class="sxs-lookup"><span data-stu-id="14d24-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="14d24-118">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="14d24-118">Child elements</span></span>  | <span data-ttu-id="14d24-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="14d24-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="14d24-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="14d24-120">Remarks</span></span>

<span data-ttu-id="14d24-121">Questo elemento specifica il marcatore in cui Windows Media Player sta per arrestare il rendering del flusso definito nella **voce** padre o nell'elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="14d24-121">This element specifies the marker where Windows Media Player is to stop rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="14d24-122">Nota</span><span class="sxs-lookup"><span data-stu-id="14d24-122">Note</span></span>

<span data-ttu-id="14d24-123">Usare l'elemento **ENDMARKER** con l'attributo **Number** o **Name** , ma non con entrambi.</span><span class="sxs-lookup"><span data-stu-id="14d24-123">Use the **ENDMARKER** element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="14d24-124">In modalità di anteprima, il raggiungimento di un marcatore finale interrompe l'anteprima, anche se non è trascorso il tempo specificato dall'elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="14d24-124">In preview mode, reaching an end marker stops the preview, even if the time specified by the **PREVIEWDURATION** element has not elapsed.</span></span> <span data-ttu-id="14d24-125">L'elemento **ENDMARKER** ha anche la precedenza sull'elemento **Duration** .</span><span class="sxs-lookup"><span data-stu-id="14d24-125">The **ENDMARKER** element also takes precedence over the **DURATION** element.</span></span>

<span data-ttu-id="14d24-126">Un elemento **ENDMARKER** definito all'interno di un elemento **ref** ha la precedenza su un **ENDMARKER** definito all'interno dell'elemento **entry** padre dell'elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="14d24-126">An **ENDMARKER** element defined within a **REF** element takes precedence over an **ENDMARKER** defined within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="14d24-127">Se il marcatore specificato da un elemento **ENDMARKER** si verifica in precedenza nel flusso rispetto al marcatore definito da un elemento **STARTMARKER** , nessun contenuto viene riprodotto, ma non viene generato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="14d24-127">If the marker specified by an **ENDMARKER** element occurs earlier in the stream than the marker defined by a **STARTMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="14d24-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="14d24-128">Examples</span></span>


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

```



## <a name="requirements"></a><span data-ttu-id="14d24-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14d24-129">Requirements</span></span>



| <span data-ttu-id="14d24-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d24-130">Requirement</span></span> | <span data-ttu-id="14d24-131">Valore</span><span class="sxs-lookup"><span data-stu-id="14d24-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="14d24-132">Versione</span><span class="sxs-lookup"><span data-stu-id="14d24-132">Version</span></span><br/> | <span data-ttu-id="14d24-133">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="14d24-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14d24-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14d24-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d24-135">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="14d24-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="14d24-136">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="14d24-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





