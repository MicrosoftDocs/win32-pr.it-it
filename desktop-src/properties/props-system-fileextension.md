---
description: Identifica l'estensione di file dell'elemento basato su file, incluso il punto iniziali.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311400"
---
# <a name="systemfileextension"></a><span data-ttu-id="c476f-103">System. FileExtension</span><span class="sxs-lookup"><span data-stu-id="c476f-103">System.FileExtension</span></span>

<span data-ttu-id="c476f-104">Identifica l'estensione di file dell'elemento basato su file, incluso il punto iniziali.</span><span class="sxs-lookup"><span data-stu-id="c476f-104">Identifies the file extension of the file-based item, including the leading period.</span></span> <span data-ttu-id="c476f-105">Questa proprietà è derivata da System. FileName.</span><span class="sxs-lookup"><span data-stu-id="c476f-105">This property is derived from System.FileName.</span></span> <span data-ttu-id="c476f-106">Se System. FileName non ha un'estensione di file o è un VT \_ vuoto, il valore di questa proprietà deve essere VT \_ vuoto.</span><span class="sxs-lookup"><span data-stu-id="c476f-106">If System.FileName either does not have a file extension or is VT\_EMPTY, the value for this property should be VT\_EMPTY.</span></span>

<span data-ttu-id="c476f-107">Per ottenere il tipo di qualsiasi elemento (incluso un elemento che non è un file), usare System. ItemType.</span><span class="sxs-lookup"><span data-stu-id="c476f-107">To obtain the type of any item (including an item that is not a file), use System.ItemType.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="c476f-108">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c476f-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="c476f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c476f-109">Remarks</span></span>

<span data-ttu-id="c476f-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="c476f-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="c476f-111">Se [System. FileName](./props-system-filename.md) è VT \_ vuoto, anche questa proprietà deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="c476f-111">If [System.FileName](./props-system-filename.md) is VT\_EMPTY, this property should also be empty.</span></span> <span data-ttu-id="c476f-112">In caso contrario, questa proprietà deve essere derivata in modo appropriato dall'origine dati da System. FileName.</span><span class="sxs-lookup"><span data-stu-id="c476f-112">Otherwise, this property should be derived appropriately by the data source from System.FileName.</span></span> <span data-ttu-id="c476f-113">Se System. FileName non include un'estensione di file, [System. FileExtension]() deve essere un VT \_ vuoto.</span><span class="sxs-lookup"><span data-stu-id="c476f-113">If System.FileName does not include a file extension, [System.FileExtension]() should be VT\_EMPTY.</span></span> <span data-ttu-id="c476f-114">Per ottenere il tipo di qualsiasi elemento (incluso un elemento che non è un file), usare [System. ItemType](./props-system-itemtype.md).</span><span class="sxs-lookup"><span data-stu-id="c476f-114">To obtain the type of any item (including an item that is not a file), use [System.ItemType](./props-system-itemtype.md).</span></span>

<span data-ttu-id="c476f-115">Esempi di proprietà di estensione di file e percorso.</span><span class="sxs-lookup"><span data-stu-id="c476f-115">Path and file extension property examples.</span></span> 

| <span data-ttu-id="c476f-116">Percorso</span><span class="sxs-lookup"><span data-stu-id="c476f-116">Path</span></span>                               | <span data-ttu-id="c476f-117">Estensione nome del file</span><span class="sxs-lookup"><span data-stu-id="c476f-117">File Extension</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="c476f-118">c: \\ file \\ personali \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="c476f-118">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="c476f-119">.txt</span><span class="sxs-lookup"><span data-stu-id="c476f-119">.txt</span></span>           |
| <span data-ttu-id="c476f-120">\\\\\\condivisione server \\ mydir \\news.doc</span><span class="sxs-lookup"><span data-stu-id="c476f-120">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="c476f-121">doc</span><span class="sxs-lookup"><span data-stu-id="c476f-121">.doc</span></span>           |
| <span data-ttu-id="c476f-122">\\\\\\numbers.xls condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="c476f-122">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="c476f-123">xls</span><span class="sxs-lookup"><span data-stu-id="c476f-123">.xls</span></span>           |
| <span data-ttu-id="c476f-124">\\\\\\cartella condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="c476f-124">\\\\server\\share\\folder</span></span>          | <span data-ttu-id="c476f-125">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c476f-125">VT\_EMPTY</span></span>      |
| <span data-ttu-id="c476f-126">c: \\ Stuff \\ cartella</span><span class="sxs-lookup"><span data-stu-id="c476f-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="c476f-127">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c476f-127">VT\_EMPTY</span></span>      |
| <span data-ttu-id="c476f-128">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="c476f-128">\[desktop\]</span></span>                        | <span data-ttu-id="c476f-129">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c476f-129">VT\_EMPTY</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="c476f-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c476f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c476f-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c476f-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c476f-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c476f-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c476f-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c476f-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c476f-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c476f-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c476f-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c476f-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c476f-136">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c476f-136">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c476f-137">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c476f-137">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c476f-138">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c476f-138">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c476f-139">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c476f-139">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c476f-140">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c476f-140">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c476f-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="c476f-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c476f-142">editControl</span><span class="sxs-lookup"><span data-stu-id="c476f-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c476f-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="c476f-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c476f-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="c476f-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
