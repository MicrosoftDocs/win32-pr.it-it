---
description: La tabella font contiene le informazioni per la registrazione dei file del tipo di carattere con il sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabella dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967807"
---
# <a name="font-table"></a><span data-ttu-id="8e3b9-103">Tabella dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="8e3b9-103">Font Table</span></span>

<span data-ttu-id="8e3b9-104">La tabella font contiene le informazioni per la registrazione dei file del tipo di carattere con il sistema.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-104">The Font table contains the information for registering font files with the system.</span></span>

<span data-ttu-id="8e3b9-105">La tabella font contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-105">The Font table has the following columns.</span></span>



| <span data-ttu-id="8e3b9-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="8e3b9-106">Column</span></span>    | <span data-ttu-id="8e3b9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e3b9-107">Type</span></span>                         | <span data-ttu-id="8e3b9-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="8e3b9-108">Key</span></span> | <span data-ttu-id="8e3b9-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="8e3b9-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="8e3b9-110">file\_</span><span class="sxs-lookup"><span data-stu-id="8e3b9-110">File\_</span></span>    | [<span data-ttu-id="8e3b9-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8e3b9-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="8e3b9-112">S</span><span class="sxs-lookup"><span data-stu-id="8e3b9-112">Y</span></span>   | <span data-ttu-id="8e3b9-113">N</span><span class="sxs-lookup"><span data-stu-id="8e3b9-113">N</span></span>        |
| <span data-ttu-id="8e3b9-114">FontTitle</span><span class="sxs-lookup"><span data-stu-id="8e3b9-114">FontTitle</span></span> | [<span data-ttu-id="8e3b9-115">Text</span><span class="sxs-lookup"><span data-stu-id="8e3b9-115">Text</span></span>](text.md)             | <span data-ttu-id="8e3b9-116">N</span><span class="sxs-lookup"><span data-stu-id="8e3b9-116">N</span></span>   | <span data-ttu-id="8e3b9-117">S</span><span class="sxs-lookup"><span data-stu-id="8e3b9-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8e3b9-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="8e3b9-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8e3b9-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="8e3b9-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="8e3b9-120">Chiave esterna nella voce della [tabella file](file-table.md) per il file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-120">External key into the [File table](file-table.md) entry for the font file.</span></span> <span data-ttu-id="8e3b9-121">È consigliabile che il componente contenente il file del tipo di carattere includa il FontsFolder specificato nella \_ colonna directory della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b9-121">It is recommended that the component containing the font file have the FontsFolder specified in the Directory\_ column of the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e3b9-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span><span class="sxs-lookup"><span data-stu-id="8e3b9-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span></span>
</dt> <dd>

<span data-ttu-id="8e3b9-123">Nome del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-123">Font name.</span></span> <span data-ttu-id="8e3b9-124">Si consiglia di lasciare questa colonna null per i tipi di carattere TrueType e le raccolte TrueType perché il programma di installazione può registrare il tipo di carattere dopo la lettura del titolo del tipo di carattere corretto dal file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-124">It is recommended that you leave this column null for TrueType Fonts and TrueType Collections because the installer can register the font after reading the correct font title from the font file.</span></span> <span data-ttu-id="8e3b9-125">Se il nome del tipo di carattere viene immesso, deve essere identico al titolo del carattere dal file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-125">If the font name is entered, it must be identical to font title from the font file.</span></span> <span data-ttu-id="8e3b9-126">È necessario specificare un titolo per i tipi di carattere che non hanno nomi incorporati, ad esempio i file con estensione fon.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-126">You must specify a title for fonts that do not have embedded names, such as .fon files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e3b9-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e3b9-127">Remarks</span></span>

<span data-ttu-id="8e3b9-128">Questa tabella viene definita quando viene eseguita l'azione [RegisterFonts](registerfonts-action.md) o [UnregisterFonts](unregisterfonts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8e3b9-128">This table is referred to when the [RegisterFonts action](registerfonts-action.md) or the [UnregisterFonts action](unregisterfonts-action.md) is executed.</span></span>

<span data-ttu-id="8e3b9-129">Se il campo FontTitle viene lasciato null, il nome del tipo di carattere viene letto direttamente dal file del tipo di carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-129">If the FontTitle field is left Null, the Font name is read directly from the font file specified.</span></span> <span data-ttu-id="8e3b9-130">Se il nome del tipo di carattere registrato nel campo FontTitle è diverso dal nome del tipo di carattere interno registrato nel file del tipo di carattere, il tipo di carattere viene registrato due volte dall' [azione RegisterFonts](registerfonts-action.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b9-130">If the font name recorded into the FontTitle field differs from the internal font name recorded in the font file, the font is registered twice by the [RegisterFonts action](registerfonts-action.md).</span></span>

<span data-ttu-id="8e3b9-131">I file del tipo di carattere non devono essere creati con un ID lingua, perché i tipi di carattere non hanno una risorsa ID lingua incorporata. In questo modo, la colonna lingua della [tabella file](file-table.md) deve essere lasciata null per i file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-131">Font files should not be authored with a language ID, as fonts do not have an embedded language ID resource.Thus the Language column of the [File table](file-table.md) should be left null for font files.</span></span>

<span data-ttu-id="8e3b9-132">Poiché il programma di installazione non refcount i file del tipo di carattere per impostazione predefinita, i file dei tipi di carattere preesistenti possono essere rimossi con il componente durante la disinstallazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-132">Because the installer does not refcount font files by default, preexisting font files may be removed with their component when uninstalling an application.</span></span> <span data-ttu-id="8e3b9-133">Per assicurarsi che un file del tipo di carattere non venga rimosso, gli autori possono impostare i flag di bit **msidbComponentAttributesSharedDllRefCount** o **MsidbComponentAttributesPermanent** nella colonna attributi della tabella dei componenti MSI della tabella dei componenti \_ \_ \_ per il componente contenente il file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8e3b9-133">To ensure that a font file is not removed, authors may set the **msidbComponentAttributesSharedDllRefCount** or **msidbComponentAttributesPermanent** bit flags in the Attributes column of the Component Table\_msi\_Component\_Table for the component containing the font file.</span></span>

## <a name="validation"></a><span data-ttu-id="8e3b9-134">Convalida</span><span class="sxs-lookup"><span data-stu-id="8e3b9-134">Validation</span></span>

<dl>

[<span data-ttu-id="8e3b9-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="8e3b9-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8e3b9-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="8e3b9-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8e3b9-137">ICE07</span><span class="sxs-lookup"><span data-stu-id="8e3b9-137">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="8e3b9-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="8e3b9-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8e3b9-139">ICE51</span><span class="sxs-lookup"><span data-stu-id="8e3b9-139">ICE51</span></span>](ice51.md)  
[<span data-ttu-id="8e3b9-140">ICE60</span><span class="sxs-lookup"><span data-stu-id="8e3b9-140">ICE60</span></span>](ice60.md)  
</dl>

 

 



