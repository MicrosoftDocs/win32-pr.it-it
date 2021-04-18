---
description: Emesso da un IFilter del contenitore per ogni URL figlio all'interno del contenitore. Gli elementi figlio vengono infine sottoposti a ricerca per indicizzazione dall'indicizzatore se sono inclusi nell'ambito.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. search. UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313473"
---
# <a name="systemsearchurltoindex"></a><span data-ttu-id="19033-104">System. search. UrlToIndex</span><span class="sxs-lookup"><span data-stu-id="19033-104">System.Search.UrlToIndex</span></span>

<span data-ttu-id="19033-105">Emesso da un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) del contenitore per ogni URL figlio all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="19033-105">Emitted by a container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) for each child URL within the container.</span></span> <span data-ttu-id="19033-106">Gli elementi figlio vengono infine sottoposti a ricerca per indicizzazione dall'indicizzatore se sono inclusi nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="19033-106">The children are eventually crawled by the indexer if they are within scope.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="19033-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19033-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="19033-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="19033-108">Remarks</span></span>

<span data-ttu-id="19033-109">Questa proprietà contiene un URL e viene emessa da un gestore di protocollo per ogni URL figlio o directory nell'URL corrente.</span><span class="sxs-lookup"><span data-stu-id="19033-109">This property contains a URL and is emitted by a protocol handler for each child URL or directoy under the current URL.</span></span> <span data-ttu-id="19033-110">L'indicizzatore richiama il gestore di protocollo e richiede che il documento venga indicizzato.</span><span class="sxs-lookup"><span data-stu-id="19033-110">The indexer calls back into the protocol handler, and asks for that document to be indexed.</span></span> <span data-ttu-id="19033-111">[System. search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) è stato chiamato PID \_ gthr \_ DIRLINK nelle versioni precedenti del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="19033-111">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) was called PID\_GTHR\_DIRLINK in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="19033-112">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="19033-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19033-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19033-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19033-114">System. search. UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="19033-114">System.Search.UrlToIndexWithModificationTime</span></span>](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

[<span data-ttu-id="19033-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="19033-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="19033-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="19033-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="19033-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="19033-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="19033-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="19033-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="19033-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="19033-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="19033-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="19033-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="19033-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="19033-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="19033-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="19033-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="19033-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="19033-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="19033-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="19033-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="19033-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="19033-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="19033-126">editControl</span><span class="sxs-lookup"><span data-stu-id="19033-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="19033-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="19033-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="19033-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="19033-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
