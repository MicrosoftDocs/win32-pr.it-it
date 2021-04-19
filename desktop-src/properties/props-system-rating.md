---
description: Sistema di classificazione che utilizza valori integer compresi tra 1 e 99. Si tratta del sistema di classificazione utilizzato dalla shell di Windows Vista.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System. rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e411e313f0fa6042a8cbe3a076a7166928020af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311161"
---
# <a name="systemrating"></a><span data-ttu-id="9f3f7-104">System. rating</span><span class="sxs-lookup"><span data-stu-id="9f3f7-104">System.Rating</span></span>

<span data-ttu-id="9f3f7-105">Sistema di classificazione che utilizza valori integer compresi tra 1 e 99.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-105">A rating system that uses integer values between 1 and 99.</span></span> <span data-ttu-id="9f3f7-106">Si tratta del sistema di classificazione utilizzato dalla shell di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-106">This is the rating system used by the Windows Vista Shell.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="9f3f7-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f3f7-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a><span data-ttu-id="9f3f7-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f3f7-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a><span data-ttu-id="9f3f7-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f3f7-109">Remarks</span></span>

<span data-ttu-id="9f3f7-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="9f3f7-111">Per la compatibilità con i sistemi di classificazione che usano valori compresi tra 1 e 5, vedere la proprietà [System. SimpleRating](./props-system-simplerating.md).</span><span class="sxs-lookup"><span data-stu-id="9f3f7-111">For compatibility with ratings systems that use values between 1 and 5, see the property [System.SimpleRating](./props-system-simplerating.md).</span></span> <span data-ttu-id="9f3f7-112">Si noti, tuttavia, che System. SimpleRating non viene utilizzato nella shell di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-112">Note, however, that System.SimpleRating is not used in the Windows Vista Shell.</span></span>

<span data-ttu-id="9f3f7-113">Nella tabella seguente viene descritto il significato del sistema di classificazione a stella utilizzato nell'interfaccia utente della shell in termini di valore [System. rating]() .</span><span class="sxs-lookup"><span data-stu-id="9f3f7-113">The following table describes what the star rating system used in the Shell UI means in terms of the [System.Rating]() value.</span></span>



| <span data-ttu-id="9f3f7-114">System. rating</span><span class="sxs-lookup"><span data-stu-id="9f3f7-114">System.Rating</span></span> | <span data-ttu-id="9f3f7-115">Classificazione a stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-115">Star Rating</span></span> |
|---------------|-------------|
| <span data-ttu-id="9f3f7-116">1-12</span><span class="sxs-lookup"><span data-stu-id="9f3f7-116">1-12</span></span>          | <span data-ttu-id="9f3f7-117">1 stella</span><span class="sxs-lookup"><span data-stu-id="9f3f7-117">1 Star</span></span>      |
| <span data-ttu-id="9f3f7-118">13-37</span><span class="sxs-lookup"><span data-stu-id="9f3f7-118">13-37</span></span>         | <span data-ttu-id="9f3f7-119">2 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-119">2 Stars</span></span>     |
| <span data-ttu-id="9f3f7-120">38-62</span><span class="sxs-lookup"><span data-stu-id="9f3f7-120">38-62</span></span>         | <span data-ttu-id="9f3f7-121">3 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-121">3 Stars</span></span>     |
| <span data-ttu-id="9f3f7-122">63-87</span><span class="sxs-lookup"><span data-stu-id="9f3f7-122">63-87</span></span>         | <span data-ttu-id="9f3f7-123">4 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-123">4 Stars</span></span>     |
| <span data-ttu-id="9f3f7-124">88-99</span><span class="sxs-lookup"><span data-stu-id="9f3f7-124">88-99</span></span>         | <span data-ttu-id="9f3f7-125">5 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-125">5 Stars</span></span>     |



 

<span data-ttu-id="9f3f7-126">Quando un utente valuta un elemento scegliendo un valore di classificazione a stella nell'interfaccia utente, i valori effettivi di [System. rating]() vengono assegnati come illustrato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="9f3f7-126">When a user rates an item by choosing a star rating value in the UI, actual [System.Rating]() values are assigned as shown in this table:</span></span>



| <span data-ttu-id="9f3f7-127">Classificazione a stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-127">Star Rating</span></span> | <span data-ttu-id="9f3f7-128">Valore assegnato tramite interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9f3f7-128">Value Assigned Through UI</span></span> |
|-------------|---------------------------|
| <span data-ttu-id="9f3f7-129">1 stella</span><span class="sxs-lookup"><span data-stu-id="9f3f7-129">1 Star</span></span>      | <span data-ttu-id="9f3f7-130">1</span><span class="sxs-lookup"><span data-stu-id="9f3f7-130">1</span></span>                         |
| <span data-ttu-id="9f3f7-131">2 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-131">2 Stars</span></span>     | <span data-ttu-id="9f3f7-132">25</span><span class="sxs-lookup"><span data-stu-id="9f3f7-132">25</span></span>                        |
| <span data-ttu-id="9f3f7-133">3 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-133">3 Stars</span></span>     | <span data-ttu-id="9f3f7-134">50</span><span class="sxs-lookup"><span data-stu-id="9f3f7-134">50</span></span>                        |
| <span data-ttu-id="9f3f7-135">4 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-135">4 Stars</span></span>     | <span data-ttu-id="9f3f7-136">75</span><span class="sxs-lookup"><span data-stu-id="9f3f7-136">75</span></span>                        |
| <span data-ttu-id="9f3f7-137">5 stelle</span><span class="sxs-lookup"><span data-stu-id="9f3f7-137">5 Stars</span></span>     | <span data-ttu-id="9f3f7-138">99</span><span class="sxs-lookup"><span data-stu-id="9f3f7-138">99</span></span>                        |



 

<span data-ttu-id="9f3f7-139">Se il file ha un valore [System. SimpleRating](./props-system-simplerating.md) anziché un valore [System. rating]() , usare la tabella seguente per convertire e specificare i valori per System. rating.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-139">If your file has a [System.SimpleRating](./props-system-simplerating.md) value rather than a [System.Rating]() value, use the table below to convert and specify values for System.Rating.</span></span>



| <span data-ttu-id="9f3f7-140">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="9f3f7-140">System.SimpleRating</span></span> | <span data-ttu-id="9f3f7-141">System. rating</span><span class="sxs-lookup"><span data-stu-id="9f3f7-141">System.Rating</span></span> |
|---------------------|---------------|
| <span data-ttu-id="9f3f7-142">1</span><span class="sxs-lookup"><span data-stu-id="9f3f7-142">1</span></span>                   | <span data-ttu-id="9f3f7-143">1</span><span class="sxs-lookup"><span data-stu-id="9f3f7-143">1</span></span>             |
| <span data-ttu-id="9f3f7-144">2</span><span class="sxs-lookup"><span data-stu-id="9f3f7-144">2</span></span>                   | <span data-ttu-id="9f3f7-145">25</span><span class="sxs-lookup"><span data-stu-id="9f3f7-145">25</span></span>            |
| <span data-ttu-id="9f3f7-146">3</span><span class="sxs-lookup"><span data-stu-id="9f3f7-146">3</span></span>                   | <span data-ttu-id="9f3f7-147">50</span><span class="sxs-lookup"><span data-stu-id="9f3f7-147">50</span></span>            |
| <span data-ttu-id="9f3f7-148">4</span><span class="sxs-lookup"><span data-stu-id="9f3f7-148">4</span></span>                   | <span data-ttu-id="9f3f7-149">75</span><span class="sxs-lookup"><span data-stu-id="9f3f7-149">75</span></span>            |
| <span data-ttu-id="9f3f7-150">5</span><span class="sxs-lookup"><span data-stu-id="9f3f7-150">5</span></span>                   | <span data-ttu-id="9f3f7-151">99</span><span class="sxs-lookup"><span data-stu-id="9f3f7-151">99</span></span>            |



 

<span data-ttu-id="9f3f7-152">Se il file contiene valori salvati in modo permanente di System [. rating]() e [System. SimpleRating](./props-system-simplerating.md) , usare sempre il valore System. rating quando viene richiesto direttamente, senza riferimento a System. SimpleRating.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-152">If your file has both [System.Rating]() and [System.SimpleRating](./props-system-simplerating.md) persisted values, always use the System.Rating value when it is directly requested, without reference to System.SimpleRating.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f3f7-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f3f7-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f3f7-154">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="9f3f7-154">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-155">searchInfo</span><span class="sxs-lookup"><span data-stu-id="9f3f7-155">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-156">labelInfo</span><span class="sxs-lookup"><span data-stu-id="9f3f7-156">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-157">typeInfo</span><span class="sxs-lookup"><span data-stu-id="9f3f7-157">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-158">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9f3f7-158">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-159">stringFormat</span><span class="sxs-lookup"><span data-stu-id="9f3f7-159">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-160">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="9f3f7-160">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-161">numberFormat</span><span class="sxs-lookup"><span data-stu-id="9f3f7-161">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-162">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9f3f7-162">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-163">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="9f3f7-163">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-164">drawControl</span><span class="sxs-lookup"><span data-stu-id="9f3f7-164">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-165">editControl</span><span class="sxs-lookup"><span data-stu-id="9f3f7-165">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-166">filterControl</span><span class="sxs-lookup"><span data-stu-id="9f3f7-166">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9f3f7-167">queryControl</span><span class="sxs-lookup"><span data-stu-id="9f3f7-167">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
