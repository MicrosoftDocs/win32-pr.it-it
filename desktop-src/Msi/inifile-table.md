---
description: La tabella IniFile contiene le informazioni. ini che l'applicazione deve impostare in un file con estensione ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabella IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049900"
---
# <a name="inifile-table"></a><span data-ttu-id="e0655-103">Tabella IniFile</span><span class="sxs-lookup"><span data-stu-id="e0655-103">IniFile Table</span></span>

<span data-ttu-id="e0655-104">La tabella IniFile contiene le informazioni. ini che l'applicazione deve impostare in un file con estensione ini.</span><span class="sxs-lookup"><span data-stu-id="e0655-104">The IniFile table contains the .ini information that the application needs to set in an .ini file.</span></span>

<span data-ttu-id="e0655-105">La tabella IniFile include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0655-105">The IniFile table has the following columns.</span></span>



| <span data-ttu-id="e0655-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="e0655-106">Column</span></span>      | <span data-ttu-id="e0655-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0655-107">Type</span></span>                         | <span data-ttu-id="e0655-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="e0655-108">Key</span></span> | <span data-ttu-id="e0655-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="e0655-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e0655-110">IniFile</span><span class="sxs-lookup"><span data-stu-id="e0655-110">IniFile</span></span>     | [<span data-ttu-id="e0655-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="e0655-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="e0655-112">S</span><span class="sxs-lookup"><span data-stu-id="e0655-112">Y</span></span>   | <span data-ttu-id="e0655-113">N</span><span class="sxs-lookup"><span data-stu-id="e0655-113">N</span></span>        |
| <span data-ttu-id="e0655-114">FileName</span><span class="sxs-lookup"><span data-stu-id="e0655-114">FileName</span></span>    | [<span data-ttu-id="e0655-115">FileName</span><span class="sxs-lookup"><span data-stu-id="e0655-115">FileName</span></span>](text.md)         | <span data-ttu-id="e0655-116">N</span><span class="sxs-lookup"><span data-stu-id="e0655-116">N</span></span>   | <span data-ttu-id="e0655-117">N</span><span class="sxs-lookup"><span data-stu-id="e0655-117">N</span></span>        |
| <span data-ttu-id="e0655-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="e0655-118">DirProperty</span></span> | [<span data-ttu-id="e0655-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="e0655-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="e0655-120">N</span><span class="sxs-lookup"><span data-stu-id="e0655-120">N</span></span>   | <span data-ttu-id="e0655-121">S</span><span class="sxs-lookup"><span data-stu-id="e0655-121">Y</span></span>        |
| <span data-ttu-id="e0655-122">Sezione</span><span class="sxs-lookup"><span data-stu-id="e0655-122">Section</span></span>     | [<span data-ttu-id="e0655-123">Formattato</span><span class="sxs-lookup"><span data-stu-id="e0655-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e0655-124">N</span><span class="sxs-lookup"><span data-stu-id="e0655-124">N</span></span>   | <span data-ttu-id="e0655-125">N</span><span class="sxs-lookup"><span data-stu-id="e0655-125">N</span></span>        |
| <span data-ttu-id="e0655-126">Chiave</span><span class="sxs-lookup"><span data-stu-id="e0655-126">Key</span></span>         | [<span data-ttu-id="e0655-127">Formattato</span><span class="sxs-lookup"><span data-stu-id="e0655-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e0655-128">N</span><span class="sxs-lookup"><span data-stu-id="e0655-128">N</span></span>   | <span data-ttu-id="e0655-129">N</span><span class="sxs-lookup"><span data-stu-id="e0655-129">N</span></span>        |
| <span data-ttu-id="e0655-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e0655-130">Value</span></span>       | [<span data-ttu-id="e0655-131">Formattato</span><span class="sxs-lookup"><span data-stu-id="e0655-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e0655-132">N</span><span class="sxs-lookup"><span data-stu-id="e0655-132">N</span></span>   | <span data-ttu-id="e0655-133">N</span><span class="sxs-lookup"><span data-stu-id="e0655-133">N</span></span>        |
| <span data-ttu-id="e0655-134">Azione</span><span class="sxs-lookup"><span data-stu-id="e0655-134">Action</span></span>      | [<span data-ttu-id="e0655-135">Integer</span><span class="sxs-lookup"><span data-stu-id="e0655-135">Integer</span></span>](integer.md)       | <span data-ttu-id="e0655-136">N</span><span class="sxs-lookup"><span data-stu-id="e0655-136">N</span></span>   | <span data-ttu-id="e0655-137">N</span><span class="sxs-lookup"><span data-stu-id="e0655-137">N</span></span>        |
| <span data-ttu-id="e0655-138">Componente\_</span><span class="sxs-lookup"><span data-stu-id="e0655-138">Component\_</span></span> | [<span data-ttu-id="e0655-139">Identificatore</span><span class="sxs-lookup"><span data-stu-id="e0655-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="e0655-140">N</span><span class="sxs-lookup"><span data-stu-id="e0655-140">N</span></span>   | <span data-ttu-id="e0655-141">N</span><span class="sxs-lookup"><span data-stu-id="e0655-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e0655-142">Colonne</span><span class="sxs-lookup"><span data-stu-id="e0655-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e0655-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span><span class="sxs-lookup"><span data-stu-id="e0655-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span></span>
</dt> <dd>

<span data-ttu-id="e0655-144">Chiave per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="e0655-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="e0655-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span><span class="sxs-lookup"><span data-stu-id="e0655-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="e0655-146">Nome localizzabile del file ini in cui scrivere le informazioni.</span><span class="sxs-lookup"><span data-stu-id="e0655-146">The localizable name of the .ini file in which to write the information.</span></span>

</dd> <dt>

<span data-ttu-id="e0655-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="e0655-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="e0655-148">Nome di una proprietà con un valore che viene risolto nel percorso completo della cartella che contiene il file ini.</span><span class="sxs-lookup"><span data-stu-id="e0655-148">Name of a property having a value that resolves to the full path of the folder containing the .ini file.</span></span> <span data-ttu-id="e0655-149">La proprietà può essere il nome di una directory nella [tabella di directory](directory-table.md), una proprietà impostata dalla [tabella AppSearch](appsearch-table.md)o qualsiasi altra proprietà che rappresenta un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="e0655-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span> <span data-ttu-id="e0655-150">Se questo campo viene lasciato vuoto, il file ini viene creato nella cartella con il percorso completo specificato dalla proprietà [**WindowsFolder**](windowsfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="e0655-150">If this field is left blank, the .ini file is created in the folder having the full path specified by the [**WindowsFolder**](windowsfolder.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="e0655-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione</span><span class="sxs-lookup"><span data-stu-id="e0655-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="e0655-152">Sezione del file con estensione ini localizzabile.</span><span class="sxs-lookup"><span data-stu-id="e0655-152">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="e0655-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave</span><span class="sxs-lookup"><span data-stu-id="e0655-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="e0655-154">Chiave del file. ini localizzabile nella sezione.</span><span class="sxs-lookup"><span data-stu-id="e0655-154">The localizable .ini file key within the section.</span></span>

</dd> <dt>

<span data-ttu-id="e0655-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="e0655-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="e0655-156">Valore localizzabile da scrivere.</span><span class="sxs-lookup"><span data-stu-id="e0655-156">The localizable value to be written.</span></span>

</dd> <dt>

<span data-ttu-id="e0655-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="e0655-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="e0655-158">Tipo di modifica da apportare.</span><span class="sxs-lookup"><span data-stu-id="e0655-158">The type of modification to be made.</span></span>



| <span data-ttu-id="e0655-159">Costante</span><span class="sxs-lookup"><span data-stu-id="e0655-159">Constant</span></span>                         | <span data-ttu-id="e0655-160">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="e0655-160">Hexadecimal</span></span> | <span data-ttu-id="e0655-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="e0655-161">Decimal</span></span> | <span data-ttu-id="e0655-162">Modifica</span><span class="sxs-lookup"><span data-stu-id="e0655-162">Modification</span></span>                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e0655-163">**msidbIniFileActionAddLine**</span><span class="sxs-lookup"><span data-stu-id="e0655-163">**msidbIniFileActionAddLine**</span></span>    | <span data-ttu-id="e0655-164">0x000</span><span class="sxs-lookup"><span data-stu-id="e0655-164">0x000</span></span>       | <span data-ttu-id="e0655-165">0</span><span class="sxs-lookup"><span data-stu-id="e0655-165">0</span></span>       | <span data-ttu-id="e0655-166">Crea o aggiorna una voce. ini.</span><span class="sxs-lookup"><span data-stu-id="e0655-166">Creates or updates a .ini entry.</span></span>                                                 |
| <span data-ttu-id="e0655-167">**msidbIniFileActionCreateLine**</span><span class="sxs-lookup"><span data-stu-id="e0655-167">**msidbIniFileActionCreateLine**</span></span> | <span data-ttu-id="e0655-168">0x001</span><span class="sxs-lookup"><span data-stu-id="e0655-168">0x001</span></span>       | <span data-ttu-id="e0655-169">1</span><span class="sxs-lookup"><span data-stu-id="e0655-169">1</span></span>       | <span data-ttu-id="e0655-170">Crea una voce. ini solo se la voce non esiste già.</span><span class="sxs-lookup"><span data-stu-id="e0655-170">Creates a .ini entry only if the entry does not already exist.</span></span>                   |
| <span data-ttu-id="e0655-171">**msidbIniFileActionAddTag**</span><span class="sxs-lookup"><span data-stu-id="e0655-171">**msidbIniFileActionAddTag**</span></span>     | <span data-ttu-id="e0655-172">0x003</span><span class="sxs-lookup"><span data-stu-id="e0655-172">0x003</span></span>       | <span data-ttu-id="e0655-173">3</span><span class="sxs-lookup"><span data-stu-id="e0655-173">3</span></span>       | <span data-ttu-id="e0655-174">Crea una nuova voce o aggiunge un nuovo valore delimitato da virgole a una voce esistente.</span><span class="sxs-lookup"><span data-stu-id="e0655-174">Creates a new entry or appends a new comma-separated value to an existing entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e0655-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="e0655-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e0655-176">Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md) che fa riferimento al componente che controlla l'installazione del valore ini.</span><span class="sxs-lookup"><span data-stu-id="e0655-176">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0655-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0655-177">Remarks</span></span>

<span data-ttu-id="e0655-178">Le informazioni sul file ini vengono scritte quando il componente corrispondente è stato selezionato per l'installazione come locale o per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="e0655-178">The .ini file information is written out when the corresponding component has been selected to be installed as local or run from source.</span></span>

<span data-ttu-id="e0655-179">Questa tabella viene definita quando viene eseguita l'azione [WriteIniValues](writeinivalues-action.md) o [RemoveIniValues](removeinivalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e0655-179">This table is referred to when the [WriteIniValues action](writeinivalues-action.md) or the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="e0655-180">Convalida</span><span class="sxs-lookup"><span data-stu-id="e0655-180">Validation</span></span>

<dl>

[<span data-ttu-id="e0655-181">ICE03</span><span class="sxs-lookup"><span data-stu-id="e0655-181">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e0655-182">ICE06</span><span class="sxs-lookup"><span data-stu-id="e0655-182">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e0655-183">ICE32</span><span class="sxs-lookup"><span data-stu-id="e0655-183">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e0655-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="e0655-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e0655-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="e0655-185">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="e0655-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="e0655-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="e0655-187">ICE91</span><span class="sxs-lookup"><span data-stu-id="e0655-187">ICE91</span></span>](ice91.md)  
</dl>

 

 



