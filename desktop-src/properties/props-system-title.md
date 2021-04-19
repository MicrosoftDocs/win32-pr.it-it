---
description: Titolo dell'elemento.
ms.assetid: 8fb948d6-2677-4e5d-b283-8757c3df574d
title: System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee57037a35c08fd3a6be4f4a0ce7a8475f82cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317966"
---
# <a name="systemtitle"></a><span data-ttu-id="b50f9-103">System.Title</span><span class="sxs-lookup"><span data-stu-id="b50f9-103">System.Title</span></span>

<span data-ttu-id="b50f9-104">Titolo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b50f9-104">The title of the item.</span></span> <span data-ttu-id="b50f9-105">Ad esempio, il titolo di un documento, l'oggetto di un messaggio, la didascalia di una foto o il nome di un brano musicale.</span><span class="sxs-lookup"><span data-stu-id="b50f9-105">For example, the title of a document, the subject of a message, the caption of a photo, or the name of a music track.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b50f9-106">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b50f9-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Title
   shellPKey = PKEY_Title
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="b50f9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b50f9-107">Remarks</span></span>

<span data-ttu-id="b50f9-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="b50f9-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="b50f9-109">Questa proprietà esegue il mapping al *titolo* della proprietà del documento OLE.</span><span class="sxs-lookup"><span data-stu-id="b50f9-109">This property maps to the OLE document property *Title*.</span></span> <span data-ttu-id="b50f9-110">[System. title]() è una proprietà comunemente utilizzata, in particolare in elenchi eterogenei di elementi in cui gli elementi possono essere di molti tipi diversi.</span><span class="sxs-lookup"><span data-stu-id="b50f9-110">[System.Title]() is a commonly used property, particularly in heterogeneous lists of items where the items can be of many different types.</span></span> <span data-ttu-id="b50f9-111">È pertanto consigliabile che i gestori delle proprietà compilano questa proprietà anche se è ridondante; un messaggio di posta elettronica, ad esempio, consente di popolare sia System. title che [System. Subject](./props-system-subject.md) con lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="b50f9-111">Therefore, it is recommended that property handlers populate this property even if it is redundant; for example, an e-mail, which would populate both System.Title and [System.Subject](./props-system-subject.md) with the same value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b50f9-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b50f9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b50f9-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b50f9-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b50f9-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="b50f9-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b50f9-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b50f9-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b50f9-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="b50f9-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b50f9-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b50f9-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b50f9-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b50f9-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b50f9-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="b50f9-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b50f9-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="b50f9-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b50f9-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b50f9-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b50f9-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="b50f9-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b50f9-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="b50f9-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b50f9-124">editControl</span><span class="sxs-lookup"><span data-stu-id="b50f9-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b50f9-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="b50f9-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b50f9-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="b50f9-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
