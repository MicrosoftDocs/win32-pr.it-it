---
description: Percorso di visualizzazione intuitivo per l'elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131574"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="13803-103">System. ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="13803-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="13803-104">Percorso di visualizzazione intuitivo per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="13803-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="13803-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13803-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="13803-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="13803-106">Remarks</span></span>

<span data-ttu-id="13803-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="13803-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="13803-108">Se l'elemento è un file o una cartella, questa proprietà include l'estensione in tutti i casi ed è localizzata se è disponibile un nome localizzato.</span><span class="sxs-lookup"><span data-stu-id="13803-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="13803-109">Per gli altri elementi, questo è l'equivalente intuitivo, supponendo che l'elemento esista nell'archivio gerarchico.</span><span class="sxs-lookup"><span data-stu-id="13803-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="13803-110">Diversamente da [System. ItemUrl](./props-system-itemurl.md), il valore di questa proprietà non include lo schema URL.</span><span class="sxs-lookup"><span data-stu-id="13803-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="13803-111">Per analizzare un percorso di elemento, usare System. ItemUrl o [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="13803-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="13803-112">Per fare riferimento agli elementi dello spazio dei nomi della shell usando le API della shell, usare System. ParsingPath.</span><span class="sxs-lookup"><span data-stu-id="13803-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="13803-113">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="13803-113">Example values:</span></span>



| <span data-ttu-id="13803-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="13803-114">Path</span></span>                                   | <span data-ttu-id="13803-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="13803-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="13803-116">c: \\ \\hello.txt della barra mydir \\</span><span class="sxs-lookup"><span data-stu-id="13803-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="13803-117">c: \\ \\hello.txt della barra mydir \\</span><span class="sxs-lookup"><span data-stu-id="13803-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="13803-118">\\\\\\condivisione server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="13803-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="13803-119">\\\\\\condivisione server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="13803-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="13803-120">\\\\\\numbers.xls condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="13803-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="13803-121">\\\\\\numbers.xls condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="13803-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="13803-122">c: \\ mydir \\ cartella</span><span class="sxs-lookup"><span data-stu-id="13803-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="13803-123">c: \\ mydir \\ cartella</span><span class="sxs-lookup"><span data-stu-id="13803-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="13803-124">/Mailbox account/Inbox/' re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="13803-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="13803-125">/Mailbox account/Inbox/' re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="13803-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="13803-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13803-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13803-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="13803-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="13803-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="13803-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="13803-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="13803-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="13803-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="13803-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="13803-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="13803-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="13803-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="13803-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="13803-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="13803-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="13803-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="13803-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="13803-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="13803-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="13803-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="13803-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="13803-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="13803-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="13803-138">editControl</span><span class="sxs-lookup"><span data-stu-id="13803-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="13803-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="13803-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="13803-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="13803-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
