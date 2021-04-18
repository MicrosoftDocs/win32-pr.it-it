---
description: La tabella MsiPatchSequence contiene tutte le informazioni richieste dal programma di installazione per determinare la sequenza di applicazione di una patch di aggiornamento ridotta rispetto a tutte le altre patch.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabella MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318657"
---
# <a name="msipatchsequence-table"></a><span data-ttu-id="8b056-103">Tabella MsiPatchSequence</span><span class="sxs-lookup"><span data-stu-id="8b056-103">MsiPatchSequence Table</span></span>

<span data-ttu-id="8b056-104">La tabella MsiPatchSequence contiene tutte le informazioni richieste dal programma di installazione per determinare la sequenza di applicazione di una patch di [aggiornamento ridotta](small-updates.md) rispetto a tutte le altre patch.</span><span class="sxs-lookup"><span data-stu-id="8b056-104">The MsiPatchSequence table contains all the information the installer requires to determine the sequence of application of a [small update](small-updates.md) patch relative to all other patches.</span></span> <span data-ttu-id="8b056-105">La tabella deve trovarsi nel database del file di correzione e non in una trasformazione della patch.</span><span class="sxs-lookup"><span data-stu-id="8b056-105">The table must be in the database of the patch file and not in a transform in the patch.</span></span> <span data-ttu-id="8b056-106">Quando si applica una patch di [aggiornamento principale](major-upgrades.md) , il programma di installazione ignora questa tabella.</span><span class="sxs-lookup"><span data-stu-id="8b056-106">The installer ignores this table when applying a [major upgrade](major-upgrades.md) patch.</span></span> <span data-ttu-id="8b056-107">Quando si applica una patch di [aggiornamento secondaria](minor-upgrades.md) , il programma di installazione usa questa tabella solo per identificare le patch sostituite che non devono essere sequenziate.</span><span class="sxs-lookup"><span data-stu-id="8b056-107">When applying a [minor upgrade](minor-upgrades.md) patch, the installer only uses this table to identify superseded patches that must not be sequenced.</span></span>

<span data-ttu-id="8b056-108">La **tabella MsiPatchSequence** include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8b056-108">The **MsiPatchSequence table** has the following columns.</span></span>



| <span data-ttu-id="8b056-109">Colonna</span><span class="sxs-lookup"><span data-stu-id="8b056-109">Column</span></span>      | <span data-ttu-id="8b056-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b056-110">Type</span></span>                         | <span data-ttu-id="8b056-111">Chiave</span><span class="sxs-lookup"><span data-stu-id="8b056-111">Key</span></span> | <span data-ttu-id="8b056-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="8b056-112">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="8b056-113">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="8b056-113">PatchFamily</span></span> | [<span data-ttu-id="8b056-114">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8b056-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="8b056-115">S</span><span class="sxs-lookup"><span data-stu-id="8b056-115">Y</span></span>   | <span data-ttu-id="8b056-116">N</span><span class="sxs-lookup"><span data-stu-id="8b056-116">N</span></span>        |
| <span data-ttu-id="8b056-117">ProductCode</span><span class="sxs-lookup"><span data-stu-id="8b056-117">ProductCode</span></span> | [<span data-ttu-id="8b056-118">GUID</span><span class="sxs-lookup"><span data-stu-id="8b056-118">GUID</span></span>](guid.md)             | <span data-ttu-id="8b056-119">S</span><span class="sxs-lookup"><span data-stu-id="8b056-119">Y</span></span>   | <span data-ttu-id="8b056-120">S</span><span class="sxs-lookup"><span data-stu-id="8b056-120">Y</span></span>        |
| <span data-ttu-id="8b056-121">Sequenza</span><span class="sxs-lookup"><span data-stu-id="8b056-121">Sequence</span></span>    | [<span data-ttu-id="8b056-122">Versione</span><span class="sxs-lookup"><span data-stu-id="8b056-122">Version</span></span>](version.md)       | <span data-ttu-id="8b056-123">N</span><span class="sxs-lookup"><span data-stu-id="8b056-123">N</span></span>   | <span data-ttu-id="8b056-124">N</span><span class="sxs-lookup"><span data-stu-id="8b056-124">N</span></span>        |
| <span data-ttu-id="8b056-125">Attributi</span><span class="sxs-lookup"><span data-stu-id="8b056-125">Attributes</span></span>  | [<span data-ttu-id="8b056-126">Integer</span><span class="sxs-lookup"><span data-stu-id="8b056-126">Integer</span></span>](integer.md)       | <span data-ttu-id="8b056-127">N</span><span class="sxs-lookup"><span data-stu-id="8b056-127">N</span></span>   | <span data-ttu-id="8b056-128">S</span><span class="sxs-lookup"><span data-stu-id="8b056-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8b056-129">Colonne</span><span class="sxs-lookup"><span data-stu-id="8b056-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8b056-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="8b056-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="8b056-131">Specifica che la patch è un membro della famiglia di patch denominata in questo campo.</span><span class="sxs-lookup"><span data-stu-id="8b056-131">Specifies that the patch is a member of the patch family named in this field.</span></span> <span data-ttu-id="8b056-132">Le patch presenti nella stessa famiglia di patch destinate alla stessa versione del prodotto vengono ordinate in base ai valori nella colonna sequenza.</span><span class="sxs-lookup"><span data-stu-id="8b056-132">Patches in the same patch family that target the same product version are sorted by the values in the Sequence column.</span></span> <span data-ttu-id="8b056-133">Le patch all'interno della famiglia di patch vengono applicate al prodotto di destinazione in ordine di sequenza crescente.</span><span class="sxs-lookup"><span data-stu-id="8b056-133">The patches within the patch family are applied to the target product in the order of increasing sequence.</span></span> <span data-ttu-id="8b056-134">PatchFamily viene utilizzato anche per determinare quali patch devono essere sostituite.</span><span class="sxs-lookup"><span data-stu-id="8b056-134">The PatchFamily is also used to determine which patches are to be superseded.</span></span> <span data-ttu-id="8b056-135">È possibile che una patch venga elencata in più righe e appartenga a più famiglie di patch se si applica a più di un prodotto o include più correzioni.</span><span class="sxs-lookup"><span data-stu-id="8b056-135">A patch may be listed in multiple rows and belong to multiple patch families if it applies to more than one product or includes multiple fixes.</span></span>

<span data-ttu-id="8b056-136">Il Windows Installer non interpreta il valore PatchFamily in alcun modo diverso dai confronti per l'uguaglianza rispetto ad altri valori PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="8b056-136">The Windows Installer does not interpret the PatchFamily value in any way other than comparisons for equality against other PatchFamily values.</span></span> <span data-ttu-id="8b056-137">Un valore PatchFamily deve essere univoco all'interno del ProductCode di destinazione dal set di patch.</span><span class="sxs-lookup"><span data-stu-id="8b056-137">A PatchFamily value must be unique within the ProductCode targeted by the set of patches.</span></span> <span data-ttu-id="8b056-138">Negli scenari di applicazione di patch complessi l'identificatore PatchFamily può essere univoco a livello globale.</span><span class="sxs-lookup"><span data-stu-id="8b056-138">In the complex patching scenarios the PatchFamily identifier may need to be globally unique.</span></span>

</dd> <dt>

<span data-ttu-id="8b056-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span><span class="sxs-lookup"><span data-stu-id="8b056-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span></span>
</dt> <dd>

<span data-ttu-id="8b056-140">Un valore in questo campo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8b056-140">A value in this field is optional.</span></span> <span data-ttu-id="8b056-141">Se in questo campo viene immesso un GUID del [Codice prodotto](product-codes.md) e la patch viene applicata al prodotto specificato, la patch viene ordinata e applicata come membro del PatchFamily specificato.</span><span class="sxs-lookup"><span data-stu-id="8b056-141">If a [product code](product-codes.md) GUID is entered in this field and the patch is being applied to the specified product, the patch is sorted and applied as a member of the specified PatchFamily.</span></span> <span data-ttu-id="8b056-142">Se in questo campo viene immesso un GUID del codice prodotto e la patch non viene applicata al prodotto specificato da ProductCode, la riga viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="8b056-142">If a product code GUID is entered in this field and the patch is not being applied to the product specified by ProductCode, this row is ignored.</span></span> <span data-ttu-id="8b056-143">Se il valore in ProductCode è NULL, la patch viene ordinata e applicata come membro di PatchFamily per tutte le destinazioni della patch, indipendentemente dal codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8b056-143">If the value in ProductCode is NULL, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

<span data-ttu-id="8b056-144">Una patch può includere più righe nello stesso PatchFamily e un ProductCode diverso per ogni prodotto di destinazione della patch.</span><span class="sxs-lookup"><span data-stu-id="8b056-144">A patch can have multiple rows in the same PatchFamily and a different ProductCode for each product targeted by the patch.</span></span> <span data-ttu-id="8b056-145">Una riga per PatchFamily può specificare NULL per ProductCode.</span><span class="sxs-lookup"><span data-stu-id="8b056-145">One row for the PatchFamily can specify NULL for ProductCode.</span></span> <span data-ttu-id="8b056-146">Se il prodotto di destinazione corrisponde a una riga con un valore di ProductCode non NULL, il programma di installazione utilizza la riga corrispondente e ignora la riga con il ProductCode NULL.</span><span class="sxs-lookup"><span data-stu-id="8b056-146">If the target product matches a row with a non-NULL ProductCode, the installer uses the matching row and ignores the row with the NULL ProductCode.</span></span> <span data-ttu-id="8b056-147">Se nessuno dei codici prodotto specificati corrisponde alla destinazione, la patch viene ordinata e applicata come membro di PatchFamily per tutte le destinazioni della patch, indipendentemente dal codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8b056-147">If none of the specified product codes match the target, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

</dd> <dt>

<span data-ttu-id="8b056-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="8b056-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="8b056-149">Il valore nella colonna sequenza specifica la sequenza di questa patch all'interno del PatchFamily specificato.</span><span class="sxs-lookup"><span data-stu-id="8b056-149">The value in the Sequence column specifies the sequence of this patch within the specified PatchFamily.</span></span> <span data-ttu-id="8b056-150">Il valore in sequenza è espresso nel formato dati della [versione](version.md) .</span><span class="sxs-lookup"><span data-stu-id="8b056-150">The value in Sequence is expressed in the format of [Version](version.md) data.</span></span> <span data-ttu-id="8b056-151">Il valore contiene tra 1 e 4 campi e ogni campo ha un intervallo compreso tra 0 e 65535.</span><span class="sxs-lookup"><span data-stu-id="8b056-151">The value contains between 1 and 4 fields and each field has a range of 0 to 65535.</span></span> <span data-ttu-id="8b056-152">I membri di PatchFamily vengono ordinati e applicati al prodotto di destinazione in ordine di incremento dei valori di sequenza.</span><span class="sxs-lookup"><span data-stu-id="8b056-152">Members of PatchFamily are sorted and applied to the target product in the order of increasing Sequence values.</span></span> <span data-ttu-id="8b056-153">Ad esempio, i sei valori seguenti sono in aumento: 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.</span><span class="sxs-lookup"><span data-stu-id="8b056-153">For example, the following six values are increasing: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.</span></span>

</dd> <dt>

<span data-ttu-id="8b056-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="8b056-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="8b056-155">La presenza dell'attributo **msidbPatchSequenceSupersedeEarlier** in una riga indica che la patch di [aggiornamento di piccole dimensioni](small-updates.md) sostituisce gli aggiornamenti forniti da tutte le patch con valori di sequenza minori nello stesso PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="8b056-155">The presence of the **msidbPatchSequenceSupersedeEarlier** attribute in a row indicates that the [small update](small-updates.md) patch supersedes the updates provided by all patches with lesser Sequence values in the same PatchFamily.</span></span> <span data-ttu-id="8b056-156">Questa patch contiene tutte le correzioni fornite dalle patch precedenti nel PatchFamily specificato.</span><span class="sxs-lookup"><span data-stu-id="8b056-156">This patch contains all fixes provided by earlier patches in the specified PatchFamily.</span></span> <span data-ttu-id="8b056-157">Questo attributo non significa che questa patch sostituisce le patch precedenti in tutti i casi, perché le patch precedenti possono appartenere a più famiglie di patch.</span><span class="sxs-lookup"><span data-stu-id="8b056-157">This attribute does not mean that this patch supersedes the earlier patches in all cases because the earlier patches can belong to multiple patch families.</span></span>

<span data-ttu-id="8b056-158">Una patch di [aggiornamento di dimensioni ridotte](small-updates.md) non può sostituire un [aggiornamento secondario](minor-upgrades.md) o una patch di [aggiornamento principale](major-upgrades.md) in qualsiasi circostanza, anche se **msidbPatchSequenceSupersedeEarlier** è impostato.</span><span class="sxs-lookup"><span data-stu-id="8b056-158">A [small update](small-updates.md) patch cannot supersede a [minor upgrade](minor-upgrades.md) or [major upgrade](major-upgrades.md) patch under any circumstances, even if the **msidbPatchSequenceSupersedeEarlier** is set.</span></span> 

| <span data-ttu-id="8b056-159">Nome</span><span class="sxs-lookup"><span data-stu-id="8b056-159">Name</span></span>                                   | <span data-ttu-id="8b056-160">Valore</span><span class="sxs-lookup"><span data-stu-id="8b056-160">Value</span></span> | <span data-ttu-id="8b056-161">Significato</span><span class="sxs-lookup"><span data-stu-id="8b056-161">Meaning</span></span>                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | <span data-ttu-id="8b056-162">0x00</span><span class="sxs-lookup"><span data-stu-id="8b056-162">0x00</span></span>  | <span data-ttu-id="8b056-163">Indica un semplice valore di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="8b056-163">Indicates a simple sequencing value.</span></span>                              |
| <span data-ttu-id="8b056-164">**msidbPatchSequenceSupersedeEarlier**</span><span class="sxs-lookup"><span data-stu-id="8b056-164">**msidbPatchSequenceSupersedeEarlier**</span></span> | <span data-ttu-id="8b056-165">0x01</span><span class="sxs-lookup"><span data-stu-id="8b056-165">0x01</span></span>  | <span data-ttu-id="8b056-166">Indica una patch che sostituisce le patch precedenti in questa famiglia.</span><span class="sxs-lookup"><span data-stu-id="8b056-166">Indicates a patch that supersedes earlier patches in this family.</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8b056-167">Convalida</span><span class="sxs-lookup"><span data-stu-id="8b056-167">Validation</span></span>

<dl>

[<span data-ttu-id="8b056-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="8b056-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8b056-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="8b056-169">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="8b056-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b056-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b056-171">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="8b056-171">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



