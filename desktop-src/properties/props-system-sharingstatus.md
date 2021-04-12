---
description: 'Indica lo stato di condivisione di un elemento: non condiviso, condiviso, Everyone (Gruppo Home o Everyone) o privato.'
ms.assetid: 61d8a4fc-d9ad-467f-aa79-b0c208d0e905
title: System. SharingStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3c930309435c14e53cfc29d0fd068be6697c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347951"
---
# <a name="systemsharingstatus"></a><span data-ttu-id="5457b-103">System. SharingStatus</span><span class="sxs-lookup"><span data-stu-id="5457b-103">System.SharingStatus</span></span>

<span data-ttu-id="5457b-104">Indica lo stato di condivisione di un elemento: non condiviso, condiviso, Everyone (Gruppo Home o Everyone) o privato.</span><span class="sxs-lookup"><span data-stu-id="5457b-104">Indicates the sharing status of an item: Not Shared, Shared, Everyone (homegroup or everyone), or Private.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="5457b-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="5457b-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.SharingStatus
   shellPKey = PKEY_SharingStatus
   formatID = EF884C5B-2BFE-41BB-AAE5-76EEDF4F9902
   propID = 300
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotShared
            value = 0
            text = Not shared
            defineToken = SHARINGSTATUS_NOTSHARED
         enum
            name = Shared
            value = 1
            text = Shared
            defineToken = SHARINGSTATUS_SHARED
         enum
            name = Private
            value = 2
            text = Private
            defineToken = SHARINGSTATUS_PRIVATE
```

## <a name="remarks"></a><span data-ttu-id="5457b-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="5457b-106">Remarks</span></span>

<span data-ttu-id="5457b-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="5457b-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5457b-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5457b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5457b-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="5457b-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5457b-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="5457b-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5457b-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="5457b-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5457b-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="5457b-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5457b-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="5457b-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5457b-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="5457b-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5457b-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="5457b-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5457b-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="5457b-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5457b-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5457b-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5457b-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="5457b-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5457b-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="5457b-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5457b-120">editControl</span><span class="sxs-lookup"><span data-stu-id="5457b-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5457b-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="5457b-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5457b-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="5457b-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
