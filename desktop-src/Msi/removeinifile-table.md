---
description: La tabella RemoveIniFile contiene le informazioni che un'applicazione deve eliminare da un file ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabella RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318650"
---
# <a name="removeinifile-table"></a><span data-ttu-id="d6b41-103">Tabella RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="d6b41-103">RemoveIniFile Table</span></span>

<span data-ttu-id="d6b41-104">La tabella RemoveIniFile contiene le informazioni che un'applicazione deve eliminare da un file ini.</span><span class="sxs-lookup"><span data-stu-id="d6b41-104">The RemoveIniFile table contains the information an application needs to delete from a .ini file.</span></span>

<span data-ttu-id="d6b41-105">La tabella RemoveIniFile include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="d6b41-105">The RemoveIniFile table has the following columns.</span></span>



| <span data-ttu-id="d6b41-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="d6b41-106">Column</span></span>        | <span data-ttu-id="d6b41-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6b41-107">Type</span></span>                         | <span data-ttu-id="d6b41-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="d6b41-108">Key</span></span> | <span data-ttu-id="d6b41-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="d6b41-109">Nullable</span></span> |
|---------------|------------------------------|-----|----------|
| <span data-ttu-id="d6b41-110">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="d6b41-110">RemoveIniFile</span></span> | [<span data-ttu-id="d6b41-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="d6b41-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d6b41-112">S</span><span class="sxs-lookup"><span data-stu-id="d6b41-112">Y</span></span>   | <span data-ttu-id="d6b41-113">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-113">N</span></span>        |
| <span data-ttu-id="d6b41-114">FileName</span><span class="sxs-lookup"><span data-stu-id="d6b41-114">FileName</span></span>      | [<span data-ttu-id="d6b41-115">FileName</span><span class="sxs-lookup"><span data-stu-id="d6b41-115">FileName</span></span>](text.md)         | <span data-ttu-id="d6b41-116">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-116">N</span></span>   | <span data-ttu-id="d6b41-117">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-117">N</span></span>        |
| <span data-ttu-id="d6b41-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="d6b41-118">DirProperty</span></span>   | [<span data-ttu-id="d6b41-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="d6b41-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="d6b41-120">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-120">N</span></span>   | <span data-ttu-id="d6b41-121">S</span><span class="sxs-lookup"><span data-stu-id="d6b41-121">Y</span></span>        |
| <span data-ttu-id="d6b41-122">Sezione</span><span class="sxs-lookup"><span data-stu-id="d6b41-122">Section</span></span>       | [<span data-ttu-id="d6b41-123">Formattato</span><span class="sxs-lookup"><span data-stu-id="d6b41-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d6b41-124">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-124">N</span></span>   | <span data-ttu-id="d6b41-125">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-125">N</span></span>        |
| <span data-ttu-id="d6b41-126">Chiave</span><span class="sxs-lookup"><span data-stu-id="d6b41-126">Key</span></span>           | [<span data-ttu-id="d6b41-127">Formattato</span><span class="sxs-lookup"><span data-stu-id="d6b41-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d6b41-128">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-128">N</span></span>   | <span data-ttu-id="d6b41-129">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-129">N</span></span>        |
| <span data-ttu-id="d6b41-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d6b41-130">Value</span></span>         | [<span data-ttu-id="d6b41-131">Formattato</span><span class="sxs-lookup"><span data-stu-id="d6b41-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d6b41-132">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-132">N</span></span>   | <span data-ttu-id="d6b41-133">S</span><span class="sxs-lookup"><span data-stu-id="d6b41-133">Y</span></span>        |
| <span data-ttu-id="d6b41-134">Azione</span><span class="sxs-lookup"><span data-stu-id="d6b41-134">Action</span></span>        | [<span data-ttu-id="d6b41-135">Integer</span><span class="sxs-lookup"><span data-stu-id="d6b41-135">Integer</span></span>](integer.md)       | <span data-ttu-id="d6b41-136">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-136">N</span></span>   | <span data-ttu-id="d6b41-137">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-137">N</span></span>        |
| <span data-ttu-id="d6b41-138">Componente\_</span><span class="sxs-lookup"><span data-stu-id="d6b41-138">Component\_</span></span>   | [<span data-ttu-id="d6b41-139">Identificatore</span><span class="sxs-lookup"><span data-stu-id="d6b41-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="d6b41-140">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-140">N</span></span>   | <span data-ttu-id="d6b41-141">N</span><span class="sxs-lookup"><span data-stu-id="d6b41-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d6b41-142">Colonne</span><span class="sxs-lookup"><span data-stu-id="d6b41-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d6b41-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="d6b41-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-144">Chiave per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="d6b41-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="d6b41-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span><span class="sxs-lookup"><span data-stu-id="d6b41-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-146">Nome del file ini in cui eliminare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="d6b41-146">The .ini file name in which to delete the information.</span></span>

</dd> <dt>

<span data-ttu-id="d6b41-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="d6b41-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-148">Nome di una proprietà il cui valore si presuppone venga risolto nel percorso completo della cartella del file ini da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d6b41-148">Name of a property whose value is assumed to resolve to the full path to the folder of the .ini file to be removed.</span></span> <span data-ttu-id="d6b41-149">La proprietà può essere il nome di una directory nella [tabella di directory](directory-table.md), una proprietà impostata dalla [tabella AppSearch](appsearch-table.md)o qualsiasi altra proprietà che rappresenta un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="d6b41-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="d6b41-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione</span><span class="sxs-lookup"><span data-stu-id="d6b41-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-151">Sezione del file con estensione ini localizzabile.</span><span class="sxs-lookup"><span data-stu-id="d6b41-151">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="d6b41-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave</span><span class="sxs-lookup"><span data-stu-id="d6b41-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-153">Chiave del file. ini localizzabile sotto la sezione.</span><span class="sxs-lookup"><span data-stu-id="d6b41-153">The localizable .ini file key below the section.</span></span>

</dd> <dt>

<span data-ttu-id="d6b41-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="d6b41-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-155">Valore localizzabile da eliminare.</span><span class="sxs-lookup"><span data-stu-id="d6b41-155">The localizable value to be deleted.</span></span> <span data-ttu-id="d6b41-156">Il valore è obbligatorio quando l'azione è 4.</span><span class="sxs-lookup"><span data-stu-id="d6b41-156">The value is required when Action is 4.</span></span>

</dd> <dt>

<span data-ttu-id="d6b41-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="d6b41-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-158">Tipo di modifica da apportare.</span><span class="sxs-lookup"><span data-stu-id="d6b41-158">The type of modification to be made.</span></span>



| <span data-ttu-id="d6b41-159">Costante</span><span class="sxs-lookup"><span data-stu-id="d6b41-159">Constant</span></span>                         | <span data-ttu-id="d6b41-160">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="d6b41-160">Hexadecimal</span></span> | <span data-ttu-id="d6b41-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="d6b41-161">Decimal</span></span> | <span data-ttu-id="d6b41-162">Significato</span><span class="sxs-lookup"><span data-stu-id="d6b41-162">Meaning</span></span>                          |
|----------------------------------|-------------|---------|----------------------------------|
| <span data-ttu-id="d6b41-163">**msidbIniFileActionRemoveLine**</span><span class="sxs-lookup"><span data-stu-id="d6b41-163">**msidbIniFileActionRemoveLine**</span></span> | <span data-ttu-id="d6b41-164">0x002</span><span class="sxs-lookup"><span data-stu-id="d6b41-164">0x002</span></span>       | <span data-ttu-id="d6b41-165">2</span><span class="sxs-lookup"><span data-stu-id="d6b41-165">2</span></span>       | <span data-ttu-id="d6b41-166">Elimina la voce. ini.</span><span class="sxs-lookup"><span data-stu-id="d6b41-166">Deletes .ini entry.</span></span>              |
| <span data-ttu-id="d6b41-167">**msidbIniFileActionRemoveTag**</span><span class="sxs-lookup"><span data-stu-id="d6b41-167">**msidbIniFileActionRemoveTag**</span></span>  | <span data-ttu-id="d6b41-168">0x004</span><span class="sxs-lookup"><span data-stu-id="d6b41-168">0x004</span></span>       | <span data-ttu-id="d6b41-169">4</span><span class="sxs-lookup"><span data-stu-id="d6b41-169">4</span></span>       | <span data-ttu-id="d6b41-170">Elimina un tag da una voce. ini.</span><span class="sxs-lookup"><span data-stu-id="d6b41-170">Deletes a tag from a .ini entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d6b41-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="d6b41-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d6b41-172">Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md) che fa riferimento al componente che controlla l'eliminazione del valore ini.</span><span class="sxs-lookup"><span data-stu-id="d6b41-172">External key into first column of the [Component table](component-table.md) referencing the component that controls the deletion of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6b41-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6b41-173">Remarks</span></span>

<span data-ttu-id="d6b41-174">Le informazioni sul file ini vengono eliminate quando il componente corrispondente è stato selezionato per l'installazione, localmente o eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="d6b41-174">The .ini file information is deleted when the corresponding Component has been selected to be installed, either locally or run from source.</span></span>

<span data-ttu-id="d6b41-175">Questa tabella viene definita quando viene eseguita l' [azione RemoveIniValues](removeinivalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d6b41-175">This table is referred to when the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

<span data-ttu-id="d6b41-176">Se la \_ colonna directory è specificata come null, il percorso del file ini è il percorso standard di Windows ini, che è la directory di Windows per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d6b41-176">If the Directory\_ column is specified as null, the ini file location is the standard Windows ini location which is the Windows directory by default.</span></span>

<span data-ttu-id="d6b41-177">La rimozione dell'ultimo valore da una sezione comporta l'eliminazione di tale sezione.</span><span class="sxs-lookup"><span data-stu-id="d6b41-177">Removing the last value from a section deletes that section.</span></span> <span data-ttu-id="d6b41-178">Non esiste un altro modo per eliminare un'intera sezione diversa dalla rimozione di tutti i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="d6b41-178">There is no other way to delete an entire section other than removing all its values.</span></span>

## <a name="validation"></a><span data-ttu-id="d6b41-179">Convalida</span><span class="sxs-lookup"><span data-stu-id="d6b41-179">Validation</span></span>

<dl>

[<span data-ttu-id="d6b41-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="d6b41-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d6b41-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="d6b41-181">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d6b41-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="d6b41-182">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d6b41-183">ICE40</span><span class="sxs-lookup"><span data-stu-id="d6b41-183">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="d6b41-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="d6b41-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d6b41-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="d6b41-185">ICE69</span></span>](ice69.md)  
</dl>

 

 



