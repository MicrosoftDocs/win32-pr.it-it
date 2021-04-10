---
description: Nome descrittivo del tipo dell'elemento.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227273"
---
# <a name="systemitemtypetext"></a><span data-ttu-id="49404-103">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="49404-103">System.ItemTypeText</span></span>

<span data-ttu-id="49404-104">Nome descrittivo del tipo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="49404-104">The user-friendly type name of the item.</span></span> <span data-ttu-id="49404-105">Questo valore non può essere analizzato a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="49404-105">This value is not intended to be programmatically parsed.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="49404-106">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49404-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="49404-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="49404-107">Remarks</span></span>

<span data-ttu-id="49404-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="49404-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="49404-109">Se [System. ItemType](./props-system-itemtype.md) è VT \_ vuoto, anche il valore di questa proprietà è VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="49404-109">If [System.ItemType](./props-system-itemtype.md) is VT\_EMPTY, the value of this property is also VT\_EMPTY.</span></span> <span data-ttu-id="49404-110">Se l'elemento è un file, il valore di questa proprietà è uguale a quello di se il valore System. ItemType del file è stato passato a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span><span class="sxs-lookup"><span data-stu-id="49404-110">If the item is a file, the value of this property is the same as if you passed the file's System.ItemType value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span></span>

<span data-ttu-id="49404-111">Questa proprietà non deve essere confusa con [System. Kind](./props-system-kind.md), che è un nome di tipo di alto livello descrittivo.</span><span class="sxs-lookup"><span data-stu-id="49404-111">This property should not be confused with [System.Kind](./props-system-kind.md), which is a high-level, user-friendly kind name.</span></span> <span data-ttu-id="49404-112">Per un file di documento con estensione doc, ad esempio, le varie proprietà sono illustrate di seguito:</span><span class="sxs-lookup"><span data-stu-id="49404-112">For example, for a .doc document file, the various properties are as shown here:</span></span>



| <span data-ttu-id="49404-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="49404-113">Property</span></span>                                               | <span data-ttu-id="49404-114">Valore</span><span class="sxs-lookup"><span data-stu-id="49404-114">Value</span></span>                   |
|--------------------------------------------------------|-------------------------|
| [<span data-ttu-id="49404-115">System. Kind</span><span class="sxs-lookup"><span data-stu-id="49404-115">System.Kind</span></span>](./props-system-kind.md)                 | <span data-ttu-id="49404-116">Documento</span><span class="sxs-lookup"><span data-stu-id="49404-116">Document</span></span>                |
| [<span data-ttu-id="49404-117">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="49404-117">System.ItemType</span></span>](./props-system-itemtype.md)         | <span data-ttu-id="49404-118">doc</span><span class="sxs-lookup"><span data-stu-id="49404-118">.doc</span></span>                    |
| [<span data-ttu-id="49404-119">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="49404-119">System.ItemTypeText</span></span>]() | <span data-ttu-id="49404-120">Documento di Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="49404-120">Microsoft Word Document</span></span> |



 

<span data-ttu-id="49404-121">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="49404-121">Example values:</span></span>



| <span data-ttu-id="49404-122">Percorso</span><span class="sxs-lookup"><span data-stu-id="49404-122">Path</span></span>                                   | <span data-ttu-id="49404-123">ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="49404-123">ItemTypeText</span></span>            |
|----------------------------------------|-------------------------|
| <span data-ttu-id="49404-124">c: \\ \\hello.txt della barra mydir \\</span><span class="sxs-lookup"><span data-stu-id="49404-124">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="49404-125">File di testo</span><span class="sxs-lookup"><span data-stu-id="49404-125">Text File</span></span>               |
| <span data-ttu-id="49404-126">\\\\\\condivisione server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="49404-126">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="49404-127">Documento di Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="49404-127">Microsoft Word Document</span></span> |
| <span data-ttu-id="49404-128">\\\\\\cartella condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="49404-128">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="49404-129">Cartella di file</span><span class="sxs-lookup"><span data-stu-id="49404-129">File Folder</span></span>             |
| <span data-ttu-id="49404-130">c: \\ mydir \\ cartella</span><span class="sxs-lookup"><span data-stu-id="49404-130">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="49404-131">Cartella di file</span><span class="sxs-lookup"><span data-stu-id="49404-131">File Folder</span></span>             |
| <span data-ttu-id="49404-132">/Mailbox account/Inbox/' re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="49404-132">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="49404-133">Messaggio di posta elettronica di Outlook</span><span class="sxs-lookup"><span data-stu-id="49404-133">Outlook E-Mail Message</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="49404-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49404-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49404-135">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="49404-135">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="49404-136">searchInfo</span><span class="sxs-lookup"><span data-stu-id="49404-136">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="49404-137">labelInfo</span><span class="sxs-lookup"><span data-stu-id="49404-137">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="49404-138">typeInfo</span><span class="sxs-lookup"><span data-stu-id="49404-138">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="49404-139">displayInfo</span><span class="sxs-lookup"><span data-stu-id="49404-139">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="49404-140">stringFormat</span><span class="sxs-lookup"><span data-stu-id="49404-140">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="49404-141">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="49404-141">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="49404-142">numberFormat</span><span class="sxs-lookup"><span data-stu-id="49404-142">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="49404-143">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="49404-143">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="49404-144">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="49404-144">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="49404-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="49404-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="49404-146">editControl</span><span class="sxs-lookup"><span data-stu-id="49404-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="49404-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="49404-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="49404-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="49404-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
