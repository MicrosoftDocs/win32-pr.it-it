---
title: Evento Player.StringCollectionChange
description: L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe. | Evento Player.StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Evento StringCollectionChange Windows Media Player
- Evento StringCollectionChange Windows Media Player , classe Player
- Classe Player Windows Media Player, evento StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a61b8e1e09e749579f323d506371138b0d9b59
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424091"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="b8168-107">Evento Player.StringCollectionChange</span><span class="sxs-lookup"><span data-stu-id="b8168-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="b8168-108">L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="b8168-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8168-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8168-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="b8168-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8168-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8168-111">*pdispStringCollection*</span><span class="sxs-lookup"><span data-stu-id="b8168-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="b8168-112">**Oggetto StringCollection** modificato.</span><span class="sxs-lookup"><span data-stu-id="b8168-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="b8168-113">*change*</span><span class="sxs-lookup"><span data-stu-id="b8168-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="b8168-114">Numero (long) che indica il tipo di modifica apportata alla raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="b8168-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="b8168-115">Include uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8168-115">Includes one of the following values.</span></span>



| <span data-ttu-id="b8168-116">Number</span><span class="sxs-lookup"><span data-stu-id="b8168-116">Number</span></span> | <span data-ttu-id="b8168-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8168-117">Description</span></span>                        |
|--------|------------------------------------|
| <span data-ttu-id="b8168-118">0</span><span class="sxs-lookup"><span data-stu-id="b8168-118">0</span></span>      | <span data-ttu-id="b8168-119">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b8168-119">Unknown.</span></span> <span data-ttu-id="b8168-120">(Non è un valore valido)</span><span class="sxs-lookup"><span data-stu-id="b8168-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="b8168-121">1</span><span class="sxs-lookup"><span data-stu-id="b8168-121">1</span></span>      | <span data-ttu-id="b8168-122">È stato inserito un elemento.</span><span class="sxs-lookup"><span data-stu-id="b8168-122">An item was inserted.</span></span>              |
| <span data-ttu-id="b8168-123">2</span><span class="sxs-lookup"><span data-stu-id="b8168-123">2</span></span>      | <span data-ttu-id="b8168-124">La raccolta di stringhe è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b8168-124">The string collection changed.</span></span>     |
| <span data-ttu-id="b8168-125">3</span><span class="sxs-lookup"><span data-stu-id="b8168-125">3</span></span>      | <span data-ttu-id="b8168-126">Un elemento è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="b8168-126">An item was deleted.</span></span>               |
| <span data-ttu-id="b8168-127">4</span><span class="sxs-lookup"><span data-stu-id="b8168-127">4</span></span>      | <span data-ttu-id="b8168-128">La raccolta di stringhe è stata cancellata.</span><span class="sxs-lookup"><span data-stu-id="b8168-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="b8168-129">5</span><span class="sxs-lookup"><span data-stu-id="b8168-129">5</span></span>      | <span data-ttu-id="b8168-130">Sono in corso gli aggiornamenti in blocco.</span><span class="sxs-lookup"><span data-stu-id="b8168-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="b8168-131">6</span><span class="sxs-lookup"><span data-stu-id="b8168-131">6</span></span>      | <span data-ttu-id="b8168-132">Gli aggiornamenti in blocco sono terminati.</span><span class="sxs-lookup"><span data-stu-id="b8168-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="b8168-133">*lCollectionIndex*</span><span class="sxs-lookup"><span data-stu-id="b8168-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="b8168-134">Numero (long) contenente l'indice dell'elemento della raccolta di stringhe modificato.</span><span class="sxs-lookup"><span data-stu-id="b8168-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8168-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8168-135">Return value</span></span>

<span data-ttu-id="b8168-136">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b8168-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8168-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8168-137">Remarks</span></span>

<span data-ttu-id="b8168-138">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b8168-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8168-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8168-139">Requirements</span></span>



| <span data-ttu-id="b8168-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8168-140">Requirement</span></span> | <span data-ttu-id="b8168-141">Valore</span><span class="sxs-lookup"><span data-stu-id="b8168-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8168-142">Versione</span><span class="sxs-lookup"><span data-stu-id="b8168-142">Version</span></span><br/> | <span data-ttu-id="b8168-143">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b8168-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="b8168-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b8168-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8168-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8168-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8168-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8168-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8168-147">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="b8168-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="b8168-148">**Oggetto StringCollection**</span><span class="sxs-lookup"><span data-stu-id="b8168-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





