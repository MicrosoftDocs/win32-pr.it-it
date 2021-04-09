---
description: La tabella FamilyFileRanges contiene informazioni su file specifici di un'immagine aggiornata con intervalli che non devono mai essere sovrascritti.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabella FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130678"
---
# <a name="familyfileranges-table-patchwizdll"></a><span data-ttu-id="f3f48-103">Tabella FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f3f48-103">FamilyFileRanges Table (Patchwiz.dll)</span></span>

<span data-ttu-id="f3f48-104">La tabella FamilyFileRanges contiene informazioni su file specifici di un'immagine aggiornata con intervalli che non devono mai essere sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="f3f48-104">The FamilyFileRanges table contains information about particular files of an upgraded image with ranges that should never be overwritten.</span></span> <span data-ttu-id="f3f48-105">Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f48-105">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="f3f48-106">La tabella FamilyFileRanges include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3f48-106">The FamilyFileRanges table has the following columns.</span></span>



| <span data-ttu-id="f3f48-107">Colonna</span><span class="sxs-lookup"><span data-stu-id="f3f48-107">Column</span></span>        | <span data-ttu-id="f3f48-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3f48-108">Type</span></span> | <span data-ttu-id="f3f48-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="f3f48-109">Key</span></span> | <span data-ttu-id="f3f48-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="f3f48-110">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="f3f48-111">Famiglia</span><span class="sxs-lookup"><span data-stu-id="f3f48-111">Family</span></span>        | <span data-ttu-id="f3f48-112">text</span><span class="sxs-lookup"><span data-stu-id="f3f48-112">text</span></span> | <span data-ttu-id="f3f48-113">S</span><span class="sxs-lookup"><span data-stu-id="f3f48-113">Y</span></span>   | <span data-ttu-id="f3f48-114">N</span><span class="sxs-lookup"><span data-stu-id="f3f48-114">N</span></span>        |
| <span data-ttu-id="f3f48-115">FTK</span><span class="sxs-lookup"><span data-stu-id="f3f48-115">FTK</span></span>           | <span data-ttu-id="f3f48-116">text</span><span class="sxs-lookup"><span data-stu-id="f3f48-116">text</span></span> | <span data-ttu-id="f3f48-117">S</span><span class="sxs-lookup"><span data-stu-id="f3f48-117">Y</span></span>   | <span data-ttu-id="f3f48-118">N</span><span class="sxs-lookup"><span data-stu-id="f3f48-118">N</span></span>        |
| <span data-ttu-id="f3f48-119">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="f3f48-119">RetainOffsets</span></span> | <span data-ttu-id="f3f48-120">text</span><span class="sxs-lookup"><span data-stu-id="f3f48-120">text</span></span> |     | <span data-ttu-id="f3f48-121">N</span><span class="sxs-lookup"><span data-stu-id="f3f48-121">N</span></span>        |
| <span data-ttu-id="f3f48-122">RetainLengths</span><span class="sxs-lookup"><span data-stu-id="f3f48-122">RetainLengths</span></span> | <span data-ttu-id="f3f48-123">text</span><span class="sxs-lookup"><span data-stu-id="f3f48-123">text</span></span> |     | <span data-ttu-id="f3f48-124">N</span><span class="sxs-lookup"><span data-stu-id="f3f48-124">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f3f48-125">Colonne</span><span class="sxs-lookup"><span data-stu-id="f3f48-125">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f3f48-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famiglia</span><span class="sxs-lookup"><span data-stu-id="f3f48-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="f3f48-127">Chiave esterna per la colonna Family della [tabella ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="f3f48-127">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3f48-128"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="f3f48-128"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="f3f48-129">Chiave esterna nelle [tabelle di file](file-table.md) di tutte le immagini aggiornate nella famiglia di immagini.</span><span class="sxs-lookup"><span data-stu-id="f3f48-129">Foreign key into the [File tables](file-table.md) of all the upgraded images in the image family.</span></span>

</dd> <dt>

<span data-ttu-id="f3f48-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="f3f48-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="f3f48-131">Offset degli intervalli che non possono essere sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="f3f48-131">The offset of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="f3f48-132">Il valore in questo campo è un elenco dei numeri di offset dell'intervallo per gli intervalli che non devono essere sovrascritti nei file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f3f48-132">The value in this field is a list of the range offset numbers for ranges that are not to be overwritten in the target files.</span></span> <span data-ttu-id="f3f48-133">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna RetainLengths.</span><span class="sxs-lookup"><span data-stu-id="f3f48-133">The order and number of the ranges in the list must match the items in the RetainLengths column.</span></span>

<span data-ttu-id="f3f48-134">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="f3f48-134">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="f3f48-135">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="f3f48-135">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="f3f48-136">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="f3f48-136">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="f3f48-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span><span class="sxs-lookup"><span data-stu-id="f3f48-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span></span>
</dt> <dd>

<span data-ttu-id="f3f48-138">Lunghezza in byte degli intervalli che non possono essere sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="f3f48-138">The length in bytes of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="f3f48-139">Il valore in questo campo è un elenco di numeri di lunghezza intervallo per gli intervalli da mantenere nei file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f3f48-139">The value in this field is a list of range length numbers for ranges to retain in target files.</span></span> <span data-ttu-id="f3f48-140">L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna RetainOffsets.</span><span class="sxs-lookup"><span data-stu-id="f3f48-140">The order and number of the ranges in the list must match the items in the RetainOffsets column.</span></span>

<span data-ttu-id="f3f48-141">I valori possono essere decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="f3f48-141">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="f3f48-142">[Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="f3f48-142">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="f3f48-143">Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.</span><span class="sxs-lookup"><span data-stu-id="f3f48-143">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3f48-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3f48-144">Remarks</span></span>

<span data-ttu-id="f3f48-145">Gli offset e le lunghezze immesse in RetainOffsets e RetainLengths non devono specificare intervalli sovrapposti.</span><span class="sxs-lookup"><span data-stu-id="f3f48-145">The offsets and lengths entered in RetainOffsets and RetainLengths must not specify overlapping ranges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3f48-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3f48-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3f48-147">Applicazione di patch alle aree selezionate di un file</span><span class="sxs-lookup"><span data-stu-id="f3f48-147">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



