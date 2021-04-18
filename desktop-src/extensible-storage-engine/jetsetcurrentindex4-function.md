---
description: 'Altre informazioni su: funzione JetSetCurrentIndex4'
title: Funzione JetSetCurrentIndex4
TOCTitle: JetSetCurrentIndex4 Function
ms:assetid: 6076d02c-5701-4021-ba0a-da36bff166d1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269262(v=EXCHG.10)
ms:contentKeyID: 32765564
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex4W
- JetSetCurrentIndex4A
- JetSetCurrentIndex4
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 234b945e9ebe4421d348eab0e72556b544578b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305726"
---
# <a name="jetsetcurrentindex4-function"></a><span data-ttu-id="3a288-103">Funzione JetSetCurrentIndex4</span><span class="sxs-lookup"><span data-stu-id="3a288-103">JetSetCurrentIndex4 Function</span></span>


<span data-ttu-id="3a288-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3a288-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex4-function"></a><span data-ttu-id="3a288-105">Funzione JetSetCurrentIndex4</span><span class="sxs-lookup"><span data-stu-id="3a288-105">JetSetCurrentIndex4 Function</span></span>

<span data-ttu-id="3a288-106">La funzione **JetSetCurrentIndex4** viene utilizzata per impostare l'indice corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="3a288-106">The **JetSetCurrentIndex4** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="3a288-107">L'indice corrente di un cursore definisce quali record di una tabella sono visibili a tale cursore e l'ordine in cui vengono visualizzati selezionando il set di voci di indice da utilizzare per esporre tali record.</span><span class="sxs-lookup"><span data-stu-id="3a288-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex4(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in_opt      JET_INDEXID* pindexid,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="3a288-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a288-108">Parameters</span></span>

<span data-ttu-id="3a288-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3a288-109">*sesid*</span></span>

<span data-ttu-id="3a288-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="3a288-110">The session to use for this call.</span></span>

<span data-ttu-id="3a288-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="3a288-111">*tableid*</span></span>

<span data-ttu-id="3a288-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="3a288-112">The cursor to use for this call.</span></span>

<span data-ttu-id="3a288-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="3a288-113">*szIndexName*</span></span>

<span data-ttu-id="3a288-114">Nome dell'indice da selezionare per il cursore.</span><span class="sxs-lookup"><span data-stu-id="3a288-114">The name of the index to be selected for the cursor.</span></span> <span data-ttu-id="3a288-115">Se questo parametro è NULL o una stringa vuota, verrà selezionato l'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="3a288-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="3a288-116">Se viene definito un indice primario per la tabella, l'indice verrà selezionato perché corrisponde all'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="3a288-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="3a288-117">Se per la tabella non è definito alcun indice primario, verrà selezionato l'indice sequenziale.</span><span class="sxs-lookup"><span data-stu-id="3a288-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="3a288-118">La definizione dell'indice sequenziale non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3a288-118">The sequential index has no index definition.</span></span> <span data-ttu-id="3a288-119">Per ulteriori informazioni, vedere [JetCreateIndex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3a288-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="3a288-120">Se *pIndexID* non è null, il nome dell'indice verrà ignorato e l'indice verrà selezionato in base al relativo ID di indice.</span><span class="sxs-lookup"><span data-stu-id="3a288-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="3a288-121">*pIndexID*</span><span class="sxs-lookup"><span data-stu-id="3a288-121">*pindexid*</span></span>

<span data-ttu-id="3a288-122">ID dell'indice da selezionare per il cursore.</span><span class="sxs-lookup"><span data-stu-id="3a288-122">The ID of the index to be selected for the cursor.</span></span>

<span data-ttu-id="3a288-123">L'ID di indice è un handle volatile e opaco che può essere utilizzato per selezionare rapidamente un indice.</span><span class="sxs-lookup"><span data-stu-id="3a288-123">The index ID is a volatile, opaque handle that can be used to quickly select an index.</span></span> <span data-ttu-id="3a288-124">Questo ID può essere recuperato utilizzando JetGetIndexInfo o JetGetTableIndexInfo utilizzando l'opzione JET_IdxInfoIndexId.</span><span class="sxs-lookup"><span data-stu-id="3a288-124">This ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo using the JET_IdxInfoIndexId option.</span></span>

<span data-ttu-id="3a288-125">Se *pIndexID* è null, l'indice verrà selezionato in base al nome dell'indice e l'ID dell'indice verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="3a288-125">If *pindexid* is NULL then the index will be selected by its index name and the index ID will be ignored.</span></span>

<span data-ttu-id="3a288-126">Se questo parametro non è presente, il relativo valore viene considerato NULL.</span><span class="sxs-lookup"><span data-stu-id="3a288-126">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="3a288-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3a288-127">*grbit*</span></span>

<span data-ttu-id="3a288-128">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a288-128">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a288-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3a288-129">Value</span></span></p></th>
<th><p><span data-ttu-id="3a288-130">Significato</span><span class="sxs-lookup"><span data-stu-id="3a288-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a288-131">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="3a288-131">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="3a288-132">Questa opzione indica che il cursore deve essere posizionato sulla prima voce dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="3a288-132">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="3a288-133">Se viene selezionato l'indice cluster (indice primario o sequenziale) e l'indice corrente è un indice secondario, viene utilizzato JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="3a288-133">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="3a288-134">Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="3a288-134">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-135">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="3a288-135">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="3a288-136">Questa opzione indica che il cursore deve essere posizionato sulla voce di indice del nuovo indice che corrisponde al record associato alla voce di indice in corrispondenza della posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="3a288-136">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="3a288-137">Se la definizione del nuovo indice contiene almeno una colonna chiave multivalore, la voce dell'indice di destinazione è ambigua.</span><span class="sxs-lookup"><span data-stu-id="3a288-137">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="3a288-138">In questo caso, l'oggetto <em>itagSequence</em> specificato viene utilizzato per selezionare il multivalore della colonna chiave multivalore più significativa utilizzata per posizionare il cursore.</span><span class="sxs-lookup"><span data-stu-id="3a288-138">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="3a288-139">È necessario passare un solo <em>itagSequence</em> , anche nel caso di più colonne chiave multivalore perché il motore espande solo tutti i valori per la colonna chiave multivalore più significativa.</span><span class="sxs-lookup"><span data-stu-id="3a288-139">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="3a288-140">Per ulteriori informazioni, vedere <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> .</span><span class="sxs-lookup"><span data-stu-id="3a288-140">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="3a288-141">Se viene specificato JET_bitMoveFirst, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="3a288-141">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="3a288-142">Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="3a288-142">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="3a288-143">Se questo parametro non è presente, il relativo valore si presume che sia JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="3a288-143">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a288-144">*itagSequence*</span><span class="sxs-lookup"><span data-stu-id="3a288-144">*itagSequence*</span></span>

<span data-ttu-id="3a288-145">Numero di sequenza del valore della colonna multivalore che verrà utilizzato per posizionare il cursore sul nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="3a288-145">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="3a288-146">Questo parametro viene usato solo in combinazione con JET_bitNoMove.</span><span class="sxs-lookup"><span data-stu-id="3a288-146">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="3a288-147">Per ulteriori informazioni, vedere la descrizione di questa opzione.</span><span class="sxs-lookup"><span data-stu-id="3a288-147">See the description of this option for more details.</span></span>

<span data-ttu-id="3a288-148">Se questo parametro non è presente o è impostato su zero, il relativo valore si presume essere 1.</span><span class="sxs-lookup"><span data-stu-id="3a288-148">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="3a288-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a288-149">Return Value</span></span>

<span data-ttu-id="3a288-150">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="3a288-150">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3a288-151">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3a288-151">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a288-152">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3a288-152">Return code</span></span></p></th>
<th><p><span data-ttu-id="3a288-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a288-153">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a288-154">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3a288-154">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3a288-155">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3a288-155">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-156">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="3a288-156">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="3a288-157">È stato selezionato un indice secondario con l'opzione JET_bitNoMove e non è presente alcun valore per la prima colonna chiave multivalore nella definizione del nuovo indice che corrisponde al numero di sequenza specificato.</span><span class="sxs-lookup"><span data-stu-id="3a288-157">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the definition for the new index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-158">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3a288-158">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3a288-159">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="3a288-159">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3a288-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3a288-161">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="3a288-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3a288-162">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3a288-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-163">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="3a288-163">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="3a288-164">Il contenuto dell'ID di indice non è valido o è scaduto e deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="3a288-164">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="3a288-165">Questo problema può verificarsi per <strong>JetSetCurrentIndex4</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="3a288-165">This can happen for <strong>JetSetCurrentIndex4</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="3a288-166">pIndexID- &gt; cbStruct non è della dimensione prevista (Windows Server 2003 e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="3a288-166">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="3a288-167">Il motore è stato arrestato perché è stato recuperato l'ID dell'indice.</span><span class="sxs-lookup"><span data-stu-id="3a288-167">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="3a288-168">Tutti i cursori che fanno riferimento alla tabella contenente l'indice corrispondente all'ID dell'indice sono stati chiusi e il motore ha rimosso la definizione di tale indice dalla cache dello schema.</span><span class="sxs-lookup"><span data-stu-id="3a288-168">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="3a288-169">L'ID di indice viene utilizzato con un cursore aperto nella tabella errata.</span><span class="sxs-lookup"><span data-stu-id="3a288-169">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="3a288-170">L'indice è stato eliminato o non è ancora visibile alla sessione.</span><span class="sxs-lookup"><span data-stu-id="3a288-170">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-171">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="3a288-171">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="3a288-172">Uno dei nomi di oggetto specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="3a288-172">One of the specified object names was invalid.</span></span> <span data-ttu-id="3a288-173">Tutti i nomi di oggetto devono essere conformi allo stesso set di regole.</span><span class="sxs-lookup"><span data-stu-id="3a288-173">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="3a288-174">Le regole sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a288-174">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3a288-175">I nomi degli oggetti devono essere composti da caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="3a288-175">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="3a288-176">I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="3a288-176">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="3a288-177">I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</span><span class="sxs-lookup"><span data-stu-id="3a288-177">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="3a288-178">I nomi degli oggetti non possono iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="3a288-178">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="3a288-179">I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="3a288-179">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="3a288-180">I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</span><span class="sxs-lookup"><span data-stu-id="3a288-180">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="3a288-181">Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a288-181">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="3a288-182">Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</span><span class="sxs-lookup"><span data-stu-id="3a288-182">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-183">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3a288-183">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3a288-184">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="3a288-184">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="3a288-185">Questo problema può verificarsi per <strong>JetSetCurrentIndex4</strong> quando <em>PINDEXID</em> non è null e pIndexID- &gt; cbStruct non è della dimensione prevista (Windows XP e versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="3a288-185">This can happen for <strong>JetSetCurrentIndex4</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-186">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="3a288-186">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="3a288-187">Un indice secondario viene selezionato con l'opzione JET_bitNoMove e non è presente alcuna voce di indice nel nuovo indice che corrisponde al record associato alla voce di indice nella posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="3a288-187">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-188">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3a288-188">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3a288-189">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="3a288-189">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-190">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="3a288-190">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="3a288-191">Il motore ha esaurito il pool di risorse utilizzate per aprire i cursori.</span><span class="sxs-lookup"><span data-stu-id="3a288-191">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="3a288-192">Il numero massimo di cursori che è possibile aprire in qualsiasi momento viene controllato utilizzando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="3a288-192">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="3a288-193">Per ulteriori informazioni, vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> .</span><span class="sxs-lookup"><span data-stu-id="3a288-193">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="3a288-194">Questo problema può verificarsi per <strong>JetSetCurrentIndex4</strong> quando è stato selezionato un indice secondario e il motore non è in grado di aprire un cursore interno per utilizzare tale indice.</span><span class="sxs-lookup"><span data-stu-id="3a288-194">This can happen for <strong>JetSetCurrentIndex4</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-195">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3a288-195">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3a288-196">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="3a288-196">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-197">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3a288-197">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3a288-198">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="3a288-198">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="3a288-199">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3a288-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-200">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3a288-200">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3a288-201">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="3a288-201">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a288-202">In seguito all'esito positivo, l'indice corrente del cursore viene impostato sull'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="3a288-202">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="3a288-203">È ora possibile cercare le voci di indice usando [JetSeek](./jetseek-function.md) in base alla definizione dell'indice dell'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="3a288-203">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="3a288-204">È inoltre possibile enumerare le voci di indice utilizzando [JetMove](./jetmove-function.md) nell'ordine specificato dalla definizione di tale indice.</span><span class="sxs-lookup"><span data-stu-id="3a288-204">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="3a288-205">La posizione corrente del cursore viene impostata sulla prima voce di indice nell'indice (JET_bitMoveFirst) o su una voce di indice specifica correlata alla posizione corrente del cursore sull'indice precedente (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="3a288-205">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="3a288-206">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="3a288-206">No change to the database state will occur.</span></span>

<span data-ttu-id="3a288-207">In caso di errore, l'indice corrente e la posizione corrente del cursore sono in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="3a288-207">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="3a288-208">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="3a288-208">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3a288-209">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a288-209">Remarks</span></span>

<span data-ttu-id="3a288-210">Se l'hint ID dell'indice non è aggiornato, l'API ha semplicemente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3a288-210">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="3a288-211">In questo caso, non esiste alcun fallback al nome di testo dell'indice, come si può prevedere.</span><span class="sxs-lookup"><span data-stu-id="3a288-211">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="3a288-212">Questo fallback deve essere eseguito manualmente dal chiamante dell'API.</span><span class="sxs-lookup"><span data-stu-id="3a288-212">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3a288-213">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a288-213">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a288-214"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3a288-214"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3a288-215">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3a288-215">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-216"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3a288-216"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3a288-217">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3a288-217">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-218"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3a288-218"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3a288-219">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3a288-219">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-220"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="3a288-220"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3a288-221">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3a288-221">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a288-222"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3a288-222"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3a288-223">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3a288-223">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a288-224"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3a288-224"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3a288-225">Implementato come <strong>JetSetCurrentIndex4W</strong> (Unicode) e <strong>JetSetCurrentIndex4A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3a288-225">Implemented as <strong>JetSetCurrentIndex4W</strong> (Unicode) and <strong>JetSetCurrentIndex4A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3a288-226">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3a288-226">See Also</span></span>

[<span data-ttu-id="3a288-227">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3a288-227">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3a288-228">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3a288-228">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3a288-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3a288-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3a288-230">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3a288-230">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3a288-231">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="3a288-231">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="3a288-232">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="3a288-232">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="3a288-233">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="3a288-233">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="3a288-234">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3a288-234">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="3a288-235">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3a288-235">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="3a288-236">JetMove</span><span class="sxs-lookup"><span data-stu-id="3a288-236">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="3a288-237">JetSeek</span><span class="sxs-lookup"><span data-stu-id="3a288-237">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="3a288-238">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3a288-238">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
