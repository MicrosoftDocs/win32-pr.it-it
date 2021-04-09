---
description: La tabella DuplicateFile contiene un elenco di file che devono essere duplicati, in una directory diversa rispetto al file originale o nella stessa directory, ma con un nome diverso. Il file originale deve essere un file installato dall'azione InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Tabella DuplicateFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050149"
---
# <a name="duplicatefile-table"></a><span data-ttu-id="7788f-104">Tabella DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="7788f-104">DuplicateFile Table</span></span>

<span data-ttu-id="7788f-105">La tabella DuplicateFile contiene un elenco di file che devono essere duplicati, in una directory diversa rispetto al file originale o nella stessa directory, ma con un nome diverso.</span><span class="sxs-lookup"><span data-stu-id="7788f-105">The DuplicateFile table contains a list of files that are to be duplicated, either to a different directory than the original file or to the same directory but with a different name.</span></span> <span data-ttu-id="7788f-106">Il file originale deve essere un file installato dall' [azione InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="7788f-106">The original file must be a file installed by the [InstallFiles action](installfiles-action.md).</span></span>

<span data-ttu-id="7788f-107">La tabella DuplicateFile include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="7788f-107">The DuplicateFile table has the following columns.</span></span>



| <span data-ttu-id="7788f-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="7788f-108">Column</span></span>      | <span data-ttu-id="7788f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7788f-109">Type</span></span>                         | <span data-ttu-id="7788f-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="7788f-110">Key</span></span> | <span data-ttu-id="7788f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7788f-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="7788f-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="7788f-112">FileKey</span></span>     | [<span data-ttu-id="7788f-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7788f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7788f-114">S</span><span class="sxs-lookup"><span data-stu-id="7788f-114">Y</span></span>   | <span data-ttu-id="7788f-115">N</span><span class="sxs-lookup"><span data-stu-id="7788f-115">N</span></span>        |
| <span data-ttu-id="7788f-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7788f-116">Component\_</span></span> | [<span data-ttu-id="7788f-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7788f-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="7788f-118">N</span><span class="sxs-lookup"><span data-stu-id="7788f-118">N</span></span>   | <span data-ttu-id="7788f-119">N</span><span class="sxs-lookup"><span data-stu-id="7788f-119">N</span></span>        |
| <span data-ttu-id="7788f-120">file\_</span><span class="sxs-lookup"><span data-stu-id="7788f-120">File\_</span></span>      | [<span data-ttu-id="7788f-121">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7788f-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="7788f-122">N</span><span class="sxs-lookup"><span data-stu-id="7788f-122">N</span></span>   | <span data-ttu-id="7788f-123">N</span><span class="sxs-lookup"><span data-stu-id="7788f-123">N</span></span>        |
| <span data-ttu-id="7788f-124">DestName</span><span class="sxs-lookup"><span data-stu-id="7788f-124">DestName</span></span>    | [<span data-ttu-id="7788f-125">Filename</span><span class="sxs-lookup"><span data-stu-id="7788f-125">Filename</span></span>](filename.md)     | <span data-ttu-id="7788f-126">N</span><span class="sxs-lookup"><span data-stu-id="7788f-126">N</span></span>   | <span data-ttu-id="7788f-127">S</span><span class="sxs-lookup"><span data-stu-id="7788f-127">Y</span></span>        |
| <span data-ttu-id="7788f-128">DestFolder</span><span class="sxs-lookup"><span data-stu-id="7788f-128">DestFolder</span></span>  | [<span data-ttu-id="7788f-129">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7788f-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="7788f-130">N</span><span class="sxs-lookup"><span data-stu-id="7788f-130">N</span></span>   | <span data-ttu-id="7788f-131">S</span><span class="sxs-lookup"><span data-stu-id="7788f-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7788f-132">Colonne</span><span class="sxs-lookup"><span data-stu-id="7788f-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7788f-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="7788f-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="7788f-134">Una chiave primaria, un token non localizzato, che identifica un record DuplicateFile univoco.</span><span class="sxs-lookup"><span data-stu-id="7788f-134">A primary key, a non-localized token, identifying a unique DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="7788f-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="7788f-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="7788f-136">Chiave esterna per la prima colonna della tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="7788f-136">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="7788f-137">Se il componente identificato dalla chiave non è selezionato per l'installazione o la rimozione, non viene eseguita alcuna azione sul record DuplicateFile.</span><span class="sxs-lookup"><span data-stu-id="7788f-137">If the component identified by the key is not selected for installation or removal, then no action is taken on this DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="7788f-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="7788f-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="7788f-139">Chiave esterna nella [tabella file](file-table.md) che rappresenta il file originale che deve essere duplicato.</span><span class="sxs-lookup"><span data-stu-id="7788f-139">Foreign key into the [File table](file-table.md) representing the original file that is to be duplicated.</span></span>

</dd> <dt>

<span data-ttu-id="7788f-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="7788f-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="7788f-141">Nome localizzabile da assegnare al file duplicato.</span><span class="sxs-lookup"><span data-stu-id="7788f-141">Localizable name to be given to the duplicate file.</span></span> <span data-ttu-id="7788f-142">Se questo campo è vuoto, al file di destinazione viene assegnato lo stesso nome del file originale.</span><span class="sxs-lookup"><span data-stu-id="7788f-142">If this field is blank, then the destination file is given the same name as the original file.</span></span>

</dd> <dt>

<span data-ttu-id="7788f-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="7788f-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="7788f-144">Nome di una proprietà che rappresenta il percorso completo in cui copiare il file duplicato.</span><span class="sxs-lookup"><span data-stu-id="7788f-144">Name of a property that is the full path to where the duplicate file is to be copied.</span></span> <span data-ttu-id="7788f-145">Se questa directory corrisponde alla directory che contiene il file originale e il nome del file duplicato proposto corrisponde a quello originale, non viene eseguita alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="7788f-145">If this directory is the same as the directory containing the original file and the name for the proposed duplicate file is the same as the original, then no action takes place.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7788f-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="7788f-146">Remarks</span></span>

<span data-ttu-id="7788f-147">La tabella viene elaborata dall' [azione DuplicateFiles](duplicatefiles-action.md) e dall' [azione RemoveDuplicateFiles](removeduplicatefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="7788f-147">The table is processed by the [DuplicateFiles action](duplicatefiles-action.md) and the [RemoveDuplicateFiles action](removeduplicatefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="7788f-148">Convalida</span><span class="sxs-lookup"><span data-stu-id="7788f-148">Validation</span></span>

<dl>

[<span data-ttu-id="7788f-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="7788f-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7788f-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="7788f-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7788f-151">ICE18</span><span class="sxs-lookup"><span data-stu-id="7788f-151">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="7788f-152">ICE32</span><span class="sxs-lookup"><span data-stu-id="7788f-152">ICE32</span></span>](ice32.md)  
</dl>

 

 



