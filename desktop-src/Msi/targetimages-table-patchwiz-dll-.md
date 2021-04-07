---
description: La tabella TargetImages contiene informazioni sulle immagini di destinazione del prodotto. Un pacchetto Windows Installer patch aggiorna un'immagine di destinazione in un'immagine aggiornata.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabella TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885094"
---
# <a name="targetimages-table-patchwizdll"></a><span data-ttu-id="08254-104">Tabella TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="08254-104">TargetImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="08254-105">La tabella TargetImages contiene informazioni sulle immagini di destinazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="08254-105">The TargetImages table contains information about the target images of the product.</span></span> <span data-ttu-id="08254-106">Un pacchetto Windows Installer patch aggiorna un'immagine di destinazione in un'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="08254-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span>

<span data-ttu-id="08254-107">Una tabella TargetImages contenente almeno un record è obbligatoria in ogni database di creazione della patch (file con estensione PCP).</span><span class="sxs-lookup"><span data-stu-id="08254-107">A TargetImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="08254-108">Questa tabella viene utilizzata dalla funzione [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="08254-108">This table is used by the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="08254-109">La tabella TargetImages include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="08254-109">The TargetImages table has the following columns.</span></span>



| <span data-ttu-id="08254-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="08254-110">Column</span></span>                | <span data-ttu-id="08254-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="08254-111">Type</span></span>    | <span data-ttu-id="08254-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="08254-112">Key</span></span> | <span data-ttu-id="08254-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="08254-113">Nullable</span></span> |
|-----------------------|---------|-----|----------|
| <span data-ttu-id="08254-114">Destinazione</span><span class="sxs-lookup"><span data-stu-id="08254-114">Target</span></span>                | <span data-ttu-id="08254-115">text</span><span class="sxs-lookup"><span data-stu-id="08254-115">text</span></span>    | <span data-ttu-id="08254-116">S</span><span class="sxs-lookup"><span data-stu-id="08254-116">Y</span></span>   | <span data-ttu-id="08254-117">N</span><span class="sxs-lookup"><span data-stu-id="08254-117">N</span></span>        |
| <span data-ttu-id="08254-118">PercorsoMSI</span><span class="sxs-lookup"><span data-stu-id="08254-118">MsiPath</span></span>               | <span data-ttu-id="08254-119">text</span><span class="sxs-lookup"><span data-stu-id="08254-119">text</span></span>    |     | <span data-ttu-id="08254-120">N</span><span class="sxs-lookup"><span data-stu-id="08254-120">N</span></span>        |
| <span data-ttu-id="08254-121">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="08254-121">SymbolPaths</span></span>           | <span data-ttu-id="08254-122">text</span><span class="sxs-lookup"><span data-stu-id="08254-122">text</span></span>    |     | <span data-ttu-id="08254-123">S</span><span class="sxs-lookup"><span data-stu-id="08254-123">Y</span></span>        |
| <span data-ttu-id="08254-124">Aggiornato</span><span class="sxs-lookup"><span data-stu-id="08254-124">Upgraded</span></span>              | <span data-ttu-id="08254-125">text</span><span class="sxs-lookup"><span data-stu-id="08254-125">text</span></span>    |     | <span data-ttu-id="08254-126">N</span><span class="sxs-lookup"><span data-stu-id="08254-126">N</span></span>        |
| <span data-ttu-id="08254-127">JSON</span><span class="sxs-lookup"><span data-stu-id="08254-127">Order</span></span>                 | <span data-ttu-id="08254-128">numero intero</span><span class="sxs-lookup"><span data-stu-id="08254-128">integer</span></span> |     | <span data-ttu-id="08254-129">N</span><span class="sxs-lookup"><span data-stu-id="08254-129">N</span></span>        |
| <span data-ttu-id="08254-130">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="08254-130">ProductValidateFlags</span></span>  | <span data-ttu-id="08254-131">text</span><span class="sxs-lookup"><span data-stu-id="08254-131">text</span></span>    |     | <span data-ttu-id="08254-132">S</span><span class="sxs-lookup"><span data-stu-id="08254-132">Y</span></span>        |
| <span data-ttu-id="08254-133">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="08254-133">IgnoreMissingSrcFiles</span></span> | <span data-ttu-id="08254-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="08254-134">integer</span></span> |     | <span data-ttu-id="08254-135">N</span><span class="sxs-lookup"><span data-stu-id="08254-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="08254-136">Colonne</span><span class="sxs-lookup"><span data-stu-id="08254-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="08254-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione</span><span class="sxs-lookup"><span data-stu-id="08254-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="08254-138">Identificatore per un'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="08254-138">Identifier for a target image.</span></span> <span data-ttu-id="08254-139">Il pacchetto patch aggiorna l'immagine di destinazione specificata in questa colonna all'immagine aggiornata specificata nella colonna aggiornata.</span><span class="sxs-lookup"><span data-stu-id="08254-139">The patch package updates the target image specified in this column to the upgraded image specified in the Upgraded column.</span></span> <span data-ttu-id="08254-140">Per ogni immagine aggiornata sono disponibili una o più immagini di destinazione.</span><span class="sxs-lookup"><span data-stu-id="08254-140">There are one or more target images for each upgraded image.</span></span> <span data-ttu-id="08254-141">L'immagine di destinazione deve essere un'immagine di configurazione completamente non compressa del prodotto, ad esempio un'immagine amministrativa o un'immagine di installazione non compressa in un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="08254-141">The target image must be a fully uncompressed setup image of the product, such as an administrative image or an uncompressed setup image on a CD-ROM.</span></span> <span data-ttu-id="08254-142">Si noti che la funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) non genera patch binarie per i file nei file CAB.</span><span class="sxs-lookup"><span data-stu-id="08254-142">Note that the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function does not generate binary patches for files in cabinets.</span></span> <span data-ttu-id="08254-143">Il valore di questo campo viene usato con il valore nel campo aggiornato per generare i nomi delle trasformazioni che il programma di installazione aggiunge al pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="08254-143">The value in this field is used with the value in the Upgraded field to generate the names of the transforms that the installer adds to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="08254-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>PercorsoMSI</span><span class="sxs-lookup"><span data-stu-id="08254-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="08254-145">Questo campo specifica il percorso completo, incluso il nome del file, al percorso del file con estensione msi per l'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="08254-145">This field specifies the full path, including the file name, to the location of the .msi file for the target image.</span></span> <span data-ttu-id="08254-146">Si tratta del percorso dei file di origine per l'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="08254-146">This is the location of the source files for the target image.</span></span>

</dd> <dt>

<span data-ttu-id="08254-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="08254-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="08254-148">Elenco delimitato da punti e virgola di cartelle in cui cercare i file di simboli che possono essere usati per ottimizzare la generazione della patch binaria.</span><span class="sxs-lookup"><span data-stu-id="08254-148">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="08254-149">Si noti che non viene eseguita la ricerca nelle sottodirectory delle cartelle specificate in questo campo.</span><span class="sxs-lookup"><span data-stu-id="08254-149">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="08254-150">Una patch binaria ottimizzata può essere più piccola.</span><span class="sxs-lookup"><span data-stu-id="08254-150">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="08254-151">Microsoft Visual C++ deve essere installato nel computer che genera la patch e utilizzato per creare i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="08254-151">Microsoft Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="08254-152">Questo campo è facoltativo e il programma di installazione crea una patch binaria anche se non è stato specificato alcun file di simboli o se i file di simboli non sono più disponibili per Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="08254-152">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="08254-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato</span><span class="sxs-lookup"><span data-stu-id="08254-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="08254-154">Chiave esterna per la colonna aggiornata della [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="08254-154">Foreign key to the Upgraded column of the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="08254-155">La funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignora tutte le immagini aggiornate a cui non viene fatto riferimento da almeno un record della tabella TargetImages.</span><span class="sxs-lookup"><span data-stu-id="08254-155">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function ignores any upgraded image that is not referenced by at least one record of the TargetImages table.</span></span>

</dd> <dt>

<span data-ttu-id="08254-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine</span><span class="sxs-lookup"><span data-stu-id="08254-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="08254-157">Ordine relativo dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="08254-157">Relative order of the target image.</span></span> <span data-ttu-id="08254-158">Poiché è possibile applicare patch a più destinazioni a un'immagine aggiornata, il campo Order fornisce un mezzo per sequenziare le trasformazioni nell'elenco delle trasformazioni delle patch.</span><span class="sxs-lookup"><span data-stu-id="08254-158">Because multiple targets can be patched to an upgraded image, the Order field provides a means to sequence the transforms in the patch transforms list.</span></span> <span data-ttu-id="08254-159">In genere, l'ordine è dall'immagine meno recente a quella più recente.</span><span class="sxs-lookup"><span data-stu-id="08254-159">Commonly, the order is from oldest to newest image.</span></span>

</dd> <dt>

<span data-ttu-id="08254-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="08254-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span></span>
</dt> <dd>

<span data-ttu-id="08254-161">Il campo ProductValidateFlags viene usato per specificare il controllo del prodotto per evitare l'applicazione di trasformazioni irrilevanti.</span><span class="sxs-lookup"><span data-stu-id="08254-161">The ProductValidateFlags field is used to specify product checking to avoid applying irrelevant transforms.</span></span> <span data-ttu-id="08254-162">Il valore immesso in questo campo deve essere un Integer esadecimale a 8 cifre e uno dei valori validi per il parametro *iValidation* della funzione [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="08254-162">The value entered in this field must be an 8-digit hex integer and one of the valid values for the *iValidation* parameter of the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="08254-163">Il valore predefinito è 0x00000922, che è uguale a **MSITRANSFORM \_ Validate \_ UPDATEVERSION**  +  **MSITRANSFORM \_ Validate \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ Validate \_** UPGRADECODE  +  **MSITRANSFORM \_ Validate \_ Product**.</span><span class="sxs-lookup"><span data-stu-id="08254-163">The default value is 0x00000922 which equals **MSITRANSFORM\_VALIDATE\_UPDATEVERSION** + **MSITRANSFORM\_VALIDATE\_NEWEQUALBASEVERSION** + **MSITRANSFORM\_VALIDATE\_UPGRADECODE** + **MSITRANSFORM\_VALIDATE\_PRODUCT**.</span></span>

</dd> <dt>

<span data-ttu-id="08254-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="08254-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span></span>
</dt> <dd>

<span data-ttu-id="08254-165">Se questo campo è impostato su un valore diverso da zero, i file mancanti nell'immagine di destinazione vengono ignorati dal programma di installazione e rimangono invariati durante l'applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="08254-165">If this field is set to a nonzero value, files missing from the target image are ignored by the installer and left unchanged during patching.</span></span> <span data-ttu-id="08254-166">Ciò consente di apportare le patch senza richiedere l'intera immagine; sono necessari solo i file modificati del prodotto e il file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="08254-166">This enables patches to be made without requiring the entire image; only the changed files of the product and the .msi file are required.</span></span> <span data-ttu-id="08254-167">Questo può ridurre il tempo necessario per generare la patch.</span><span class="sxs-lookup"><span data-stu-id="08254-167">This may reduce the time required to generate the patch.</span></span>

> [!Note]  
> <span data-ttu-id="08254-168">Non usare il valore IgnoreMissingSrcFiles con TrustMsi impostato su 1 nella [tabella Properties](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="08254-168">Do not use the IgnoreMissingSrcFiles value with TrustMsi set to 1 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08254-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="08254-169">Remarks</span></span>

<span data-ttu-id="08254-170">Questa tabella accetta le variabili di ambiente come percorsi che iniziano con la versione 4,0 di Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="08254-170">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



