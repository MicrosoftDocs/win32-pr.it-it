---
description: Questa proprietà è simile a System. ItemNameDisplay, con la differenza che è impostata solo per le cartelle, per i file sarà vuota.
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. FolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60922054e80a6589bcb04c3962a4527ee62eaf7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313961"
---
# <a name="systemfoldernamedisplay"></a><span data-ttu-id="f3eff-103">System. FolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="f3eff-103">System.FolderNameDisplay</span></span>

<span data-ttu-id="f3eff-104">Questa proprietà è simile a System. ItemNameDisplay, con la differenza che è impostata solo per le cartelle, per i file sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="f3eff-104">This property is similar to System.ItemNameDisplay except it is only set for folders, for files it will be empty.</span></span> <span data-ttu-id="f3eff-105">Questa operazione è utile per separare i file e le cartelle utilizzando come prima chiave di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="f3eff-105">This is useful to segregate files and folders by using this as the first sort key.</span></span> <span data-ttu-id="f3eff-106">Quando System. ItemDate viene usato come seconda chiave di ordinamento, produce i risultati con le cartelle prima ordinate in base al nome, quindi i file ordinati per data.</span><span class="sxs-lookup"><span data-stu-id="f3eff-106">When System.ItemDate is used as a second sort key it produces results with folders first ordered by name, then files ordered by date.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="f3eff-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f3eff-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="f3eff-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3eff-108">Remarks</span></span>

<span data-ttu-id="f3eff-109">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="f3eff-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3eff-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3eff-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3eff-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f3eff-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f3eff-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f3eff-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f3eff-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f3eff-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f3eff-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f3eff-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f3eff-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f3eff-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f3eff-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f3eff-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f3eff-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f3eff-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f3eff-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f3eff-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f3eff-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f3eff-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f3eff-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f3eff-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f3eff-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="f3eff-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f3eff-122">editControl</span><span class="sxs-lookup"><span data-stu-id="f3eff-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f3eff-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="f3eff-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f3eff-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="f3eff-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
