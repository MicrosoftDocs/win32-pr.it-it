---
description: Percorso di visualizzazione intuitivo per l'elemento.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233024"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="e5a23-103">System. ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="e5a23-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="e5a23-104">Percorso di visualizzazione intuitivo per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="e5a23-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="e5a23-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5a23-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="e5a23-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5a23-106">Remarks</span></span>

<span data-ttu-id="e5a23-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="e5a23-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="e5a23-108">Per ottimizzare una colonna di visualizzazione più stretta, il formato della stringa deve essere personalizzato in modo che il nome venga visualizzato per primo.</span><span class="sxs-lookup"><span data-stu-id="e5a23-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="e5a23-109">Se l'elemento è un file, il valore della proprietà esclude l'estensione del file, ma include i nomi localizzati, se presenti.</span><span class="sxs-lookup"><span data-stu-id="e5a23-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="e5a23-110">Se l'elemento è un messaggio, il valore include [System. ItemNamePrefix](./props-system-itemnameprefix.md).</span><span class="sxs-lookup"><span data-stu-id="e5a23-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="e5a23-111">Per analizzare un percorso di elemento, usare [System. ItemUrl](./props-system-itemurl.md) o [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="e5a23-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="e5a23-112">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="e5a23-112">Example values:</span></span>



| <span data-ttu-id="e5a23-113">Percorso</span><span class="sxs-lookup"><span data-stu-id="e5a23-113">Path</span></span>                                   | <span data-ttu-id="e5a23-114">ItemPathDisplayName</span><span class="sxs-lookup"><span data-stu-id="e5a23-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="e5a23-115">c: \\ \\hello.txt della barra mydir \\</span><span class="sxs-lookup"><span data-stu-id="e5a23-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="e5a23-116">Hello (c: \\ mydir \\ barra)</span><span class="sxs-lookup"><span data-stu-id="e5a23-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="e5a23-117">\\\\\\condivisione server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="e5a23-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="e5a23-118">goodnews ( \\ \\ server \\ share \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="e5a23-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="e5a23-119">\\\\\\cartella condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="e5a23-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="e5a23-120">cartella ( \\ \\ server \\ share)</span><span class="sxs-lookup"><span data-stu-id="e5a23-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="e5a23-121">c: \\ mydir \\ cartella</span><span class="sxs-lookup"><span data-stu-id="e5a23-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="e5a23-122">Cartella (c: \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="e5a23-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="e5a23-123">/Mailbox account/Inbox/' re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="e5a23-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="e5a23-124">Re: Hello!</span><span class="sxs-lookup"><span data-stu-id="e5a23-124">Re: Hello!</span></span> <span data-ttu-id="e5a23-125">(Account/Mailbox/posta in arrivo)</span><span class="sxs-lookup"><span data-stu-id="e5a23-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e5a23-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5a23-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a23-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e5a23-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e5a23-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e5a23-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e5a23-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e5a23-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e5a23-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e5a23-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e5a23-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e5a23-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e5a23-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e5a23-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e5a23-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e5a23-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e5a23-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e5a23-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e5a23-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e5a23-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e5a23-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e5a23-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e5a23-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="e5a23-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e5a23-138">editControl</span><span class="sxs-lookup"><span data-stu-id="e5a23-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e5a23-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="e5a23-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e5a23-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="e5a23-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
