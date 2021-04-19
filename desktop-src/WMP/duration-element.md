---
title: DURATION-elemento
description: L'elemento DURATION definisce l'intervallo di tempo in cui Windows Media Player eseguirà il rendering della voce della playlist associata.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Finestra di Media Player elemento DURATION
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331746"
---
# <a name="duration-element"></a><span data-ttu-id="4f5d1-104">DURATION-elemento</span><span class="sxs-lookup"><span data-stu-id="4f5d1-104">DURATION Element</span></span>

<span data-ttu-id="4f5d1-105">L'elemento **Duration** definisce l'intervallo di tempo in cui Windows Media Player eseguirà il rendering della voce della playlist associata.</span><span class="sxs-lookup"><span data-stu-id="4f5d1-105">The **DURATION** element defines the length of time Windows Media Player will render the associated playlist entry.</span></span>

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="4f5d1-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="4f5d1-106">Attributes</span></span>

<span data-ttu-id="4f5d1-107">**Valore** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="4f5d1-107">**VALUE** (required)</span></span>

<span data-ttu-id="4f5d1-108">Periodo di tempo, in ore, minuti, secondi e centesimi di secondo, in base al quale viene eseguito il rendering di una voce da parte di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4f5d1-108">The length of time, in hours, minutes, seconds, and hundredths of a second, that an entry is rendered by Windows Media Player.</span></span> <span data-ttu-id="4f5d1-109">Il valore predefinito è l'intera lunghezza della voce.</span><span class="sxs-lookup"><span data-stu-id="4f5d1-109">The default value is the entire length of the entry.</span></span> <span data-ttu-id="4f5d1-110">Se la voce è un file grafico, è necessario specificare un valore Duration.</span><span class="sxs-lookup"><span data-stu-id="4f5d1-110">If the entry is a graphic file, a duration value must be specified.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="4f5d1-111">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="4f5d1-111">Parent/Child Elements</span></span>



| <span data-ttu-id="4f5d1-112">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="4f5d1-112">Hierarchy</span></span>       | <span data-ttu-id="4f5d1-113">Elementi</span><span class="sxs-lookup"><span data-stu-id="4f5d1-113">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="4f5d1-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="4f5d1-114">Parent elements</span></span> | <span data-ttu-id="4f5d1-115">**voce**, **ref**</span><span class="sxs-lookup"><span data-stu-id="4f5d1-115">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="4f5d1-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4f5d1-116">Child elements</span></span>  | <span data-ttu-id="4f5d1-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="4f5d1-117">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="4f5d1-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="4f5d1-118">Remarks</span></span>

<span data-ttu-id="4f5d1-119">Questo elemento definisce l'intervallo di tempo in cui deve essere eseguito il rendering di un flusso.</span><span class="sxs-lookup"><span data-stu-id="4f5d1-119">This element defines the length of time a stream is to be rendered.</span></span> <span data-ttu-id="4f5d1-120">Se l'attributo **value** supera la lunghezza del flusso di contenuto, il flusso termina in corrispondenza del normale endpoint.</span><span class="sxs-lookup"><span data-stu-id="4f5d1-120">If the **VALUE** attribute exceeds the length of the content stream, the stream terminates at its normal end-point.</span></span>

<span data-ttu-id="4f5d1-121">Questo elemento può essere presente all'interno di un elemento **ref** o all'interno di un elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="4f5d1-121">This element can appear either within a **REF** element or within an **ENTRY** element.</span></span> <span data-ttu-id="4f5d1-122">Tuttavia, un elemento **Duration** definito all'interno di un elemento **ref** esegue l'override di uno che viene visualizzato all'interno dell'elemento **entry** padre dell'elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="4f5d1-122">However, a **DURATION** element defined within a **REF** element overrides one that appears within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="4f5d1-123">L'elemento **Duration** esegue l'override di un elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="4f5d1-123">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="4f5d1-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="4f5d1-124">Examples</span></span>


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a><span data-ttu-id="4f5d1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f5d1-125">Requirements</span></span>



| <span data-ttu-id="4f5d1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f5d1-126">Requirement</span></span> | <span data-ttu-id="4f5d1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4f5d1-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4f5d1-128">Versione</span><span class="sxs-lookup"><span data-stu-id="4f5d1-128">Version</span></span><br/> | <span data-ttu-id="4f5d1-129">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="4f5d1-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f5d1-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f5d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5d1-131">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4f5d1-131">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4f5d1-132">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4f5d1-132">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





