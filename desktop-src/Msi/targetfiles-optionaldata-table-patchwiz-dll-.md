---
description: La \_ tabella TargetFiles OptionalData contiene informazioni su file specifici in un'immagine di destinazione. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Tabella TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967900"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="143ae-104">\_Tabella TargetFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="143ae-104">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="143ae-105">La \_ tabella TargetFiles OptionalData contiene informazioni su file specifici in un'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="143ae-105">The TargetFiles\_OptionalData table contains information about specific files in a target image.</span></span> <span data-ttu-id="143ae-106">Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="143ae-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="143ae-107">La \_ tabella OptionalData di TargetFiles include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="143ae-107">The TargetFiles\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="143ae-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="143ae-108">Column</span></span>        | <span data-ttu-id="143ae-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="143ae-109">Type</span></span> | <span data-ttu-id="143ae-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="143ae-110">Key</span></span> | <span data-ttu-id="143ae-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="143ae-111">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="143ae-112">Destinazione</span><span class="sxs-lookup"><span data-stu-id="143ae-112">Target</span></span>        | <span data-ttu-id="143ae-113">text</span><span class="sxs-lookup"><span data-stu-id="143ae-113">text</span></span> | <span data-ttu-id="143ae-114">S</span><span class="sxs-lookup"><span data-stu-id="143ae-114">Y</span></span>   | <span data-ttu-id="143ae-115">N</span><span class="sxs-lookup"><span data-stu-id="143ae-115">N</span></span>        |
| <span data-ttu-id="143ae-116">FTK</span><span class="sxs-lookup"><span data-stu-id="143ae-116">FTK</span></span>           | <span data-ttu-id="143ae-117">text</span><span class="sxs-lookup"><span data-stu-id="143ae-117">text</span></span> | <span data-ttu-id="143ae-118">S</span><span class="sxs-lookup"><span data-stu-id="143ae-118">Y</span></span>   | <span data-ttu-id="143ae-119">N</span><span class="sxs-lookup"><span data-stu-id="143ae-119">N</span></span>        |
| <span data-ttu-id="143ae-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="143ae-120">SymbolPaths</span></span>   | <span data-ttu-id="143ae-121">text</span><span class="sxs-lookup"><span data-stu-id="143ae-121">text</span></span> |     | <span data-ttu-id="143ae-122">S</span><span class="sxs-lookup"><span data-stu-id="143ae-122">Y</span></span>        |
| <span data-ttu-id="143ae-123">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="143ae-123">IgnoreOffsets</span></span> | <span data-ttu-id="143ae-124">text</span><span class="sxs-lookup"><span data-stu-id="143ae-124">text</span></span> |     | <span data-ttu-id="143ae-125">S</span><span class="sxs-lookup"><span data-stu-id="143ae-125">Y</span></span>        |
| <span data-ttu-id="143ae-126">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="143ae-126">IgnoreLengths</span></span> | <span data-ttu-id="143ae-127">text</span><span class="sxs-lookup"><span data-stu-id="143ae-127">text</span></span> |     | <span data-ttu-id="143ae-128">S</span><span class="sxs-lookup"><span data-stu-id="143ae-128">Y</span></span>        |
| <span data-ttu-id="143ae-129">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="143ae-129">RetainOffsets</span></span> | <span data-ttu-id="143ae-130">text</span><span class="sxs-lookup"><span data-stu-id="143ae-130">text</span></span> |     | <span data-ttu-id="143ae-131">S</span><span class="sxs-lookup"><span data-stu-id="143ae-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="143ae-132">Colonne</span><span class="sxs-lookup"><span data-stu-id="143ae-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="143ae-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione</span><span class="sxs-lookup"><span data-stu-id="143ae-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="143ae-134">Chiave esterna per la colonna di destinazione della [tabella TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="143ae-134">Foreign key to the Target column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="143ae-135"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="143ae-135"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="143ae-136">Chiave esterna nella [tabella file](file-table.md) dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="143ae-136">Foreign key into the [File table](file-table.md) of target image.</span></span>

</dd> <dt>

<span data-ttu-id="143ae-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="143ae-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="143ae-138">Il valore in questo campo viene aggiunto all'elenco delimitato da punti e virgola di cartelle nella colonna SymbolPaths della [tabella TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) al momento della generazione della patch e può essere usato per aggiungere i file di simboli per un file specifico.</span><span class="sxs-lookup"><span data-stu-id="143ae-138">The value in this field is added to the semicolon delimited list of folders in the SymbolPaths column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="143ae-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="143ae-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="143ae-140">Il valore in questo campo è un elenco delimitato da virgole di numeri di offset intervallo per gli intervalli da ignorare nel file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="143ae-140">The value in this field is a comma delimited list of range offset numbers for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="143ae-141">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="143ae-141">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="143ae-142">Questa colonna è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="143ae-142">This column is optional.</span></span>

<span data-ttu-id="143ae-143">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="143ae-143">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="143ae-144">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="143ae-144">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="143ae-145">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="143ae-145">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="143ae-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="143ae-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="143ae-147">Il valore in questo campo è un elenco delimitato da virgole di lunghezze di intervallo in byte per gli intervalli da ignorare nel file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="143ae-147">The value in this field is a comma delimited list of range lengths in bytes for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="143ae-148">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="143ae-148">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="143ae-149">Questa colonna è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="143ae-149">This column is optional.</span></span>

<span data-ttu-id="143ae-150">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="143ae-150">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="143ae-151">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="143ae-151">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="143ae-152">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="143ae-152">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="143ae-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="143ae-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="143ae-154">Il valore in questo campo è un elenco delimitato da virgole di numeri di offset intervallo per gli intervalli da conservare nel file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="143ae-154">The value in this field is a comma delimited list of range offset numbers for the ranges to be retained in the Target file.</span></span> <span data-ttu-id="143ae-155">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna RetainOffsets del record corrispondente nella [tabella FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span><span class="sxs-lookup"><span data-stu-id="143ae-155">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span></span>

<span data-ttu-id="143ae-156">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="143ae-156">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="143ae-157">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="143ae-157">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="143ae-158">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="143ae-158">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="143ae-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="143ae-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="143ae-160">Applicazione di patch alle aree selezionate di un file</span><span class="sxs-lookup"><span data-stu-id="143ae-160">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



