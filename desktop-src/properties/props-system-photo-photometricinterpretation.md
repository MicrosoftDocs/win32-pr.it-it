---
description: Composizione dei pixel.
ms.assetid: e2bb7f82-10dc-4fa0-875d-fc58c133024d
title: System. Photo. PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f6b431470780def946dbb8958e9e3eb6698322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049934"
---
# <a name="systemphotophotometricinterpretation"></a><span data-ttu-id="4b27d-103">System. Photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="4b27d-103">System.Photo.PhotometricInterpretation</span></span>

<span data-ttu-id="4b27d-104">Composizione dei pixel.</span><span class="sxs-lookup"><span data-stu-id="4b27d-104">The pixel composition.</span></span> <span data-ttu-id="4b27d-105">Nei dati compressi JPEG viene utilizzato un marcatore JPEG anziché questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b27d-105">In JPEG compressed data, a JPEG marker is used instead of this property.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="4b27d-106">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b27d-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.PhotometricInterpretation
   shellPKey = PKEY_Photo_PhotometricInterpretation
   formatID = 341796F1-1DF9-4B1C-A564-91BDEFA43877
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = RGB
            value = 2
            text = RGB
            defineToken = PHOTO_PHOTOMETRIC_RGB
         enum
            name = YCbCr
            value = 6
            text = YCbCr
            defineToken = PHOTO_PHOTOMETRIC_YCBCR
```

## <a name="windows-vista"></a><span data-ttu-id="4b27d-107">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b27d-107">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.PhotometricInterpretation
   shellPKey = PKEY_Photo_PhotometricInterpretation
   formatID = 341796F1-1DF9-4B1C-A564-91BDEFA43877
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 2
            text = RGB
            defineName = PHOTO_PHOTOMETRIC_RGB
         enum
            value = 6
            text = YCbCr
            defineName = PHOTO_PHOTOMETRIC_YCBCR
```

## <a name="remarks"></a><span data-ttu-id="4b27d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b27d-108">Remarks</span></span>

<span data-ttu-id="4b27d-109">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="4b27d-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="4b27d-110">Il valore predefinito dell' `isInnate` attributo dell'elemento **TypeInfo** è stato modificato da **false** a **true** a partire da Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4b27d-110">The default value of the `isInnate` attribute of the **typeInfo** element was changed from **false** to **true** as of Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b27d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b27d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b27d-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4b27d-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4b27d-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4b27d-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4b27d-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4b27d-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4b27d-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4b27d-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4b27d-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4b27d-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4b27d-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4b27d-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4b27d-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4b27d-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4b27d-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="4b27d-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4b27d-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4b27d-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4b27d-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4b27d-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4b27d-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="4b27d-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4b27d-123">editControl</span><span class="sxs-lookup"><span data-stu-id="4b27d-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4b27d-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="4b27d-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4b27d-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="4b27d-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
