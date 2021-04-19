---
description: Nome del file, inclusa l'estensione.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311398"
---
# <a name="systemfilename"></a><span data-ttu-id="2927a-103">System. FileName</span><span class="sxs-lookup"><span data-stu-id="2927a-103">System.FileName</span></span>

<span data-ttu-id="2927a-104">Nome del file, inclusa l'estensione.</span><span class="sxs-lookup"><span data-stu-id="2927a-104">The file name, including its extension.</span></span> <span data-ttu-id="2927a-105">System. FileExtension deriva da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2927a-105">System.FileExtension is derived from this property.</span></span>

<span data-ttu-id="2927a-106">È possibile che l'elemento non esista in un file System (ovvero, potrebbe non essere aperto con CreateFile).</span><span class="sxs-lookup"><span data-stu-id="2927a-106">It is possible that the item might not exist on a filesystem (that is, it may not be opened using CreateFile).</span></span> <span data-ttu-id="2927a-107">Tuttavia, se l'elemento è rappresentato come un file e il nome segue la sintassi standard di denominazione dei file Win32, l'origine dati deve emettere questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2927a-107">Nonetheless, if the item is represented as a file and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="2927a-108">Se l'elemento non è un file, l'origine dati deve emettere questa proprietà come VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="2927a-108">If the item is not a file, then the data source should emit this property as VT\_EMPTY.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="2927a-109">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="2927a-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="2927a-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2927a-110">Windows Vista</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a><span data-ttu-id="2927a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2927a-111">Remarks</span></span>

<span data-ttu-id="2927a-112">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="2927a-112">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2927a-113">L'elemento potrebbe non esistere in un file System (ovvero, potrebbe non essere aperto utilizzando CreateFile), ma se l'elemento è rappresentato come file dal senso logico e il nome segue la sintassi standard per la denominazione dei file Win32, l'origine dati deve emettere questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2927a-113">The item might not exist on a filesystem (that is, it may not be opened using CreateFile), but if the item is represented as a file from the logical sense and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="2927a-114">Se un elemento non è un file, il valore di questa proprietà è VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="2927a-114">If an item is not a file, then the value for this property is VT\_EMPTY.</span></span> <span data-ttu-id="2927a-115">Vedere System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="2927a-115">See System.ItemNameDisplay.</span></span> <span data-ttu-id="2927a-116">Ha lo stesso valore di System. ParsingName per gli elementi forniti dalla cartella di file della shell.</span><span class="sxs-lookup"><span data-stu-id="2927a-116">This has the same value as System.ParsingName for items that are provided by the Shell's file folder.</span></span>

<span data-ttu-id="2927a-117">Nella tabella seguente sono elencati esempi di valori di proprietà Path e FileName:</span><span class="sxs-lookup"><span data-stu-id="2927a-117">The following table lists examples of path and filename property values:</span></span>



| <span data-ttu-id="2927a-118">Percorso</span><span class="sxs-lookup"><span data-stu-id="2927a-118">Path</span></span>                               | <span data-ttu-id="2927a-119">Valore della proprietà</span><span class="sxs-lookup"><span data-stu-id="2927a-119">Property Value</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="2927a-120">c: \\ file \\ personali \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="2927a-120">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="2927a-121">hello.txt</span><span class="sxs-lookup"><span data-stu-id="2927a-121">hello.txt</span></span>      |
| <span data-ttu-id="2927a-122">\\\\\\condivisione server \\ mydir \\news.doc</span><span class="sxs-lookup"><span data-stu-id="2927a-122">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="2927a-123">news.doc</span><span class="sxs-lookup"><span data-stu-id="2927a-123">news.doc</span></span>       |
| <span data-ttu-id="2927a-124">\\\\\\numbers.xls condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="2927a-124">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="2927a-125">numbers.xls</span><span class="sxs-lookup"><span data-stu-id="2927a-125">numbers.xls</span></span>    |
| <span data-ttu-id="2927a-126">c: \\ Stuff \\ cartella</span><span class="sxs-lookup"><span data-stu-id="2927a-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="2927a-127">MyFolder</span><span class="sxs-lookup"><span data-stu-id="2927a-127">MyFolder</span></span>       |
| <span data-ttu-id="2927a-128">\[Messaggio di posta elettronica\]</span><span class="sxs-lookup"><span data-stu-id="2927a-128">\[email message\]</span></span>                  | <span data-ttu-id="2927a-129">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="2927a-129">VT\_EMPTY</span></span>      |
| <span data-ttu-id="2927a-130">\[Song. WMA sul dispositivo portatile\]</span><span class="sxs-lookup"><span data-stu-id="2927a-130">\[song.wma on portable device\]</span></span>    | <span data-ttu-id="2927a-131">Song. WMA</span><span class="sxs-lookup"><span data-stu-id="2927a-131">song.wma</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="2927a-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2927a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2927a-133">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2927a-133">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2927a-134">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2927a-134">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2927a-135">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2927a-135">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2927a-136">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2927a-136">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2927a-137">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2927a-137">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2927a-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2927a-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2927a-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2927a-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2927a-140">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2927a-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2927a-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2927a-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2927a-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2927a-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2927a-143">drawControl</span><span class="sxs-lookup"><span data-stu-id="2927a-143">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2927a-144">editControl</span><span class="sxs-lookup"><span data-stu-id="2927a-144">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2927a-145">filterControl</span><span class="sxs-lookup"><span data-stu-id="2927a-145">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2927a-146">queryControl</span><span class="sxs-lookup"><span data-stu-id="2927a-146">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
