---
description: Questa tabella contiene un elenco di file da spostare o copiare da una directory di origine specificata a una directory di destinazione specificata.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Tabella MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760166"
---
# <a name="movefile-table"></a><span data-ttu-id="26cb8-103">Tabella MoveFile</span><span class="sxs-lookup"><span data-stu-id="26cb8-103">MoveFile Table</span></span>

<span data-ttu-id="26cb8-104">Questa tabella contiene un elenco di file da spostare o copiare da una directory di origine specificata a una directory di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="26cb8-104">This table contains a list of files to be moved or copied from a specified source directory to a specified destination directory.</span></span>

<span data-ttu-id="26cb8-105">La tabella MoveFile include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="26cb8-105">The MoveFile table has the following columns.</span></span>



| <span data-ttu-id="26cb8-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="26cb8-106">Column</span></span>       | <span data-ttu-id="26cb8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="26cb8-107">Type</span></span>                         | <span data-ttu-id="26cb8-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="26cb8-108">Key</span></span> | <span data-ttu-id="26cb8-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="26cb8-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="26cb8-110">FileKey</span><span class="sxs-lookup"><span data-stu-id="26cb8-110">FileKey</span></span>      | [<span data-ttu-id="26cb8-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="26cb8-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="26cb8-112">S</span><span class="sxs-lookup"><span data-stu-id="26cb8-112">Y</span></span>   | <span data-ttu-id="26cb8-113">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-113">N</span></span>        |
| <span data-ttu-id="26cb8-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="26cb8-114">Component\_</span></span>  | [<span data-ttu-id="26cb8-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="26cb8-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="26cb8-116">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-116">N</span></span>   | <span data-ttu-id="26cb8-117">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-117">N</span></span>        |
| <span data-ttu-id="26cb8-118">SourceName</span><span class="sxs-lookup"><span data-stu-id="26cb8-118">SourceName</span></span>   | [<span data-ttu-id="26cb8-119">Text</span><span class="sxs-lookup"><span data-stu-id="26cb8-119">Text</span></span>](text.md)             | <span data-ttu-id="26cb8-120">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-120">N</span></span>   | <span data-ttu-id="26cb8-121">S</span><span class="sxs-lookup"><span data-stu-id="26cb8-121">Y</span></span>        |
| <span data-ttu-id="26cb8-122">DestName</span><span class="sxs-lookup"><span data-stu-id="26cb8-122">DestName</span></span>     | [<span data-ttu-id="26cb8-123">Filename</span><span class="sxs-lookup"><span data-stu-id="26cb8-123">Filename</span></span>](filename.md)     | <span data-ttu-id="26cb8-124">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-124">N</span></span>   | <span data-ttu-id="26cb8-125">S</span><span class="sxs-lookup"><span data-stu-id="26cb8-125">Y</span></span>        |
| <span data-ttu-id="26cb8-126">SourceFolder</span><span class="sxs-lookup"><span data-stu-id="26cb8-126">SourceFolder</span></span> | [<span data-ttu-id="26cb8-127">Identificatore</span><span class="sxs-lookup"><span data-stu-id="26cb8-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="26cb8-128">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-128">N</span></span>   | <span data-ttu-id="26cb8-129">S</span><span class="sxs-lookup"><span data-stu-id="26cb8-129">Y</span></span>        |
| <span data-ttu-id="26cb8-130">DestFolder</span><span class="sxs-lookup"><span data-stu-id="26cb8-130">DestFolder</span></span>   | [<span data-ttu-id="26cb8-131">Identificatore</span><span class="sxs-lookup"><span data-stu-id="26cb8-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="26cb8-132">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-132">N</span></span>   | <span data-ttu-id="26cb8-133">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-133">N</span></span>        |
| <span data-ttu-id="26cb8-134">Opzioni</span><span class="sxs-lookup"><span data-stu-id="26cb8-134">Options</span></span>      | [<span data-ttu-id="26cb8-135">Integer</span><span class="sxs-lookup"><span data-stu-id="26cb8-135">Integer</span></span>](integer.md)       | <span data-ttu-id="26cb8-136">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-136">N</span></span>   | <span data-ttu-id="26cb8-137">N</span><span class="sxs-lookup"><span data-stu-id="26cb8-137">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="26cb8-138">Colonne</span><span class="sxs-lookup"><span data-stu-id="26cb8-138">Columns</span></span>

<dl> <dt>

<span data-ttu-id="26cb8-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="26cb8-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="26cb8-140">Chiave primaria che identifica in modo univoco un particolare record MoveFile.</span><span class="sxs-lookup"><span data-stu-id="26cb8-140">Primary key that uniquely identifies a particular MoveFile record.</span></span>

</dd> <dt>

<span data-ttu-id="26cb8-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="26cb8-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="26cb8-142">Chiave esterna nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="26cb8-142">External key into the [Component table](component-table.md).</span></span> <span data-ttu-id="26cb8-143">Se il componente a cui fa riferimento questa chiave non è selezionato per l'installazione o la rimozione, non viene eseguita alcuna azione sulla voce MoveFile.</span><span class="sxs-lookup"><span data-stu-id="26cb8-143">If the component referenced by this key is not selected for installation or removal, then no action is taken on this MoveFile entry.</span></span>

</dd> <dt>

<span data-ttu-id="26cb8-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span><span class="sxs-lookup"><span data-stu-id="26cb8-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span></span>
</dt> <dd>

<span data-ttu-id="26cb8-145">Questa colonna contiene il nome localizzabile dei file di origine da spostare o copiare.</span><span class="sxs-lookup"><span data-stu-id="26cb8-145">This column contains the localizable name of the source files to be moved or copied.</span></span> <span data-ttu-id="26cb8-146">Questa colonna può essere lasciata vuota.</span><span class="sxs-lookup"><span data-stu-id="26cb8-146">This column may be left blank.</span></span> <span data-ttu-id="26cb8-147">Vedere la descrizione della colonna SourceFolder.</span><span class="sxs-lookup"><span data-stu-id="26cb8-147">See the description of the SourceFolder column.</span></span> <span data-ttu-id="26cb8-148">Questo campo deve contenere un nome di file lungo e può contenere caratteri jolly ( \* e?).</span><span class="sxs-lookup"><span data-stu-id="26cb8-148">This field must contain a long file name and may contain wildcard characters (\* and ?).</span></span>

</dd> <dt>

<span data-ttu-id="26cb8-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="26cb8-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="26cb8-150">Questa colonna contiene il nome localizzabile da assegnare al file originale dopo lo spostamento o la copia.</span><span class="sxs-lookup"><span data-stu-id="26cb8-150">This column contains the localizable name to be given to the original file after it is moved or copied.</span></span> <span data-ttu-id="26cb8-151">Se questo campo è vuoto, al file di destinazione viene assegnato lo stesso nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="26cb8-151">If this field is blank, then the destination file is given the same name as the source file.</span></span>

</dd> <dt>

<span data-ttu-id="26cb8-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span><span class="sxs-lookup"><span data-stu-id="26cb8-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span></span>
</dt> <dd>

<span data-ttu-id="26cb8-153">Questa colonna contiene il nome di una proprietà con un valore che viene risolto nel percorso completo della directory di origine.</span><span class="sxs-lookup"><span data-stu-id="26cb8-153">This column contains the name of a property having a value that resolves to the full path to the source directory.</span></span> <span data-ttu-id="26cb8-154">Se la colonna SourceName viene lasciata vuota, si presuppone che la proprietà denominata nella colonna SourceFolder contenga il percorso completo del file di origine, incluso il nome del file.</span><span class="sxs-lookup"><span data-stu-id="26cb8-154">If the SourceName column is left blank, then the property named in the SourceFolder column is assumed to contain the full path to the source file itself (including the file name).</span></span>

</dd> <dt>

<span data-ttu-id="26cb8-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="26cb8-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="26cb8-156">Nome di una proprietà il cui valore viene risolto nel percorso completo della directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26cb8-156">The name of a property whose value resolves to the full path to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="26cb8-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opzioni</span><span class="sxs-lookup"><span data-stu-id="26cb8-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="26cb8-158">Valore integer che specifica la modalità operativa.</span><span class="sxs-lookup"><span data-stu-id="26cb8-158">Integer value specifying the operating mode.</span></span>



| <span data-ttu-id="26cb8-159">Costante</span><span class="sxs-lookup"><span data-stu-id="26cb8-159">Constant</span></span>                     | <span data-ttu-id="26cb8-160">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="26cb8-160">Hexadecimal</span></span> | <span data-ttu-id="26cb8-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="26cb8-161">Decimal</span></span> | <span data-ttu-id="26cb8-162">Significato</span><span class="sxs-lookup"><span data-stu-id="26cb8-162">Meaning</span></span>               |
|------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="26cb8-163">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="26cb8-163">(none)</span></span>                       | <span data-ttu-id="26cb8-164">0x000</span><span class="sxs-lookup"><span data-stu-id="26cb8-164">0x000</span></span>       | <span data-ttu-id="26cb8-165">0</span><span class="sxs-lookup"><span data-stu-id="26cb8-165">0</span></span>       | <span data-ttu-id="26cb8-166">Copiare il file di origine.</span><span class="sxs-lookup"><span data-stu-id="26cb8-166">Copy the source file.</span></span> |
| <span data-ttu-id="26cb8-167">**msidbMoveFileOptionsMove**</span><span class="sxs-lookup"><span data-stu-id="26cb8-167">**msidbMoveFileOptionsMove**</span></span> | <span data-ttu-id="26cb8-168">0x001</span><span class="sxs-lookup"><span data-stu-id="26cb8-168">0x001</span></span>       | <span data-ttu-id="26cb8-169">1</span><span class="sxs-lookup"><span data-stu-id="26cb8-169">1</span></span>       | <span data-ttu-id="26cb8-170">Spostare il file di origine.</span><span class="sxs-lookup"><span data-stu-id="26cb8-170">Move the source file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26cb8-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="26cb8-171">Remarks</span></span>

<span data-ttu-id="26cb8-172">Se un \* carattere jolly "" viene immesso nella colonna SourceName della tabella MoveFile e nella colonna destName viene specificato un nome file di destinazione, tutti i file spostati o copiati manterranno i nomi nelle origini.</span><span class="sxs-lookup"><span data-stu-id="26cb8-172">If a "\*" wildcard is entered in the SourceName column of the MoveFile table and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="26cb8-173">Questa tabella viene elaborata dall' [azione MoveFiles](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="26cb8-173">This table is processed by the [MoveFiles action](movefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="26cb8-174">Convalida</span><span class="sxs-lookup"><span data-stu-id="26cb8-174">Validation</span></span>

<dl>

[<span data-ttu-id="26cb8-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="26cb8-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="26cb8-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="26cb8-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="26cb8-177">ICE18</span><span class="sxs-lookup"><span data-stu-id="26cb8-177">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="26cb8-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="26cb8-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="26cb8-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="26cb8-179">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="26cb8-180">ICE85</span><span class="sxs-lookup"><span data-stu-id="26cb8-180">ICE85</span></span>](ice85.md)  
</dl>

 

 



