---
description: Percorso di visualizzazione semplice e intuitivo della cartella padre di un elemento.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System. ItemFolderPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898927c23aae95b5037919c908a3ae86e020e1fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050089"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="b7bf6-103">System. ItemFolderPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="b7bf6-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="b7bf6-104">Percorso di visualizzazione semplice e intuitivo della cartella padre di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b7bf6-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b7bf6-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7bf6-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="b7bf6-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7bf6-106">Remarks</span></span>

<span data-ttu-id="b7bf6-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="b7bf6-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="b7bf6-108">Il formato della stringa deve essere personalizzato in modo che il nome della cartella venga innanzitutto ottimizzato per una colonna di visualizzazione ristretta.</span><span class="sxs-lookup"><span data-stu-id="b7bf6-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="b7bf6-109">Se la cartella è una cartella di file, il valore include tutti i nomi localizzati.</span><span class="sxs-lookup"><span data-stu-id="b7bf6-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="b7bf6-110">Se [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) è un VT \_ vuoto, anche questa proprietà deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="b7bf6-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="b7bf6-111">In caso contrario, deve essere derivato in modo appropriato dall'origine dati da System. ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="b7bf6-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7bf6-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7bf6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7bf6-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b7bf6-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="b7bf6-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b7bf6-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="b7bf6-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b7bf6-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b7bf6-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="b7bf6-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="b7bf6-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b7bf6-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="b7bf6-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="b7bf6-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-124">editControl</span><span class="sxs-lookup"><span data-stu-id="b7bf6-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="b7bf6-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b7bf6-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="b7bf6-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
