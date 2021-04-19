---
description: La tabella IniLocator include le informazioni necessarie per cercare un file o una directory usando un file ini o per cercare una particolare voce. ini. Il file ini deve essere presente nella directory predefinita di Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabella IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310800"
---
# <a name="inilocator-table"></a><span data-ttu-id="ab827-104">Tabella IniLocator</span><span class="sxs-lookup"><span data-stu-id="ab827-104">IniLocator Table</span></span>

<span data-ttu-id="ab827-105">La tabella IniLocator include le informazioni necessarie per cercare un file o una directory usando un file ini o per cercare una particolare voce. ini.</span><span class="sxs-lookup"><span data-stu-id="ab827-105">The IniLocator table holds the information needed to search for a file or directory using an .ini file or to search for a particular .ini entry itself.</span></span> <span data-ttu-id="ab827-106">Il file ini deve essere presente nella directory predefinita di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ab827-106">The .ini file must be present in the default Microsoft Windows directory.</span></span>

<span data-ttu-id="ab827-107">La tabella IniLocator include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="ab827-107">The IniLocator table has the following columns.</span></span>



| <span data-ttu-id="ab827-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="ab827-108">Column</span></span>      | <span data-ttu-id="ab827-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab827-109">Type</span></span>                         | <span data-ttu-id="ab827-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="ab827-110">Key</span></span> | <span data-ttu-id="ab827-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="ab827-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="ab827-112">Firma\_</span><span class="sxs-lookup"><span data-stu-id="ab827-112">Signature\_</span></span> | [<span data-ttu-id="ab827-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="ab827-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="ab827-114">S</span><span class="sxs-lookup"><span data-stu-id="ab827-114">Y</span></span>   | <span data-ttu-id="ab827-115">N</span><span class="sxs-lookup"><span data-stu-id="ab827-115">N</span></span>        |
| <span data-ttu-id="ab827-116">FileName</span><span class="sxs-lookup"><span data-stu-id="ab827-116">FileName</span></span>    | [<span data-ttu-id="ab827-117">FileName</span><span class="sxs-lookup"><span data-stu-id="ab827-117">FileName</span></span>](text.md)         | <span data-ttu-id="ab827-118">N</span><span class="sxs-lookup"><span data-stu-id="ab827-118">N</span></span>   | <span data-ttu-id="ab827-119">N</span><span class="sxs-lookup"><span data-stu-id="ab827-119">N</span></span>        |
| <span data-ttu-id="ab827-120">Sezione</span><span class="sxs-lookup"><span data-stu-id="ab827-120">Section</span></span>     | [<span data-ttu-id="ab827-121">Text</span><span class="sxs-lookup"><span data-stu-id="ab827-121">Text</span></span>](text.md)             | <span data-ttu-id="ab827-122">N</span><span class="sxs-lookup"><span data-stu-id="ab827-122">N</span></span>   | <span data-ttu-id="ab827-123">N</span><span class="sxs-lookup"><span data-stu-id="ab827-123">N</span></span>        |
| <span data-ttu-id="ab827-124">Chiave</span><span class="sxs-lookup"><span data-stu-id="ab827-124">Key</span></span>         | [<span data-ttu-id="ab827-125">Text</span><span class="sxs-lookup"><span data-stu-id="ab827-125">Text</span></span>](text.md)             | <span data-ttu-id="ab827-126">N</span><span class="sxs-lookup"><span data-stu-id="ab827-126">N</span></span>   | <span data-ttu-id="ab827-127">N</span><span class="sxs-lookup"><span data-stu-id="ab827-127">N</span></span>        |
| <span data-ttu-id="ab827-128">Campo</span><span class="sxs-lookup"><span data-stu-id="ab827-128">Field</span></span>       | [<span data-ttu-id="ab827-129">Integer</span><span class="sxs-lookup"><span data-stu-id="ab827-129">Integer</span></span>](integer.md)       | <span data-ttu-id="ab827-130">N</span><span class="sxs-lookup"><span data-stu-id="ab827-130">N</span></span>   | <span data-ttu-id="ab827-131">Y</span><span class="sxs-lookup"><span data-stu-id="ab827-131">Y</span></span>        |
| <span data-ttu-id="ab827-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab827-132">Type</span></span>        | [<span data-ttu-id="ab827-133">Integer</span><span class="sxs-lookup"><span data-stu-id="ab827-133">Integer</span></span>](integer.md)       | <span data-ttu-id="ab827-134">N</span><span class="sxs-lookup"><span data-stu-id="ab827-134">N</span></span>   | <span data-ttu-id="ab827-135">S</span><span class="sxs-lookup"><span data-stu-id="ab827-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ab827-136">Colonne</span><span class="sxs-lookup"><span data-stu-id="ab827-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ab827-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_</span><span class="sxs-lookup"><span data-stu-id="ab827-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="ab827-138">Chiave esterna nella prima colonna della [tabella della firma](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab827-138">An external key into the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="ab827-139">La firma \_ rappresenta una firma univoca ed è anche la chiave esterna nella colonna uno della tabella di firma.</span><span class="sxs-lookup"><span data-stu-id="ab827-139">The Signature\_ represents a unique signature and is also the external key into column one of the Signature table.</span></span> <span data-ttu-id="ab827-140">Se la firma è presente nella tabella della firma, la ricerca è relativa a un file.</span><span class="sxs-lookup"><span data-stu-id="ab827-140">If this signature is present in the Signature table, then the search is for a file.</span></span> <span data-ttu-id="ab827-141">Se questa chiave non è presente nella tabella della firma e il valore della colonna del tipo è **msidbLocatorTypeRawValue**, la ricerca è relativa alla voce. ini specificata dalla tabella IniLocator.</span><span class="sxs-lookup"><span data-stu-id="ab827-141">If this key is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the .ini entry specified by the IniLocator table.</span></span> <span data-ttu-id="ab827-142">In caso contrario, la ricerca è relativa a una directory specificata dalla tabella IniLocator.</span><span class="sxs-lookup"><span data-stu-id="ab827-142">Otherwise the search is for a directory specified by the IniLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="ab827-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span><span class="sxs-lookup"><span data-stu-id="ab827-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="ab827-144">Nome del file ini.</span><span class="sxs-lookup"><span data-stu-id="ab827-144">The .ini file name.</span></span>

</dd> <dt>

<span data-ttu-id="ab827-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione</span><span class="sxs-lookup"><span data-stu-id="ab827-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="ab827-146">Nome della sezione all'interno del file ini.</span><span class="sxs-lookup"><span data-stu-id="ab827-146">Section name within the .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="ab827-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave</span><span class="sxs-lookup"><span data-stu-id="ab827-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="ab827-148">Valore della chiave nella sezione.</span><span class="sxs-lookup"><span data-stu-id="ab827-148">Key value within the section.</span></span>

</dd> <dt>

<span data-ttu-id="ab827-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo</span><span class="sxs-lookup"><span data-stu-id="ab827-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Field</span></span>
</dt> <dd>

<span data-ttu-id="ab827-150">Campo nella riga ini.</span><span class="sxs-lookup"><span data-stu-id="ab827-150">The field in the .ini line.</span></span> <span data-ttu-id="ab827-151">Se Field è null o 0, viene letta l'intera riga.</span><span class="sxs-lookup"><span data-stu-id="ab827-151">If Field is Null or 0, then the entire line is read.</span></span> <span data-ttu-id="ab827-152">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="ab827-152">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="ab827-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo</span><span class="sxs-lookup"><span data-stu-id="ab827-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="ab827-154">Valore che determina se il valore ini è un percorso di file, un percorso di directory o un valore RAW. ini.</span><span class="sxs-lookup"><span data-stu-id="ab827-154">A value that determines whether the .ini value is a file location, a directory location, or raw .ini value.</span></span>

<span data-ttu-id="ab827-155">Nella tabella seguente sono elencati i valori validi.</span><span class="sxs-lookup"><span data-stu-id="ab827-155">The following table lists valid values.</span></span> <span data-ttu-id="ab827-156">Se assente, Type è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="ab827-156">If absent, Type is set to be 1.</span></span>



| <span data-ttu-id="ab827-157">Costante</span><span class="sxs-lookup"><span data-stu-id="ab827-157">Constant</span></span>                      | <span data-ttu-id="ab827-158">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="ab827-158">Hexadecimal</span></span> | <span data-ttu-id="ab827-159">Decimal</span><span class="sxs-lookup"><span data-stu-id="ab827-159">Decimal</span></span> | <span data-ttu-id="ab827-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab827-160">Description</span></span>           |
|-------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="ab827-161">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="ab827-161">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="ab827-162">0x000</span><span class="sxs-lookup"><span data-stu-id="ab827-162">0x000</span></span>       | <span data-ttu-id="ab827-163">0</span><span class="sxs-lookup"><span data-stu-id="ab827-163">0</span></span>       | <span data-ttu-id="ab827-164">Percorso della directory.</span><span class="sxs-lookup"><span data-stu-id="ab827-164">A directory location.</span></span> |
| <span data-ttu-id="ab827-165">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="ab827-165">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="ab827-166">0x001</span><span class="sxs-lookup"><span data-stu-id="ab827-166">0x001</span></span>       | <span data-ttu-id="ab827-167">1</span><span class="sxs-lookup"><span data-stu-id="ab827-167">1</span></span>       | <span data-ttu-id="ab827-168">Percorso del file.</span><span class="sxs-lookup"><span data-stu-id="ab827-168">A file location.</span></span>      |
| <span data-ttu-id="ab827-169">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="ab827-169">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="ab827-170">0x002</span><span class="sxs-lookup"><span data-stu-id="ab827-170">0x002</span></span>       | <span data-ttu-id="ab827-171">2</span><span class="sxs-lookup"><span data-stu-id="ab827-171">2</span></span>       | <span data-ttu-id="ab827-172">Valore RAW. ini.</span><span class="sxs-lookup"><span data-stu-id="ab827-172">A raw .ini value.</span></span>     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab827-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab827-173">Remarks</span></span>

<span data-ttu-id="ab827-174">Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab827-174">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="ab827-175">Generalmente, le colonne della tabella non sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="ab827-175">This table's columns are generally not localized.</span></span> <span data-ttu-id="ab827-176">Se un autore decide di cercare i prodotti in più lingue, è possibile che nella tabella sia inclusa una voce separata per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="ab827-176">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="ab827-177">Il testo localizzato associato per la visualizzazione o la registrazione dello stato di avanzamento è specificato nella [tabella ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab827-177">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="ab827-178">Vedere [ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="ab827-178">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ab827-179">Convalida</span><span class="sxs-lookup"><span data-stu-id="ab827-179">Validation</span></span>

<dl>

[<span data-ttu-id="ab827-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="ab827-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ab827-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="ab827-181">ICE06</span></span>](ice06.md)  
</dl>

 

 



