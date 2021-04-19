---
title: Attributo UserEffectiveRating
description: L'attributo UserEffectiveRating è la classificazione calcolata da Windows Media Player in base alla frequenza con cui l'elemento è stato riprodotto.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Attributo UserEffectiveRating Windows Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325983"
---
# <a name="usereffectiverating-attribute"></a><span data-ttu-id="df749-104">Attributo UserEffectiveRating</span><span class="sxs-lookup"><span data-stu-id="df749-104">UserEffectiveRating Attribute</span></span>

<span data-ttu-id="df749-105">L'attributo **UserEffectiveRating** è la classificazione calcolata da Windows Media Player in base alla frequenza con cui l'elemento è stato riprodotto.</span><span class="sxs-lookup"><span data-stu-id="df749-105">The **UserEffectiveRating** attribute is the rating computed by Windows Media Player based on how often the item has been played.</span></span>

## <a name="applies-to"></a><span data-ttu-id="df749-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="df749-106">Applies To</span></span>

-   [<span data-ttu-id="df749-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="df749-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="df749-108">Altri elementi</span><span class="sxs-lookup"><span data-stu-id="df749-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="df749-109">Playlist</span><span class="sxs-lookup"><span data-stu-id="df749-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="df749-110">Elementi video</span><span class="sxs-lookup"><span data-stu-id="df749-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="df749-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="df749-111">Remarks</span></span>

<span data-ttu-id="df749-112">Le classificazioni utente sono rappresentate da valori integer, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="df749-112">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="df749-113">Quando si specifica un valore, usare uno dei valori della colonna valore di scrittura.</span><span class="sxs-lookup"><span data-stu-id="df749-113">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="df749-114">Quando si recuperano i valori, è possibile utilizzare gli intervalli nella colonna valori di lettura per determinare il numero di stelle.</span><span class="sxs-lookup"><span data-stu-id="df749-114">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="df749-115">Classificazione</span><span class="sxs-lookup"><span data-stu-id="df749-115">Rating</span></span>  | <span data-ttu-id="df749-116">Valore di scrittura</span><span class="sxs-lookup"><span data-stu-id="df749-116">Writing value</span></span> | <span data-ttu-id="df749-117">Lettura di valori</span><span class="sxs-lookup"><span data-stu-id="df749-117">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="df749-118">Senza classificazione</span><span class="sxs-lookup"><span data-stu-id="df749-118">Unrated</span></span> | <span data-ttu-id="df749-119">0</span><span class="sxs-lookup"><span data-stu-id="df749-119">0</span></span>             | <span data-ttu-id="df749-120">0</span><span class="sxs-lookup"><span data-stu-id="df749-120">0</span></span>              |
| <span data-ttu-id="df749-121">1 stella</span><span class="sxs-lookup"><span data-stu-id="df749-121">1 star</span></span>  | <span data-ttu-id="df749-122">1</span><span class="sxs-lookup"><span data-stu-id="df749-122">1</span></span>             | <span data-ttu-id="df749-123">Da 1 a 12</span><span class="sxs-lookup"><span data-stu-id="df749-123">1 to 12</span></span>        |
| <span data-ttu-id="df749-124">2 stelle</span><span class="sxs-lookup"><span data-stu-id="df749-124">2 stars</span></span> | <span data-ttu-id="df749-125">25</span><span class="sxs-lookup"><span data-stu-id="df749-125">25</span></span>            | <span data-ttu-id="df749-126">da 13 a 37</span><span class="sxs-lookup"><span data-stu-id="df749-126">13 to 37</span></span>       |
| <span data-ttu-id="df749-127">3 stelle</span><span class="sxs-lookup"><span data-stu-id="df749-127">3 stars</span></span> | <span data-ttu-id="df749-128">50</span><span class="sxs-lookup"><span data-stu-id="df749-128">50</span></span>            | <span data-ttu-id="df749-129">da 38 a 62</span><span class="sxs-lookup"><span data-stu-id="df749-129">38 to 62</span></span>       |
| <span data-ttu-id="df749-130">4 stelle</span><span class="sxs-lookup"><span data-stu-id="df749-130">4 stars</span></span> | <span data-ttu-id="df749-131">75</span><span class="sxs-lookup"><span data-stu-id="df749-131">75</span></span>            | <span data-ttu-id="df749-132">da 63 a 86</span><span class="sxs-lookup"><span data-stu-id="df749-132">63 to 86</span></span>       |
| <span data-ttu-id="df749-133">5 stelle</span><span class="sxs-lookup"><span data-stu-id="df749-133">5 stars</span></span> | <span data-ttu-id="df749-134">99</span><span class="sxs-lookup"><span data-stu-id="df749-134">99</span></span>            | <span data-ttu-id="df749-135">da 87 a 99</span><span class="sxs-lookup"><span data-stu-id="df749-135">87 to 99</span></span>       |



 

<span data-ttu-id="df749-136">Questo attributo viene archiviato solo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="df749-136">This attribute is stored only in the library.</span></span>

<span data-ttu-id="df749-137">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="df749-137">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df749-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df749-138">Requirements</span></span>



| <span data-ttu-id="df749-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="df749-139">Requirement</span></span> | <span data-ttu-id="df749-140">Valore</span><span class="sxs-lookup"><span data-stu-id="df749-140">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="df749-141">Versione</span><span class="sxs-lookup"><span data-stu-id="df749-141">Version</span></span><br/> | <span data-ttu-id="df749-142">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="df749-142">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df749-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df749-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df749-144">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="df749-144">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





