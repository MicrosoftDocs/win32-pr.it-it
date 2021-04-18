---
description: Questa proprietà corrisponde a System. search. UrlToIndex con la differenza che include l'ora dell'Ultima modifica apportata all'URL.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316879"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a><span data-ttu-id="cb166-103">System. search. UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="cb166-103">System.Search.UrlToIndexWithModificationTime</span></span>

<span data-ttu-id="cb166-104">Questa proprietà corrisponde a [**System. search. UrlToIndex**](props-system-search-urltoindex.md) con la differenza che include l'ora dell'Ultima modifica apportata all'URL.</span><span class="sxs-lookup"><span data-stu-id="cb166-104">This property is the same as [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) except that it includes the time that the URL was last modified.</span></span> <span data-ttu-id="cb166-105">Si tratta di un'ottimizzazione per l'indicizzatore, in modo da non dover richiamarlo nel gestore di protocollo per richiedere queste informazioni per determinare se il contenuto deve essere indicizzato nuovamente.</span><span class="sxs-lookup"><span data-stu-id="cb166-105">This is an optimization for the indexer so that it does not have to call back into the protocol handler to ask for this information to determine whether the content needs to be indexed again.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="cb166-106">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb166-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a><span data-ttu-id="cb166-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb166-107">Remarks</span></span>

<span data-ttu-id="cb166-108">Questa proprietà [System. search. UrlToIndexWithModificationTime]() equivale alla proprietà [System. search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , con la differenza che si passa anche l'ora dell'Ultima modifica del documento.</span><span class="sxs-lookup"><span data-stu-id="cb166-108">This [System.Search.UrlToIndexWithModificationTime]() property is the same as the [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) property, except that you also pass in the last modified time of the document.</span></span> <span data-ttu-id="cb166-109">Se l'ora dell'Ultima modifica corrisponde, l'indicizzatore presuppone che il documento sia già indicizzato e genera la notifica.</span><span class="sxs-lookup"><span data-stu-id="cb166-109">If the last modified time matches, the indexer assumes that the document is already indexed and throws away the notification.</span></span> <span data-ttu-id="cb166-110">Questa proprietà è un vettore con due elementi, un valore **VT \_ LPWSTR** che contiene l'URL e un valore di **\_ FILETIME VT** che contiene l'ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="cb166-110">This property is a vector with two elements, a **VT\_LPWSTR** value that contains the URL and a **VT\_FILETIME** value that contains the last modified time.</span></span>

<span data-ttu-id="cb166-111">[System. search. UrlToIndexWithModificationTime]() è stato chiamato PID \_ gthr \_ DIRLINK \_ con \_ il tempo nelle versioni precedenti del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="cb166-111">[System.Search.UrlToIndexWithModificationTime]() was called PID\_GTHR\_DIRLINK\_WITH\_TIME in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="cb166-112">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="cb166-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb166-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb166-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cb166-114">[System. search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb166-114">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cb166-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="cb166-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="cb166-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="cb166-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="cb166-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="cb166-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="cb166-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="cb166-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="cb166-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="cb166-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="cb166-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="cb166-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="cb166-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="cb166-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="cb166-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="cb166-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="cb166-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="cb166-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="cb166-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="cb166-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="cb166-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="cb166-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="cb166-126">editControl</span><span class="sxs-lookup"><span data-stu-id="cb166-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="cb166-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="cb166-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="cb166-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="cb166-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
