---
title: Elemento PREVIEWDURATION
description: L'elemento PREVIEWDURATION definisce l'intervallo di tempo in cui una clip viene riprodotta in modalità di anteprima.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Finestra elementi PREVIEWDURATION Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325991"
---
# <a name="previewduration-element"></a><span data-ttu-id="1af90-104">Elemento PREVIEWDURATION</span><span class="sxs-lookup"><span data-stu-id="1af90-104">PREVIEWDURATION Element</span></span>

<span data-ttu-id="1af90-105">L'elemento **PREVIEWDURATION** definisce l'intervallo di tempo in cui una clip viene riprodotta in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="1af90-105">The **PREVIEWDURATION** element defines the length of time a clip plays in preview mode.</span></span>

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="1af90-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="1af90-106">Attributes</span></span>

<span data-ttu-id="1af90-107">**Valore** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="1af90-107">**VALUE** (required)</span></span>

<span data-ttu-id="1af90-108">Periodo di tempo (in ore, minuti, secondi e centesimi di secondo) in cui il clip viene riprodotto in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="1af90-108">Length of time (in hours, minutes, seconds, and hundredths of a second) that the clip plays in preview mode.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="1af90-109">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="1af90-109">Parent/Child Elements</span></span>



| <span data-ttu-id="1af90-110">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="1af90-110">Hierarchy</span></span>       | <span data-ttu-id="1af90-111">Elementi</span><span class="sxs-lookup"><span data-stu-id="1af90-111">Elements</span></span>                    |
|-----------------|-----------------------------|
| <span data-ttu-id="1af90-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="1af90-112">Parent elements</span></span> | <span data-ttu-id="1af90-113">**ASX**, **entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="1af90-113">**ASX**, **ENTRY**, **REF**</span></span> |
| <span data-ttu-id="1af90-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1af90-114">Child elements</span></span>  | <span data-ttu-id="1af90-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="1af90-115">None</span></span>                        |



 

## <a name="remarks"></a><span data-ttu-id="1af90-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1af90-116">Remarks</span></span>

<span data-ttu-id="1af90-117">Questo elemento definisce l'intervallo di tempo in cui una clip viene riprodotta in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="1af90-117">This element defines the length of time that a clip plays in preview mode.</span></span> <span data-ttu-id="1af90-118">Se questo elemento viene visualizzato all'interno di un elemento **entry** o di un elemento **ref** , si applica alla clip definita da tale elemento.</span><span class="sxs-lookup"><span data-stu-id="1af90-118">If this element appears within an **ENTRY** element or a **REF** element, it applies to the clip defined by that element.</span></span> <span data-ttu-id="1af90-119">Se viene visualizzato all'interno dell'ambito di un elemento **ASX** , viene applicato a ogni clip del metafile.</span><span class="sxs-lookup"><span data-stu-id="1af90-119">If it appears within the scope of an **ASX** element, it applies to every clip in the metafile.</span></span> <span data-ttu-id="1af90-120">Un elemento **PREVIEWDURATION** in un elemento **ref** ha la precedenza su uno in un **elemento** entry e ha la precedenza su un elemento **PREVIEWDURATION** in un elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="1af90-120">A **PREVIEWDURATION** element in a **REF** element takes precedence over one in an ENTRY **element**, and either takes precedence over a **PREVIEWDURATION** element in an **ASX** element.</span></span> <span data-ttu-id="1af90-121">Se per una clip non è definito alcun elemento **PREVIEWDURATION** , il tempo di anteprima predefinito è di 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="1af90-121">If no **PREVIEWDURATION** element is defined for a clip, the default preview time is 10 seconds.</span></span>

<span data-ttu-id="1af90-122">Se è presente un elemento **StartTime** o **STARTMARKER** per il clip, Windows Media Player esegue il rendering della clip a partire dal punto definito da uno di questi elementi. in caso contrario, viene eseguito il rendering dall'inizio della clip.</span><span class="sxs-lookup"><span data-stu-id="1af90-122">If there is a **STARTTIME** or **STARTMARKER** element for the clip, Windows Media Player renders the clip starting at the point defined by one of these elements; otherwise it renders from the beginning of the clip.</span></span> <span data-ttu-id="1af90-123">Il clip si interrompe normalmente se è più breve del tempo definito dall'elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="1af90-123">The clip stops normally if it is shorter than the time defined by the **PREVIEWDURATION** element.</span></span>

<span data-ttu-id="1af90-124">L'elemento **Duration** esegue l'override di un elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="1af90-124">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="1af90-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="1af90-125">Examples</span></span>


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="1af90-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1af90-126">Requirements</span></span>



| <span data-ttu-id="1af90-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af90-127">Requirement</span></span> | <span data-ttu-id="1af90-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1af90-128">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="1af90-129">Versione</span><span class="sxs-lookup"><span data-stu-id="1af90-129">Version</span></span><br/> | <span data-ttu-id="1af90-130">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="1af90-130">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1af90-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af90-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af90-132">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1af90-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="1af90-133">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1af90-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





