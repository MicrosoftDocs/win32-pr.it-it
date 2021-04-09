---
description: Tipo di file percepito in base al relativo tipo canonico.
ms.assetid: dc5122a1-43b3-4c91-a44f-315fec5b4862
title: System.PerceivedType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc0be5e2ba481d113981efc264c4da66428e675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967332"
---
# <a name="systemperceivedtype"></a><span data-ttu-id="190d4-103">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="190d4-103">System.PerceivedType</span></span>

<span data-ttu-id="190d4-104">Tipo di file percepito in base al relativo tipo canonico.</span><span class="sxs-lookup"><span data-stu-id="190d4-104">The perceived file type based on its canonical type.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="190d4-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="190d4-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Custom
            value = -3
            text = Custom
         enum
            name = Unspecified
            value = -2
            text = Unspecified
         enum
            name = Folder
            value = -1
            text = Folder
            mnemonics = folders
         enum
            name = Unknown
            value = 0
            text = Unknown
         enum
            name = Text
            value = 1
            text = Text
         enum
            name = Image
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            name = Audio
            value = 3
            text = Audio
         enum
            name = Video
            value = 4
            text = Video
            mnemonics = videos
         enum
            name = Compressed
            value = 5
            text = Compressed
         enum
            name = Document
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            name = System
            value = 7
            text = System
         enum
            name = Application
            value = 8
            text = Application
         enum
            name = GameMedia
            value = 9
            text = Game Media
         enum
            name = Contacts
            value = 10
            text = Contacts
```

## <a name="windows-vista"></a><span data-ttu-id="190d4-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="190d4-106">Windows Vista</span></span>

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = -3
            text = Custom
         enum
            value = -2
            text = Unspecified
         enum
            value = -1
            text = Folder
            mnemonics = folders
         enum
            value = 0
            text = Unknown
         enum
            value = 1
            text = Text
         enum
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            value = 3
            text = Audio
         enum
            value = 4
            text = Video
            mnemonics = videos
         enum
            value = 5
            text = Compressed
         enum
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            value = 7
            text = System
         enum
            value = 8
            text = Application
         enum
            value = 9
            text = Game Media
         enum
            value = 10
            text = Contacts
```

## <a name="remarks"></a><span data-ttu-id="190d4-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="190d4-107">Remarks</span></span>

<span data-ttu-id="190d4-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="190d4-108">PKEY values are defined in Propkey.h.</span></span> <span data-ttu-id="190d4-109">Questo valore viene assegnato automaticamente dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="190d4-109">This value is automatically assigned by the Shell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="190d4-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="190d4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="190d4-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="190d4-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="190d4-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="190d4-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="190d4-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="190d4-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="190d4-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="190d4-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="190d4-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="190d4-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="190d4-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="190d4-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="190d4-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="190d4-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="190d4-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="190d4-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="190d4-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="190d4-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="190d4-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="190d4-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="190d4-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="190d4-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="190d4-122">editControl</span><span class="sxs-lookup"><span data-stu-id="190d4-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="190d4-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="190d4-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="190d4-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="190d4-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
