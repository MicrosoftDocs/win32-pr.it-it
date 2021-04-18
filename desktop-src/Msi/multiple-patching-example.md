---
description: Nell'esempio seguente viene illustrato come è possibile utilizzare Windows Installer 3,0 e versioni successive per applicare le patch nell'ordine in cui vengono create.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Esempio di applicazione di patch multipla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310516"
---
# <a name="multiple-patching-example"></a><span data-ttu-id="7cf2d-103">Esempio di applicazione di patch multipla</span><span class="sxs-lookup"><span data-stu-id="7cf2d-103">Multiple Patching Example</span></span>

<span data-ttu-id="7cf2d-104">Nell'esempio seguente viene illustrato come è possibile utilizzare Windows Installer 3,0 e versioni successive per applicare le patch nell'ordine in cui vengono create.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-104">The following example shows how Windows Installer 3.0 and later can be used to apply patches in the order in which they are authored.</span></span>

## <a name="example"></a><span data-ttu-id="7cf2d-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="7cf2d-105">Example</span></span>

<span data-ttu-id="7cf2d-106">In questo esempio sono presenti tre patch, QFE1, QFE2 e ServicePack1, ognuno con una tabella [MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="7cf2d-106">In this example there are three patches, QFE1, QFE2, and ServicePack1, and they each have a [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="7cf2d-107">Queste patch sono state create per essere applicate alla versione 1,0 dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-107">These patches have been authored to be applied to version 1.0 of the application.</span></span>



| <span data-ttu-id="7cf2d-108">Nome patch</span><span class="sxs-lookup"><span data-stu-id="7cf2d-108">Patch Name</span></span>   | <span data-ttu-id="7cf2d-109">Tipo di patch</span><span class="sxs-lookup"><span data-stu-id="7cf2d-109">Patch Type</span></span>    | <span data-ttu-id="7cf2d-110">Numero sequenza</span><span class="sxs-lookup"><span data-stu-id="7cf2d-110">Sequence Number</span></span> |
|--------------|---------------|-----------------|
| <span data-ttu-id="7cf2d-111">QFE1</span><span class="sxs-lookup"><span data-stu-id="7cf2d-111">QFE1</span></span>         | <span data-ttu-id="7cf2d-112">Aggiornamento ridotto</span><span class="sxs-lookup"><span data-stu-id="7cf2d-112">Small Update</span></span>  | <span data-ttu-id="7cf2d-113">1.1.0</span><span class="sxs-lookup"><span data-stu-id="7cf2d-113">1.1.0</span></span>           |
| <span data-ttu-id="7cf2d-114">QFE2</span><span class="sxs-lookup"><span data-stu-id="7cf2d-114">QFE2</span></span>         | <span data-ttu-id="7cf2d-115">Aggiornamento ridotto</span><span class="sxs-lookup"><span data-stu-id="7cf2d-115">Small Update</span></span>  | <span data-ttu-id="7cf2d-116">1.2.0</span><span class="sxs-lookup"><span data-stu-id="7cf2d-116">1.2.0</span></span>           |
| <span data-ttu-id="7cf2d-117">ServicePack1</span><span class="sxs-lookup"><span data-stu-id="7cf2d-117">ServicePack1</span></span> | <span data-ttu-id="7cf2d-118">Aggiornamento secondario</span><span class="sxs-lookup"><span data-stu-id="7cf2d-118">Minor Upgrade</span></span> | <span data-ttu-id="7cf2d-119">1.3.0</span><span class="sxs-lookup"><span data-stu-id="7cf2d-119">1.3.0</span></span>           |



 

<span data-ttu-id="7cf2d-120">La tabella [MsiPatchSequence](msipatchsequence-table.md) di ogni patch ha un solo record che contiene la famiglia di patch, il codice prodotto e il numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-120">The [MsiPatchSequence](msipatchsequence-table.md) table of each patch has only one record that contains the patch family, product code, and sequence number.</span></span> <span data-ttu-id="7cf2d-121">Le tre patch sono tutte applicate allo stesso prodotto e appartengono alla stessa famiglia di patch, denominata AppPatch.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-121">The three patches are all applied to the same product and belong to the same patch family, named AppPatch.</span></span> <span data-ttu-id="7cf2d-122">Nessuna delle patch ha l'attributo **msidbPatchSequenceSupersedeEarlier** .</span><span class="sxs-lookup"><span data-stu-id="7cf2d-122">None of the patches have the **msidbPatchSequenceSupersedeEarlier** attribute.</span></span>

<span data-ttu-id="7cf2d-123">[Tabella MsiPatchSequence](msipatchsequence-table.md) per l'aggiornamento di QFE1 [small](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="7cf2d-123">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE1 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="7cf2d-124">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="7cf2d-124">PatchFamily</span></span> | <span data-ttu-id="7cf2d-125">ProductCode</span><span class="sxs-lookup"><span data-stu-id="7cf2d-125">ProductCode</span></span>                            | <span data-ttu-id="7cf2d-126">Sequenza</span><span class="sxs-lookup"><span data-stu-id="7cf2d-126">Sequence</span></span> | <span data-ttu-id="7cf2d-127">Attributi</span><span class="sxs-lookup"><span data-stu-id="7cf2d-127">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="7cf2d-128">AppPatch</span><span class="sxs-lookup"><span data-stu-id="7cf2d-128">AppPatch</span></span>    | <span data-ttu-id="7cf2d-129">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="7cf2d-129">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="7cf2d-130">1.1.0</span><span class="sxs-lookup"><span data-stu-id="7cf2d-130">1.1.0</span></span>    |            |



 

<span data-ttu-id="7cf2d-131">[Tabella MsiPatchSequence](msipatchsequence-table.md) per l'aggiornamento di QFE2 [small](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="7cf2d-131">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE2 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="7cf2d-132">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="7cf2d-132">PatchFamily</span></span> | <span data-ttu-id="7cf2d-133">ProductCode</span><span class="sxs-lookup"><span data-stu-id="7cf2d-133">ProductCode</span></span>                            | <span data-ttu-id="7cf2d-134">Sequenza</span><span class="sxs-lookup"><span data-stu-id="7cf2d-134">Sequence</span></span> | <span data-ttu-id="7cf2d-135">Attributi</span><span class="sxs-lookup"><span data-stu-id="7cf2d-135">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="7cf2d-136">AppPatch</span><span class="sxs-lookup"><span data-stu-id="7cf2d-136">AppPatch</span></span>    | <span data-ttu-id="7cf2d-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="7cf2d-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="7cf2d-138">1.2.0</span><span class="sxs-lookup"><span data-stu-id="7cf2d-138">1.2.0</span></span>    |            |



 

<span data-ttu-id="7cf2d-139">[Tabella MsiPatchSequence](msipatchsequence-table.md) per l' [aggiornamento](minor-upgrades.md)di Servicepack1 minor.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-139">[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md).</span></span> 

| <span data-ttu-id="7cf2d-140">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="7cf2d-140">PatchFamily</span></span> | <span data-ttu-id="7cf2d-141">ProductCode</span><span class="sxs-lookup"><span data-stu-id="7cf2d-141">ProductCode</span></span>                            | <span data-ttu-id="7cf2d-142">Sequenza</span><span class="sxs-lookup"><span data-stu-id="7cf2d-142">Sequence</span></span> | <span data-ttu-id="7cf2d-143">Attributi</span><span class="sxs-lookup"><span data-stu-id="7cf2d-143">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="7cf2d-144">AppPatch</span><span class="sxs-lookup"><span data-stu-id="7cf2d-144">AppPatch</span></span>    | <span data-ttu-id="7cf2d-145">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="7cf2d-145">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="7cf2d-146">1.3.0</span><span class="sxs-lookup"><span data-stu-id="7cf2d-146">1.3.0</span></span>    |            |



 

<span data-ttu-id="7cf2d-147">Se un utente installa la versione 1,0 del prodotto e quindi applica QFE2, quindi in un secondo momento decide di applicare QFE1, Windows Installer garantisce che la sequenza effettiva di applicazione patch al prodotto sia QFE1 applicata prima di QFE2.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-147">If a user installs version 1.0 of the product, and then applies QFE2, and then at a later date decides to apply QFE1, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 applied ahead of QFE2.</span></span> <span data-ttu-id="7cf2d-148">Se l'utente applica ServicePack1, applica QFE2 e QFE1 insieme in un secondo momento, Windows Installer garantisce che la sequenza effettiva di applicazione patch al prodotto sia QFE1 avanti rispetto a QFE2 e Ahead ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-148">If the user applies ServicePack1, then applies QFE2 and QFE1 together at a later date, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 ahead of QFE2 and ahead of ServicePack1.</span></span>

<span data-ttu-id="7cf2d-149">Se ServicePack1 ha **msidbPatchSequenceSupersedeEarlier** impostato nella colonna Attributes della relativa tabella [MsiPatchSequence](msipatchsequence-table.md) , significa che il Service Pack contiene tutte le modifiche apportate a QFE1 e QFE2.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-149">If ServicePack1 has **msidbPatchSequenceSupersedeEarlier** set in the Attributes column of its [MsiPatchSequence](msipatchsequence-table.md) table, this means that the service pack contains all the changes in QFE1 and QFE2.</span></span> <span data-ttu-id="7cf2d-150">In questo caso, QFE1 e QFE2 non vengono applicati quando viene applicato ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-150">In this case, QFE1 and QFE2 are not applied when ServicePack1 is applied.</span></span>

<span data-ttu-id="7cf2d-151">**Windows Installer 2,0:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-151">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="7cf2d-152">Le versioni precedenti a Windows Installer 3,0 possono installare solo una patch per ogni transazione e le patch vengono applicate nella sequenza specificata.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-152">Versions earlier than Windows Installer 3.0 can install only one patch per transaction and patches are applied in the sequence that they are provided.</span></span> <span data-ttu-id="7cf2d-153">Per l'esempio precedente, se QFE2 viene applicato per primo e viene applicato QFE1, ovvero due transazioni, le patch vengono applicate alla versione 1,0 dell'applicazione nella sequenza QFE2 seguita da QFE1.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-153">For the preceding example, if QFE2 is applied first and then QFE1 is applied, that is two transactions and the patches are applied to version 1.0 of the application in the sequence QFE2 followed by QFE1.</span></span> <span data-ttu-id="7cf2d-154">Se ServicePack1 viene applicato per primo, non è possibile applicare QFE1 o QFE2 in una transazione successiva, perché ServicePack1 è un aggiornamento secondario che modifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-154">If ServicePack1 is applied first, then QFE1 or QFE2 cannot be applied in a later transaction because ServicePack1 is a minor upgrade that changes the application version.</span></span> <span data-ttu-id="7cf2d-155">QFE1 e QFE2 possono essere applicati solo alla versione 1,0 dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-155">QFE1 and QFE2 can only be applied to version 1.0 of the application.</span></span>

 

 



