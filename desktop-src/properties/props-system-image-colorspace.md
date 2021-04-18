---
description: Spazio dei colore incorporato nell'immagine. Ricavato dalle informazioni sul file di immagine scambiabile (EXIF).
ms.assetid: 2375e132-e400-419f-a0f9-cbb6f9acdf45
title: System. image. spazio colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d99e0f88fd793d0a0f8207b43a52c7be47c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311354"
---
# <a name="systemimagecolorspace"></a><span data-ttu-id="480db-104">System. image. spazio colore</span><span class="sxs-lookup"><span data-stu-id="480db-104">System.Image.ColorSpace</span></span>

<span data-ttu-id="480db-105">Spazio dei colore incorporato nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="480db-105">The colorspace embedded in the image.</span></span> <span data-ttu-id="480db-106">Ricavato dalle informazioni sul file di immagine scambiabile (EXIF).</span><span class="sxs-lookup"><span data-stu-id="480db-106">Taken from the Exchangeable Image File (EXIF) information.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="480db-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="480db-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SRGB
            value = 1
            text = sRGB
            defineToken = IMAGE_COLORSPACE_SRGB
         enum
            name = Uncalibrated
            value = 0xFFFF
            text = Uncalibrated
            defineToken = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="windows-vista"></a><span data-ttu-id="480db-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="480db-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = sRGB
            defineName = IMAGE_COLORSPACE_SRGB
         enum
            value = 0xFFFF
            text = Uncalibrated
            defineName = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="remarks"></a><span data-ttu-id="480db-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="480db-109">Remarks</span></span>

<span data-ttu-id="480db-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="480db-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="480db-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="480db-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="480db-112">Exchangeable Image File Format per fotocamere digitali ancora: EXIF versione 2,2</span><span class="sxs-lookup"><span data-stu-id="480db-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="480db-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="480db-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="480db-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="480db-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="480db-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="480db-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="480db-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="480db-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="480db-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="480db-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="480db-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="480db-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="480db-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="480db-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="480db-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="480db-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="480db-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="480db-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="480db-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="480db-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="480db-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="480db-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="480db-124">editControl</span><span class="sxs-lookup"><span data-stu-id="480db-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="480db-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="480db-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="480db-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="480db-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
