---
description: Consente di visualizzare come un'icona se un percorso è il percorso di salvataggio predefinito per il proprietario e/o non proprietari di una libreria.
ms.assetid: 42375796-bf95-4092-bce0-c77e7b5bfeea
title: System. DefaultSaveLocationDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1147a7c0fce8b4bc564b57bac2476b1826e4313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311501"
---
# <a name="systemdefaultsavelocationdisplay"></a><span data-ttu-id="fadef-103">System. DefaultSaveLocationDisplay</span><span class="sxs-lookup"><span data-stu-id="fadef-103">System.DefaultSaveLocationDisplay</span></span>

<span data-ttu-id="fadef-104">Consente di visualizzare come un'icona se un percorso è il percorso di salvataggio predefinito per il proprietario e/o non i proprietari di una libreria.</span><span class="sxs-lookup"><span data-stu-id="fadef-104">Helps display as an icon whether or not a location is the default save location for owner and/or non-owners of a library</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="fadef-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="fadef-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.DefaultSaveLocationDisplay
   shellPKey = PKEY_DefaultSaveLocationDisplay
   formatID = 5D76B67F-9B3D-44BB-B6AE-25DA4F638A67
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = DefaultSaveNone
            value = 0
            text
            defineToken = ISDEFAULTSAVE_NONE
         enum
            name = DefaultSaveOwner
            value = 1
            text = Default save location
            defineToken = ISDEFAULTSAVE_OWNER
         enum
            name = DefaultSavePublic
            value = 2
            text = Public save location
            defineToken = ISDEFAULTSAVE_NONOWNER
         enum
            name = DefaultSaveBoth
            value = 3
            text = Default and public save location
            defineToken = ISDEFAULTSAVE_BOTH
```

## <a name="remarks"></a><span data-ttu-id="fadef-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="fadef-106">Remarks</span></span>

<span data-ttu-id="fadef-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="fadef-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fadef-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fadef-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fadef-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="fadef-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fadef-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="fadef-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fadef-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="fadef-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fadef-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="fadef-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fadef-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fadef-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fadef-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="fadef-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fadef-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="fadef-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fadef-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="fadef-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fadef-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fadef-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fadef-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="fadef-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fadef-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="fadef-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fadef-120">editControl</span><span class="sxs-lookup"><span data-stu-id="fadef-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fadef-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="fadef-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fadef-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="fadef-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
