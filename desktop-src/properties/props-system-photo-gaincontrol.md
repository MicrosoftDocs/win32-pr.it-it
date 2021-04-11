---
description: Indica il grado di regolazione complessiva del guadagno dell'immagine. Calcolato da PKEY \_ Photo \_ GAINCONTROLNUMERATOR e PKEY \_ Photo \_ GainControlDenominator.
ms.assetid: 5076e03b-2c8a-4ef4-93d6-271a4bd697a6
title: System. Photo. GainControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8278120e5e65137eda491f52af7bc36f1c163c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967322"
---
# <a name="systemphotogaincontrol"></a><span data-ttu-id="f272e-104">System. Photo. GainControl</span><span class="sxs-lookup"><span data-stu-id="f272e-104">System.Photo.GainControl</span></span>

<span data-ttu-id="f272e-105">Indica il grado di regolazione complessiva del guadagno dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f272e-105">Indicates the degree of overall image gain adjustment.</span></span> <span data-ttu-id="f272e-106">Calcolato da PKEY \_ Photo \_ GAINCONTROLNUMERATOR e PKEY \_ Photo \_ GainControlDenominator.</span><span class="sxs-lookup"><span data-stu-id="f272e-106">Calculated from PKEY\_Photo\_GainControlNumerator and PKEY\_Photo\_GainControlDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="f272e-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f272e-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0.0
            text = None
            defineToken = PHOTO_GAINCONTROL_NONE
         enum
            name = LowGainUp
            value = 1.0
            text = Low gain up
            defineToken = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            name = HighGainUp
            value = 2.0
            text = High gain up
            defineToken = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            name = LowGainDown
            value = 3.0
            text = Low gain down
            defineToken = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            name = HighGainDown
            value = 4.0
            text = High gain down
            defineToken = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="windows-vista"></a><span data-ttu-id="f272e-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f272e-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0.0
            text = None
            defineName = PHOTO_GAINCONTROL_NONE
         enum
            value = 1.0
            text = Low gain up
            defineName = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            value = 2.0
            text = High gain up
            defineName = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            value = 3.0
            text = Low gain down
            defineName = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            value = 4.0
            text = High gain down
            defineName = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="remarks"></a><span data-ttu-id="f272e-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="f272e-109">Remarks</span></span>

<span data-ttu-id="f272e-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="f272e-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f272e-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f272e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f272e-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f272e-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f272e-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f272e-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f272e-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f272e-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f272e-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f272e-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f272e-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f272e-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f272e-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f272e-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f272e-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f272e-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f272e-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f272e-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f272e-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f272e-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f272e-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f272e-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f272e-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="f272e-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f272e-123">editControl</span><span class="sxs-lookup"><span data-stu-id="f272e-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f272e-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="f272e-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f272e-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="f272e-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
