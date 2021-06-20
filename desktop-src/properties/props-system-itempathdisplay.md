---
description: Informazioni sulla proprietà System.ItemPathDisplay, che rappresenta il percorso di visualizzazione descrittivo dell'elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System.ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddad0edbc1a77a3de1fab7956d8ce6e6f906f06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403904"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="d1a3e-103">System.ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="d1a3e-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="d1a3e-104">Percorso di visualizzazione descrittivo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="d1a3e-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1a3e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="d1a3e-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1a3e-106">Remarks</span></span>

<span data-ttu-id="d1a3e-107">I valori PKEY sono definiti in Propkey.h.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="d1a3e-108">Se l'elemento è un file o una cartella, questa proprietà include l'estensione in tutti i casi e viene localizzata se è disponibile un nome localizzato.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="d1a3e-109">Per altri elementi, si tratta dell'equivalente descrittivo, presupponendo che l'elemento esista nell'archiviazione gerarchica.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="d1a3e-110">A [differenza di System.ItemUrl,](./props-system-itemurl.md)questo valore della proprietà non include lo schema URL.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="d1a3e-111">Per analizzare il percorso di un elemento, usare System.ItemUrl [o System.ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="d1a3e-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="d1a3e-112">Per fare riferimento agli elementi dello spazio dei nomi shell usando le API shell, usare System.ParsingPath.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="d1a3e-113">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="d1a3e-113">Example values:</span></span>



| <span data-ttu-id="d1a3e-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="d1a3e-114">Path</span></span>                                   | <span data-ttu-id="d1a3e-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="d1a3e-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="d1a3e-116">c: \\ barra mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="d1a3e-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="d1a3e-117">c: \\ barra mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="d1a3e-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="d1a3e-118">\\\\condivisione \\ server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="d1a3e-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="d1a3e-119">\\\\condivisione \\ server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="d1a3e-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="d1a3e-120">\\\\condivisione \\ \\ servernumbers.xls</span><span class="sxs-lookup"><span data-stu-id="d1a3e-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="d1a3e-121">\\\\condivisione \\ \\ servernumbers.xls</span><span class="sxs-lookup"><span data-stu-id="d1a3e-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="d1a3e-122">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="d1a3e-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="d1a3e-123">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="d1a3e-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="d1a3e-124">/Mailbox Account/Inbox/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="d1a3e-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="d1a3e-125">/Mailbox Account/Inbox/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="d1a3e-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="d1a3e-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1a3e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1a3e-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d1a3e-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d1a3e-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="d1a3e-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-130">Typeinfo</span><span class="sxs-lookup"><span data-stu-id="d1a3e-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d1a3e-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-132">Stringformat</span><span class="sxs-lookup"><span data-stu-id="d1a3e-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="d1a3e-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="d1a3e-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-135">Datetimeformat</span><span class="sxs-lookup"><span data-stu-id="d1a3e-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="d1a3e-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="d1a3e-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-138">editControl</span><span class="sxs-lookup"><span data-stu-id="d1a3e-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="d1a3e-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d1a3e-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="d1a3e-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
