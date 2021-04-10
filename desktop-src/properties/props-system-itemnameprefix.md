---
description: "Prefisso di un elemento, utilizzato per i messaggi di posta elettronica in cui l'oggetto inizia con il prefisso &\\# 0034; Re: &\\# 0034;."
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966882"
---
# <a name="systemitemnameprefix"></a><span data-ttu-id="c2e6d-103">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="c2e6d-103">System.ItemNamePrefix</span></span>

<span data-ttu-id="c2e6d-104">Prefisso di un elemento, utilizzato per i messaggi di posta elettronica in cui l'oggetto inizia con il prefisso "Re:".</span><span class="sxs-lookup"><span data-stu-id="c2e6d-104">The prefix of an item, used for e-mail messages where the subject begins with the prefix "Re:".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="c2e6d-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2e6d-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="c2e6d-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2e6d-106">Remarks</span></span>

<span data-ttu-id="c2e6d-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="c2e6d-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="c2e6d-108">Se l'elemento è un file, il valore di questa proprietà è VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="c2e6d-108">If the item is a file, then the value of this property is VT\_EMPTY.</span></span> <span data-ttu-id="c2e6d-109">Se l'elemento è un messaggio, il valore di questa proprietà corrisponde ai prefissi di inoltro o di risposta (inclusi i due punti di delimitazione, ma senza spazi vuoti) o VT \_ vuoti se non è presente alcun prefisso.</span><span class="sxs-lookup"><span data-stu-id="c2e6d-109">If the item is a message, then the value of this property is the forwarding or reply prefixes (including the delimiting colon, but no whitespace), or VT\_EMPTY if there is no prefix.</span></span>

<span data-ttu-id="c2e6d-110">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="c2e6d-110">Example values:</span></span>



| <span data-ttu-id="c2e6d-111">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="c2e6d-111">System.ItemNamePrefix</span></span> | <span data-ttu-id="c2e6d-112">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="c2e6d-112">System.ItemName</span></span>  | <span data-ttu-id="c2e6d-113">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="c2e6d-113">System.ItemNameDisplay</span></span> |
|-----------------------|------------------|------------------------|
| <span data-ttu-id="c2e6d-114">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c2e6d-114">VT\_EMPTY</span></span>             | <span data-ttu-id="c2e6d-115">"Giorno splendido"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-115">"Great day"</span></span>      | <span data-ttu-id="c2e6d-116">"Giorno splendido"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-116">"Great day"</span></span>            |
| <span data-ttu-id="c2e6d-117">"Re:"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-117">"Re:"</span></span>                 | <span data-ttu-id="c2e6d-118">"Giorno splendido"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-118">"Great day"</span></span>      | <span data-ttu-id="c2e6d-119">"Re: grande giorno"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-119">"Re: Great day"</span></span>        |
| <span data-ttu-id="c2e6d-120">"FWD:"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-120">"Fwd: "</span></span>               | <span data-ttu-id="c2e6d-121">"Budget mensile"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-121">"Monthly budget"</span></span> | <span data-ttu-id="c2e6d-122">"FWD: budget mensile"</span><span class="sxs-lookup"><span data-stu-id="c2e6d-122">"Fwd: Monthly budget"</span></span>  |
| <span data-ttu-id="c2e6d-123">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c2e6d-123">VT\_EMPTY</span></span>             | <span data-ttu-id="c2e6d-124">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="c2e6d-124">accounts.xls</span></span>     | <span data-ttu-id="c2e6d-125">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="c2e6d-125">accounts.xls</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="c2e6d-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2e6d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2e6d-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c2e6d-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c2e6d-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c2e6d-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c2e6d-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c2e6d-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c2e6d-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c2e6d-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c2e6d-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c2e6d-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c2e6d-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="c2e6d-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-138">editControl</span><span class="sxs-lookup"><span data-stu-id="c2e6d-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="c2e6d-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c2e6d-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="c2e6d-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
