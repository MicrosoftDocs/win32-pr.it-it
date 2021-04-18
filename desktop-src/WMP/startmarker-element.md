---
title: Elemento STARTMARKER
description: L'elemento STARTMARKER specifica un marcatore dal quale Windows Media Player avvierà il rendering del flusso.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Finestra elementi STARTMARKER Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331734"
---
# <a name="startmarker-element"></a><span data-ttu-id="5ab0c-104">Elemento STARTMARKER</span><span class="sxs-lookup"><span data-stu-id="5ab0c-104">STARTMARKER Element</span></span>

<span data-ttu-id="5ab0c-105">L'elemento **STARTMARKER** specifica un marcatore dal quale Windows Media Player avvierà il rendering del flusso.</span><span class="sxs-lookup"><span data-stu-id="5ab0c-105">The **STARTMARKER** element specifies a marker from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="5ab0c-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="5ab0c-106">Attributes</span></span>

<span data-ttu-id="5ab0c-107">**NUMERO**</span><span class="sxs-lookup"><span data-stu-id="5ab0c-107">**NUMBER**</span></span>

<span data-ttu-id="5ab0c-108">Numero di un marcatore numerico nell'indice.</span><span class="sxs-lookup"><span data-stu-id="5ab0c-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="5ab0c-109">Il valore predefinito è l'inizio del contenuto su richiesta o la posizione corrente in un flusso in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="5ab0c-109">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

<span data-ttu-id="5ab0c-110">**NOME**</span><span class="sxs-lookup"><span data-stu-id="5ab0c-110">**NAME**</span></span>

<span data-ttu-id="5ab0c-111">Nome di un marcatore denominato nell'indice.</span><span class="sxs-lookup"><span data-stu-id="5ab0c-111">The name of a named marker in the index.</span></span> <span data-ttu-id="5ab0c-112">Il valore predefinito è l'inizio del contenuto su richiesta o la posizione corrente in un flusso in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="5ab0c-112">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="5ab0c-113">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="5ab0c-113">Parent/Child Elements</span></span>



| <span data-ttu-id="5ab0c-114">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="5ab0c-114">Hierarchy</span></span>       | <span data-ttu-id="5ab0c-115">Elementi</span><span class="sxs-lookup"><span data-stu-id="5ab0c-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="5ab0c-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5ab0c-116">Parent elements</span></span> | <span data-ttu-id="5ab0c-117">**voce**, **ref**</span><span class="sxs-lookup"><span data-stu-id="5ab0c-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="5ab0c-118">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5ab0c-118">Child elements</span></span>  | <span data-ttu-id="5ab0c-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="5ab0c-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="5ab0c-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="5ab0c-120">Remarks</span></span>

<span data-ttu-id="5ab0c-121">Questo elemento specifica il marcatore da cui Windows Media Player deve avviare il rendering del flusso definito nella **voce** padre o nell'elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="5ab0c-121">This element specifies the marker from which Windows Media Player is to start rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="5ab0c-122">**Nota**</span><span class="sxs-lookup"><span data-stu-id="5ab0c-122">**Note**</span></span>

<span data-ttu-id="5ab0c-123">Usare questo elemento con l'attributo **Number** o **Name** , ma non con entrambi.</span><span class="sxs-lookup"><span data-stu-id="5ab0c-123">Use this element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="5ab0c-124">Un elemento **STARTMARKER** definito all'interno di un elemento **ref** ha la precedenza su un elemento **STARTMARKER** definito all'interno dell'elemento **entry** padre dell'elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="5ab0c-124">A **STARTMARKER** element defined within a **REF** element takes precedence over a **STARTMARKER** element defined within the **REF** element's parent **ENTRY** element.</span></span> <span data-ttu-id="5ab0c-125">Un elemento **STARTMARKER** ha anche la precedenza su un elemento **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="5ab0c-125">A **STARTMARKER** element also takes precedence over a **STARTTIME** element.</span></span>

<span data-ttu-id="5ab0c-126">Se il marcatore specificato da un elemento **STARTMARKER** si trova in un secondo momento nel flusso rispetto al marcatore definito da un elemento **ENDMARKER** , nessun contenuto viene riprodotto, ma non viene generato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="5ab0c-126">If the marker specified by a **STARTMARKER** element occurs later in the stream than the marker defined by an **ENDMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="5ab0c-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="5ab0c-127">Examples</span></span>


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a><span data-ttu-id="5ab0c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ab0c-128">Requirements</span></span>



| <span data-ttu-id="5ab0c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ab0c-129">Requirement</span></span> | <span data-ttu-id="5ab0c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5ab0c-130">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="5ab0c-131">Versione</span><span class="sxs-lookup"><span data-stu-id="5ab0c-131">Version</span></span><br/> | <span data-ttu-id="5ab0c-132">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="5ab0c-132">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ab0c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ab0c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab0c-134">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5ab0c-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="5ab0c-135">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5ab0c-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





