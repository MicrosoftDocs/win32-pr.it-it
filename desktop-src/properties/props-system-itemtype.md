---
description: Tipo canonico dell'elemento.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233580"
---
# <a name="systemitemtype"></a><span data-ttu-id="89141-103">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="89141-103">System.ItemType</span></span>

<span data-ttu-id="89141-104">Tipo canonico dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="89141-104">The canonical type of the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="89141-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89141-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="89141-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="89141-106">Remarks</span></span>

<span data-ttu-id="89141-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="89141-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="89141-108">Il valore di System. ItemType deve essere analizzato a livello di codice e può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="89141-108">The value for System.ItemType is intended to be programmatically parsed, and can be either:</span></span>

-   <span data-ttu-id="89141-109">Estensione di file che punta a un valore ProgID ( \_ radice delle classi HKEY) che \_ \\ <ProgID> contiene il nome visualizzato per il tipo.</span><span class="sxs-lookup"><span data-stu-id="89141-109">A file extension that points to a ProgID value (HKEY\_CLASSES\_ROOT\\<ProgID>) holding the display name for the type.</span></span>
-   <span data-ttu-id="89141-110">Valore ProgID (classi HKEY \_ \_ RROOT \\ <ProgID> ), contenente il nome visualizzato per il tipo.</span><span class="sxs-lookup"><span data-stu-id="89141-110">A ProgID value (HKEY\_CLASSES\_RROOT\\<ProgID>), containing the display name for the type.</span></span>

<span data-ttu-id="89141-111">L'elemento FriendlyTypeName di un ProgID deve essere una versione localizzata del nome dell'applicazione ( @winword.dll ,-42), mentre il valore predefinito della chiave ProgID è un nome non localizzato (Word.Document. 12).</span><span class="sxs-lookup"><span data-stu-id="89141-111">The FriendlyTypeName element of a ProgID should be a localized version of the application name (@winword.dll,-42), while the default value of the ProgID key is a non-localized name (Word.Document.12).</span></span>

<span data-ttu-id="89141-112">Se non è presente alcun tipo canonico, il valore è VT \_ vuoto.</span><span class="sxs-lookup"><span data-stu-id="89141-112">If there is no canonical type, the value is VT\_EMPTY.</span></span> <span data-ttu-id="89141-113">Se l'elemento è un file ([System. FileName](./props-system-filename.md) non è un VT \_ vuoto), il valore corrisponde a [System. FileExtension](./props-system-fileextension.md).</span><span class="sxs-lookup"><span data-stu-id="89141-113">If the item is a file ([System.FileName](./props-system-filename.md) is not VT\_EMPTY), the value is the same as [System.FileExtension](./props-system-fileextension.md).</span></span> <span data-ttu-id="89141-114">Utilizzare [System. ItemTypeText](./props-system-itemtypetext.md) quando si desidera visualizzare il tipo agli utenti finali in una vista.</span><span class="sxs-lookup"><span data-stu-id="89141-114">Use [System.ItemTypeText](./props-system-itemtypetext.md) when you want to display the type to end users in a view.</span></span>

> [!Note]  
> <span data-ttu-id="89141-115">Se l'elemento è un file, il passaggio del valore [System. ItemType]() a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) restituisce lo stesso valore di [System. ItemTypeText](./props-system-itemtypetext.md).</span><span class="sxs-lookup"><span data-stu-id="89141-115">If the item is a file, passing the [System.ItemType]() value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) results in the same value as [System.ItemTypeText](./props-system-itemtypetext.md).</span></span>

 

<span data-ttu-id="89141-116">Valori di esempio</span><span class="sxs-lookup"><span data-stu-id="89141-116">Example values:</span></span>



| <span data-ttu-id="89141-117">Percorso</span><span class="sxs-lookup"><span data-stu-id="89141-117">Path</span></span>                                   | <span data-ttu-id="89141-118">ItemType</span><span class="sxs-lookup"><span data-stu-id="89141-118">ItemType</span></span>         |
|----------------------------------------|------------------|
| <span data-ttu-id="89141-119">c: \\ \\hello.txt della barra mydir \\</span><span class="sxs-lookup"><span data-stu-id="89141-119">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="89141-120">.txt</span><span class="sxs-lookup"><span data-stu-id="89141-120">.txt</span></span>             |
| <span data-ttu-id="89141-121">\\\\\\condivisione server \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="89141-121">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="89141-122">doc</span><span class="sxs-lookup"><span data-stu-id="89141-122">.doc</span></span>             |
| <span data-ttu-id="89141-123">\\\\\\cartella condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="89141-123">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="89141-124">Directory</span><span class="sxs-lookup"><span data-stu-id="89141-124">Directory</span></span>        |
| <span data-ttu-id="89141-125">c: \\ mydir \\ cartella</span><span class="sxs-lookup"><span data-stu-id="89141-125">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="89141-126">Directory</span><span class="sxs-lookup"><span data-stu-id="89141-126">Directory</span></span>        |
| <span data-ttu-id="89141-127">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="89141-127">\[desktop\]</span></span>                            | <span data-ttu-id="89141-128">Cartella</span><span class="sxs-lookup"><span data-stu-id="89141-128">Folder</span></span>           |
| <span data-ttu-id="89141-129">/Mailbox account/Inbox/' re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="89141-129">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="89141-130">MAPI/IPM. Messaggio</span><span class="sxs-lookup"><span data-stu-id="89141-130">MAPI/IPM.Message</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="89141-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89141-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89141-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="89141-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="89141-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="89141-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="89141-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="89141-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="89141-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="89141-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="89141-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="89141-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="89141-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="89141-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="89141-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="89141-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="89141-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="89141-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="89141-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="89141-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="89141-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="89141-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="89141-142">drawControl</span><span class="sxs-lookup"><span data-stu-id="89141-142">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="89141-143">editControl</span><span class="sxs-lookup"><span data-stu-id="89141-143">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="89141-144">filterControl</span><span class="sxs-lookup"><span data-stu-id="89141-144">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="89141-145">queryControl</span><span class="sxs-lookup"><span data-stu-id="89141-145">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="89141-146">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="89141-146">Programmatic Identifiers</span></span>](../shell/fa-progids.md)
</dt> </dl>

 

 
