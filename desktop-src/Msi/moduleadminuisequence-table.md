---
description: Uno strumento di merge valuta la tabella ModuleAdminUISequence e quindi inserisce le azioni calcolate nella tabella AdminUISequence con un numero di sequenza corretto.
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: Tabella ModuleAdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317126"
---
# <a name="moduleadminuisequence-table"></a><span data-ttu-id="e7ccd-103">Tabella ModuleAdminUISequence</span><span class="sxs-lookup"><span data-stu-id="e7ccd-103">ModuleAdminUISequence Table</span></span>

<span data-ttu-id="e7ccd-104">Uno strumento di merge valuta la tabella ModuleAdminUISequence e quindi inserisce le azioni calcolate nella [tabella AdminUISequence](adminuisequence-table.md) con un numero di sequenza corretto.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-104">A merge tool evaluates the ModuleAdminUISequence table and then inserts the calculated actions into the [AdminUISequence table](adminuisequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="e7ccd-105">La tabella ModuleAdminUISequence include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-105">The ModuleAdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="e7ccd-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="e7ccd-106">Column</span></span>     | <span data-ttu-id="e7ccd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7ccd-107">Type</span></span>                         | <span data-ttu-id="e7ccd-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="e7ccd-108">Key</span></span> | <span data-ttu-id="e7ccd-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="e7ccd-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="e7ccd-110">Azione</span><span class="sxs-lookup"><span data-stu-id="e7ccd-110">Action</span></span>     | [<span data-ttu-id="e7ccd-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="e7ccd-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="e7ccd-112">S</span><span class="sxs-lookup"><span data-stu-id="e7ccd-112">Y</span></span>   | <span data-ttu-id="e7ccd-113">N</span><span class="sxs-lookup"><span data-stu-id="e7ccd-113">N</span></span>        |
| <span data-ttu-id="e7ccd-114">Sequenza</span><span class="sxs-lookup"><span data-stu-id="e7ccd-114">Sequence</span></span>   | [<span data-ttu-id="e7ccd-115">Integer</span><span class="sxs-lookup"><span data-stu-id="e7ccd-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="e7ccd-116">S</span><span class="sxs-lookup"><span data-stu-id="e7ccd-116">Y</span></span>        |
| <span data-ttu-id="e7ccd-117">BaseAction</span><span class="sxs-lookup"><span data-stu-id="e7ccd-117">BaseAction</span></span> | [<span data-ttu-id="e7ccd-118">Identificatore</span><span class="sxs-lookup"><span data-stu-id="e7ccd-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="e7ccd-119">S</span><span class="sxs-lookup"><span data-stu-id="e7ccd-119">Y</span></span>        |
| <span data-ttu-id="e7ccd-120">After</span><span class="sxs-lookup"><span data-stu-id="e7ccd-120">After</span></span>      | [<span data-ttu-id="e7ccd-121">Integer</span><span class="sxs-lookup"><span data-stu-id="e7ccd-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="e7ccd-122">S</span><span class="sxs-lookup"><span data-stu-id="e7ccd-122">Y</span></span>        |
| <span data-ttu-id="e7ccd-123">Condizione</span><span class="sxs-lookup"><span data-stu-id="e7ccd-123">Condition</span></span>  | [<span data-ttu-id="e7ccd-124">Condition</span><span class="sxs-lookup"><span data-stu-id="e7ccd-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="e7ccd-125">S</span><span class="sxs-lookup"><span data-stu-id="e7ccd-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e7ccd-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="e7ccd-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e7ccd-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="e7ccd-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="e7ccd-128">Azione da inserire in sequenza.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-128">Action to insert into sequence.</span></span> <span data-ttu-id="e7ccd-129">Fa riferimento a una delle [azioni standard](standard-actions.md)del programma di installazione o a una voce nella tabella [CustomAction](customaction-table.md) o nella tabella di [dialogo](dialog-table.md)del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="e7ccd-130">Se nella colonna Action di una tabella di sequenza di un modulo merge viene utilizzata un' [azione standard](standard-actions.md) , le colonne BaseAction e After del record devono essere null.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="e7ccd-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="e7ccd-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="e7ccd-132">Numero di sequenza di un'azione standard.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-132">The sequence number of a standard action.</span></span> <span data-ttu-id="e7ccd-133">Se una finestra di dialogo o un'azione personalizzata viene immessa nella colonna azione di questa riga, questo campo deve essere impostato su null.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="e7ccd-134">Quando si utilizzano [azioni standard](standard-actions.md) nelle tabelle di sequenza dei moduli di merge, il valore nella colonna sequenza deve essere il numero di sequenza dell'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="e7ccd-135">Se il numero di sequenza nel modulo merge è diverso da quello per la stessa azione nella tabella di sequenza dei file con estensione msi, lo strumento di merge utilizza il numero di sequenza del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="e7ccd-136">Vedere le sequenze suggerite nell' [uso di una tabella di sequenza](using-a-sequence-table.md) per i numeri di sequenza consigliati per le azioni standard.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="e7ccd-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span><span class="sxs-lookup"><span data-stu-id="e7ccd-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="e7ccd-138">La colonna BaseAction può contenere un'azione standard, un'azione personalizzata specificata nella tabella delle azioni personalizzata del modulo merge o una finestra di dialogo specificata nella tabella delle finestre di dialogo del modulo.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="e7ccd-139">La colonna BaseAction è una chiave nella colonna Action della tabella.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="e7ccd-140">Non può essere una chiave esterna in un'altra tabella o tabella di merge nel file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="e7ccd-141">Ciò significa che ogni azione standard, azione personalizzata o finestra di dialogo elencata nella colonna BaseAction deve essere elencata anche nella colonna azione di un altro record in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="e7ccd-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Dopo</span><span class="sxs-lookup"><span data-stu-id="e7ccd-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="e7ccd-143">Valore booleano che indica se l'azione precede o dopo BaseAction.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="e7ccd-144">Valore</span><span class="sxs-lookup"><span data-stu-id="e7ccd-144">Value</span></span> | <span data-ttu-id="e7ccd-145">Significato</span><span class="sxs-lookup"><span data-stu-id="e7ccd-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="e7ccd-146">0</span><span class="sxs-lookup"><span data-stu-id="e7ccd-146">0</span></span>     | <span data-ttu-id="e7ccd-147">Azione da passare prima di BaseAction</span><span class="sxs-lookup"><span data-stu-id="e7ccd-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="e7ccd-148">1</span><span class="sxs-lookup"><span data-stu-id="e7ccd-148">1</span></span>     | <span data-ttu-id="e7ccd-149">Azione da eseguire dopo BaseAction</span><span class="sxs-lookup"><span data-stu-id="e7ccd-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e7ccd-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="e7ccd-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="e7ccd-151">Istruzione condizionale che indica se l'azione viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="e7ccd-152">Null restituisce true.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7ccd-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7ccd-153">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="e7ccd-154"><span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>Se questa tabella è presente, è necessario che la [tabella AdminUISequence](adminuisequence-table.md) sia presente anche nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="e7ccd-154"><span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>If this table is present the [AdminUISequence Table](adminuisequence-table.md) must also be present in the merge module.</span></span>
<span data-ttu-id="e7ccd-155"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e7ccd-155"></dt> <dd></dd> </dl></span></span>

 

 



