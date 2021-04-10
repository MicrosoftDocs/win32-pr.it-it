---
description: 'Stato di un flag. Values: (0 = None 1 = white 2 = Red).'
ms.assetid: 0485deab-2408-4147-acaa-cb09e9e0032a
title: System. FlagStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dde42493f2d450854c3f53de5ecab26394f0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227296"
---
# <a name="systemflagstatus"></a><span data-ttu-id="e94f7-104">System. FlagStatus</span><span class="sxs-lookup"><span data-stu-id="e94f7-104">System.FlagStatus</span></span>

<span data-ttu-id="e94f7-105">Stato di un flag.</span><span class="sxs-lookup"><span data-stu-id="e94f7-105">The status of a flag.</span></span> <span data-ttu-id="e94f7-106">Values: (0 = None 1 = white 2 = Red).</span><span class="sxs-lookup"><span data-stu-id="e94f7-106">Values: (0=none 1=white 2=Red).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e94f7-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e94f7-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotFlagged
            value = 0
            text = Not flagged
            defineToken = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            name = Completed
            value = 1
            text = Completed
            defineToken = FLAGSTATUS_COMPLETED
         enum
            name = FollowUp
            value = 2
            text = Follow Up
            defineToken = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="windows-vista"></a><span data-ttu-id="e94f7-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e94f7-108">Windows Vista</span></span>

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not flagged
            defineName = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            value = 1
            text = Completed
            defineName = FLAGSTATUS_COMPLETED
         enum
            value = 2
            text = Follow Up
            defineName = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="remarks"></a><span data-ttu-id="e94f7-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e94f7-109">Remarks</span></span>

<span data-ttu-id="e94f7-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="e94f7-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e94f7-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e94f7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e94f7-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e94f7-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e94f7-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e94f7-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e94f7-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e94f7-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e94f7-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e94f7-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e94f7-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e94f7-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e94f7-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e94f7-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e94f7-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e94f7-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e94f7-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e94f7-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e94f7-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e94f7-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e94f7-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e94f7-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e94f7-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="e94f7-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e94f7-123">editControl</span><span class="sxs-lookup"><span data-stu-id="e94f7-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e94f7-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="e94f7-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e94f7-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="e94f7-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
