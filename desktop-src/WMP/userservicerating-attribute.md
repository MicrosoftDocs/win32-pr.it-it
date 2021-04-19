---
title: Attributo UserServiceRating
description: L'attributo UserServiceRating è riservato per un utilizzo futuro.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Attributo UserServiceRating Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324081"
---
# <a name="userservicerating-attribute"></a><span data-ttu-id="07eb8-104">Attributo UserServiceRating</span><span class="sxs-lookup"><span data-stu-id="07eb8-104">UserServiceRating Attribute</span></span>

<span data-ttu-id="07eb8-105">L'attributo **UserServiceRating** è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="07eb8-105">The **UserServiceRating** attribute is reserved for future use.</span></span>

## <a name="applies-to"></a><span data-ttu-id="07eb8-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="07eb8-106">Applies To</span></span>

-   [<span data-ttu-id="07eb8-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="07eb8-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="07eb8-108">Playlist</span><span class="sxs-lookup"><span data-stu-id="07eb8-108">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="07eb8-109">Elementi video</span><span class="sxs-lookup"><span data-stu-id="07eb8-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="07eb8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="07eb8-110">Remarks</span></span>

<span data-ttu-id="07eb8-111">Le classificazioni utente sono rappresentate da valori integer, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="07eb8-111">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="07eb8-112">Quando si specifica un valore, usare uno dei valori della colonna valore di scrittura.</span><span class="sxs-lookup"><span data-stu-id="07eb8-112">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="07eb8-113">Quando si recuperano i valori, è possibile utilizzare gli intervalli nella colonna valori di lettura per determinare il numero di stelle.</span><span class="sxs-lookup"><span data-stu-id="07eb8-113">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="07eb8-114">Classificazione</span><span class="sxs-lookup"><span data-stu-id="07eb8-114">Rating</span></span>  | <span data-ttu-id="07eb8-115">Valore di scrittura</span><span class="sxs-lookup"><span data-stu-id="07eb8-115">Writing value</span></span> | <span data-ttu-id="07eb8-116">Lettura di valori</span><span class="sxs-lookup"><span data-stu-id="07eb8-116">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="07eb8-117">Senza classificazione</span><span class="sxs-lookup"><span data-stu-id="07eb8-117">Unrated</span></span> | <span data-ttu-id="07eb8-118">0</span><span class="sxs-lookup"><span data-stu-id="07eb8-118">0</span></span>             | <span data-ttu-id="07eb8-119">0</span><span class="sxs-lookup"><span data-stu-id="07eb8-119">0</span></span>              |
| <span data-ttu-id="07eb8-120">1 stella</span><span class="sxs-lookup"><span data-stu-id="07eb8-120">1 star</span></span>  | <span data-ttu-id="07eb8-121">1</span><span class="sxs-lookup"><span data-stu-id="07eb8-121">1</span></span>             | <span data-ttu-id="07eb8-122">Da 1 a 12</span><span class="sxs-lookup"><span data-stu-id="07eb8-122">1 to 12</span></span>        |
| <span data-ttu-id="07eb8-123">2 stelle</span><span class="sxs-lookup"><span data-stu-id="07eb8-123">2 stars</span></span> | <span data-ttu-id="07eb8-124">25</span><span class="sxs-lookup"><span data-stu-id="07eb8-124">25</span></span>            | <span data-ttu-id="07eb8-125">da 13 a 37</span><span class="sxs-lookup"><span data-stu-id="07eb8-125">13 to 37</span></span>       |
| <span data-ttu-id="07eb8-126">3 stelle</span><span class="sxs-lookup"><span data-stu-id="07eb8-126">3 stars</span></span> | <span data-ttu-id="07eb8-127">50</span><span class="sxs-lookup"><span data-stu-id="07eb8-127">50</span></span>            | <span data-ttu-id="07eb8-128">da 38 a 62</span><span class="sxs-lookup"><span data-stu-id="07eb8-128">38 to 62</span></span>       |
| <span data-ttu-id="07eb8-129">4 stelle</span><span class="sxs-lookup"><span data-stu-id="07eb8-129">4 stars</span></span> | <span data-ttu-id="07eb8-130">75</span><span class="sxs-lookup"><span data-stu-id="07eb8-130">75</span></span>            | <span data-ttu-id="07eb8-131">da 63 a 86</span><span class="sxs-lookup"><span data-stu-id="07eb8-131">63 to 86</span></span>       |
| <span data-ttu-id="07eb8-132">5 stelle</span><span class="sxs-lookup"><span data-stu-id="07eb8-132">5 stars</span></span> | <span data-ttu-id="07eb8-133">99</span><span class="sxs-lookup"><span data-stu-id="07eb8-133">99</span></span>            | <span data-ttu-id="07eb8-134">da 87 a 99</span><span class="sxs-lookup"><span data-stu-id="07eb8-134">87 to 99</span></span>       |



 

<span data-ttu-id="07eb8-135">Questo attributo viene archiviato solo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="07eb8-135">This attribute is stored only in the library.</span></span>

<span data-ttu-id="07eb8-136">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="07eb8-136">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07eb8-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07eb8-137">Requirements</span></span>



| <span data-ttu-id="07eb8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="07eb8-138">Requirement</span></span> | <span data-ttu-id="07eb8-139">Valore</span><span class="sxs-lookup"><span data-stu-id="07eb8-139">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="07eb8-140">Versione</span><span class="sxs-lookup"><span data-stu-id="07eb8-140">Version</span></span><br/> | <span data-ttu-id="07eb8-141">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="07eb8-141">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07eb8-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07eb8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07eb8-143">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="07eb8-143">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





