---
title: Attributo UserRating
description: L'attributo UserRating è la classificazione specificata dall'utente nella libreria.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Attributo UserRating Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324083"
---
# <a name="userrating-attribute"></a><span data-ttu-id="1cba7-104">Attributo UserRating</span><span class="sxs-lookup"><span data-stu-id="1cba7-104">UserRating Attribute</span></span>

<span data-ttu-id="1cba7-105">L'attributo **UserRating** è la classificazione specificata dall'utente nella libreria.</span><span class="sxs-lookup"><span data-stu-id="1cba7-105">The **UserRating** attribute is the rating specified by the user in the library.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1cba7-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="1cba7-106">Applies To</span></span>

-   [<span data-ttu-id="1cba7-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="1cba7-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1cba7-108">Altri elementi</span><span class="sxs-lookup"><span data-stu-id="1cba7-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="1cba7-109">Elementi foto</span><span class="sxs-lookup"><span data-stu-id="1cba7-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="1cba7-110">Playlist</span><span class="sxs-lookup"><span data-stu-id="1cba7-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="1cba7-111">Elementi video</span><span class="sxs-lookup"><span data-stu-id="1cba7-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1cba7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cba7-112">Remarks</span></span>

<span data-ttu-id="1cba7-113">Le classificazioni utente sono rappresentate da valori integer, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1cba7-113">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="1cba7-114">Quando si specifica un valore, usare uno dei valori della colonna valore di scrittura.</span><span class="sxs-lookup"><span data-stu-id="1cba7-114">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="1cba7-115">Quando si recuperano i valori, è possibile utilizzare gli intervalli nella colonna valori di lettura per determinare il numero di stelle.</span><span class="sxs-lookup"><span data-stu-id="1cba7-115">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="1cba7-116">Classificazione</span><span class="sxs-lookup"><span data-stu-id="1cba7-116">Rating</span></span>  | <span data-ttu-id="1cba7-117">Valore di scrittura</span><span class="sxs-lookup"><span data-stu-id="1cba7-117">Writing value</span></span> | <span data-ttu-id="1cba7-118">Lettura di valori</span><span class="sxs-lookup"><span data-stu-id="1cba7-118">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="1cba7-119">Senza classificazione</span><span class="sxs-lookup"><span data-stu-id="1cba7-119">Unrated</span></span> | <span data-ttu-id="1cba7-120">0</span><span class="sxs-lookup"><span data-stu-id="1cba7-120">0</span></span>             | <span data-ttu-id="1cba7-121">0</span><span class="sxs-lookup"><span data-stu-id="1cba7-121">0</span></span>              |
| <span data-ttu-id="1cba7-122">1 stella</span><span class="sxs-lookup"><span data-stu-id="1cba7-122">1 star</span></span>  | <span data-ttu-id="1cba7-123">1</span><span class="sxs-lookup"><span data-stu-id="1cba7-123">1</span></span>             | <span data-ttu-id="1cba7-124">Da 1 a 12</span><span class="sxs-lookup"><span data-stu-id="1cba7-124">1 to 12</span></span>        |
| <span data-ttu-id="1cba7-125">2 stelle</span><span class="sxs-lookup"><span data-stu-id="1cba7-125">2 stars</span></span> | <span data-ttu-id="1cba7-126">25</span><span class="sxs-lookup"><span data-stu-id="1cba7-126">25</span></span>            | <span data-ttu-id="1cba7-127">da 13 a 37</span><span class="sxs-lookup"><span data-stu-id="1cba7-127">13 to 37</span></span>       |
| <span data-ttu-id="1cba7-128">3 stelle</span><span class="sxs-lookup"><span data-stu-id="1cba7-128">3 stars</span></span> | <span data-ttu-id="1cba7-129">50</span><span class="sxs-lookup"><span data-stu-id="1cba7-129">50</span></span>            | <span data-ttu-id="1cba7-130">da 38 a 62</span><span class="sxs-lookup"><span data-stu-id="1cba7-130">38 to 62</span></span>       |
| <span data-ttu-id="1cba7-131">4 stelle</span><span class="sxs-lookup"><span data-stu-id="1cba7-131">4 stars</span></span> | <span data-ttu-id="1cba7-132">75</span><span class="sxs-lookup"><span data-stu-id="1cba7-132">75</span></span>            | <span data-ttu-id="1cba7-133">da 63 a 86</span><span class="sxs-lookup"><span data-stu-id="1cba7-133">63 to 86</span></span>       |
| <span data-ttu-id="1cba7-134">5 stelle</span><span class="sxs-lookup"><span data-stu-id="1cba7-134">5 stars</span></span> | <span data-ttu-id="1cba7-135">99</span><span class="sxs-lookup"><span data-stu-id="1cba7-135">99</span></span>            | <span data-ttu-id="1cba7-136">da 87 a 99</span><span class="sxs-lookup"><span data-stu-id="1cba7-136">87 to 99</span></span>       |



 

<span data-ttu-id="1cba7-137">Questo attributo viene archiviato solo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="1cba7-137">This attribute is stored only in the library.</span></span>

<span data-ttu-id="1cba7-138">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1cba7-138">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cba7-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cba7-139">Requirements</span></span>



| <span data-ttu-id="1cba7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cba7-140">Requirement</span></span> | <span data-ttu-id="1cba7-141">Valore</span><span class="sxs-lookup"><span data-stu-id="1cba7-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cba7-142">Versione</span><span class="sxs-lookup"><span data-stu-id="1cba7-142">Version</span></span><br/> | <span data-ttu-id="1cba7-143">Windows Media Player 9 Series o versione successiva (l'elemento Photo è supportato solo in Windows Media Player 10 o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="1cba7-143">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1cba7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cba7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cba7-145">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="1cba7-145">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





