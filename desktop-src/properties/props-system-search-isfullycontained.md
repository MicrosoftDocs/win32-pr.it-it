---
description: Emesso come TRUE da tutti gli elementi figlio di un contenitore, ad esempio un messaggio di posta elettronica o un file compresso con estensione zip, che genera System. search. IsClosedDirectory come TRUE. In questo modo si garantisce che gli elementi figlio siano inclusi nell'indice di ricerca.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530049"
---
# <a name="systemsearchisfullycontained"></a><span data-ttu-id="3c06b-104">System. search. IsFullyContained</span><span class="sxs-lookup"><span data-stu-id="3c06b-104">System.Search.IsFullyContained</span></span>

<span data-ttu-id="3c06b-105">Emesso come **true** da tutti gli elementi figlio di un contenitore, ad esempio un messaggio di posta elettronica o un file compresso con estensione zip, che genera [System. search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) come **true**.</span><span class="sxs-lookup"><span data-stu-id="3c06b-105">Emitted as **TRUE** by all child items of a container (such as an e-mail or a compressed file with a .zip name extension) that emits [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) as **TRUE**.</span></span> <span data-ttu-id="3c06b-106">In questo modo si garantisce che gli elementi figlio siano inclusi nell'indice di ricerca.</span><span class="sxs-lookup"><span data-stu-id="3c06b-106">This ensures that the child items are included in the search index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="3c06b-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c06b-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="3c06b-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c06b-108">Remarks</span></span>

<span data-ttu-id="3c06b-109">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="3c06b-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="3c06b-110">La proprietà [System. search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) consente di ottimizzare le prestazioni dell'indicizzatore consentendo all'indicizzatore di ignorare l'enumerazione degli elementi figlio di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="3c06b-110">The [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) property helps to optimize indexer performance by allowing the indexer to skip the enumeration of a container's child items.</span></span> <span data-ttu-id="3c06b-111">Tuttavia, tali elementi figlio vengono contrassegnati dall'indicizzatore come non visitati e, in quanto tali, verranno eliminati dall'indice.</span><span class="sxs-lookup"><span data-stu-id="3c06b-111">However, those child items are marked by the indexer as not visited, and as such will be deleted from the index.</span></span> <span data-ttu-id="3c06b-112">Con l'emissione di [System. search. IsFullyContained]() come **true**, un elemento non viene eliminato dall'indice, sebbene non sia stato visitato.</span><span class="sxs-lookup"><span data-stu-id="3c06b-112">By emitting [System.Search.IsFullyContained]() as **TRUE**, an item is not deleted from the index despite having not been visited.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c06b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c06b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c06b-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="3c06b-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3c06b-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="3c06b-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3c06b-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="3c06b-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3c06b-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="3c06b-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3c06b-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3c06b-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3c06b-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3c06b-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3c06b-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3c06b-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3c06b-121">numberFormat</span><span class="sxs-lookup"><span data-stu-id="3c06b-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3c06b-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3c06b-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3c06b-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3c06b-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3c06b-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="3c06b-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3c06b-125">editControl</span><span class="sxs-lookup"><span data-stu-id="3c06b-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3c06b-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="3c06b-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3c06b-127">queryControl</span><span class="sxs-lookup"><span data-stu-id="3c06b-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
