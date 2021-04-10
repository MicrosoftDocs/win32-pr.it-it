---
description: Valore di apertura dell'immagine, in unità di apice.
ms.assetid: ec8c0271-1e1e-4d37-a09a-f430d0682213
title: System. Photo. aperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2273425c1974617b7d76657f818c4f1c39cd3aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227256"
---
# <a name="systemphotoaperture"></a><span data-ttu-id="e38fd-103">System. Photo. aperture</span><span class="sxs-lookup"><span data-stu-id="e38fd-103">System.Photo.Aperture</span></span>

<span data-ttu-id="e38fd-104">Valore di apertura dell'immagine, in unità di apice.</span><span class="sxs-lookup"><span data-stu-id="e38fd-104">The aperture value of the image, in APEX units.</span></span> <span data-ttu-id="e38fd-105">Per un confronto tra i numeri di [System. Photo. aperture]() e i valori [System. Photo. fnumber](./props-system-photo-fnumber.md) , vedere la specifica del file di immagine exchange (EXIF) 2,2, allegato C.</span><span class="sxs-lookup"><span data-stu-id="e38fd-105">See the Exchangeable Image File (EXIF) 2.2 specification, Annex C, for a comparison of [System.Photo.Aperture]() numbers and [System.Photo.FNumber](./props-system-photo-fnumber.md) values.</span></span> <span data-ttu-id="e38fd-106">Questa proprietà viene calcolata da [System. Photo. ApertureNumerator](./props-system-photo-aperturenumerator.md) e [System. Photo. ApertureDenominator](./props-system-photo-aperturedenominator.md).</span><span class="sxs-lookup"><span data-stu-id="e38fd-106">This property is calculated from [System.Photo.ApertureNumerator](./props-system-photo-aperturenumerator.md) and [System.Photo.ApertureDenominator](./props-system-photo-aperturedenominator.md).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e38fd-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e38fd-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="e38fd-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e38fd-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="e38fd-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e38fd-109">Remarks</span></span>

<span data-ttu-id="e38fd-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="e38fd-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e38fd-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e38fd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e38fd-112">Exchangeable Image File Format per fotocamere digitali ancora: EXIF versione 2,2</span><span class="sxs-lookup"><span data-stu-id="e38fd-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="e38fd-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e38fd-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e38fd-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e38fd-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e38fd-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e38fd-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e38fd-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e38fd-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e38fd-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e38fd-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e38fd-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e38fd-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e38fd-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e38fd-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e38fd-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e38fd-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e38fd-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e38fd-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e38fd-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e38fd-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e38fd-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="e38fd-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e38fd-124">editControl</span><span class="sxs-lookup"><span data-stu-id="e38fd-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e38fd-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="e38fd-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e38fd-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="e38fd-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
