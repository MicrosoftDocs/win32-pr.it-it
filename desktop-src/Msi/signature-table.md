---
description: La tabella Signature include le informazioni che identificano in modo univoco una firma del file. Per altre informazioni sulle firme, vedere firme digitali e Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabella di firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314196"
---
# <a name="signature-table"></a><span data-ttu-id="b93f0-104">Tabella di firma</span><span class="sxs-lookup"><span data-stu-id="b93f0-104">Signature Table</span></span>

<span data-ttu-id="b93f0-105">La tabella Signature include le informazioni che identificano in modo univoco una firma del file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-105">The Signature table holds the information that uniquely identifies a file signature.</span></span> <span data-ttu-id="b93f0-106">Per altre informazioni sulle firme [, vedere firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="b93f0-106">For more information regarding signatures see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="b93f0-107">La tabella Signature contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="b93f0-107">The Signature table has the following columns.</span></span>



| <span data-ttu-id="b93f0-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="b93f0-108">Column</span></span>     | <span data-ttu-id="b93f0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b93f0-109">Type</span></span>                               | <span data-ttu-id="b93f0-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="b93f0-110">Key</span></span> | <span data-ttu-id="b93f0-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="b93f0-111">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="b93f0-112">Firma</span><span class="sxs-lookup"><span data-stu-id="b93f0-112">Signature</span></span>  | [<span data-ttu-id="b93f0-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="b93f0-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="b93f0-114">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-114">Y</span></span>   | <span data-ttu-id="b93f0-115">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-115">N</span></span>        |
| <span data-ttu-id="b93f0-116">FileName</span><span class="sxs-lookup"><span data-stu-id="b93f0-116">FileName</span></span>   | [<span data-ttu-id="b93f0-117">Text</span><span class="sxs-lookup"><span data-stu-id="b93f0-117">Text</span></span>](text.md)                   | <span data-ttu-id="b93f0-118">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-118">N</span></span>   | <span data-ttu-id="b93f0-119">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-119">N</span></span>        |
| <span data-ttu-id="b93f0-120">MinVersion</span><span class="sxs-lookup"><span data-stu-id="b93f0-120">MinVersion</span></span> | [<span data-ttu-id="b93f0-121">Text</span><span class="sxs-lookup"><span data-stu-id="b93f0-121">Text</span></span>](text.md)                   | <span data-ttu-id="b93f0-122">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-122">N</span></span>   | <span data-ttu-id="b93f0-123">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-123">Y</span></span>        |
| <span data-ttu-id="b93f0-124">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="b93f0-124">MaxVersion</span></span> | [<span data-ttu-id="b93f0-125">Text</span><span class="sxs-lookup"><span data-stu-id="b93f0-125">Text</span></span>](text.md)                   | <span data-ttu-id="b93f0-126">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-126">N</span></span>   | <span data-ttu-id="b93f0-127">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-127">Y</span></span>        |
| <span data-ttu-id="b93f0-128">MinSize</span><span class="sxs-lookup"><span data-stu-id="b93f0-128">MinSize</span></span>    | [<span data-ttu-id="b93f0-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b93f0-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b93f0-130">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-130">N</span></span>   | <span data-ttu-id="b93f0-131">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-131">Y</span></span>        |
| <span data-ttu-id="b93f0-132">MaxSize</span><span class="sxs-lookup"><span data-stu-id="b93f0-132">MaxSize</span></span>    | [<span data-ttu-id="b93f0-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b93f0-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b93f0-134">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-134">N</span></span>   | <span data-ttu-id="b93f0-135">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-135">Y</span></span>        |
| <span data-ttu-id="b93f0-136">MinDate</span><span class="sxs-lookup"><span data-stu-id="b93f0-136">MinDate</span></span>    | [<span data-ttu-id="b93f0-137">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b93f0-137">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b93f0-138">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-138">N</span></span>   | <span data-ttu-id="b93f0-139">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-139">Y</span></span>        |
| <span data-ttu-id="b93f0-140">MaxDate</span><span class="sxs-lookup"><span data-stu-id="b93f0-140">MaxDate</span></span>    | [<span data-ttu-id="b93f0-141">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b93f0-141">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b93f0-142">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-142">N</span></span>   | <span data-ttu-id="b93f0-143">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-143">Y</span></span>        |
| <span data-ttu-id="b93f0-144">Linguaggi</span><span class="sxs-lookup"><span data-stu-id="b93f0-144">Languages</span></span>  | [<span data-ttu-id="b93f0-145">Text</span><span class="sxs-lookup"><span data-stu-id="b93f0-145">Text</span></span>](text.md)                   | <span data-ttu-id="b93f0-146">N</span><span class="sxs-lookup"><span data-stu-id="b93f0-146">N</span></span>   | <span data-ttu-id="b93f0-147">S</span><span class="sxs-lookup"><span data-stu-id="b93f0-147">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b93f0-148">Colonne</span><span class="sxs-lookup"><span data-stu-id="b93f0-148">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b93f0-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma</span><span class="sxs-lookup"><span data-stu-id="b93f0-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-150">La colonna Signature è una firma di file univoca.</span><span class="sxs-lookup"><span data-stu-id="b93f0-150">The Signature column is a unique file signature.</span></span>

</dd> <dt>

<span data-ttu-id="b93f0-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span><span class="sxs-lookup"><span data-stu-id="b93f0-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-152">Nome del file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-152">The name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="b93f0-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span><span class="sxs-lookup"><span data-stu-id="b93f0-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-154">Versione minima del file, con un confronto di lingua.</span><span class="sxs-lookup"><span data-stu-id="b93f0-154">The minimum version of the file, with a language comparison.</span></span> <span data-ttu-id="b93f0-155">Se questo campo è specificato, la versione del file deve essere almeno uguale a MinVersion.</span><span class="sxs-lookup"><span data-stu-id="b93f0-155">If this field is specified, then the file must have a version that is at least equal to MinVersion.</span></span> <span data-ttu-id="b93f0-156">Se il file ha una versione uguale al valore del campo MinVersion ma la lingua specificata nella colonna Languages è diversa, il file non soddisfa i criteri di filtro della firma.</span><span class="sxs-lookup"><span data-stu-id="b93f0-156">If the file has an equal version to the MinVersion field value but the language specified in the Languages column differs, the file does not satisfy the signature filter criteria.</span></span>

> [!Note]  
> <span data-ttu-id="b93f0-157">Il linguaggio specificato nella colonna lingue viene utilizzato nel confronto e non è possibile ignorare la lingua.</span><span class="sxs-lookup"><span data-stu-id="b93f0-157">The language specified in the Languages column is used in the comparison and there is no way to ignore language.</span></span> <span data-ttu-id="b93f0-158">Se si vuole che un file soddisfi il requisito di campo MinVersion indipendentemente dalla lingua, è necessario immettere un valore nel campo MinVersion, che corrisponde a uno minore del valore effettivo.</span><span class="sxs-lookup"><span data-stu-id="b93f0-158">If you want a file to meet the MinVersion field requirement regardless of language, you must enter a value in the MinVersion field that is one less than the actual value.</span></span> <span data-ttu-id="b93f0-159">Se, ad esempio, la versione minima del filtro è 2.0.2600.1183, utilizzare 2.0.2600.1182 per trovare il file senza corrispondenti alle informazioni sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="b93f0-159">For example, if the minimum version for the filter is 2.0.2600.1183, use 2.0.2600.1182 to find the file without matching the language information.</span></span>

 

</dd> <dt>

<span data-ttu-id="b93f0-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span><span class="sxs-lookup"><span data-stu-id="b93f0-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-161">Versione massima del file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-161">The maximum version of the file.</span></span> <span data-ttu-id="b93f0-162">Se questo campo è specificato, il file deve avere una versione maggiore o uguale a MaxVersion.</span><span class="sxs-lookup"><span data-stu-id="b93f0-162">If this field is specified, then the file must have a version that is at most equal to MaxVersion.</span></span>

</dd> <dt>

<span data-ttu-id="b93f0-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span><span class="sxs-lookup"><span data-stu-id="b93f0-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-164">Dimensioni minime del file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-164">The minimum size of the file.</span></span> <span data-ttu-id="b93f0-165">Se questo campo è specificato, il file in ispezione deve avere una dimensione almeno uguale a MinSize.</span><span class="sxs-lookup"><span data-stu-id="b93f0-165">If this field is specified, then the file under inspection must have a size that is at least equal to MinSize.</span></span> <span data-ttu-id="b93f0-166">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b93f0-166">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="b93f0-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span><span class="sxs-lookup"><span data-stu-id="b93f0-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-168">Dimensione massima del file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-168">The maximum size of the file.</span></span> <span data-ttu-id="b93f0-169">Se viene specificato questo campo, il file in ispezione deve avere una dimensione maggiore o uguale a MaxSize.</span><span class="sxs-lookup"><span data-stu-id="b93f0-169">If this field is specified, then the file under inspection must have a size that is at most equal to MaxSize.</span></span> <span data-ttu-id="b93f0-170">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b93f0-170">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="b93f0-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span><span class="sxs-lookup"><span data-stu-id="b93f0-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-172">Data e ora di modifica minime del file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-172">The minimum modification date and time of the file.</span></span> <span data-ttu-id="b93f0-173">Se questo campo è specificato, il file in ispezione deve avere una data e un'ora di modifica almeno uguali a MinDe.</span><span class="sxs-lookup"><span data-stu-id="b93f0-173">If this field is specified, then the file under inspection must have a modification date and time that is at least equal to MinDate.</span></span> <span data-ttu-id="b93f0-174">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b93f0-174">This must be a non-negative number.</span></span> <span data-ttu-id="b93f0-175">Il formato di questo campo è costituito da due valori a 16 bit compressi di tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="b93f0-175">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="b93f0-176">Il valore **Word** di ordine superiore specifica la data nel formato di data MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="b93f0-176">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="b93f0-177">Il valore di **Word** di ordine inferiore specifica l'ora nel formato di ora di MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="b93f0-177">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="b93f0-178">Il valore 0 per il valore time rappresenta la mezzanotte.</span><span class="sxs-lookup"><span data-stu-id="b93f0-178">A value of 0 for the time value represents midnight.</span></span> <span data-ttu-id="b93f0-179">Vedere la sezione relativa alle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b93f0-179">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b93f0-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span><span class="sxs-lookup"><span data-stu-id="b93f0-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-181">Data massima di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-181">The maximum creation date of the file.</span></span> <span data-ttu-id="b93f0-182">Se questo campo è specificato, il file in ispezione deve avere una data di creazione maggiore o uguale a MaxDate.</span><span class="sxs-lookup"><span data-stu-id="b93f0-182">If this field is specified, then the file under inspection must have a creation date that is at most equal to MaxDate.</span></span> <span data-ttu-id="b93f0-183">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b93f0-183">This must be a non-negative number.</span></span> <span data-ttu-id="b93f0-184">Il formato di questo campo è costituito da due valori a 16 bit compressi di tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="b93f0-184">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="b93f0-185">Il valore **Word** di ordine superiore specifica la data nel formato di data MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="b93f0-185">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="b93f0-186">Il valore di **Word** di ordine inferiore specifica l'ora nel formato di ora di MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="b93f0-186">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="b93f0-187">Il valore 0 per il valore time rappresenta la mezzanotte.</span><span class="sxs-lookup"><span data-stu-id="b93f0-187">A value of 0 for the time value represent midnight.</span></span> <span data-ttu-id="b93f0-188">Vedere la sezione relativa alle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b93f0-188">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b93f0-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Lingue</span><span class="sxs-lookup"><span data-stu-id="b93f0-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Languages</span></span>
</dt> <dd>

<span data-ttu-id="b93f0-190">Lingue supportate dal file.</span><span class="sxs-lookup"><span data-stu-id="b93f0-190">The languages supported by the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b93f0-191">Commenti</span><span class="sxs-lookup"><span data-stu-id="b93f0-191">Remarks</span></span>

<span data-ttu-id="b93f0-192">Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="b93f0-192">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="b93f0-193">Viene eseguita la ricerca della firma utilizzando la tabella [RegLocator](reglocator-table.md), la tabella [IniLocator](inilocator-table.md), la [tabella CompLocator](complocator-table.md)e la [tabella DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="b93f0-193">The signature is searched for using the [RegLocator table](reglocator-table.md), the [IniLocator table](inilocator-table.md), the [CompLocator table](complocator-table.md), and the [DrLocator table](drlocator-table.md).</span></span> <span data-ttu-id="b93f0-194">Generalmente, le colonne della tabella non sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="b93f0-194">This table's columns are generally not localized.</span></span> <span data-ttu-id="b93f0-195">Se un autore decide di cercare i prodotti in più lingue, è possibile che nella tabella sia inclusa una voce separata per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="b93f0-195">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="b93f0-196">La tabella Signature segue in genere le [regole di controllo delle versioni dei File](file-versioning-rules.md)Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b93f0-196">The Signature table generally follows the Windows Installer [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="b93f0-197">Le lingue specificate nella colonna lingue della tabella di firma non vengono valutate a meno che le versioni dei file non siano equivalenti.</span><span class="sxs-lookup"><span data-stu-id="b93f0-197">Languages specified in the Languages column of the Signature table are not evaluated unless the file versions are equivalent.</span></span> <span data-ttu-id="b93f0-198">La colonna lingue garantisce che un file sia di una determinata lingua se è della versione richiesta.</span><span class="sxs-lookup"><span data-stu-id="b93f0-198">The Languages column will ensure that a file is of a particular language if it is of the requested version.</span></span> <span data-ttu-id="b93f0-199">Non è disponibile alcun metodo per ignorare la colonna lingue.</span><span class="sxs-lookup"><span data-stu-id="b93f0-199">There is no method available to ignore the Languages column.</span></span> <span data-ttu-id="b93f0-200">Un valore NULL immesso nella colonna lingue viene considerato come un file senza una lingua e non corrisponde alla firma del file con una lingua visualizzata nella tabella della firma.</span><span class="sxs-lookup"><span data-stu-id="b93f0-200">A NULL value entered in the Languages column is treated as a file without a language and does not match the file signature of a file with a language appearing in the Signature table.</span></span> <span data-ttu-id="b93f0-201">Nell'esempio seguente viene eseguita la ricerca di una particolare versione di MSI.DLL.</span><span class="sxs-lookup"><span data-stu-id="b93f0-201">The following example searches for a particular version of MSI.DLL.</span></span>

[<span data-ttu-id="b93f0-202">Tabella DrLocator</span><span class="sxs-lookup"><span data-stu-id="b93f0-202">DrLocator table</span></span>](drlocator-table.md)

| <span data-ttu-id="b93f0-203">Firma\_</span><span class="sxs-lookup"><span data-stu-id="b93f0-203">Signature\_</span></span> | <span data-ttu-id="b93f0-204">Padre</span><span class="sxs-lookup"><span data-stu-id="b93f0-204">Parent</span></span> | <span data-ttu-id="b93f0-205">Percorso</span><span class="sxs-lookup"><span data-stu-id="b93f0-205">Path</span></span>                  | <span data-ttu-id="b93f0-206">Profondità</span><span class="sxs-lookup"><span data-stu-id="b93f0-206">Depth</span></span> |
|-------------|--------|-----------------------|-------|
| <span data-ttu-id="b93f0-207">MsiDll</span><span class="sxs-lookup"><span data-stu-id="b93f0-207">MsiDll</span></span>      | <span data-ttu-id="b93f0-208">null</span><span class="sxs-lookup"><span data-stu-id="b93f0-208">{null}</span></span> | <span data-ttu-id="b93f0-209">c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="b93f0-209">c:\\windows\\system32</span></span> | <span data-ttu-id="b93f0-210">0</span><span class="sxs-lookup"><span data-stu-id="b93f0-210">0</span></span>     |



 

[<span data-ttu-id="b93f0-211">Tabella AppSearch</span><span class="sxs-lookup"><span data-stu-id="b93f0-211">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="b93f0-212">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b93f0-212">Property</span></span> | <span data-ttu-id="b93f0-213">Firma\_</span><span class="sxs-lookup"><span data-stu-id="b93f0-213">Signature\_</span></span> |
|----------|-------------|
| <span data-ttu-id="b93f0-214">MSIDLL</span><span class="sxs-lookup"><span data-stu-id="b93f0-214">MSIDLL</span></span>   | <span data-ttu-id="b93f0-215">MsiDll</span><span class="sxs-lookup"><span data-stu-id="b93f0-215">MsiDll</span></span>      |



 

<span data-ttu-id="b93f0-216">Tabella di firma</span><span class="sxs-lookup"><span data-stu-id="b93f0-216">Signature table</span></span>



| <span data-ttu-id="b93f0-217">Firma</span><span class="sxs-lookup"><span data-stu-id="b93f0-217">Signature</span></span> | <span data-ttu-id="b93f0-218">FileName</span><span class="sxs-lookup"><span data-stu-id="b93f0-218">FileName</span></span> | <span data-ttu-id="b93f0-219">MinVersion</span><span class="sxs-lookup"><span data-stu-id="b93f0-219">MinVersion</span></span>    | <span data-ttu-id="b93f0-220">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="b93f0-220">MaxVersion</span></span> | <span data-ttu-id="b93f0-221">MinSize</span><span class="sxs-lookup"><span data-stu-id="b93f0-221">MinSize</span></span> | <span data-ttu-id="b93f0-222">MaxSize</span><span class="sxs-lookup"><span data-stu-id="b93f0-222">MaxSize</span></span> | <span data-ttu-id="b93f0-223">MinDate</span><span class="sxs-lookup"><span data-stu-id="b93f0-223">MinDate</span></span> | <span data-ttu-id="b93f0-224">MaxDate</span><span class="sxs-lookup"><span data-stu-id="b93f0-224">MaxDate</span></span> | <span data-ttu-id="b93f0-225">Linguaggi</span><span class="sxs-lookup"><span data-stu-id="b93f0-225">Languages</span></span> |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| <span data-ttu-id="b93f0-226">MsiDll</span><span class="sxs-lookup"><span data-stu-id="b93f0-226">MsiDll</span></span>    | <span data-ttu-id="b93f0-227">msi.dll</span><span class="sxs-lookup"><span data-stu-id="b93f0-227">msi.dll</span></span>  | <span data-ttu-id="b93f0-228">2.0.2600.1106</span><span class="sxs-lookup"><span data-stu-id="b93f0-228">2.0.2600.1106</span></span> | <span data-ttu-id="b93f0-229">null</span><span class="sxs-lookup"><span data-stu-id="b93f0-229">{null}</span></span>     | <span data-ttu-id="b93f0-230">null</span><span class="sxs-lookup"><span data-stu-id="b93f0-230">{null}</span></span>  | <span data-ttu-id="b93f0-231">null</span><span class="sxs-lookup"><span data-stu-id="b93f0-231">{null}</span></span>  | <span data-ttu-id="b93f0-232">null</span><span class="sxs-lookup"><span data-stu-id="b93f0-232">{null}</span></span>  | <span data-ttu-id="b93f0-233">null</span><span class="sxs-lookup"><span data-stu-id="b93f0-233">{null}</span></span>  | <span data-ttu-id="b93f0-234">0</span><span class="sxs-lookup"><span data-stu-id="b93f0-234">0</span></span>         |



 

<span data-ttu-id="b93f0-235">In questo caso, e in Windows XP SP1, l' [azione AppSearch](appsearch-action.md) imposta MSIDLL su c: \\ Windows \\ system32 \\msi.dll perché MSI.DLL è un file indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="b93f0-235">In this case, and on Windows XP SP1, the [AppSearch action](appsearch-action.md) sets MSIDLL to c:\\windows\\system32\\msi.dll because MSI.DLL is a language neutral file.</span></span> <span data-ttu-id="b93f0-236">Se il valore della colonna languages viene modificato da 0 a 1033, l'azione AppSearch non riesce a trovare il msi.dll corrispondente e la proprietà MSIDLL non è definita.</span><span class="sxs-lookup"><span data-stu-id="b93f0-236">If the value of the Languages column is changed from 0 to 1033, then the AppSearch action fails to find the matching msi.dll and the MSIDLL property is undefined.</span></span>

<span data-ttu-id="b93f0-237">Non è possibile usare la tabella Signature per eseguire query solo su linguaggi.</span><span class="sxs-lookup"><span data-stu-id="b93f0-237">You cannot use the Signature table to query on languages alone.</span></span> <span data-ttu-id="b93f0-238">Per cercare versioni in lingue diverse di un file, è necessario disporre di una voce separata nella tabella della firma per ogni versione della lingua.</span><span class="sxs-lookup"><span data-stu-id="b93f0-238">To search for different language versions of a file, you must have a separate entry in the Signature table for each language version.</span></span> <span data-ttu-id="b93f0-239">Se nella colonna lingue sono disponibili più lingue, la ricerca è relativa a un file che supporta tutte le lingue.</span><span class="sxs-lookup"><span data-stu-id="b93f0-239">If multiple languages are provided in the Languages column, then the search is for a file that supports all of those languages.</span></span>

<span data-ttu-id="b93f0-240">Il formato delle colonne MinDe e MaxDate è costituito da due valori a 16 bit compressi di tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="b93f0-240">The format of MinDate and MaxDate columns are two packed 16-bit values of type **WORD**.</span></span>

<span data-ttu-id="b93f0-241">**Parola** data</span><span class="sxs-lookup"><span data-stu-id="b93f0-241">Date **WORD**</span></span>



| <span data-ttu-id="b93f0-242">BITS</span><span class="sxs-lookup"><span data-stu-id="b93f0-242">Bits</span></span> | <span data-ttu-id="b93f0-243">Content</span><span class="sxs-lookup"><span data-stu-id="b93f0-243">Content</span></span>                                             |
|------|-----------------------------------------------------|
| <span data-ttu-id="b93f0-244">0 – 4</span><span class="sxs-lookup"><span data-stu-id="b93f0-244">0–4</span></span>  | <span data-ttu-id="b93f0-245">Giorno del mese (1-31)</span><span class="sxs-lookup"><span data-stu-id="b93f0-245">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="b93f0-246">5-8</span><span class="sxs-lookup"><span data-stu-id="b93f0-246">5-8</span></span>  | <span data-ttu-id="b93f0-247">Month (1 = gennaio, 2 = febbraio e così via)</span><span class="sxs-lookup"><span data-stu-id="b93f0-247">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="b93f0-248">9-15</span><span class="sxs-lookup"><span data-stu-id="b93f0-248">9-15</span></span> | <span data-ttu-id="b93f0-249">Offset anno da 1980 (aggiungere 1980 per ottenere l'anno effettivo)</span><span class="sxs-lookup"><span data-stu-id="b93f0-249">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

<span data-ttu-id="b93f0-250">**Parola** temporale</span><span class="sxs-lookup"><span data-stu-id="b93f0-250">Time **WORD**</span></span>



| <span data-ttu-id="b93f0-251">BITS</span><span class="sxs-lookup"><span data-stu-id="b93f0-251">Bits</span></span>  | <span data-ttu-id="b93f0-252">Content</span><span class="sxs-lookup"><span data-stu-id="b93f0-252">Content</span></span>                     |
|-------|-----------------------------|
| <span data-ttu-id="b93f0-253">0 – 4</span><span class="sxs-lookup"><span data-stu-id="b93f0-253">0–4</span></span>   | <span data-ttu-id="b93f0-254">Secondi divisi per 2</span><span class="sxs-lookup"><span data-stu-id="b93f0-254">Seconds divided by 2</span></span>        |
| <span data-ttu-id="b93f0-255">5-10</span><span class="sxs-lookup"><span data-stu-id="b93f0-255">5-10</span></span>  | <span data-ttu-id="b93f0-256">Minuti (0-59)</span><span class="sxs-lookup"><span data-stu-id="b93f0-256">Minutes (0-59)</span></span>              |
| <span data-ttu-id="b93f0-257">11-15</span><span class="sxs-lookup"><span data-stu-id="b93f0-257">11-15</span></span> | <span data-ttu-id="b93f0-258">Ora (da 0 a 23 in formato 24 ore)</span><span class="sxs-lookup"><span data-stu-id="b93f0-258">Hour(0-23 on 24 hour clock)</span></span> |



 

<span data-ttu-id="b93f0-259">La formula per il calcolo dei valori dei campi MinDe e MaxDate è:</span><span class="sxs-lookup"><span data-stu-id="b93f0-259">The formula for calculating the MinDate and MaxDate field values is:</span></span>

<span data-ttu-id="b93f0-260">((Anno-1980) \* 512 + mese \* 32 + giorno) \* 65536 + ore \* 2048 + minuti \* 32 + secondi/2</span><span class="sxs-lookup"><span data-stu-id="b93f0-260">( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2</span></span>

## <a name="validation"></a><span data-ttu-id="b93f0-261">Convalida</span><span class="sxs-lookup"><span data-stu-id="b93f0-261">Validation</span></span>

<dl>

[<span data-ttu-id="b93f0-262">ICE03</span><span class="sxs-lookup"><span data-stu-id="b93f0-262">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b93f0-263">ICE06</span><span class="sxs-lookup"><span data-stu-id="b93f0-263">ICE06</span></span>](ice06.md)  
</dl>

 

 



