---
description: 'Altre informazioni su: funzione JetMove'
title: Funzione JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225877"
---
# <a name="jetmove-function"></a><span data-ttu-id="c5180-103">Funzione JetMove</span><span class="sxs-lookup"><span data-stu-id="c5180-103">JetMove Function</span></span>


<span data-ttu-id="c5180-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c5180-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmove-function"></a><span data-ttu-id="c5180-105">Funzione JetMove</span><span class="sxs-lookup"><span data-stu-id="c5180-105">JetMove Function</span></span>

<span data-ttu-id="c5180-106">La funzione **JetMove** posiziona un cursore all'inizio o alla fine di un indice e attraversa le voci dell'indice in avanti o indietro.</span><span class="sxs-lookup"><span data-stu-id="c5180-106">The **JetMove** function positions a cursor at the start or end of an index and traverses the entries in that index either forward or backward.</span></span> <span data-ttu-id="c5180-107">È anche possibile spostare il cursore avanti o indietro sull'indice corrente in base a un numero specificato di voci di indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-107">It is also possible to move the cursor forward or backward on the current index by a specified number of index entries.</span></span> <span data-ttu-id="c5180-108">Un altro approccio consiste nel limitare artificialmente le voci di indice che possono essere enumerate usando **JetMove** impostando un intervallo di indice sul cursore usando [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5180-108">Another approach is to artificially limit the index entries that can be enumerated using **JetMove** by setting up an index range on the cursor using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c5180-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5180-109">Parameters</span></span>

<span data-ttu-id="c5180-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c5180-110">*sesid*</span></span>

<span data-ttu-id="c5180-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c5180-111">The session to use for this call.</span></span>

<span data-ttu-id="c5180-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c5180-112">*tableid*</span></span>

<span data-ttu-id="c5180-113">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c5180-113">The cursor to use for this call.</span></span>

<span data-ttu-id="c5180-114">*Corvo*</span><span class="sxs-lookup"><span data-stu-id="c5180-114">*cRow*</span></span>

<span data-ttu-id="c5180-115">Offset arbitrario che indica lo spostamento desiderato del cursore sull'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="c5180-115">An arbitrary offset that indicates the desired movement of the cursor on the current index.</span></span>

<span data-ttu-id="c5180-116">Oltre agli offset standard, questo parametro può essere impostato anche con una delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5180-116">In addition to standard offsets, this parameter can also be set with one of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5180-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c5180-117">Value</span></span></p></th>
<th><p><span data-ttu-id="c5180-118">Significato</span><span class="sxs-lookup"><span data-stu-id="c5180-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5180-119">JET_MoveFirst</span><span class="sxs-lookup"><span data-stu-id="c5180-119">JET_MoveFirst</span></span></p></td>
<td><p><span data-ttu-id="c5180-120">Sposta il cursore sulla prima voce di indice nell'indice (se presente).</span><span class="sxs-lookup"><span data-stu-id="c5180-120">Moves the cursor to the first index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="c5180-121"><strong>Nota</strong>   Il valore letterale di-2147483648 viene utilizzato per indicare questa opzione.</span><span class="sxs-lookup"><span data-stu-id="c5180-121"><strong>Note</strong>   The literal value of -2147483648 is used to denote this option.</span></span> <span data-ttu-id="c5180-122">Non usare questo valore come un offset normale o un comportamento imprevisto può verificarsi.</span><span class="sxs-lookup"><span data-stu-id="c5180-122">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-123">JET_MoveLast</span><span class="sxs-lookup"><span data-stu-id="c5180-123">JET_MoveLast</span></span></p></td>
<td><p><span data-ttu-id="c5180-124">Sposta il cursore sull'ultima voce di indice nell'indice (se presente).</span><span class="sxs-lookup"><span data-stu-id="c5180-124">Moves the cursor to the last index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="c5180-125"><strong>Nota</strong>   Il valore letterale 2147483647 viene utilizzato per indicare questa opzione.</span><span class="sxs-lookup"><span data-stu-id="c5180-125"><strong>Note</strong>   The literal value of 2147483647 is used to denote this option.</span></span> <span data-ttu-id="c5180-126">Non usare questo valore come un offset normale o un comportamento imprevisto può verificarsi.</span><span class="sxs-lookup"><span data-stu-id="c5180-126">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5180-127">JET_MoveNext</span><span class="sxs-lookup"><span data-stu-id="c5180-127">JET_MoveNext</span></span></p></td>
<td><p><span data-ttu-id="c5180-128">Sposta il cursore sulla voce di indice successiva nell'indice (se presente).</span><span class="sxs-lookup"><span data-stu-id="c5180-128">Moves the cursor to the next index entry in the index (if one exists).</span></span> <span data-ttu-id="c5180-129">Questo valore è esattamente uguale a un offset normale di + 1.</span><span class="sxs-lookup"><span data-stu-id="c5180-129">This value is exactly equal to an ordinary offset of +1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-130">JET_MovePrevious</span><span class="sxs-lookup"><span data-stu-id="c5180-130">JET_MovePrevious</span></span></p></td>
<td><p><span data-ttu-id="c5180-131">Sposta il cursore sulla voce di indice precedente nell'indice (se ne esiste uno).</span><span class="sxs-lookup"><span data-stu-id="c5180-131">Moves the cursor to the previous index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="c5180-132">Questo valore è esattamente uguale a un offset normale di-1 o 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c5180-132">This value is exactly equal to an ordinary offset of -1, or 0 (Zero).</span></span></p>
<p><span data-ttu-id="c5180-133">Il cursore rimane in corrispondenza della posizione logica corrente e viene verificata l'esistenza della voce di indice corrispondente a tale posizione logica.</span><span class="sxs-lookup"><span data-stu-id="c5180-133">The cursor remains at the current logical position and the existence of the index entry that corresponds to that logical position will be tested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5180-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c5180-134">*grbit*</span></span>

<span data-ttu-id="c5180-135">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5180-135">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5180-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c5180-136">Value</span></span></p></th>
<th><p><span data-ttu-id="c5180-137">Significato</span><span class="sxs-lookup"><span data-stu-id="c5180-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5180-138">JET_bitMoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="c5180-138">JET_bitMoveKeyNE</span></span></p></td>
<td><p><span data-ttu-id="c5180-139">Sposta il cursore avanti o indietro per il numero di voci di indice necessarie per ignorare il numero richiesto di valori di chiave di indice rilevati nell'indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-139">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="c5180-140">Questo ha l'effetto di comprimere le voci di indice con valori di chiave duplicati in una singola voce di indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-140">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span> <span data-ttu-id="c5180-141">In genere, un offset sposta il cursore in base al numero di voci di indice specificato indipendentemente dai valori di chiave.</span><span class="sxs-lookup"><span data-stu-id="c5180-141">Ordinarily, an offset will move the cursor by the specified number of index entries regardless of their key values.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c5180-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5180-142">Return Value</span></span>

<span data-ttu-id="c5180-143">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="c5180-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c5180-144">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c5180-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5180-145">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c5180-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="c5180-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5180-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5180-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c5180-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c5180-148">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c5180-148">The operation completed successfully.</span></span> <span data-ttu-id="c5180-149">Per <strong>JetMove</strong>, ciò significa che è stata trovata una voce di indice in corrispondenza della posizione o dell'offset richiesto nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="c5180-149">For <strong>JetMove</strong>, this means that an index entry was found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-150">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c5180-150">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c5180-151">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c5180-151">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5180-152">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c5180-152">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c5180-153">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="c5180-153">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c5180-154"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5180-154"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="c5180-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="c5180-156">Il cursore non è attualmente posizionato in corrispondenza di una voce di indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-156">The cursor is not currently positioned on an index entry.</span></span> <span data-ttu-id="c5180-157">Per <strong>JetMove</strong>, ciò significa che non è stata trovata una voce di indice nella posizione o nell'offset richiesto per l'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="c5180-157">For <strong>JetMove</strong>, this means that an index entry was not found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5180-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c5180-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c5180-159">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c5180-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-160">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="c5180-160">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="c5180-161">Il cursore è attualmente posizionato logicamente su una voce di indice che corrisponde a un record che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="c5180-161">The cursor is currently logically positioned on an index entry that corresponds to a record that has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5180-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c5180-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c5180-163">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="c5180-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c5180-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c5180-165">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="c5180-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c5180-166"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5180-166"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5180-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c5180-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c5180-168">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="c5180-168">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5180-169">Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice che corrisponde alla posizione o all'offset richiesto.</span><span class="sxs-lookup"><span data-stu-id="c5180-169">If this function succeeds, the cursor will be positioned at an index entry that matches the requested location or offset.</span></span> <span data-ttu-id="c5180-170">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="c5180-170">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="c5180-171">Se è attivo un intervallo di indici e JET_MoveFirst o JET_MoveLast è stato specificato, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="c5180-171">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="c5180-172">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="c5180-172">No change to the database state will occur.</span></span>

<span data-ttu-id="c5180-173">Se questa funzione ha esito negativo, la posizione del cursore rimarrà invariata a meno che non venga restituito JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="c5180-173">If this function fails, the position of the cursor will remain unchanged unless JET_errNoCurrentRecord was returned.</span></span> <span data-ttu-id="c5180-174">In tal caso, il cursore viene posizionato in corrispondenza del punto in cui la voce di indice corrispondente al percorso o all'offset richiesto è stata.</span><span class="sxs-lookup"><span data-stu-id="c5180-174">In that case, the cursor will be positioned where the index entry that matches the requested location or offset would have been.</span></span> <span data-ttu-id="c5180-175">Il cursore può essere spostato in relazione a tale posizione, ma non è ancora presente in una voce di indice valida.</span><span class="sxs-lookup"><span data-stu-id="c5180-175">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="c5180-176">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="c5180-176">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="c5180-177">Se è attivo un intervallo di indici e JET_MoveFirst o JET_MoveLast è stato specificato, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="c5180-177">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="c5180-178">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="c5180-178">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c5180-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5180-179">Remarks</span></span>

<span data-ttu-id="c5180-180">È possibile spostare un cursore in due posizioni speciali usando **JetMove**, prima e dopo l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="c5180-180">A cursor can be moved to two special positions using **JetMove**, Before First and After Last.</span></span> <span data-ttu-id="c5180-181">Se il cursore si trova nella prima voce di indice della tabella e **JetMove** viene chiamato con JET_MovePrevious, la chiamata avrà esito negativo con JET_errNoCurrentRecord e il cursore verrà posizionato logicamente prima della prima voce nell'indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-181">If the cursor is on the first index entry in the table and **JetMove** is called with JET_MovePrevious, the call will fail with JET_errNoCurrentRecord and the cursor will be logically positioned before the first entry in the index.</span></span> <span data-ttu-id="c5180-182">Questa posizione logica viene mantenuta anche se viene inserita un'altra voce di indice prima della prima voce nell'indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-182">This logical position is maintained even if another index entry is inserted prior to the first entry in the index.</span></span> <span data-ttu-id="c5180-183">Una situazione analoga si verifica per dopo l'ultimo rispetto alla fine dell'indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-183">An analogous situation occurs for After Last relative to the end of the index.</span></span> <span data-ttu-id="c5180-184">Prima e dopo l'ultimo sono particolarmente utili quando si configura un intervallo di voci di indice da iterare usando **JetMove**, usando un modello iteratore che prevede di passare sempre all'elemento successivo (o precedente) prima di usare tale elemento.</span><span class="sxs-lookup"><span data-stu-id="c5180-184">Before First and After Last are most useful when setting up a range of index entries to be iterated using **JetMove**, using an iterator model that expects to always move to the next (or previous) element prior to using that element.</span></span>

<span data-ttu-id="c5180-185">Il set di voci di indice che possono essere visitate da **JetMove** può essere limitato impostando un intervallo di indice sul cursore.</span><span class="sxs-lookup"><span data-stu-id="c5180-185">The set of index entries that can be visited by **JetMove** can be limited by setting up an index range on the cursor.</span></span> <span data-ttu-id="c5180-186">Questa operazione è utile per le applicazioni che enumerano un set di voci di indice che corrispondono a criteri semplici che possono essere espressi tramite una coppia di chiavi di ricerca compilate per l'indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-186">This is useful for applications that enumerate a set of index entries that match simple criteria that can be expressed through a pair of search keys built for that index.</span></span> <span data-ttu-id="c5180-187">Per ulteriori informazioni, vedere [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5180-187">For more information, see [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="c5180-188">Nelle versioni precedenti a Windows Server 2003 SP1, si verifica un problema in **JetMove** che si verifica in alcuni casi specifici, che influiscono sull'applicazione corretta di un intervallo di indice impostato dalla funzione [JetSetIndexRange](./jetsetindexrange-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c5180-188">On releases prior to Windows Server 2003 SP1, there is a problem in **JetMove** that occurs in some specific cases, that affects the correct enforcement of an index range as set up by the [JetSetIndexRange](./jetsetindexrange-function.md) function.</span></span> <span data-ttu-id="c5180-189">Se il cursore si trova attualmente prima della prima voce di indice e un intervallo di indici è impostato con un limite superiore minore della prima voce di indice, la chiamata successiva a **JetMove** verrà erroneamente inviata a tale voce di indice invece di non avere esito positivo con JET_errNoCurrentRecord, come previsto.</span><span class="sxs-lookup"><span data-stu-id="c5180-189">If the cursor is currently before the first index entry and an index range is set with an upper limit that is less than the first index entry, the next call to **JetMove** will erroneously go to that index entry instead of failing with JET_errNoCurrentRecord, as expected.</span></span> <span data-ttu-id="c5180-190">Lo stesso errore si verifica per la situazione analoga a partire dalla fine dell'indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-190">The same error will happen for the analogous situation starting from the end of the index.</span></span> <span data-ttu-id="c5180-191">Questa situazione può verificarsi in un'applicazione che imposta un intervallo di indici e la sposta usando un iteratore che prevede l'avvio prima della prima voce di indice che è membro del set di voci da enumerare, anziché iniziare sulla prima voce di indice di tale set.</span><span class="sxs-lookup"><span data-stu-id="c5180-191">This situation can occur in an application that sets up an index range and navigates it using an iterator that expects to start before the first index entry that is a member of the set of entries to enumerate, rather than starting on the first index entry of that set.</span></span> <span data-ttu-id="c5180-192">Questa situazione si verifica anche nel caso analogo a partire dalla fine dell'indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-192">This situation also occurs on the analogous case starting from the end of the index.</span></span> <span data-ttu-id="c5180-193">La soluzione alternativa consiste nell'applicazione per verificare manualmente che la voce di indice acquisita si trovi all'interno dell'intervallo di indici confrontando la chiave per la voce di indice corrente (recuperata utilizzando [JetRetrieveKey](./jetretrievekey-function.md)) con la chiave che rappresenta la fine dell'intervallo di indici corrente (recuperato utilizzando [JetRetrieveKey](./jetretrievekey-function.md) utilizzando JET_bitRetrieveCopy).</span><span class="sxs-lookup"><span data-stu-id="c5180-193">The workaround is for the application to manually verify that the index entry acquired is inside the index range by comparing the key for the current index entry (retrieved using [JetRetrieveKey](./jetretrievekey-function.md)) with the key representing the end of the current index range (retrieved using [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy).</span></span>

<span data-ttu-id="c5180-194">È importante prestare attenzione quando si passano gli offset calcolati a **JetMove**.</span><span class="sxs-lookup"><span data-stu-id="c5180-194">It is important to be careful when passing computed offsets to **JetMove**.</span></span> <span data-ttu-id="c5180-195">Se l'offset calcolato è minore o uguale a JET_MoveFirst, tale offset deve essere suddiviso in più parti, ognuna delle quali viene passata a **JetMove** separatamente ma all'interno di una singola transazione per ottenere l'effetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="c5180-195">If the computed offset is less than or equal to JET_MoveFirst, that offset must be broken up into multiple pieces, each of which is passed to **JetMove** separately but within a single transaction to get the desired effect.</span></span> <span data-ttu-id="c5180-196">Lo stesso vale per gli offset maggiori o uguali a JET_MoveNext.</span><span class="sxs-lookup"><span data-stu-id="c5180-196">The same is true for offsets greater than or equal to JET_MoveNext.</span></span> <span data-ttu-id="c5180-197">È improbabile che un'applicazione venga sottoposta a questa situazione nel mondo reale, ma è bene avere una difesa contro questo caso, data la semantica molto diversa di JET_MoveFirst e JET_MoveLast da un offset normale.</span><span class="sxs-lookup"><span data-stu-id="c5180-197">It is unlikely that an application would undergo this in the real world, but it is good to have a defense against this case given the very different semantics of JET_MoveFirst and JET_MoveLast from an ordinary offset.</span></span>

<span data-ttu-id="c5180-198">Quando **JetMove** viene chiamato con un offset molto grande, ad esempio quando il parametro Crow è impostato su 1000, **JetMove** attraversa tutte le voci di indice 1000 per raggiungere la posizione finale.</span><span class="sxs-lookup"><span data-stu-id="c5180-198">When **JetMove** is called with a very large offset, such as when the cRow parameter is set to 1000, **JetMove** traverses all 1000 index entries to reach the final position.</span></span> <span data-ttu-id="c5180-199">Attualmente, l'API ESE non fornisce un modo efficiente per passare direttamente a una voce di indice specificata per offset senza attraversare ogni voce di indice.</span><span class="sxs-lookup"><span data-stu-id="c5180-199">Currently, the ESE API does not provide an efficient way to move directly to a given index entry by offset without traversing each index entry.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c5180-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5180-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5180-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c5180-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c5180-202">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c5180-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c5180-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c5180-204">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c5180-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5180-205"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c5180-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c5180-206">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c5180-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5180-207"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="c5180-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c5180-208">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c5180-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5180-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c5180-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c5180-210">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c5180-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c5180-211">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c5180-211">See Also</span></span>

[<span data-ttu-id="c5180-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c5180-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c5180-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c5180-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c5180-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c5180-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c5180-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c5180-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c5180-216">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="c5180-216">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="c5180-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="c5180-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
