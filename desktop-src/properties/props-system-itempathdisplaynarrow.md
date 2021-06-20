---
description: Informazioni sulla proprietà System.ItemPathDisplayNarrow, che rappresenta il percorso di visualizzazione descrittivo dell'elemento.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System.ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84455a8b69ebf42cb91c191d1c275b70eeeb5ac
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403894"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="93184-103">System.ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="93184-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="93184-104">Percorso di visualizzazione descrittivo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="93184-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="93184-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93184-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="93184-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="93184-106">Remarks</span></span>

<span data-ttu-id="93184-107">I valori PKEY sono definiti in Propkey.h.</span><span class="sxs-lookup"><span data-stu-id="93184-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="93184-108">Per ottimizzare una colonna di visualizzazione ridotta, il formato della stringa deve essere personalizzato in modo che il nome venga visualizzato per primo.</span><span class="sxs-lookup"><span data-stu-id="93184-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="93184-109">Se l'elemento è un file, il valore della proprietà esclude l'estensione di file, ma include i nomi localizzati, se presenti.</span><span class="sxs-lookup"><span data-stu-id="93184-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="93184-110">Se l'elemento è un messaggio, il valore include [System.ItemNamePrefix.](./props-system-itemnameprefix.md)</span><span class="sxs-lookup"><span data-stu-id="93184-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="93184-111">Per analizzare il percorso di un elemento, [usare System.ItemUrl](./props-system-itemurl.md) [o System.ParsingPath.](./props-system-parsingpath.md)</span><span class="sxs-lookup"><span data-stu-id="93184-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="93184-112">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="93184-112">Example values:</span></span>



| <span data-ttu-id="93184-113">Percorso</span><span class="sxs-lookup"><span data-stu-id="93184-113">Path</span></span>                                   | <span data-ttu-id="93184-114">ItemPathDisplayName</span><span class="sxs-lookup"><span data-stu-id="93184-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="93184-115">c: \\ barra mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="93184-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="93184-116">hello (c: \\ barra \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="93184-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="93184-117">\\\\condivisione \\ server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="93184-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="93184-118">goodnews \\ \\ (condivisione \\ server \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="93184-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="93184-119">\\\\cartella \\ di condivisione \\ server</span><span class="sxs-lookup"><span data-stu-id="93184-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="93184-120">folder \\ \\ (condivisione \\ server)</span><span class="sxs-lookup"><span data-stu-id="93184-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="93184-121">c: \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="93184-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="93184-122">Cartella (c: \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="93184-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="93184-123">/Mailbox Account/Inbox/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="93184-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="93184-124">Re: Hello!</span><span class="sxs-lookup"><span data-stu-id="93184-124">Re: Hello!</span></span> <span data-ttu-id="93184-125">(/Account cassetta postale/Posta in arrivo)</span><span class="sxs-lookup"><span data-stu-id="93184-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="93184-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93184-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93184-127">proprietàDescrizione</span><span class="sxs-lookup"><span data-stu-id="93184-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="93184-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="93184-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="93184-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="93184-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="93184-130">Typeinfo</span><span class="sxs-lookup"><span data-stu-id="93184-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="93184-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="93184-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="93184-132">Stringformat</span><span class="sxs-lookup"><span data-stu-id="93184-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="93184-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="93184-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="93184-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="93184-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="93184-135">Datetimeformat</span><span class="sxs-lookup"><span data-stu-id="93184-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="93184-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="93184-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="93184-137">DrawControl</span><span class="sxs-lookup"><span data-stu-id="93184-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="93184-138">editControl</span><span class="sxs-lookup"><span data-stu-id="93184-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="93184-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="93184-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="93184-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="93184-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
