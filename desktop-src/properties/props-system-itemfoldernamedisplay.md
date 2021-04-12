---
description: Nome visualizzato descrittivo della cartella padre di un elemento.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232500"
---
# <a name="systemitemfoldernamedisplay"></a><span data-ttu-id="0b7f6-103">System. ItemFolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="0b7f6-103">System.ItemFolderNameDisplay</span></span>

<span data-ttu-id="0b7f6-104">Nome visualizzato descrittivo della cartella padre di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-104">The user-friendly display name of an item's parent folder.</span></span>

<span data-ttu-id="0b7f6-105">Questa operazione deriva da [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="0b7f6-105">This is derived from [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span></span> <span data-ttu-id="0b7f6-106">Se la proprietà è VT \_ vuota, anche questa proprietà deve essere.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-106">If that property is VT\_EMPTY, then this property should be too.</span></span>

<span data-ttu-id="0b7f6-107">Se la cartella è una cartella di file, il valore verrà localizzato se è disponibile un nome localizzato.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-107">If the folder is a file folder, the value will be localized if a localized name is available.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="0b7f6-108">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b7f6-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="0b7f6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b7f6-109">Remarks</span></span>

<span data-ttu-id="0b7f6-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="0b7f6-111">Se [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) è un VT \_ vuoto, anche questa proprietà deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-111">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="0b7f6-112">In caso contrario, deve essere derivato in modo appropriato dall'origine dati da System. ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-112">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

<span data-ttu-id="0b7f6-113">Esempi:</span><span class="sxs-lookup"><span data-stu-id="0b7f6-113">Examples:</span></span>



| <span data-ttu-id="0b7f6-114">Percorso specificato</span><span class="sxs-lookup"><span data-stu-id="0b7f6-114">Given path</span></span>                             | <span data-ttu-id="0b7f6-115">Nome visualizzato cartella</span><span class="sxs-lookup"><span data-stu-id="0b7f6-115">Folder Display Name</span></span> |
|----------------------------------------|---------------------|
| <span data-ttu-id="0b7f6-116">c: \\ MyFile \\ testo \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="0b7f6-116">c:\\MyFiles\\Text\\hello.txt</span></span>           | <span data-ttu-id="0b7f6-117">Testo</span><span class="sxs-lookup"><span data-stu-id="0b7f6-117">Text</span></span>                |
| <span data-ttu-id="0b7f6-118">\\\\\\condivisione server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="0b7f6-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="0b7f6-119">mydir</span><span class="sxs-lookup"><span data-stu-id="0b7f6-119">mydir</span></span>               |
| <span data-ttu-id="0b7f6-120">\\\\\\numbers.xls condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="0b7f6-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="0b7f6-121">condividi</span><span class="sxs-lookup"><span data-stu-id="0b7f6-121">share</span></span>               |
| <span data-ttu-id="0b7f6-122">c: \\ cartelle \\ cartella</span><span class="sxs-lookup"><span data-stu-id="0b7f6-122">c:\\Folders\\MyFolder</span></span>                  | <span data-ttu-id="0b7f6-123">Cartelle</span><span class="sxs-lookup"><span data-stu-id="0b7f6-123">Folders</span></span>             |
| <span data-ttu-id="0b7f6-124">/Mailbox account/Inbox/' re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="0b7f6-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="0b7f6-125">Posta in arrivo</span><span class="sxs-lookup"><span data-stu-id="0b7f6-125">Inbox</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="0b7f6-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b7f6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b7f6-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0b7f6-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0b7f6-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0b7f6-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7f6-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0b7f6-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0b7f6-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0b7f6-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0b7f6-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0b7f6-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0b7f6-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="0b7f6-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-138">editControl</span><span class="sxs-lookup"><span data-stu-id="0b7f6-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="0b7f6-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0b7f6-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="0b7f6-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
