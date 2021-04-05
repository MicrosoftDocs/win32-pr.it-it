---
description: La tabella RemoveFile contiene un elenco di file che devono essere rimossi dall'azione RemoveFiles. L'impostazione della colonna FileName della tabella su null supporta la rimozione di cartelle vuote.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Tabella RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883358"
---
# <a name="removefile-table"></a><span data-ttu-id="33a1e-104">Tabella RemoveFile</span><span class="sxs-lookup"><span data-stu-id="33a1e-104">RemoveFile Table</span></span>

<span data-ttu-id="33a1e-105">La tabella RemoveFile contiene un elenco di file che devono essere rimossi dall' [azione RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="33a1e-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="33a1e-106">L'impostazione della colonna FileName della tabella su null supporta la rimozione di cartelle vuote.</span><span class="sxs-lookup"><span data-stu-id="33a1e-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="33a1e-107">La tabella RemoveFile include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="33a1e-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="33a1e-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="33a1e-108">Column</span></span>      | <span data-ttu-id="33a1e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="33a1e-109">Type</span></span>                                     | <span data-ttu-id="33a1e-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="33a1e-110">Key</span></span> | <span data-ttu-id="33a1e-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="33a1e-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="33a1e-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="33a1e-112">FileKey</span></span>     | [<span data-ttu-id="33a1e-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="33a1e-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="33a1e-114">S</span><span class="sxs-lookup"><span data-stu-id="33a1e-114">Y</span></span>   | <span data-ttu-id="33a1e-115">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-115">N</span></span>        |
| <span data-ttu-id="33a1e-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="33a1e-116">Component\_</span></span> | [<span data-ttu-id="33a1e-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="33a1e-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="33a1e-118">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-118">N</span></span>   | <span data-ttu-id="33a1e-119">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-119">N</span></span>        |
| <span data-ttu-id="33a1e-120">FileName</span><span class="sxs-lookup"><span data-stu-id="33a1e-120">FileName</span></span>    | [<span data-ttu-id="33a1e-121">WildCardFilename</span><span class="sxs-lookup"><span data-stu-id="33a1e-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="33a1e-122">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-122">N</span></span>   | <span data-ttu-id="33a1e-123">S</span><span class="sxs-lookup"><span data-stu-id="33a1e-123">Y</span></span>        |
| <span data-ttu-id="33a1e-124">DirProperty</span><span class="sxs-lookup"><span data-stu-id="33a1e-124">DirProperty</span></span> | [<span data-ttu-id="33a1e-125">Identificatore</span><span class="sxs-lookup"><span data-stu-id="33a1e-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="33a1e-126">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-126">N</span></span>   | <span data-ttu-id="33a1e-127">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-127">N</span></span>        |
| <span data-ttu-id="33a1e-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="33a1e-128">InstallMode</span></span> | [<span data-ttu-id="33a1e-129">Integer</span><span class="sxs-lookup"><span data-stu-id="33a1e-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="33a1e-130">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-130">N</span></span>   | <span data-ttu-id="33a1e-131">N</span><span class="sxs-lookup"><span data-stu-id="33a1e-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="33a1e-132">Colonne</span><span class="sxs-lookup"><span data-stu-id="33a1e-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="33a1e-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="33a1e-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="33a1e-134">Chiave primaria utilizzata per identificare questa particolare voce di tabella.</span><span class="sxs-lookup"><span data-stu-id="33a1e-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="33a1e-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="33a1e-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="33a1e-136">Chiave esterna la prima colonna della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="33a1e-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="33a1e-137">Questo campo fa riferimento al componente che controlla il file da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="33a1e-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="33a1e-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span><span class="sxs-lookup"><span data-stu-id="33a1e-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="33a1e-139">Questa colonna contiene il nome localizzabile del file da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="33a1e-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="33a1e-140">Se questa colonna è null, la cartella specificata verrà rimossa se è vuota.</span><span class="sxs-lookup"><span data-stu-id="33a1e-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="33a1e-141">Tutti i file che corrispondono al carattere jolly verranno rimossi dalla directory specificata.</span><span class="sxs-lookup"><span data-stu-id="33a1e-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="33a1e-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="33a1e-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="33a1e-143">Nome di una proprietà il cui valore si presuppone venga risolto nel percorso completo della cartella del file da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="33a1e-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="33a1e-144">La proprietà può essere il nome di una directory nella [tabella di directory](directory-table.md), una proprietà impostata dalla [tabella AppSearch](appsearch-table.md)o qualsiasi altra proprietà che rappresenta un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="33a1e-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="33a1e-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span><span class="sxs-lookup"><span data-stu-id="33a1e-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="33a1e-146">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="33a1e-146">Must be one of the following values.</span></span>



| <span data-ttu-id="33a1e-147">Costante</span><span class="sxs-lookup"><span data-stu-id="33a1e-147">Constant</span></span>                                | <span data-ttu-id="33a1e-148">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="33a1e-148">Hexadecimal</span></span> | <span data-ttu-id="33a1e-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="33a1e-149">Decimal</span></span> | <span data-ttu-id="33a1e-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33a1e-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a1e-151">**msidbRemoveFileInstallModeOnInstall**</span><span class="sxs-lookup"><span data-stu-id="33a1e-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="33a1e-152">0x001</span><span class="sxs-lookup"><span data-stu-id="33a1e-152">0x001</span></span>       | <span data-ttu-id="33a1e-153">1</span><span class="sxs-lookup"><span data-stu-id="33a1e-153">1</span></span>       | <span data-ttu-id="33a1e-154">Rimuovere solo quando viene installato il componente associato (msiInstallStateLocal o msiInstallStateSource).</span><span class="sxs-lookup"><span data-stu-id="33a1e-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="33a1e-155">**msidbRemoveFileInstallModeOnRemove**</span><span class="sxs-lookup"><span data-stu-id="33a1e-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="33a1e-156">0x002</span><span class="sxs-lookup"><span data-stu-id="33a1e-156">0x002</span></span>       | <span data-ttu-id="33a1e-157">2</span><span class="sxs-lookup"><span data-stu-id="33a1e-157">2</span></span>       | <span data-ttu-id="33a1e-158">Rimuovere solo quando il componente associato viene rimosso (msiInstallStateAbsent).</span><span class="sxs-lookup"><span data-stu-id="33a1e-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="33a1e-159">**msidbRemoveFileInstallModeOnBoth**</span><span class="sxs-lookup"><span data-stu-id="33a1e-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="33a1e-160">0x003</span><span class="sxs-lookup"><span data-stu-id="33a1e-160">0x003</span></span>       | <span data-ttu-id="33a1e-161">3</span><span class="sxs-lookup"><span data-stu-id="33a1e-161">3</span></span>       | <span data-ttu-id="33a1e-162">Rimuovere in uno dei casi precedenti.</span><span class="sxs-lookup"><span data-stu-id="33a1e-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33a1e-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="33a1e-163">Remarks</span></span>

<span data-ttu-id="33a1e-164">I riferimenti ai file in questa tabella vengono elaborati dall' [azione RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="33a1e-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="33a1e-165">Convalida</span><span class="sxs-lookup"><span data-stu-id="33a1e-165">Validation</span></span>

<dl>

[<span data-ttu-id="33a1e-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="33a1e-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="33a1e-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="33a1e-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="33a1e-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="33a1e-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="33a1e-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="33a1e-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="33a1e-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="33a1e-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="33a1e-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="33a1e-171">ICE64</span></span>](ice64.md)  
</dl>

 

 



