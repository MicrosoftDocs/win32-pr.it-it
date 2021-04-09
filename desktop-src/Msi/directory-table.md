---
description: La tabella directory specifica il layout di directory per il prodotto. Ogni riga della tabella indica una directory sia nell'origine che nella destinazione.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabella directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967810"
---
# <a name="directory-table"></a><span data-ttu-id="c5e41-104">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="c5e41-104">Directory Table</span></span>

<span data-ttu-id="c5e41-105">La tabella directory specifica il layout di directory per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="c5e41-105">The Directory table specifies the directory layout for the product.</span></span> <span data-ttu-id="c5e41-106">Ogni riga della tabella indica una directory sia nell'origine che nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="c5e41-106">Each row of the table indicates a directory both at the source and the target.</span></span>

<span data-ttu-id="c5e41-107">La tabella di directory contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5e41-107">The Directory table has the following columns.</span></span>



| <span data-ttu-id="c5e41-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="c5e41-108">Column</span></span>            | <span data-ttu-id="c5e41-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5e41-109">Type</span></span>                         | <span data-ttu-id="c5e41-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="c5e41-110">Key</span></span> | <span data-ttu-id="c5e41-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="c5e41-111">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="c5e41-112">Directory</span><span class="sxs-lookup"><span data-stu-id="c5e41-112">Directory</span></span>         | [<span data-ttu-id="c5e41-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5e41-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="c5e41-114">S</span><span class="sxs-lookup"><span data-stu-id="c5e41-114">Y</span></span>   | <span data-ttu-id="c5e41-115">N</span><span class="sxs-lookup"><span data-stu-id="c5e41-115">N</span></span>        |
| <span data-ttu-id="c5e41-116">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="c5e41-116">Directory\_Parent</span></span> | [<span data-ttu-id="c5e41-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5e41-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="c5e41-118">N</span><span class="sxs-lookup"><span data-stu-id="c5e41-118">N</span></span>   | <span data-ttu-id="c5e41-119">S</span><span class="sxs-lookup"><span data-stu-id="c5e41-119">Y</span></span>        |
| <span data-ttu-id="c5e41-120">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="c5e41-120">DefaultDir</span></span>        | [<span data-ttu-id="c5e41-121">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="c5e41-121">DefaultDir</span></span>](defaultdir.md) | <span data-ttu-id="c5e41-122">N</span><span class="sxs-lookup"><span data-stu-id="c5e41-122">N</span></span>   | <span data-ttu-id="c5e41-123">N</span><span class="sxs-lookup"><span data-stu-id="c5e41-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c5e41-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="c5e41-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c5e41-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span><span class="sxs-lookup"><span data-stu-id="c5e41-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span></span>
</dt> <dd>

<span data-ttu-id="c5e41-126">La colonna directory contiene un identificatore univoco per una directory o un percorso di directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-126">The Directory column contains a unique identifier for a directory or directory path.</span></span> <span data-ttu-id="c5e41-127">Questa colonna può contenere il nome di una proprietà impostata sul percorso completo di una directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c5e41-127">This column can contain the name of a property that is set to the full path of a target directory.</span></span> <span data-ttu-id="c5e41-128">Se questa colonna contiene una proprietà, la directory di destinazione acquisisce il nome specificato nella colonna DefaultDir e acquisisce la directory padre specificata nella \_ colonna padre della directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-128">If this column contains a property, the target directory takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="c5e41-129">La directory di origine accetta sempre il nome specificato nella colonna DefaultDir e accetta la directory padre specificata nella \_ colonna padre della directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-129">The source directory always takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="c5e41-130">Se la \_ colonna padre della directory è null o uguale al valore della colonna directory, la colonna directory rappresenta una directory di destinazione radice.</span><span class="sxs-lookup"><span data-stu-id="c5e41-130">If the Directory\_Parent column is either null or equal to the value of the Directory column, the Directory column represents a root target directory.</span></span> <span data-ttu-id="c5e41-131">Nella tabella directory è possibile specificare una sola directory radice.</span><span class="sxs-lookup"><span data-stu-id="c5e41-131">Only one root directory may be specified in the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="c5e41-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="c5e41-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directory\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="c5e41-133">Questa colonna è un riferimento alla directory padre della directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-133">This column is a reference to the directory's parent directory.</span></span> <span data-ttu-id="c5e41-134">Un record con una \_ colonna padre della directory uguale a null o uguale alla colonna di directory rappresenta una directory radice.</span><span class="sxs-lookup"><span data-stu-id="c5e41-134">A record that has a Directory\_Parent column equal to null or equal to the Directory column represents a root directory.</span></span> <span data-ttu-id="c5e41-135">Il percorso completo della directory padre viene risolto per riferimento nella \_ colonna padre della directory è una chiave esterna nella colonna directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-135">The full path of the parent directory is resolved by reference in the Directory\_Parent column is an external key into the Directory column.</span></span> <span data-ttu-id="c5e41-136">Se, ad esempio, in una cartella è presente una directory padre denominata PDIR, la directory padre di PDIR viene specificata nella \_ colonna padre della directory della riga con PDIR nella colonna directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-136">For example, if a folder has a parent directory named PDIR, the parent directory of PDIR is given in the Directory\_Parent column of the row with PDIR in the Directory column.</span></span>

</dd> <dt>

<span data-ttu-id="c5e41-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span><span class="sxs-lookup"><span data-stu-id="c5e41-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span></span>
</dt> <dd>

<span data-ttu-id="c5e41-138">La colonna DefaultDir contiene il nome della directory (localizzabile) nella directory padre.</span><span class="sxs-lookup"><span data-stu-id="c5e41-138">The DefaultDir column contains the directory's name (localizable)under the parent directory.</span></span> <span data-ttu-id="c5e41-139">Per impostazione predefinita, si tratta del nome delle directory di destinazione e di origine.</span><span class="sxs-lookup"><span data-stu-id="c5e41-139">By default, this is the name of both the target and source directories.</span></span> <span data-ttu-id="c5e41-140">Per specificare nomi di directory di origine e di destinazione diversi, separare i nomi di destinazione e di origine con i due punti, come indicato di seguito: \[ TargetName \] : \[ SourceName \] .</span><span class="sxs-lookup"><span data-stu-id="c5e41-140">To specify different source and target directory names, separate the target and source names with a colon as follows: \[targetname\]:\[sourcename\].</span></span>

<span data-ttu-id="c5e41-141">Se il valore della \_ colonna padre della directory è null o è uguale alla colonna di directory, la colonna DefaultDir specifica il nome di una directory di origine radice.</span><span class="sxs-lookup"><span data-stu-id="c5e41-141">If the value of the Directory\_Parent column is null or is equal to the Directory column, the DefaultDir column specifies the name of a root source directory.</span></span>

<span data-ttu-id="c5e41-142">Per una directory di origine non radice, un punto (.) immesso nella colonna DefaultDir per il nome della directory di origine o il nome della directory di destinazione indica che la directory deve trovarsi nella directory padre senza una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-142">For a non-root source directory, a period (.) entered in the DefaultDir column for the source directory name or the target directory name indicates the directory should be located in its parent directory without a subdirectory.</span></span>

<span data-ttu-id="c5e41-143">I nomi di directory in questa colonna possono essere formattati come coppie nome file breve nomefile \| lungo.</span><span class="sxs-lookup"><span data-stu-id="c5e41-143">The directory names in this column may be formatted as short filename \| long filename pairs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5e41-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5e41-144">Remarks</span></span>

<span data-ttu-id="c5e41-145">Ogni record della tabella rappresenta una directory nelle immagini di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c5e41-145">Each record in the table represents a directory in both the source and the destination images.</span></span> <span data-ttu-id="c5e41-146">La tabella directory deve specificare una singola directory radice con un valore di colonna di directory uguale alla proprietà [**targetdir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e41-146">The Directory table must specify a single root directory with a Directory column value equal to the [**TARGETDIR**](targetdir.md) property.</span></span>

<span data-ttu-id="c5e41-147">Per un' [installazione amministrativa](administrative-installation.md), installare l'immagine amministrativa nella directory radice denominata TARGETDIR e usare i nomi delle directory di origine per risolvere le directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c5e41-147">For an [administrative installation](administrative-installation.md), install the administrative image into the root directory named TARGETDIR and use the source directory names to resolve the target directories.</span></span>

<span data-ttu-id="c5e41-148">Si noti che il programma di installazione imposta una serie di [Proprietà](properties.md) standard sui percorsi di cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="c5e41-148">Note the installer sets a number of standard [properties](properties.md) to system folder paths.</span></span> <span data-ttu-id="c5e41-149">Per un elenco delle proprietà impostate sulle cartelle di sistema, vedere il [riferimento alla proprietà](property-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e41-149">See the [Property Reference](property-reference.md) for a list of the properties that are set to system folders.</span></span>

<span data-ttu-id="c5e41-150">La risoluzione della directory viene eseguita durante l' [azione CostFinalize secondo](costfinalize-action.md) e viene eseguita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c5e41-150">Directory resolution is performed during the [CostFinalize action](costfinalize-action.md) and is done as follows:</span></span>

### <a name="root-destination-directory"></a><span data-ttu-id="c5e41-151">Directory di destinazione radice</span><span class="sxs-lookup"><span data-stu-id="c5e41-151">Root Destination Directory</span></span>

<span data-ttu-id="c5e41-152">Può essere presente una sola directory di destinazione radice.</span><span class="sxs-lookup"><span data-stu-id="c5e41-152">There may only be a single root destination directory.</span></span> <span data-ttu-id="c5e41-153">Per specificare la directory di destinazione radice, impostare la colonna della directory sulla proprietà [**targetdir**](targetdir.md) e la colonna DefaultDir sulla proprietà [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e41-153">To specify the root destination directory, set the Directory column to the [**TARGETDIR**](targetdir.md) property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="c5e41-154">Se la proprietà **targetdir** è definita, la directory di destinazione viene risolta nel valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5e41-154">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="c5e41-155">Se la proprietà **targetdir** è indefinita, per risolvere il percorso viene utilizzata la proprietà [**ROOTDRIVE**](rootdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e41-155">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span>

### <a name="root-source-directory"></a><span data-ttu-id="c5e41-156">Directory di origine radice</span><span class="sxs-lookup"><span data-stu-id="c5e41-156">Root Source Directory</span></span>

<span data-ttu-id="c5e41-157">Il valore della colonna DefaultDir per la voce della directory radice deve essere impostato sulla proprietà [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e41-157">The value of the DefaultDir column for the root directory entry must be set to the [**SourceDir**](sourcedir.md) property.</span></span>

### <a name="non-root-destination-directories"></a><span data-ttu-id="c5e41-158">Directory di destinazione non radice</span><span class="sxs-lookup"><span data-stu-id="c5e41-158">Non-root Destination Directories</span></span>

<span data-ttu-id="c5e41-159">Il valore della directory per una directory non radice viene anche interpretato come il nome di una proprietà che definisce la posizione della destinazione.</span><span class="sxs-lookup"><span data-stu-id="c5e41-159">The Directory value for a non-root directory is also interpreted as the name of a property defining the location of the destination.</span></span> <span data-ttu-id="c5e41-160">Se la proprietà è definita, la directory di destinazione viene risolta nel valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5e41-160">If the property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="c5e41-161">Se la proprietà non è definita, la directory di destinazione viene risolta in una sottodirectory sotto la directory di destinazione risolta per la \_ voce padre della directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-161">If the property is not defined, the destination directory is resolved to a subdirectory beneath the resolved destination directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="c5e41-162">Il valore DefaultDir definisce il nome della sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-162">The DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="non-root-source-directories"></a><span data-ttu-id="c5e41-163">Directory di origine non radice</span><span class="sxs-lookup"><span data-stu-id="c5e41-163">Non-root Source Directories</span></span>

<span data-ttu-id="c5e41-164">La directory di origine per una directory non radice viene risolta in una sottodirectory della directory di origine risolta per la \_ voce padre della directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-164">The source directory for a non-root directory is resolved to a subdirectory of the resolved source directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="c5e41-165">Anche in questo caso, il valore di DefaultDir definisce il nome della sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-165">Again, the DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="short-or-long-file-names"></a><span data-ttu-id="c5e41-166">Nomi di file brevi o lunghi</span><span class="sxs-lookup"><span data-stu-id="c5e41-166">Short or Long File Names</span></span>

<span data-ttu-id="c5e41-167">Quando si risolvono le directory di destinazione, i nomi di file brevi specificati nella colonna DefaultDir vengono utilizzati se la proprietà [**SHORTFILENAMES**](shortfilenames.md) è impostata o se il volume in cui si trova la directory non supporta nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="c5e41-167">When resolving destination directories, the short file names specified in the DefaultDir column are used if either the [**SHORTFILENAMES**](shortfilenames.md) property is set or the volume the directory is located on does not support long file names.</span></span> <span data-ttu-id="c5e41-168">In caso contrario, viene utilizzato il nome file lungo.</span><span class="sxs-lookup"><span data-stu-id="c5e41-168">Otherwise, the long file name is used.</span></span>

<span data-ttu-id="c5e41-169">Si noti che quando le directory vengono risolte durante l'azione CostFinalize secondo, le chiavi della tabella directory diventano [Proprietà](properties.md) impostate sui percorsi di directory.</span><span class="sxs-lookup"><span data-stu-id="c5e41-169">Note that when the directories are resolved during the CostFinalize action, the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span>

[<span data-ttu-id="c5e41-170">Tabella CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c5e41-170">CreateFolder Table</span></span>](createfolder-table.md)

<span data-ttu-id="c5e41-171">Per la creazione di cartelle vuote durante un'installazione, vedere [tabella CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="c5e41-171">For creating empty folders during an installation, see [CreateFolder Table](createfolder-table.md).</span></span>

[<span data-ttu-id="c5e41-172">Uso della tabella di directory</span><span class="sxs-lookup"><span data-stu-id="c5e41-172">Using the Directory Table</span></span>](using-the-directory-table.md)

<span data-ttu-id="c5e41-173">Per ulteriori informazioni sulla tabella di directory, inclusi gli esempi, vedere [utilizzo della tabella directory](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="c5e41-173">For more information about the Directory table, including samples, see [Using the Directory Table](using-the-directory-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="c5e41-174">Convalida</span><span class="sxs-lookup"><span data-stu-id="c5e41-174">Validation</span></span>

<dl>

[<span data-ttu-id="c5e41-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="c5e41-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c5e41-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="c5e41-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c5e41-177">ICE07</span><span class="sxs-lookup"><span data-stu-id="c5e41-177">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="c5e41-178">ICE30</span><span class="sxs-lookup"><span data-stu-id="c5e41-178">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="c5e41-179">ICE32</span><span class="sxs-lookup"><span data-stu-id="c5e41-179">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c5e41-180">ICE38</span><span class="sxs-lookup"><span data-stu-id="c5e41-180">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="c5e41-181">ICE46</span><span class="sxs-lookup"><span data-stu-id="c5e41-181">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c5e41-182">ICE48</span><span class="sxs-lookup"><span data-stu-id="c5e41-182">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="c5e41-183">ICE56</span><span class="sxs-lookup"><span data-stu-id="c5e41-183">ICE56</span></span>](ice56.md)  
[<span data-ttu-id="c5e41-184">ICE57</span><span class="sxs-lookup"><span data-stu-id="c5e41-184">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="c5e41-185">ICE64</span><span class="sxs-lookup"><span data-stu-id="c5e41-185">ICE64</span></span>](ice64.md)  
[<span data-ttu-id="c5e41-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="c5e41-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="c5e41-187">ICE90</span><span class="sxs-lookup"><span data-stu-id="c5e41-187">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="c5e41-188">ICE91</span><span class="sxs-lookup"><span data-stu-id="c5e41-188">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="c5e41-189">ICE99</span><span class="sxs-lookup"><span data-stu-id="c5e41-189">ICE99</span></span>](ice99.md)  
</dl>

 

 



