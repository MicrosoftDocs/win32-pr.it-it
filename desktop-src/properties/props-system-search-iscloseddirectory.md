---
description: Generato come TRUE da un elemento contenitore per indicare che i relativi elementi figlio non devono essere enumerati da un indicizzatore se l'elemento contenitore non è stato modificato dopo l'ultima ricerca per indicizzazione di verifica indicizzazione.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316881"
---
# <a name="systemsearchiscloseddirectory"></a><span data-ttu-id="40ca7-103">System. search. IsClosedDirectory</span><span class="sxs-lookup"><span data-stu-id="40ca7-103">System.Search.IsClosedDirectory</span></span>

<span data-ttu-id="40ca7-104">Generato come **true** da un elemento contenitore per indicare che i relativi elementi figlio non devono essere enumerati da un indicizzatore se l'elemento contenitore non è stato modificato dopo l'ultima ricerca per indicizzazione di verifica indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="40ca7-104">Emitted as **TRUE** by a container item to indicate that its child items do not need to be enumerated by an indexer if the container item has not changed since the last incremental index verification crawl.</span></span> <span data-ttu-id="40ca7-105">Ciò contribuisce all'ottimizzazione delle prestazioni dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="40ca7-105">This contributes to the optimization of indexer performance.</span></span> <span data-ttu-id="40ca7-106">In questi casi di contenitori (ad esempio un messaggio di posta elettronica con allegati o un file compresso con estensione zip), gli elementi figlio sono inseparabili dal relativo elemento padre.</span><span class="sxs-lookup"><span data-stu-id="40ca7-106">In these container cases (examples are an e-mail with attachments or a compressed file with a .zip name extension), child items are inseparable from their parent item.</span></span> <span data-ttu-id="40ca7-107">Ad esempio, se la proprietà [System. DateModified](./props-system-datemodified.md) di un elemento contenuto cambia, il valore System. DateModified del contenitore viene modificato in modo che corrisponda.</span><span class="sxs-lookup"><span data-stu-id="40ca7-107">For instance, if the [System.DateModified](./props-system-datemodified.md) property of a contained item changes, then the System.DateModified value of the container changes to match.</span></span> <span data-ttu-id="40ca7-108">Inoltre, se un elemento padre viene eliminato, vengono eliminati anche tutti gli elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="40ca7-108">Also, if a parent item is deleted, all of the child items are deleted as well.</span></span> <span data-ttu-id="40ca7-109">Se pertanto il contenitore non è stato modificato, l'indicizzatore sa che non è stato modificato alcun elemento al suo interno e non è necessario aprire il contenitore per esaminare il contenuto singolarmente.</span><span class="sxs-lookup"><span data-stu-id="40ca7-109">Therefore, if the container has not changed, the indexer knows that nothing within it has changed and does not need to open the container to examine the contents individually.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="40ca7-110">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40ca7-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="40ca7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="40ca7-111">Remarks</span></span>

<span data-ttu-id="40ca7-112">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="40ca7-112">PKEY values are defined in Propkey.h.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40ca7-113">Se un elemento genera **true** per questa proprietà, ognuno dei relativi elementi figlio deve creare la proprietà [System. search. IsFullyContained](./props-system-search-isfullycontained.md) su **true** per impedire che tali elementi vengano eliminati dall'indice.</span><span class="sxs-lookup"><span data-stu-id="40ca7-113">If an item emits **TRUE** for this property, each of its child items must emit the [System.Search.IsFullyContained](./props-system-search-isfullycontained.md) property as **TRUE** to prevent those items from being deleted from the index.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="40ca7-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40ca7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ca7-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="40ca7-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="40ca7-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="40ca7-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="40ca7-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="40ca7-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="40ca7-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="40ca7-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="40ca7-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="40ca7-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="40ca7-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="40ca7-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="40ca7-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="40ca7-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="40ca7-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="40ca7-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="40ca7-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="40ca7-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="40ca7-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="40ca7-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="40ca7-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="40ca7-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="40ca7-126">editControl</span><span class="sxs-lookup"><span data-stu-id="40ca7-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="40ca7-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="40ca7-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="40ca7-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="40ca7-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
