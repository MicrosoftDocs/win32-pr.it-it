---
description: 'Altre informazioni su: funzione JetSetCurrentIndex3'
title: Funzione JetSetCurrentIndex3
TOCTitle: JetSetCurrentIndex3 Function
ms:assetid: 50050bd3-4b74-4be7-985c-754ced8aded1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269244(v=EXCHG.10)
ms:contentKeyID: 32765546
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex3A
- JetSetCurrentIndex3W
- JetSetCurrentIndex3
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97aa356d44ab72f7cd240a42351d9962777ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306216"
---
# <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="96152-103">Funzione JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="96152-103">JetSetCurrentIndex3 Function</span></span>


<span data-ttu-id="96152-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="96152-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="96152-105">Funzione JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="96152-105">JetSetCurrentIndex3 Function</span></span>

<span data-ttu-id="96152-106">La funzione **JetSetCurrentIndex3** viene utilizzata per impostare l'indice corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="96152-106">The **JetSetCurrentIndex3** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="96152-107">L'indice corrente di un cursore definisce quali record di una tabella sono visibili a tale cursore e l'ordine in cui vengono visualizzati selezionando il set di voci di indice da utilizzare per esporre tali record.</span><span class="sxs-lookup"><span data-stu-id="96152-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="96152-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96152-108">Parameters</span></span>

<span data-ttu-id="96152-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="96152-109">*sesid*</span></span>

<span data-ttu-id="96152-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="96152-110">The session to use for this call.</span></span>

<span data-ttu-id="96152-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="96152-111">*tableid*</span></span>

<span data-ttu-id="96152-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="96152-112">The cursor to use for this call.</span></span>

<span data-ttu-id="96152-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="96152-113">*szIndexName*</span></span>

<span data-ttu-id="96152-114">Nome dell'indice da selezionare per il cursore.</span><span class="sxs-lookup"><span data-stu-id="96152-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="96152-115">Se questo parametro è NULL o una stringa vuota, verrà selezionato l'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="96152-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="96152-116">Se viene definito un indice primario per la tabella, l'indice verrà selezionato perché corrisponde all'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="96152-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="96152-117">Se per la tabella non è definito alcun indice primario, verrà selezionato l'indice sequenziale.</span><span class="sxs-lookup"><span data-stu-id="96152-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="96152-118">La definizione dell'indice sequenziale non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="96152-118">The sequential index has no index definition.</span></span> <span data-ttu-id="96152-119">Per ulteriori informazioni, vedere [JetCreateIndex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="96152-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="96152-120">Se *pIndexID* non è null, il nome dell'indice verrà ignorato e l'indice verrà selezionato in base al relativo ID di indice.</span><span class="sxs-lookup"><span data-stu-id="96152-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="96152-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="96152-121">*grbit*</span></span>

<span data-ttu-id="96152-122">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="96152-122">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96152-123">Valore</span><span class="sxs-lookup"><span data-stu-id="96152-123">Value</span></span></p></th>
<th><p><span data-ttu-id="96152-124">Significato</span><span class="sxs-lookup"><span data-stu-id="96152-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96152-125">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="96152-125">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="96152-126">Questa opzione indica che il cursore deve essere posizionato sulla prima voce dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="96152-126">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="96152-127">Se viene selezionato l'indice cluster (indice primario o sequenziale) e l'indice corrente è un indice secondario, viene utilizzato JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="96152-127">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="96152-128">Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="96152-128">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-129">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="96152-129">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="96152-130">Questa opzione indica che il cursore deve essere posizionato sulla voce di indice del nuovo indice che corrisponde al record associato alla voce di indice in corrispondenza della posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="96152-130">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="96152-131">Se la definizione del nuovo indice contiene almeno una colonna chiave multivalore, la voce dell'indice di destinazione è ambigua.</span><span class="sxs-lookup"><span data-stu-id="96152-131">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="96152-132">In questo caso, l'oggetto <em>itagSequence</em> specificato viene utilizzato per selezionare il multivalore della colonna chiave multivalore più significativa utilizzata per posizionare il cursore.</span><span class="sxs-lookup"><span data-stu-id="96152-132">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="96152-133">È necessario passare un solo <em>itagSequence</em> , anche nel caso di più colonne chiave multivalore perché il motore espande solo tutti i valori per la colonna chiave multivalore più significativa.</span><span class="sxs-lookup"><span data-stu-id="96152-133">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="96152-134">Per ulteriori informazioni, vedere <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> .</span><span class="sxs-lookup"><span data-stu-id="96152-134">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="96152-135">Se viene specificato JET_bitMoveFirst, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="96152-135">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="96152-136">Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="96152-136">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="96152-137">Se questo parametro non è presente, il relativo valore si presume che sia JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="96152-137">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96152-138">*itagSequence*</span><span class="sxs-lookup"><span data-stu-id="96152-138">*itagSequence*</span></span>

<span data-ttu-id="96152-139">Numero di sequenza del valore della colonna multivalore che verrà utilizzato per posizionare il cursore sul nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="96152-139">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="96152-140">Questo parametro viene usato solo in combinazione con JET_bitNoMove.</span><span class="sxs-lookup"><span data-stu-id="96152-140">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="96152-141">Per ulteriori informazioni, vedere la descrizione di questa opzione.</span><span class="sxs-lookup"><span data-stu-id="96152-141">See the description of this option for more details.</span></span>

<span data-ttu-id="96152-142">Se questo parametro non è presente o è impostato su zero, il relativo valore si presume essere 1.</span><span class="sxs-lookup"><span data-stu-id="96152-142">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="96152-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96152-143">Return Value</span></span>

<span data-ttu-id="96152-144">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="96152-144">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="96152-145">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="96152-145">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96152-146">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="96152-146">Return code</span></span></p></th>
<th><p><span data-ttu-id="96152-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96152-147">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96152-148">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="96152-148">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="96152-149">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="96152-149">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-150">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="96152-150">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="96152-151">Viene selezionato un indice secondario con l'opzione JET_bitNoMove e non è presente alcun valore per la prima colonna chiave multivalore nella definizione del nuovo indice che corrisponde al numero di sequenza specificato.</span><span class="sxs-lookup"><span data-stu-id="96152-151">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-152">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="96152-152">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="96152-153">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="96152-153">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-154">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="96152-154">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="96152-155">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="96152-155">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="96152-156">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="96152-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-157">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="96152-157">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="96152-158">Il contenuto dell'ID di indice non è valido o è scaduto e deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="96152-158">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="96152-159">Questo problema può verificarsi per <strong>JetSetCurrentIndex3</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="96152-159">This can happen for <strong>JetSetCurrentIndex3</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="96152-160">pIndexID- &gt; cbStruct non è della dimensione prevista (Windows Server 2003 e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="96152-160">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="96152-161">Il motore è stato arrestato perché è stato recuperato l'ID dell'indice.</span><span class="sxs-lookup"><span data-stu-id="96152-161">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="96152-162">Tutti i cursori che fanno riferimento alla tabella contenente l'indice corrispondente all'ID dell'indice sono stati chiusi e il motore ha eliminato la definizione per tale indice dalla cache dello schema.</span><span class="sxs-lookup"><span data-stu-id="96152-162">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for that index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="96152-163">L'ID di indice viene utilizzato con un cursore aperto nella tabella errata.</span><span class="sxs-lookup"><span data-stu-id="96152-163">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="96152-164">L'indice è stato eliminato o non è ancora visibile alla sessione.</span><span class="sxs-lookup"><span data-stu-id="96152-164">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-165">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="96152-165">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="96152-166">Uno dei nomi di oggetto specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="96152-166">One of the specified object names was invalid.</span></span> <span data-ttu-id="96152-167">Tutti i nomi di oggetto devono essere conformi allo stesso set di regole.</span><span class="sxs-lookup"><span data-stu-id="96152-167">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="96152-168">Le regole sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="96152-168">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="96152-169">I nomi degli oggetti devono essere composti da caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="96152-169">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="96152-170">I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="96152-170">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="96152-171">I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</span><span class="sxs-lookup"><span data-stu-id="96152-171">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="96152-172">I nomi degli oggetti non possono iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="96152-172">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="96152-173">I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="96152-173">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="96152-174">I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</span><span class="sxs-lookup"><span data-stu-id="96152-174">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="96152-175">Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="96152-175">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="96152-176">Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</span><span class="sxs-lookup"><span data-stu-id="96152-176">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-177">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="96152-177">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="96152-178">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="96152-178">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="96152-179">Questo problema può verificarsi per <strong>JetSetCurrentIndex3</strong> quando <em>PINDEXID</em> non è null e pIndexID- &gt; cbStruct non è della dimensione prevista (Windows XP e versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="96152-179">This can happen for <strong>JetSetCurrentIndex3</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-180">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="96152-180">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="96152-181">Un indice secondario viene selezionato con l'opzione JET_bitNoMove e non è presente alcuna voce di indice nel nuovo indice che corrisponde al record associato alla voce di indice nella posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="96152-181">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-182">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="96152-182">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="96152-183">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="96152-183">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-184">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="96152-184">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="96152-185">Il motore ha esaurito il pool di risorse utilizzate per aprire i cursori.</span><span class="sxs-lookup"><span data-stu-id="96152-185">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="96152-186">Il numero massimo di cursori che è possibile aprire in qualsiasi momento viene controllato utilizzando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="96152-186">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="96152-187">Per ulteriori informazioni, vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> .</span><span class="sxs-lookup"><span data-stu-id="96152-187">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="96152-188">Questo problema può verificarsi per <strong>JetSetCurrentIndex3</strong> quando è stato selezionato un indice secondario e il motore non è in grado di aprire un cursore interno per utilizzare tale indice.</span><span class="sxs-lookup"><span data-stu-id="96152-188">This can happen for <strong>JetSetCurrentIndex3</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-189">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="96152-189">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="96152-190">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="96152-190">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-191">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="96152-191">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="96152-192">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="96152-192">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="96152-193">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="96152-193">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-194">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="96152-194">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="96152-195">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="96152-195">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96152-196">In seguito all'esito positivo, l'indice corrente del cursore viene impostato sull'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="96152-196">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="96152-197">È ora possibile cercare le voci di indice usando [JetSeek](./jetseek-function.md) in base alla definizione dell'indice dell'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="96152-197">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="96152-198">È inoltre possibile enumerare le voci di indice utilizzando [JetMove](./jetmove-function.md) nell'ordine specificato dalla definizione di tale indice.</span><span class="sxs-lookup"><span data-stu-id="96152-198">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="96152-199">La posizione corrente del cursore viene impostata sulla prima voce di indice nell'indice (JET_bitMoveFirst) o su una voce di indice specifica correlata alla posizione corrente del cursore sull'indice precedente (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="96152-199">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="96152-200">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="96152-200">No change to the database state will occur.</span></span>

<span data-ttu-id="96152-201">In caso di errore, l'indice corrente e la posizione corrente del cursore sono in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="96152-201">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="96152-202">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="96152-202">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="96152-203">Commenti</span><span class="sxs-lookup"><span data-stu-id="96152-203">Remarks</span></span>

<span data-ttu-id="96152-204">Se l'hint ID dell'indice non è aggiornato, l'API ha semplicemente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="96152-204">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="96152-205">In questo caso, non esiste alcun fallback al nome di testo dell'indice, come si può prevedere.</span><span class="sxs-lookup"><span data-stu-id="96152-205">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="96152-206">Questo fallback deve essere eseguito manualmente dal chiamante dell'API.</span><span class="sxs-lookup"><span data-stu-id="96152-206">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="96152-207">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96152-207">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96152-208"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="96152-208"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="96152-209">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="96152-209">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-210"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="96152-210"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="96152-211">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="96152-211">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-212"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="96152-212"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="96152-213">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="96152-213">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-214"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="96152-214"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="96152-215">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="96152-215">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96152-216"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="96152-216"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="96152-217">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="96152-217">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96152-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="96152-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="96152-219">Implementato come <strong>JetSetCurrentIndex3W</strong> (Unicode) e <strong>JetSetCurrentIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="96152-219">Implemented as <strong>JetSetCurrentIndex3W</strong> (Unicode) and <strong>JetSetCurrentIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="96152-220">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="96152-220">See Also</span></span>

[<span data-ttu-id="96152-221">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="96152-221">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="96152-222">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="96152-222">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="96152-223">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="96152-223">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="96152-224">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="96152-224">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="96152-225">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="96152-225">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="96152-226">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="96152-226">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="96152-227">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="96152-227">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="96152-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="96152-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="96152-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="96152-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="96152-230">JetMove</span><span class="sxs-lookup"><span data-stu-id="96152-230">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="96152-231">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="96152-231">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="96152-232">JetSeek</span><span class="sxs-lookup"><span data-stu-id="96152-232">JetSeek</span></span>](./jetseek-function.md)
