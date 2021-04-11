---
description: Indica la longitudine.
ms.assetid: ef28141f-1b63-4694-b6df-fcc11ce7e50b
title: System. GPS. Longitudine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65431412b0d46ad7b68100febd4d6e8efd31a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132050"
---
# <a name="systemgpslongitude"></a><span data-ttu-id="d9383-103">System. GPS. Longitudine</span><span class="sxs-lookup"><span data-stu-id="d9383-103">System.GPS.Longitude</span></span>

<span data-ttu-id="d9383-104">Indica la longitudine.</span><span class="sxs-lookup"><span data-stu-id="d9383-104">Indicates the longitude.</span></span> <span data-ttu-id="d9383-105">Si tratta di una matrice di tre valori, come indicato di seguito: index 0 è il degrees, index 1 is the minutes, index 2 is the seconds.</span><span class="sxs-lookup"><span data-stu-id="d9383-105">This is an array of three values, as follows: Index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="d9383-106">Ogni viene calcolato in base ai valori in PKEY \_ GPS \_ LONGITUDENUMERATOR e PKEY \_ GPS \_ LongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="d9383-106">Each is calculated from the values in PKEY\_GPS\_LongitudeNumerator and PKEY\_GPS\_LongitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="d9383-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="d9383-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a><span data-ttu-id="d9383-108">Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9383-108">Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="d9383-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9383-109">Remarks</span></span>

<span data-ttu-id="d9383-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="d9383-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="d9383-111">`label`Per Windows Vista con Service Pack 1 (SP1) è stato aggiunto il requisito di un riferimento di stringa indiretto specifico per l'attributo di **labelInfo** .</span><span class="sxs-lookup"><span data-stu-id="d9383-111">The requirement of a specific indirect string reference for the `label` attribute of **labelInfo** was added for Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9383-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9383-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9383-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d9383-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d9383-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d9383-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d9383-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="d9383-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d9383-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d9383-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d9383-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d9383-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d9383-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="d9383-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d9383-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="d9383-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d9383-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="d9383-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d9383-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d9383-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d9383-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="d9383-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d9383-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="d9383-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d9383-124">editControl</span><span class="sxs-lookup"><span data-stu-id="d9383-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d9383-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="d9383-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d9383-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="d9383-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
