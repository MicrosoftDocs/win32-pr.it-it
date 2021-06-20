---
description: Informazioni sulla proprietà System.ItemFolderPathDisplay, che rappresenta il percorso di visualizzazione descrittivo della cartella padre di un elemento.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System.ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12909b29790ea2c016154cea9fccf7c53e45630
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403934"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="63f89-103">System.ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="63f89-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="63f89-104">Percorso di visualizzazione descrittivo della cartella padre di un elemento.</span><span class="sxs-lookup"><span data-stu-id="63f89-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="63f89-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63f89-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="63f89-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="63f89-106">Remarks</span></span>

<span data-ttu-id="63f89-107">I valori PKEY sono definiti in Propkey.h.</span><span class="sxs-lookup"><span data-stu-id="63f89-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="63f89-108">Se [System.ItemPathDisplay è](./props-system-itempathdisplay.md) VT \_ EMPTY, anche questa proprietà deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="63f89-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="63f89-109">In caso contrario, deve essere derivato in modo appropriato dall'origine dati da System.ItemPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="63f89-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="63f89-110">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="63f89-110">Example values:</span></span>



| <span data-ttu-id="63f89-111">Percorso</span><span class="sxs-lookup"><span data-stu-id="63f89-111">Path</span></span>                                   | <span data-ttu-id="63f89-112">ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="63f89-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="63f89-113">c: \\ file \\ personali \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="63f89-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="63f89-114">c: \\ file \\ personali</span><span class="sxs-lookup"><span data-stu-id="63f89-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="63f89-115">\\\\condivisione \\ server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="63f89-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="63f89-116">\\\\condivisione \\ server \\ mydir</span><span class="sxs-lookup"><span data-stu-id="63f89-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="63f89-117">\\\\condivisione \\ server \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="63f89-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="63f89-118">\\\\condivisione \\ server</span><span class="sxs-lookup"><span data-stu-id="63f89-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="63f89-119">c: \\ food \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="63f89-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="63f89-120">c: \\ food</span><span class="sxs-lookup"><span data-stu-id="63f89-120">c:\\food</span></span>                 |
| <span data-ttu-id="63f89-121">/Mailbox Account/Inbox/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="63f89-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="63f89-122">/Mailbox Account/Inbox</span><span class="sxs-lookup"><span data-stu-id="63f89-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="63f89-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63f89-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63f89-124">proprietàDescrizione</span><span class="sxs-lookup"><span data-stu-id="63f89-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="63f89-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="63f89-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="63f89-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="63f89-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="63f89-127">Typeinfo</span><span class="sxs-lookup"><span data-stu-id="63f89-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="63f89-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="63f89-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="63f89-129">Stringformat</span><span class="sxs-lookup"><span data-stu-id="63f89-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="63f89-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="63f89-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="63f89-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="63f89-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="63f89-132">Datetimeformat</span><span class="sxs-lookup"><span data-stu-id="63f89-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="63f89-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="63f89-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="63f89-134">DrawControl</span><span class="sxs-lookup"><span data-stu-id="63f89-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="63f89-135">editControl</span><span class="sxs-lookup"><span data-stu-id="63f89-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="63f89-136">filterControl</span><span class="sxs-lookup"><span data-stu-id="63f89-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="63f89-137">queryControl</span><span class="sxs-lookup"><span data-stu-id="63f89-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
