---
description: Sistema di classificazione che utilizza un intervallo di valori integer compreso tra 0 e 5.
ms.assetid: 50353ba9-86dd-4172-91b4-1898c8fc5522
title: System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4741edd076b6027bc5f8dfbe3b2ff2a31374a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317973"
---
# <a name="systemsimplerating"></a><span data-ttu-id="35082-103">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="35082-103">System.SimpleRating</span></span>

<span data-ttu-id="35082-104">Sistema di classificazione che utilizza un intervallo di valori integer compreso tra 0 e 5.</span><span class="sxs-lookup"><span data-stu-id="35082-104">A rating system that uses a range of integer values between 0 and 5.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="35082-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35082-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.SimpleRating
   shellPKey = PKEY_SimpleRating
   formatID = A09F084E-AD41-489F-8076-AA5BE3082BCA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="35082-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="35082-106">Remarks</span></span>

<span data-ttu-id="35082-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="35082-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="35082-108">Per la compatibilità con il sistema di classificazione della shell di Windows Vista, il gestore delle proprietà deve anche popolare la proprietà [System. rating](./props-system-rating.md) con il mapping come descritto per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="35082-108">For compatibility with the Windows Vista Shell rating system, your property handler should also populate the [System.Rating](./props-system-rating.md) property with the mapping as described for that property.</span></span>

<span data-ttu-id="35082-109">Usare la tabella seguente per eseguire la conversione da [System. rating](./props-system-rating.md) a [System. SimpleRating]().</span><span class="sxs-lookup"><span data-stu-id="35082-109">Use the following table to convert from [System.Rating](./props-system-rating.md) to [System.SimpleRating]().</span></span>



| <span data-ttu-id="35082-110">System. rating</span><span class="sxs-lookup"><span data-stu-id="35082-110">System.Rating</span></span> | <span data-ttu-id="35082-111">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="35082-111">System.SimpleRating</span></span> |
|---------------|---------------------|
| <span data-ttu-id="35082-112">0</span><span class="sxs-lookup"><span data-stu-id="35082-112">0</span></span>             | <span data-ttu-id="35082-113">0</span><span class="sxs-lookup"><span data-stu-id="35082-113">0</span></span>                   |
| <span data-ttu-id="35082-114">1-12</span><span class="sxs-lookup"><span data-stu-id="35082-114">1-12</span></span>          | <span data-ttu-id="35082-115">1</span><span class="sxs-lookup"><span data-stu-id="35082-115">1</span></span>                   |
| <span data-ttu-id="35082-116">13-37</span><span class="sxs-lookup"><span data-stu-id="35082-116">13-37</span></span>         | <span data-ttu-id="35082-117">2</span><span class="sxs-lookup"><span data-stu-id="35082-117">2</span></span>                   |
| <span data-ttu-id="35082-118">38-62</span><span class="sxs-lookup"><span data-stu-id="35082-118">38-62</span></span>         | <span data-ttu-id="35082-119">3</span><span class="sxs-lookup"><span data-stu-id="35082-119">3</span></span>                   |
| <span data-ttu-id="35082-120">63-87</span><span class="sxs-lookup"><span data-stu-id="35082-120">63-87</span></span>         | <span data-ttu-id="35082-121">4</span><span class="sxs-lookup"><span data-stu-id="35082-121">4</span></span>                   |
| <span data-ttu-id="35082-122">88-99</span><span class="sxs-lookup"><span data-stu-id="35082-122">88-99</span></span>         | <span data-ttu-id="35082-123">5</span><span class="sxs-lookup"><span data-stu-id="35082-123">5</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="35082-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35082-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35082-125">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="35082-125">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="35082-126">searchInfo</span><span class="sxs-lookup"><span data-stu-id="35082-126">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="35082-127">labelInfo</span><span class="sxs-lookup"><span data-stu-id="35082-127">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="35082-128">typeInfo</span><span class="sxs-lookup"><span data-stu-id="35082-128">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="35082-129">displayInfo</span><span class="sxs-lookup"><span data-stu-id="35082-129">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="35082-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="35082-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="35082-131">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="35082-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="35082-132">numberFormat</span><span class="sxs-lookup"><span data-stu-id="35082-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="35082-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="35082-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="35082-134">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="35082-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="35082-135">drawControl</span><span class="sxs-lookup"><span data-stu-id="35082-135">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="35082-136">editControl</span><span class="sxs-lookup"><span data-stu-id="35082-136">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="35082-137">filterControl</span><span class="sxs-lookup"><span data-stu-id="35082-137">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="35082-138">queryControl</span><span class="sxs-lookup"><span data-stu-id="35082-138">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
