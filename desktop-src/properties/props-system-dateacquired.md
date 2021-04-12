---
description: Data di acquisizione del file o del supporto.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233591"
---
# <a name="systemdateacquired"></a><span data-ttu-id="22cbe-103">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="22cbe-103">System.DateAcquired</span></span>

<span data-ttu-id="22cbe-104">Data di acquisizione del file o del supporto.</span><span class="sxs-lookup"><span data-stu-id="22cbe-104">The acquisition date of the file or media.</span></span> <span data-ttu-id="22cbe-105">Questa proprietà è correlata a un utente o a un gruppo di utenti specifico.</span><span class="sxs-lookup"><span data-stu-id="22cbe-105">This property is related to a particular user or group of users.</span></span> <span data-ttu-id="22cbe-106">Questi dati, ad esempio, vengono usati come asse di ordinamento principale per la cartella virtuale **New Music**, che consente agli utenti di esplorare le aggiunte più recenti alla propria raccolta.</span><span class="sxs-lookup"><span data-stu-id="22cbe-106">For example, this data is used as the main sorting axis for the virtual folder **New Music**, which enables people to browse the latest additions to their collection.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="22cbe-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="22cbe-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a><span data-ttu-id="22cbe-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22cbe-108">Windows Vista</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a><span data-ttu-id="22cbe-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="22cbe-109">Remarks</span></span>

<span data-ttu-id="22cbe-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="22cbe-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="22cbe-111">[DateAcquired]() viene archiviato come valore nel flusso principale del file, ma potrebbe non essere sempre presente.</span><span class="sxs-lookup"><span data-stu-id="22cbe-111">[DateAcquired]() is stored as a value in the main stream of the file, but it may not always be present.</span></span> <span data-ttu-id="22cbe-112">In tali casi, la data di acquisizione può essere approssimata in base alle altre date note per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="22cbe-112">In those instances, the acquisition date can be approximated based on other known dates for the content.</span></span> <span data-ttu-id="22cbe-113">Il gestore di metadati deve usare un set di regole per determinare la data da restituire.</span><span class="sxs-lookup"><span data-stu-id="22cbe-113">The metadata handler should use a set of rules to determine the date to return.</span></span> <span data-ttu-id="22cbe-114">Nell'esempio seguente viene illustrato questo per i file musicali.</span><span class="sxs-lookup"><span data-stu-id="22cbe-114">The following example demonstrates this for music files.</span></span>

-   <span data-ttu-id="22cbe-115">Per la musica acquistata, è consigliabile usare l'ora di creazione del file se non è presente alcuna data acquisita.</span><span class="sxs-lookup"><span data-stu-id="22cbe-115">For purchased music, the file's creation time should be used if no acquired date is present.</span></span> <span data-ttu-id="22cbe-116">Tuttavia, il provider di download deve impostare la proprietà [DateAcquired]() nel file.</span><span class="sxs-lookup"><span data-stu-id="22cbe-116">However, the download provider should set the [DateAcquired]() property in the file.</span></span>
-   <span data-ttu-id="22cbe-117">Per i file musicali che l'utente o il gruppo ha copiato (copiando musica o video da un CD o DVD a un disco rigido), la data di acquisizione deve essere la data in cui si è verificata l'azione.</span><span class="sxs-lookup"><span data-stu-id="22cbe-117">For music files that the user or group "ripped" (copying music or video from a CD or DVD to a hard disk), the acquisition date should be the date that action took place.</span></span> <span data-ttu-id="22cbe-118">Ad esempio, l'attributo [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="22cbe-118">For instance, the [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) attribute.</span></span>
-   <span data-ttu-id="22cbe-119">Per la musica copiata da un altro percorso, è necessario usare l'ora di creazione del file come data di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="22cbe-119">For music copied from another location, the file's creation time should be used as the acquisition date.</span></span>

<span data-ttu-id="22cbe-120">Esempi di [System. DateAcquired]() sono la data e l'ora in cui le immagini vengono acquistate da una fotocamera o quando la musica viene acquistata online.</span><span class="sxs-lookup"><span data-stu-id="22cbe-120">Examples of [System.DateAcquired]() are the date and time when pictures are acquired from a camera or when music is purchased online.</span></span> <span data-ttu-id="22cbe-121">Questa operazione non corrisponde a [System. DateImported](./props-system-dateimported.md).</span><span class="sxs-lookup"><span data-stu-id="22cbe-121">This is not the same as [System.DateImported](./props-system-dateimported.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22cbe-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22cbe-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22cbe-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="22cbe-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="22cbe-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="22cbe-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="22cbe-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="22cbe-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="22cbe-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="22cbe-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="22cbe-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="22cbe-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="22cbe-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="22cbe-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="22cbe-129">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="22cbe-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="22cbe-130">numberFormat</span><span class="sxs-lookup"><span data-stu-id="22cbe-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="22cbe-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="22cbe-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="22cbe-132">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="22cbe-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="22cbe-133">drawControl</span><span class="sxs-lookup"><span data-stu-id="22cbe-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="22cbe-134">editControl</span><span class="sxs-lookup"><span data-stu-id="22cbe-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="22cbe-135">filterControl</span><span class="sxs-lookup"><span data-stu-id="22cbe-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="22cbe-136">queryControl</span><span class="sxs-lookup"><span data-stu-id="22cbe-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
