---
description: La tabella PatchSequence viene utilizzata per generare la tabella MsiPatchSequence in una patch. La tabella richiede la versione di PATCHWIZ.DLL disponibile con Windows Installer&\# 160; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabella PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885490"
---
# <a name="patchsequence-table-patchwizdll"></a><span data-ttu-id="bb491-104">Tabella PatchSequence (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="bb491-104">PatchSequence Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="bb491-105">La tabella PatchSequence viene utilizzata per generare la [tabella MsiPatchSequence](msipatchsequence-table.md) in una patch.</span><span class="sxs-lookup"><span data-stu-id="bb491-105">The PatchSequence Table is used to generate the [MsiPatchSequence Table](msipatchsequence-table.md) in a patch.</span></span> <span data-ttu-id="bb491-106">La tabella richiede la versione di [PATCHWIZ.DLL](patchwiz-dll.md) disponibile con Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="bb491-106">The table requires the version of [PATCHWIZ.DLL](patchwiz-dll.md) that is available with Windows Installer 3.0.</span></span>

<span data-ttu-id="bb491-107">Nella tabella seguente vengono identificate le colonne della tabella PatchSequence.</span><span class="sxs-lookup"><span data-stu-id="bb491-107">The following table identifies the columns of the PatchSequence Table.</span></span>



| <span data-ttu-id="bb491-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="bb491-108">Column</span></span>      | <span data-ttu-id="bb491-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb491-109">Type</span></span>       | <span data-ttu-id="bb491-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="bb491-110">Key</span></span> | <span data-ttu-id="bb491-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="bb491-111">Nullable</span></span> |
|-------------|------------|-----|----------|
| <span data-ttu-id="bb491-112">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="bb491-112">PatchFamily</span></span> | <span data-ttu-id="bb491-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="bb491-113">Identifier</span></span> | <span data-ttu-id="bb491-114">S</span><span class="sxs-lookup"><span data-stu-id="bb491-114">Y</span></span>   | <span data-ttu-id="bb491-115">N</span><span class="sxs-lookup"><span data-stu-id="bb491-115">N</span></span>        |
| <span data-ttu-id="bb491-116">Destinazione</span><span class="sxs-lookup"><span data-stu-id="bb491-116">Target</span></span>      | <span data-ttu-id="bb491-117">Testo</span><span class="sxs-lookup"><span data-stu-id="bb491-117">Text</span></span>       | <span data-ttu-id="bb491-118">S</span><span class="sxs-lookup"><span data-stu-id="bb491-118">Y</span></span>   | <span data-ttu-id="bb491-119">S</span><span class="sxs-lookup"><span data-stu-id="bb491-119">Y</span></span>        |
| <span data-ttu-id="bb491-120">Sequenza</span><span class="sxs-lookup"><span data-stu-id="bb491-120">Sequence</span></span>    | <span data-ttu-id="bb491-121">Versione</span><span class="sxs-lookup"><span data-stu-id="bb491-121">Version</span></span>    |     | <span data-ttu-id="bb491-122">S</span><span class="sxs-lookup"><span data-stu-id="bb491-122">Y</span></span>        |
| <span data-ttu-id="bb491-123">Sostituire</span><span class="sxs-lookup"><span data-stu-id="bb491-123">Supersede</span></span>   | <span data-ttu-id="bb491-124">Integer</span><span class="sxs-lookup"><span data-stu-id="bb491-124">Integer</span></span>    |     | <span data-ttu-id="bb491-125">S</span><span class="sxs-lookup"><span data-stu-id="bb491-125">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="bb491-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="bb491-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bb491-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="bb491-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="bb491-128">Identificatore che indica le famiglie di sequenze a cui appartiene questa patch.</span><span class="sxs-lookup"><span data-stu-id="bb491-128">The identifier that indicates the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="bb491-129">I valori nelle colonne target e PatchFamily definiscono la chiave primaria per la tabella.</span><span class="sxs-lookup"><span data-stu-id="bb491-129">The values in the Target and PatchFamily columns together define the primary key for the table.</span></span> <span data-ttu-id="bb491-130">Una patch che appartiene a più famiglie di sequenze o ha sequenze diverse a seconda del codice prodotto della destinazione, può avere una riga per ogni associazione.</span><span class="sxs-lookup"><span data-stu-id="bb491-130">A patch that belongs to multiple sequence families, or has different sequences depending on the product code of the target, can have one row for each pairing.</span></span> <span data-ttu-id="bb491-131">Questo valore viene usato per popolare la colonna PatchFamily della [tabella MsiPatchSequence](msipatchsequence-table.md) che appartiene alla patch.</span><span class="sxs-lookup"><span data-stu-id="bb491-131">This value is used to populate the PatchFamily column of the [MsiPatchSequence Table](msipatchsequence-table.md) that belongs to the patch.</span></span>

</dd> <dt>

<span data-ttu-id="bb491-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione</span><span class="sxs-lookup"><span data-stu-id="bb491-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="bb491-133">La colonna di destinazione viene utilizzata per filtrare il PatchFamily in base al codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="bb491-133">The Target column is used to filter the PatchFamily by product code.</span></span>

<span data-ttu-id="bb491-134">Un valore NULL in questa colonna indica che questo PatchFamily si applica a tutte le destinazioni della patch.</span><span class="sxs-lookup"><span data-stu-id="bb491-134">A NULL value in this column indicates that this PatchFamily applies to all targets of the patch.</span></span> <span data-ttu-id="bb491-135">Se questa colonna contiene una chiave esterna per la [tabella TargetImages](targetimages-table-patchwiz-dll-.md), il codice prodotto dell'immagine specificata viene recuperato e utilizzato per popolare il valore del codice prodotto nella riga della nuova patch della [tabella MsiPatchSequence](msipatchsequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="bb491-135">If this column contains a foreign key to the [TargetImages Table](targetimages-table-patchwiz-dll-.md), the product code of the specified image is retrieved and used to populate the product code value in the new patch's row of the [MsiPatchSequence Table](msipatchsequence-table.md).</span></span> <span data-ttu-id="bb491-136">Se questa colonna contiene un GUID, il GUID viene utilizzato per popolare il valore del codice prodotto della riga nella tabella MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="bb491-136">If this column contains a GUID, the GUID is used to populate the product code value of the row in the MsiPatchSequence Table.</span></span>

</dd> <dt>

<span data-ttu-id="bb491-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="bb491-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="bb491-138">Il valore nella colonna sequenza viene utilizzato per popolare la colonna sequenza della [tabella MsiPatchSequence](msipatchsequence-table.md) del nuovo file di patch.</span><span class="sxs-lookup"><span data-stu-id="bb491-138">The value in the Sequence column is used to populate the Sequence column of the [MsiPatchSequence Table](msipatchsequence-table.md) of the new patch file.</span></span>

<span data-ttu-id="bb491-139">Se il valore è NULL, viene generato automaticamente un numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="bb491-139">If the value is NULL, a sequence number is generated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="bb491-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Sostituire</span><span class="sxs-lookup"><span data-stu-id="bb491-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Supersede</span></span>
</dt> <dd>

<span data-ttu-id="bb491-141">Il valore **msidbPatchSequenceSupersedeEarlier** o 1 in questo campo indica che questa patch sostituisce [gli aggiornamenti più](small-updates.md) recenti nelle famiglie di sequenze a cui appartiene questa patch.</span><span class="sxs-lookup"><span data-stu-id="bb491-141">A value of **msidbPatchSequenceSupersedeEarlier** or 1 in this field indicates that this patch supersedes earlier [small updates](small-updates.md) in the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="bb491-142">Il valore in questa colonna viene usato per impostare la colonna attributi della riga della nuova patch nella [tabella MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bb491-142">The value in this column is used to set the Attributes column of the new patch's row in the [MsiPatchSequence Table](msipatchsequence-table.md) .</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="bb491-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb491-143">Remarks</span></span>

<span data-ttu-id="bb491-144">Disponibile a partire da Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="bb491-144">Available beginning in Windows Installer 3.0.</span></span>

 

 



