---
description: Percorso di visualizzazione semplice e intuitivo della cartella padre di un elemento.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311340"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="71f33-103">System. ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="71f33-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="71f33-104">Percorso di visualizzazione semplice e intuitivo della cartella padre di un elemento.</span><span class="sxs-lookup"><span data-stu-id="71f33-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="71f33-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71f33-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="71f33-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="71f33-106">Remarks</span></span>

<span data-ttu-id="71f33-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="71f33-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="71f33-108">Se [System. ItemPathDisplay](./props-system-itempathdisplay.md) è un VT \_ vuoto, anche questa proprietà deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="71f33-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="71f33-109">In caso contrario, deve essere derivato in modo appropriato dall'origine dati da System. ItemPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="71f33-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="71f33-110">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="71f33-110">Example values:</span></span>



| <span data-ttu-id="71f33-111">Percorso</span><span class="sxs-lookup"><span data-stu-id="71f33-111">Path</span></span>                                   | <span data-ttu-id="71f33-112">ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="71f33-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="71f33-113">c: \\ file \\ personali \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="71f33-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="71f33-114">c: \\ file \\ personali</span><span class="sxs-lookup"><span data-stu-id="71f33-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="71f33-115">\\\\\\condivisione server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="71f33-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="71f33-116">\\\\\\mydir condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="71f33-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="71f33-117">\\\\\\numbers.xls condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="71f33-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="71f33-118">\\\\\\condivisione server</span><span class="sxs-lookup"><span data-stu-id="71f33-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="71f33-119">c: \\ cartella di alimenti \\</span><span class="sxs-lookup"><span data-stu-id="71f33-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="71f33-120">c: \\ cibo</span><span class="sxs-lookup"><span data-stu-id="71f33-120">c:\\food</span></span>                 |
| <span data-ttu-id="71f33-121">/Mailbox account/Inbox/' re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="71f33-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="71f33-122">Account/posta in arrivo di/Mailbox</span><span class="sxs-lookup"><span data-stu-id="71f33-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="71f33-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71f33-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f33-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="71f33-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="71f33-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="71f33-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="71f33-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="71f33-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="71f33-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="71f33-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="71f33-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="71f33-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="71f33-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="71f33-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="71f33-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="71f33-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="71f33-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="71f33-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="71f33-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="71f33-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="71f33-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="71f33-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="71f33-134">drawControl</span><span class="sxs-lookup"><span data-stu-id="71f33-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="71f33-135">editControl</span><span class="sxs-lookup"><span data-stu-id="71f33-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="71f33-136">filterControl</span><span class="sxs-lookup"><span data-stu-id="71f33-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="71f33-137">queryControl</span><span class="sxs-lookup"><span data-stu-id="71f33-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
