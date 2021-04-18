---
description: Valore di luminosità dell'immagine, in unità di apice, in genere nell'intervallo compreso tra-99,99 e 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311244"
---
# <a name="systemphotobrightness"></a><span data-ttu-id="5b398-103">System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="5b398-103">System.Photo.Brightness</span></span>

<span data-ttu-id="5b398-104">Valore di luminosità dell'immagine, in unità di apice, in genere nell'intervallo compreso tra-99,99 e 99,99.</span><span class="sxs-lookup"><span data-stu-id="5b398-104">The brightness value of the image, in APEX units, usually in the range of -99.99 to 99.99.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="5b398-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b398-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="5b398-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b398-106">Remarks</span></span>

<span data-ttu-id="5b398-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="5b398-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="5b398-108">Vedere la specifica EXIF 2,2, Annex C, per un confronto tra i numeri di [System. Photo. Brightness]() e le misurazioni Foot-Lambert.</span><span class="sxs-lookup"><span data-stu-id="5b398-108">See the EXIF 2.2 specification, Annex C, for a comparison of [System.Photo.Brightness]() numbers and Foot-Lambert measurements.</span></span> <span data-ttu-id="5b398-109">Questa proprietà viene calcolata da [System. Photo. BrightnessNumerator](./props-system-photo-brightnessnumerator.md) e [System. Photo. BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span><span class="sxs-lookup"><span data-stu-id="5b398-109">This property is calculated from [System.Photo.BrightnessNumerator](./props-system-photo-brightnessnumerator.md) and [System.Photo.BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span></span> <span data-ttu-id="5b398-110">Se il numeratore del valore registrato è FFFFFFFF. È necessario indicare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="5b398-110">If the numerator of the recorded value is FFFFFFFF.H, "Unknown" should be indicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b398-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b398-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b398-112">Exchangeable Image File Format per fotocamere digitali ancora: EXIF versione 2,2</span><span class="sxs-lookup"><span data-stu-id="5b398-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="5b398-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="5b398-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5b398-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="5b398-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5b398-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="5b398-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5b398-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="5b398-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5b398-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="5b398-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5b398-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="5b398-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5b398-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="5b398-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5b398-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="5b398-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5b398-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5b398-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5b398-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="5b398-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5b398-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="5b398-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5b398-124">editControl</span><span class="sxs-lookup"><span data-stu-id="5b398-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5b398-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="5b398-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5b398-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="5b398-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
