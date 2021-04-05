---
description: Nome visualizzato nel form &\# 0034; più completo&\# 0034;.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753111"
---
# <a name="systemitemnamedisplay"></a><span data-ttu-id="2d161-103">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="2d161-103">System.ItemNameDisplay</span></span>

<span data-ttu-id="2d161-104">Nome visualizzato nel form "più completo".</span><span class="sxs-lookup"><span data-stu-id="2d161-104">The display name in "most complete" form.</span></span> <span data-ttu-id="2d161-105">Si tratta della rappresentazione univoca del nome dell'elemento più appropriato per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="2d161-105">It is the unique representation of the item name most appropriate for end users.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2d161-106">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d161-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="2d161-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d161-107">Remarks</span></span>

<span data-ttu-id="2d161-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="2d161-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2d161-109">Questo valore è concatentation di [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="2d161-109">This value is the concatentation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span>

<span data-ttu-id="2d161-110">Se l'elemento è un file, questa proprietà include il nome visualizzato, come illustrato in Esplora file.</span><span class="sxs-lookup"><span data-stu-id="2d161-110">If the item is a file, this property includes the display name as shown in File Explorer.</span></span> <span data-ttu-id="2d161-111">Esistono casi accettabili quando [System. FileName](./props-system-filename.md) viene specificato, ma il valore di questa proprietà è completamente diverso.</span><span class="sxs-lookup"><span data-stu-id="2d161-111">There are acceptable cases when [System.FileName](./props-system-filename.md) is given but the value of this property is completely different.</span></span> <span data-ttu-id="2d161-112">I messaggi di posta elettronica rappresentano un valido esempio.</span><span class="sxs-lookup"><span data-stu-id="2d161-112">E-mail messages are a good example.</span></span> <span data-ttu-id="2d161-113">Se l'elemento è un messaggio di posta elettronica, il nome dell'elemento corrisponde in genere al soggetto.</span><span class="sxs-lookup"><span data-stu-id="2d161-113">If the item is an e-mail message, the item name is normally the subject.</span></span> <span data-ttu-id="2d161-114">In tal caso, il valore deve essere la concatenazione di [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="2d161-114">In that case, the value must be the concatenation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span> <span data-ttu-id="2d161-115">Poiché il valore di System. ItemNamePrefix esclude tutti gli spazi finali, la concatenazione deve includere uno spazio durante la generazione di [System. ItemNameDisplay]().</span><span class="sxs-lookup"><span data-stu-id="2d161-115">Since the value of System.ItemNamePrefix excludes any trailing spaces, the concatenation must include a space when generating [System.ItemNameDisplay]().</span></span> <span data-ttu-id="2d161-116">Si noti che questa proprietà non è necessariamente univoca, ma è progettata per promuovere la candidatura più probabile che può essere univoca e anche sensata per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="2d161-116">Note that this property is not guaranteed to be unique, but is designed to promote the most likely candidate that can be unique and also makes sense to end users.</span></span>

<span data-ttu-id="2d161-117">Per i documenti, ad esempio, è possibile usare [System. title](./props-system-title.md) come [System. ItemNameDisplay](), ma in pratica il titolo dei documenti potrebbe non essere utile o sufficientemente univoco per funzionare come unico System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="2d161-117">For example, for documents, the [System.Title](./props-system-title.md) could be used as the [System.ItemNameDisplay](), but in practice the title of the documents may not be useful or unique enough to function as the sole System.ItemNameDisplay.</span></span> <span data-ttu-id="2d161-118">È invece preferibile fornire [System. FileName](./props-system-filename.md) come valore di System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="2d161-118">Instead, providing [System.FileName](./props-system-filename.md) as the value of System.ItemNameDisplay is a better choice.</span></span> <span data-ttu-id="2d161-119">In Windows Mail, i messaggi di posta elettronica vengono archiviati nel file system file con estensione eml.</span><span class="sxs-lookup"><span data-stu-id="2d161-119">In Windows Mail, e-mail is stored in the file system as .eml files.</span></span> <span data-ttu-id="2d161-120">I valori System. FileName per questi file non sono intuitivi perché sono GUID.</span><span class="sxs-lookup"><span data-stu-id="2d161-120">The System.FileName values for those files are not human-friendly as they are GUIDs.</span></span> <span data-ttu-id="2d161-121">In questo esempio la promozione di [System. Subject](./props-system-subject.md) come System. ItemNameDisplay risulta più sensata.</span><span class="sxs-lookup"><span data-stu-id="2d161-121">In this example, promoting [System.Subject](./props-system-subject.md) as System.ItemNameDisplay makes more sense.</span></span>

<span data-ttu-id="2d161-122">**Note sulla compatibilità:**</span><span class="sxs-lookup"><span data-stu-id="2d161-122">**Compatibility notes:**</span></span>

-   <span data-ttu-id="2d161-123">Implementazioni di cartelle della shell in Windows Vista: usare PKEY \_ ItemNameDisplay per la colonna Name quando si desidera che Esplora risorse chiami [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ Normal) per ottenere il valore del nome.</span><span class="sxs-lookup"><span data-stu-id="2d161-123">Shell folder implementations on Windows Vista: use PKEY\_ItemNameDisplay for the name column when you want Windows Explorer to call [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN\_NORMAL) to get the value of the name.</span></span> <span data-ttu-id="2d161-124">Utilizzare un altro PKEY, ad esempio PKEY \_ itemName, quando si desidera che Esplora risorse chiami l'archivio delle proprietà della cartella o [**IShellFolder2:: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) per ottenere il valore del nome.</span><span class="sxs-lookup"><span data-stu-id="2d161-124">Use another PKEY, such as PKEY\_ItemName, when you want Windows Explorer to call either the folder's property store or [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) to get the value of the name.</span></span>
-   <span data-ttu-id="2d161-125">Implementazioni di cartelle della shell in Windows XP: la prima colonna deve essere la colonna Name e Esplora risorse chiama [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per ottenere il valore del nome.</span><span class="sxs-lookup"><span data-stu-id="2d161-125">Shell folder implementations on Windows XP: the first column must be the name column, and Windows Explorer calls [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to get the value of the name.</span></span> <span data-ttu-id="2d161-126">PKEY/SCID non è rilevante.</span><span class="sxs-lookup"><span data-stu-id="2d161-126">The PKEY/SCID does not matter.</span></span>



| <span data-ttu-id="2d161-127">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="2d161-127">Item type</span></span>     | <span data-ttu-id="2d161-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="2d161-128">Example</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="2d161-129">File</span><span class="sxs-lookup"><span data-stu-id="2d161-129">File</span></span>          | <span data-ttu-id="2d161-130">hello.txt</span><span class="sxs-lookup"><span data-stu-id="2d161-130">hello.txt</span></span>                 |
| <span data-ttu-id="2d161-131">Message</span><span class="sxs-lookup"><span data-stu-id="2d161-131">Message</span></span>       | <span data-ttu-id="2d161-132">Re: dove si trova la riunione?</span><span class="sxs-lookup"><span data-stu-id="2d161-132">Re: Where is the meeting?</span></span> |
| <span data-ttu-id="2d161-133">Cartella del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2d161-133">Device folder</span></span> | <span data-ttu-id="2d161-134">Song. WMA</span><span class="sxs-lookup"><span data-stu-id="2d161-134">song.wma</span></span>                  |
| <span data-ttu-id="2d161-135">Cartella</span><span class="sxs-lookup"><span data-stu-id="2d161-135">Folder</span></span>        | <span data-ttu-id="2d161-136">Documenti</span><span class="sxs-lookup"><span data-stu-id="2d161-136">Documents</span></span>                 |



 

## <a name="related-topics"></a><span data-ttu-id="2d161-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d161-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d161-138">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2d161-138">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2d161-139">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2d161-139">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2d161-140">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2d161-140">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2d161-141">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2d161-141">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2d161-142">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2d161-142">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2d161-143">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2d161-143">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2d161-144">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2d161-144">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2d161-145">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2d161-145">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2d161-146">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2d161-146">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2d161-147">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2d161-147">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2d161-148">drawControl</span><span class="sxs-lookup"><span data-stu-id="2d161-148">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2d161-149">editControl</span><span class="sxs-lookup"><span data-stu-id="2d161-149">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2d161-150">filterControl</span><span class="sxs-lookup"><span data-stu-id="2d161-150">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2d161-151">queryControl</span><span class="sxs-lookup"><span data-stu-id="2d161-151">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
