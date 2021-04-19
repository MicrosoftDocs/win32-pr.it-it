---
description: Indica la direzione di elaborazione della saturazione applicata dalla fotocamera quando è stata eseguita la foto.
ms.assetid: 209edf55-fd6c-416b-b175-346f5158fc2a
title: System. Photo. saturazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50655b1d9344bb3c25576de9ece3ac6ef2bba95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311192"
---
# <a name="systemphotosaturation"></a><span data-ttu-id="6f487-103">System. Photo. saturazione</span><span class="sxs-lookup"><span data-stu-id="6f487-103">System.Photo.Saturation</span></span>

<span data-ttu-id="6f487-104">Indica la direzione di elaborazione della saturazione applicata dalla fotocamera quando è stata eseguita la foto.</span><span class="sxs-lookup"><span data-stu-id="6f487-104">Indicates the direction of saturation processing applied by the camera when the photo was taken.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="6f487-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f487-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_SATURATION_NORMAL
         enum
            name = Low
            value = 1
            text = Low saturation
            defineToken = PHOTO_SATURATION_LOW
         enum
            name = High
            value = 2
            text = High saturation
            defineToken = PHOTO_SATURATION_HIGH
```

## <a name="windows-vista"></a><span data-ttu-id="6f487-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f487-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_SATURATION_NORMAL
         enum
            value = 1
            text = Low saturation
            defineName = PHOTO_SATURATION_LOW
         enum
            value = 2
            text = High saturation
            defineName = PHOTO_SATURATION_HIGH
```

## <a name="remarks"></a><span data-ttu-id="6f487-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f487-107">Remarks</span></span>

<span data-ttu-id="6f487-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6f487-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f487-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f487-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f487-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6f487-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6f487-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6f487-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6f487-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6f487-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6f487-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6f487-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6f487-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6f487-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6f487-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6f487-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6f487-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6f487-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6f487-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6f487-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6f487-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6f487-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6f487-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6f487-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6f487-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="6f487-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6f487-121">editControl</span><span class="sxs-lookup"><span data-stu-id="6f487-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6f487-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="6f487-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6f487-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="6f487-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
