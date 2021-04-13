---
description: La tabella ExternalFiles contiene informazioni su file specifici che non fanno parte di un'immagine di destinazione normale.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Tabella ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528195"
---
# <a name="externalfiles-table-patchwizdll"></a><span data-ttu-id="d5321-103">Tabella ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="d5321-103">ExternalFiles Table (Patchwiz.dll)</span></span>

<span data-ttu-id="d5321-104">La tabella ExternalFiles contiene informazioni su file specifici che non fanno parte di un'immagine di destinazione normale.</span><span class="sxs-lookup"><span data-stu-id="d5321-104">The ExternalFiles table contains information about specific files that are not part of a regular target image.</span></span> <span data-ttu-id="d5321-105">Questi file possono esistere nei prodotti che sono stati aggiornati da un altro prodotto, aggiornamento o patch.</span><span class="sxs-lookup"><span data-stu-id="d5321-105">These files may exist in products that have been updated by another product, upgrade, or patch.</span></span> <span data-ttu-id="d5321-106">Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="d5321-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="d5321-107">La tabella ExternalFiles include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5321-107">The ExternalFiles table has the following columns.</span></span>



| <span data-ttu-id="d5321-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="d5321-108">Column</span></span>        | <span data-ttu-id="d5321-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5321-109">Type</span></span>    | <span data-ttu-id="d5321-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="d5321-110">Key</span></span> | <span data-ttu-id="d5321-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="d5321-111">Nullable</span></span> |
|---------------|---------|-----|----------|
| <span data-ttu-id="d5321-112">Famiglia</span><span class="sxs-lookup"><span data-stu-id="d5321-112">Family</span></span>        | <span data-ttu-id="d5321-113">text</span><span class="sxs-lookup"><span data-stu-id="d5321-113">text</span></span>    | <span data-ttu-id="d5321-114">S</span><span class="sxs-lookup"><span data-stu-id="d5321-114">Y</span></span>   | <span data-ttu-id="d5321-115">N</span><span class="sxs-lookup"><span data-stu-id="d5321-115">N</span></span>        |
| <span data-ttu-id="d5321-116">FTK</span><span class="sxs-lookup"><span data-stu-id="d5321-116">FTK</span></span>           | <span data-ttu-id="d5321-117">text</span><span class="sxs-lookup"><span data-stu-id="d5321-117">text</span></span>    | <span data-ttu-id="d5321-118">S</span><span class="sxs-lookup"><span data-stu-id="d5321-118">Y</span></span>   | <span data-ttu-id="d5321-119">N</span><span class="sxs-lookup"><span data-stu-id="d5321-119">N</span></span>        |
| <span data-ttu-id="d5321-120">FilePath</span><span class="sxs-lookup"><span data-stu-id="d5321-120">FilePath</span></span>      | <span data-ttu-id="d5321-121">text</span><span class="sxs-lookup"><span data-stu-id="d5321-121">text</span></span>    | <span data-ttu-id="d5321-122">S</span><span class="sxs-lookup"><span data-stu-id="d5321-122">Y</span></span>   | <span data-ttu-id="d5321-123">N</span><span class="sxs-lookup"><span data-stu-id="d5321-123">N</span></span>        |
| <span data-ttu-id="d5321-124">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="d5321-124">SymbolPaths</span></span>   | <span data-ttu-id="d5321-125">text</span><span class="sxs-lookup"><span data-stu-id="d5321-125">text</span></span>    |     | <span data-ttu-id="d5321-126">S</span><span class="sxs-lookup"><span data-stu-id="d5321-126">Y</span></span>        |
| <span data-ttu-id="d5321-127">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="d5321-127">IgnoreOffsets</span></span> | <span data-ttu-id="d5321-128">text</span><span class="sxs-lookup"><span data-stu-id="d5321-128">text</span></span>    |     | <span data-ttu-id="d5321-129">S</span><span class="sxs-lookup"><span data-stu-id="d5321-129">Y</span></span>        |
| <span data-ttu-id="d5321-130">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="d5321-130">IgnoreLengths</span></span> | <span data-ttu-id="d5321-131">text</span><span class="sxs-lookup"><span data-stu-id="d5321-131">text</span></span>    |     | <span data-ttu-id="d5321-132">S</span><span class="sxs-lookup"><span data-stu-id="d5321-132">Y</span></span>        |
| <span data-ttu-id="d5321-133">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="d5321-133">RetainOffsets</span></span> | <span data-ttu-id="d5321-134">text</span><span class="sxs-lookup"><span data-stu-id="d5321-134">text</span></span>    |     | <span data-ttu-id="d5321-135">N</span><span class="sxs-lookup"><span data-stu-id="d5321-135">N</span></span>        |
| <span data-ttu-id="d5321-136">JSON</span><span class="sxs-lookup"><span data-stu-id="d5321-136">Order</span></span>         | <span data-ttu-id="d5321-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="d5321-137">integer</span></span> |     | <span data-ttu-id="d5321-138">S</span><span class="sxs-lookup"><span data-stu-id="d5321-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d5321-139">Colonne</span><span class="sxs-lookup"><span data-stu-id="d5321-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d5321-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famiglia</span><span class="sxs-lookup"><span data-stu-id="d5321-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="d5321-141">Chiave esterna per la colonna Family della [tabella ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="d5321-141">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5321-142"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="d5321-142"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="d5321-143">Chiave esterna nella [tabella file](file-table.md) del file con estensione msi dell'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="d5321-143">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="d5321-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span><span class="sxs-lookup"><span data-stu-id="d5321-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span></span>
</dt> <dd>

<span data-ttu-id="d5321-145">Percorso completo del file esterno, incluso il nome del file.</span><span class="sxs-lookup"><span data-stu-id="d5321-145">Full path of the external file including the file name.</span></span> <span data-ttu-id="d5321-146">Il campo FilePath viene usato per individuare il file specificato nella colonna FTK.</span><span class="sxs-lookup"><span data-stu-id="d5321-146">FilePath field is used to locate the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="d5321-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="d5321-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="d5321-148">Percorso completo in cui sono stati cercati i file di simboli del file specificato nella colonna FTK.</span><span class="sxs-lookup"><span data-stu-id="d5321-148">Full path searched for symbol files of the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="d5321-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="d5321-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="d5321-150">Il valore in questo campo è un elenco delimitato da virgole di numeri di offset dell'intervallo per gli intervalli da ignorare nel file esterno.</span><span class="sxs-lookup"><span data-stu-id="d5321-150">The value in this field is a comma-delimited list of range offset numbers for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="d5321-151">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="d5321-151">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="d5321-152">Questa colonna è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d5321-152">This column is optional.</span></span>

<span data-ttu-id="d5321-153">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="d5321-153">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="d5321-154">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="d5321-154">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="d5321-155">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="d5321-155">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="d5321-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="d5321-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="d5321-157">Il valore in questo campo è un elenco delimitato da virgole di lunghezze di intervallo in byte per gli intervalli da ignorare nel file esterno.</span><span class="sxs-lookup"><span data-stu-id="d5321-157">The value in this field is a comma-delimited list of range lengths in bytes for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="d5321-158">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="d5321-158">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="d5321-159">Questa colonna è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d5321-159">This column is optional.</span></span>

<span data-ttu-id="d5321-160">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="d5321-160">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="d5321-161">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="d5321-161">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="d5321-162">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="d5321-162">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="d5321-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="d5321-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="d5321-164">Il valore in questo campo è un elenco delimitato da virgole di numeri di offset dell'intervallo per gli intervalli da conservare nel file esterno.</span><span class="sxs-lookup"><span data-stu-id="d5321-164">The value in this field is a comma-delimited list of range offset numbers for the ranges to be retained in the External file.</span></span> <span data-ttu-id="d5321-165">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna RetainOffsets del record corrispondente nella [tabella FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="d5321-165">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span></span>

<span data-ttu-id="d5321-166">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="d5321-166">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="d5321-167">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="d5321-167">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="d5321-168">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="d5321-168">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="d5321-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine</span><span class="sxs-lookup"><span data-stu-id="d5321-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="d5321-170">Se vengono specificate due o più versioni per lo stesso file esterno, la tabella può contenere più record con valori corrispondenti nei campi FTK e Family.</span><span class="sxs-lookup"><span data-stu-id="d5321-170">If two or more versions are specified for the same external file, the table may contain multiple records with matching values in the FTK and Family fields.</span></span> <span data-ttu-id="d5321-171">In questo caso, il campo Order può specificare l'ordine dei file esterni da usare durante la creazione della patch.</span><span class="sxs-lookup"><span data-stu-id="d5321-171">In this case, the Order field may specify the order of external files to use when creating the patch.</span></span> <span data-ttu-id="d5321-172">L'ordine è dalla versione meno recente a quella più recente.</span><span class="sxs-lookup"><span data-stu-id="d5321-172">The order is from the oldest to the most recent version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5321-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5321-173">Remarks</span></span>

<span data-ttu-id="d5321-174">Questa tabella accetta le variabili di ambiente come percorsi che iniziano con la versione 4,0 di Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="d5321-174">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5321-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5321-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5321-176">Applicazione di patch alle aree selezionate di un file</span><span class="sxs-lookup"><span data-stu-id="d5321-176">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



