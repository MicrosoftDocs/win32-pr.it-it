---
description: Questa stringa deve essere impostata sulla versione fonetica del nome visualizzato come definito in System. ItemNameDisplay nelle impostazioni locali CJK (CHS pinyin, JPN hiragana, KOR KOR e così via).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232716"
---
# <a name="systemitemnamesortoverride"></a><span data-ttu-id="6c4a9-103">System. ItemNameSortOverride</span><span class="sxs-lookup"><span data-stu-id="6c4a9-103">System.ItemNameSortOverride</span></span>

<span data-ttu-id="6c4a9-104">Questa stringa deve essere impostata sulla versione fonetica del nome visualizzato come definito in System. ItemNameDisplay nelle impostazioni locali CJK (CHS pinyin, JPN hiragana, KOR KOR e così via).</span><span class="sxs-lookup"><span data-stu-id="6c4a9-104">This string should be set to the phonetic version of the display name as defined in System.ItemNameDisplay in CJK locales(CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).</span></span> <span data-ttu-id="6c4a9-105">Il primo carattere di questo campo viene usato anche per raggruppare i nomi in base a FirstLetter.</span><span class="sxs-lookup"><span data-stu-id="6c4a9-105">The first character of this field is also used for grouping names by firstletter.</span></span> <span data-ttu-id="6c4a9-106">Per la maggior parte dei linguaggi non CJK, questo campo non deve essere impostato, nel qual caso verrà usato System. ItemNameDisplay. Tuttavia, se si desidera eseguire l'override della lettera di raggruppamento, ad esempio per rimuovere gli articoli iniziali come "a" e "The", è possibile specificare una stringa alternativa.</span><span class="sxs-lookup"><span data-stu-id="6c4a9-106">For most non-CJK languages, this field does not need to be set (in which case System.ItemNameDisplay will be used).However, if it is desirable to override the grouping letter (for example, to remove leading articles such as "a" and "the"),an alternate string can be provided here.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="6c4a9-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="6c4a9-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6c4a9-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c4a9-108">Remarks</span></span>

<span data-ttu-id="6c4a9-109">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6c4a9-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c4a9-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c4a9-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c4a9-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6c4a9-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6c4a9-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6c4a9-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6c4a9-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6c4a9-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6c4a9-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6c4a9-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6c4a9-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6c4a9-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6c4a9-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="6c4a9-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-122">editControl</span><span class="sxs-lookup"><span data-stu-id="6c4a9-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="6c4a9-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6c4a9-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="6c4a9-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
