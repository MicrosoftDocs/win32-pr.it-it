---
description: Quantità di spazio disponibile in un volume, espresso in byte.
ms.assetid: 84c85468-d3c2-49bf-b52b-bbd3d9ecb914
title: System. FreeSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a605cc75dc2b7b36f6d9baf3c293c8bac8323dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881321"
---
# <a name="systemfreespace"></a><span data-ttu-id="a50c8-103">System. FreeSpace</span><span class="sxs-lookup"><span data-stu-id="a50c8-103">System.FreeSpace</span></span>

<span data-ttu-id="a50c8-104">Quantità di spazio disponibile in un volume, espresso in byte.</span><span class="sxs-lookup"><span data-stu-id="a50c8-104">The amount of free space in a volume, in bytes.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a50c8-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a50c8-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FreeSpace
   shellPKey = PKEY_FreeSpace
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = Full
            minValue = 0
            setValue = 0
            text = Full
            defineToken = FREESPACE_FULL
            mnemonics = full
         enumRange
            name = Tiny
            minValue = 1
            setValue = 1
            text = Tiny (0 - 2 GB)
            defineToken = FREESPACE_TINY
            mnemonics = tiny
         enumRange
            name = Small
            minValue = 2147483649
            setValue = 2147483649
            text = Small (2 - 10 GB)
            defineToken = FREESPACE_SMALL
            mnemonics = small
         enumRange
            name = Medium
            minValue = 10737418241
            setValue = 10737418241
            text = Medium (10 - 40 GB)
            defineToken = FREESPACE_MEDIUM
            mnemonics = medium
         enumRange
            name = Large
            minValue = 42949672961
            setValue = 42949672961
            text = Large (40 - 80 GB)
            defineToken = FREESPACE_LARGE
            mnemonics = large
         enumRange
            name = Huge
            minValue = 85899345921
            setValue = 85899345921
            text = Huge (80 - 120 GB)
            defineToken = FREESPACE_HUGE
            mnemonics = huge
         enumRange
            name = Gigantic
            minValue = 137438953473
            setValue = 137438953473
            text = Gigantic (over 120 GB)
            defineToken = FREESPACE_GIGANTIC
            mnemonics = gigantic
```

## <a name="windows-vista"></a><span data-ttu-id="a50c8-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a50c8-106">Windows Vista</span></span>

```
propertyDescription
   name = System.FreeSpace
   shellPKey = PKEY_FreeSpace
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = Zero
            mnemonics = empty
         enumRange
            minValue = 1
            setValue = 1
            text = Tiny (0 - 2 GB)
            mnemonics = tiny
         enumRange
            minValue = 2147483649
            setValue = 2147483649
            text = Small (2 - 10 GB)
            mnemonics = small
         enumRange
            minValue = 10737418241
            setValue = 10737418241
            text = Medium (10 - 40 GB)
            mnemonics = medium
         enumRange
            minValue = 42949672961
            setValue = 42949672961
            text = Large (40 - 80 GB)
            mnemonics = large
         enumRange
            minValue = 85899345921
            setValue = 85899345921
            text = Huge (80 - 120 GB)
            mnemonics = huge
         enumRange
            minValue = 137438953473
            setValue = 137438953473
            text = Gigantic (over 120 GB)
            mnemonics = gigantic
```

## <a name="remarks"></a><span data-ttu-id="a50c8-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a50c8-107">Remarks</span></span>

<span data-ttu-id="a50c8-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="a50c8-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a50c8-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a50c8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a50c8-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a50c8-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a50c8-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a50c8-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a50c8-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a50c8-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a50c8-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a50c8-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a50c8-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a50c8-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a50c8-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a50c8-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a50c8-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a50c8-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a50c8-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a50c8-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a50c8-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a50c8-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a50c8-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a50c8-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a50c8-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="a50c8-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a50c8-121">editControl</span><span class="sxs-lookup"><span data-stu-id="a50c8-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a50c8-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="a50c8-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a50c8-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="a50c8-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
