---
description: Rappresenta un URL ben formato che punta all'elemento.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. ItemUrl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317989"
---
# <a name="systemitemurl"></a><span data-ttu-id="509f1-103">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="509f1-103">System.ItemUrl</span></span>

<span data-ttu-id="509f1-104">Rappresenta un URL ben formato che punta all'elemento.</span><span class="sxs-lookup"><span data-stu-id="509f1-104">Represents a well-formed URL that points to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="509f1-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="509f1-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="509f1-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="509f1-106">Remarks</span></span>

<span data-ttu-id="509f1-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="509f1-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="509f1-108">Per fare riferimento agli elementi dello spazio dei nomi della shell tramite le API della shell, usare [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="509f1-108">To reference Shell namespace items through Shell APIs, use [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="509f1-109">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="509f1-109">Example values:</span></span>



| <span data-ttu-id="509f1-110">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="509f1-110">Item type</span></span> | <span data-ttu-id="509f1-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="509f1-111">Example</span></span>                        |
|-----------|--------------------------------|
| <span data-ttu-id="509f1-112">File</span><span class="sxs-lookup"><span data-stu-id="509f1-112">File</span></span>      | <span data-ttu-id="509f1-113">hello.txt file:///c:/mydir/bar/</span><span class="sxs-lookup"><span data-stu-id="509f1-113">file:///c:/mydir/bar/hello.txt</span></span> |
| <span data-ttu-id="509f1-114">File</span><span class="sxs-lookup"><span data-stu-id="509f1-114">File</span></span>      | <span data-ttu-id="509f1-115">CSC:///{GUID}/...</span><span class="sxs-lookup"><span data-stu-id="509f1-115">csc://{GUID}/...</span></span>               |
| <span data-ttu-id="509f1-116">Message</span><span class="sxs-lookup"><span data-stu-id="509f1-116">Message</span></span>   | <span data-ttu-id="509f1-117">mapi://...</span><span class="sxs-lookup"><span data-stu-id="509f1-117">mapi://...</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="509f1-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="509f1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="509f1-119">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="509f1-119">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="509f1-120">searchInfo</span><span class="sxs-lookup"><span data-stu-id="509f1-120">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="509f1-121">labelInfo</span><span class="sxs-lookup"><span data-stu-id="509f1-121">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="509f1-122">typeInfo</span><span class="sxs-lookup"><span data-stu-id="509f1-122">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="509f1-123">displayInfo</span><span class="sxs-lookup"><span data-stu-id="509f1-123">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="509f1-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="509f1-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="509f1-125">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="509f1-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="509f1-126">numberFormat</span><span class="sxs-lookup"><span data-stu-id="509f1-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="509f1-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="509f1-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="509f1-128">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="509f1-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="509f1-129">drawControl</span><span class="sxs-lookup"><span data-stu-id="509f1-129">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="509f1-130">editControl</span><span class="sxs-lookup"><span data-stu-id="509f1-130">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="509f1-131">filterControl</span><span class="sxs-lookup"><span data-stu-id="509f1-131">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="509f1-132">queryControl</span><span class="sxs-lookup"><span data-stu-id="509f1-132">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
