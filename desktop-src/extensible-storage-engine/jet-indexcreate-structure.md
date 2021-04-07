---
description: 'Altre informazioni su: struttura JET_INDEXCREATE'
title: Struttura JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757937"
---
# <a name="jet_indexcreate-structure"></a><span data-ttu-id="b1664-103">Struttura JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="b1664-103">JET_INDEXCREATE Structure</span></span>


<span data-ttu-id="b1664-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b1664-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="b1664-105">La struttura **JET_INDEXCREATE** contiene le informazioni necessarie per creare un indice sui dati in un database Extensible Storage Engine (ESE).</span><span class="sxs-lookup"><span data-stu-id="b1664-105">The **JET_INDEXCREATE** structure contains the information needed to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="b1664-106">La struttura viene utilizzata da funzioni quali [JetCreateIndex2](./jetcreateindex2-function.md)e in strutture quali [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span><span class="sxs-lookup"><span data-stu-id="b1664-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="b1664-107">Membri</span><span class="sxs-lookup"><span data-stu-id="b1664-107">Members</span></span>

<span data-ttu-id="b1664-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="b1664-108">**cbStruct**</span></span>

<span data-ttu-id="b1664-109">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="b1664-109">The size, in bytes, of this structure.</span></span> <span data-ttu-id="b1664-110">Impostare questo membro su sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="b1664-110">Set this member to sizeof( JET_INDEXCREATE ).</span></span>

<span data-ttu-id="b1664-111">**szIndexName**</span><span class="sxs-lookup"><span data-stu-id="b1664-111">**szIndexName**</span></span>

<span data-ttu-id="b1664-112">Nome dell'indice da creare.</span><span class="sxs-lookup"><span data-stu-id="b1664-112">The name of the index to create.</span></span>

<span data-ttu-id="b1664-113">Il nome dell'indice deve soddisfare le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1664-113">The name of the index must meet the following conditions:</span></span>

  - <span data-ttu-id="b1664-114">Deve essere minore di JET_cbNameMost, escluso il valore null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="b1664-114">It must be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="b1664-115">Deve essere costituito dai caratteri seguenti: 0 (zero) a 9, da A A Z, da a a z e tutti gli altri segni di punteggiatura, ad eccezione di " \! "</span><span class="sxs-lookup"><span data-stu-id="b1664-115">It must consist of the following characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="b1664-116">(punto esclamativo), "," (virgola), " \[ " (parentesi di apertura) e " \] " (parentesi di chiusura), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c, 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="b1664-116">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="b1664-117">Non deve iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="b1664-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="b1664-118">Deve essere costituito da almeno un carattere non di spazio.</span><span class="sxs-lookup"><span data-stu-id="b1664-118">It must consist of at least one nonspace character.</span></span>

<span data-ttu-id="b1664-119">**szKey**</span><span class="sxs-lookup"><span data-stu-id="b1664-119">**szKey**</span></span>

<span data-ttu-id="b1664-120">Puntatore a una stringa con terminazione null di token delimitati da null.</span><span class="sxs-lookup"><span data-stu-id="b1664-120">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="b1664-121">Ogni token è nel formato " \<direction-specifier\> \<column-name\> ", dove Direction-Specification è "+" o "-".</span><span class="sxs-lookup"><span data-stu-id="b1664-121">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="b1664-122">Ad esempio, un **szKey** di "+ ABC \\ 0-def \\ 0 + ghi \\ 0" effettuerà l'indice sulle tre colonne "ABC" (in ordine crescente), "def" (in ordine decrescente) e "ghi" (in ordine crescente).</span><span class="sxs-lookup"><span data-stu-id="b1664-122">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="b1664-123">Nel linguaggio C i valori letterali stringa hanno un carattere di terminazione **null** implicito; Pertanto, la stringa precedente verrà terminata da un valore Double NULL.</span><span class="sxs-lookup"><span data-stu-id="b1664-123">In the C language, string literals have an implied **NULL** terminator; therefore, the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="b1664-124">Il numero di colonne specificato in **szKey** non può superare il valore di **JET_ccolKeyMost** , ovvero una costante dipendente dalla versione.</span><span class="sxs-lookup"><span data-stu-id="b1664-124">The number of columns specified in **szKey** may not exceed the value of **JET_ccolKeyMost** (a version-dependent constant).</span></span>

<span data-ttu-id="b1664-125">Almeno una colonna deve essere denominata in **szKey**.</span><span class="sxs-lookup"><span data-stu-id="b1664-125">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="b1664-126">Comportamento obsoleto: dopo il carattere di terminazione doppio NULL, è possibile specificare un ID lingua (una parola che viene passata in MAKELCID (LangID, SORT_DEFAULT)) come metodo per specificare l'LCID per l'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-126">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="b1664-127">Non è consentito specificare sia un ID lingua in **szKey** che un LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) , impostando JET_bitIndexUnicode in *grbit*.</span><span class="sxs-lookup"><span data-stu-id="b1664-127">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="b1664-128">Deprecato: dopo l'ID lingua, è possibile passare **cbVarSegMac** come UShort.</span><span class="sxs-lookup"><span data-stu-id="b1664-128">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a USHORT.</span></span> <span data-ttu-id="b1664-129">Il comportamento non è definito se USHORT è impostato in **szKey** e se **cbVarSegMac** è impostato nella struttura.</span><span class="sxs-lookup"><span data-stu-id="b1664-129">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="b1664-130">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="b1664-130">**cbKey**</span></span>

<span data-ttu-id="b1664-131">Lunghezza, in byte, di **szKey** , inclusi i due valori null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="b1664-131">The length, in bytes, of **szKey** including the two terminating nulls.</span></span>

<span data-ttu-id="b1664-132">**grbit**</span><span class="sxs-lookup"><span data-stu-id="b1664-132">**grbit**</span></span>

<span data-ttu-id="b1664-133">Gruppo di bit che include zero o più valori elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b1664-133">A group of bits that includes zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1664-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b1664-134">Value</span></span></p></th>
<th><p><span data-ttu-id="b1664-135">Significato</span><span class="sxs-lookup"><span data-stu-id="b1664-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1664-136">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="b1664-136">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="b1664-137">Non sono consentite voci di indice duplicate (chiavi).</span><span class="sxs-lookup"><span data-stu-id="b1664-137">Duplicate index entries (keys) are not allowed.</span></span> <span data-ttu-id="b1664-138">Questa operazione viene applicata quando viene chiamato <a href="gg269288(v=exchg.10).md">JetUpdate</a> , non quando viene chiamato <a href="gg294137(v=exchg.10).md">JetSetColumn</a> .</span><span class="sxs-lookup"><span data-stu-id="b1664-138">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-139">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="b1664-139">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="b1664-140">L'indice è un indice primario (cluster).</span><span class="sxs-lookup"><span data-stu-id="b1664-140">The index is a primary (clustered) index.</span></span> <span data-ttu-id="b1664-141">Ogni tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="b1664-141">Every table must have exactly one primary index.</span></span> <span data-ttu-id="b1664-142">Se nessun indice primario viene definito in modo esplicito su una tabella, il motore di database creerà il proprio indice primario.</span><span class="sxs-lookup"><span data-stu-id="b1664-142">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-143">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="b1664-143">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="b1664-144">Nessuna delle colonne in cui viene creato l'indice può contenere un valore <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1664-144">None of the columns over which the index is created can contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-145">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="b1664-145">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="b1664-146">Non aggiungere una voce di indice per una riga se tutte le colonne indicizzate sono <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1664-146">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-147">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="b1664-147">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="b1664-148">Non aggiungere una voce di indice per una riga se una delle colonne indicizzate è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1664-148">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-149">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="b1664-149">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="b1664-150">Non aggiungere una voce di indice per una riga se la prima colonna indicizzata è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1664-150">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-151">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="b1664-151">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="b1664-152">Le operazioni sugli indici verranno registrate in modalità differita.</span><span class="sxs-lookup"><span data-stu-id="b1664-152">Index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="b1664-153">JET_bitIndexLazyFlush non influisce sulla pigrizia degli aggiornamenti dei dati.</span><span class="sxs-lookup"><span data-stu-id="b1664-153">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="b1664-154">Se l'operazione di indicizzazione viene interrotta dalla terminazione del processo, il ripristino soft sarà comunque in grado di ottenere il database in uno stato coerente, ma l'indice potrebbe non essere presente.</span><span class="sxs-lookup"><span data-stu-id="b1664-154">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index might not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-155">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="b1664-155">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="b1664-156">Non tentare di compilare l'indice perché tutte le voci restituiscono <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1664-156">Do not attempt to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="b1664-157"><strong>grbit</strong> deve inoltre specificare JET_bitIgnoreAnyNull quando viene passato JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="b1664-157"><strong>grbit</strong> must also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="b1664-158">Si tratta di un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b1664-158">This is a performance enhancement.</span></span> <span data-ttu-id="b1664-159">Se, ad esempio, viene aggiunta una nuova colonna a una tabella, viene creato un indice sulla colonna appena aggiunta e tutti i record della tabella vengono analizzati anche se non vengono aggiunti all'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-159">For example, if a new column is added to a table, an index is created over this newly added column, and all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="b1664-160">La specifica di JET_bitIndexEmpty ignora l'analisi della tabella, che potrebbe richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="b1664-160">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-161">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="b1664-161">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="b1664-162">Causa la visibilità della creazione dell'indice in altre transazioni.</span><span class="sxs-lookup"><span data-stu-id="b1664-162">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="b1664-163">In genere, una sessione in una transazione non sarà in grado di visualizzare un'operazione di creazione dell'indice in un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="b1664-163">Typically a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="b1664-164">Questo flag può essere utile se è probabile che un'altra transazione crei lo stesso indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-164">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="b1664-165">La seconda creazione dell'indice avrà esito negativo anziché causare potenzialmente molte operazioni di database non necessarie.</span><span class="sxs-lookup"><span data-stu-id="b1664-165">The second index-create will fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="b1664-166">La seconda transazione potrebbe non essere in grado di utilizzare immediatamente l'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-166">The second transaction might not be able to use the index immediately.</span></span> <span data-ttu-id="b1664-167">L'operazione di creazione dell'indice deve essere completata prima che sia utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="b1664-167">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="b1664-168">La sessione non deve attualmente trovarsi in una transazione per creare un indice senza informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="b1664-168">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-169">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="b1664-169">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="b1664-170">Se si specifica questo flag, i valori <strong>null</strong> verranno ordinati dopo i dati per tutte le colonne dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-170">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-171">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="b1664-171">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="b1664-172">L'impostazione di questo flag influiscono sull'interpretazione del campo di Unione LCID/pidxunicde nella struttura.</span><span class="sxs-lookup"><span data-stu-id="b1664-172">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="b1664-173">L'impostazione del bit significa che il campo <strong>pidxunicode</strong> punta effettivamente a una struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> .</span><span class="sxs-lookup"><span data-stu-id="b1664-173">Setting the bit means that the <strong>pidxunicode</strong> field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="b1664-174">JET_bitIndexUnicode non è necessario per indicizzare i dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1664-174">JET_bitIndexUnicode is not required in order to index Unicode data.</span></span> <span data-ttu-id="b1664-175">Viene utilizzato solo per personalizzare la normalizzazione dei dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1664-175">It is only used to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-176">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="b1664-176">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="b1664-177">Specifica che l'indice è un indice della tupla.</span><span class="sxs-lookup"><span data-stu-id="b1664-177">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="b1664-178">Per una descrizione di un indice di tupla, vedere <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="b1664-178">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="b1664-179">JET_bitIndexTuples è stato introdotto nel sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1664-179">JET_bitIndexTuples was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-180">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="b1664-180">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="b1664-181">L'impostazione di questo flag influiscono sull'interpretazione del campo di Unione <strong>cbVarSegMac/ptuplelimits</strong> nella struttura.</span><span class="sxs-lookup"><span data-stu-id="b1664-181">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="b1664-182">L'impostazione di questo bit significa che il campo <strong>ptuplelimits</strong> punta effettivamente a una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> per consentire limiti di indice di tupla personalizzati (implica JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="b1664-182">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="b1664-183">JET_bitIndexTupleLimits è stato introdotto nel sistema operativo Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b1664-183">JET_bitIndexTupleLimits was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-184">JET_bitIndexCrossProduct 0x00004000</span><span class="sxs-lookup"><span data-stu-id="b1664-184">JET_bitIndexCrossProduct 0x00004000</span></span></p></td>
<td><p><span data-ttu-id="b1664-185">Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave.</span><span class="sxs-lookup"><span data-stu-id="b1664-185">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="b1664-186">In caso contrario, l'indice avrà una sola voce per ogni valore multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice utilizzerà il primo valore multivalore di qualsiasi altra colonna chiave che è costituita da colonne multivalore.</span><span class="sxs-lookup"><span data-stu-id="b1664-186">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multivalued columns.</span></span></p>
<p><span data-ttu-id="b1664-187">Se, ad esempio, si specifica questo flag per un indice sulla colonna A con i valori &quot; rosso &quot; e &quot; blu &quot; e sulla colonna B con i valori &quot; 1 &quot; e 2 &quot; , &quot; verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; rosso &quot; , &quot; 2 &quot; ; &quot; blu &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="b1664-187">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="b1664-188">In caso contrario, verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="b1664-188">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="b1664-189">JET_bitIndexCrossProduct è stato introdotto nel sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1664-189">JET_bitIndexCrossProduct was introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-190">JET_bitIndexKeyMost 0x00008000</span><span class="sxs-lookup"><span data-stu-id="b1664-190">JET_bitIndexKeyMost 0x00008000</span></span></p></td>
<td><p><span data-ttu-id="b1664-191">Se si specifica questo flag, l'indice utilizzerà la dimensione massima della chiave specificata nel campo <strong>cbKeyMost</strong> della struttura.</span><span class="sxs-lookup"><span data-stu-id="b1664-191">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="b1664-192">In caso contrario, l'indice utilizzerà JET_cbKeyMost (255) come dimensione massima della chiave.</span><span class="sxs-lookup"><span data-stu-id="b1664-192">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="b1664-193">JET_bitIndexKeyMost è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1664-193">JET_bitIndexKeyMost was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-194">JET_bitIndexDisallowTruncation 0x00010000</span><span class="sxs-lookup"><span data-stu-id="b1664-194">JET_bitIndexDisallowTruncation 0x00010000</span></span></p></td>
<td><p><span data-ttu-id="b1664-195">Se si specifica questo flag, eventuali aggiornamenti all'indice che comporteranno la mancata riuscita di una chiave troncata con JET_errKeyTruncated.</span><span class="sxs-lookup"><span data-stu-id="b1664-195">Specifying this flag will cause any update to the index that would result in a truncated key to fail with JET_errKeyTruncated.</span></span> <span data-ttu-id="b1664-196">In caso contrario, le chiavi verranno troncate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b1664-196">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="b1664-197">Per ulteriori informazioni sul troncamento delle chiavi, vedere la funzione <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="b1664-197">For more information on key truncation, see the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p>
<p><span data-ttu-id="b1664-198"><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1664-198"><strong>Windows Vista:  JET_bitIndexDisallowTruncation</strong> is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-199">JET_bitIndexNestedTable 0x00020000</span><span class="sxs-lookup"><span data-stu-id="b1664-199">JET_bitIndexNestedTable 0x00020000</span></span></p></td>
<td><p><span data-ttu-id="b1664-200">Se si specifica questo flag, l'indice verrà aggiornato su più colonne multivalore, ma solo con valori dello stesso <strong>itagSequence</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1664-200">Specifying this flag will cause update the index over multiple multivalued columns but only with values of same <strong>itagSequence</strong>.</span></span></p>
<p><span data-ttu-id="b1664-201">JET_bitIndexNestedTable è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1664-201">JET_bitIndexNestedTable was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1664-202">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="b1664-202">**ulDensity**</span></span>

<span data-ttu-id="b1664-203">Densità percentuale dell'albero iniziale B + dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-203">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="b1664-204">Se si specifica un numero inferiore a 100, viene utilizzato un maggior numero di spazio per la creazione iniziale dell'indice, ma è possibile applicare una crescita futura dell'indice, evitando così la frammentazione interna.</span><span class="sxs-lookup"><span data-stu-id="b1664-204">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="b1664-205">**lcid**</span><span class="sxs-lookup"><span data-stu-id="b1664-205">**lcid**</span></span>

<span data-ttu-id="b1664-206">Identificatore delle impostazioni locali (LCID) da usare per la normalizzazione dei dati quando il valore di JET_bitIndexUnicode non è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="b1664-206">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="b1664-207">L'LCID influiscono sulla normalizzazione se l'indice è sovrascrivendo le colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1664-207">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="b1664-208">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="b1664-208">**pidxunicode**</span></span>

<span data-ttu-id="b1664-209">Puntatore a una struttura [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se il valore di JET_bitIndexUnicode è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="b1664-209">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="b1664-210">Ciò consente all'utente di specificare i flag personalizzati che vengono passati alla funzione [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante la normalizzazione Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1664-210">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="b1664-211">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="b1664-211">**cbVarSegMac**</span></span>

<span data-ttu-id="b1664-212">Lunghezza massima, in byte, di ogni colonna da archiviare nell'indice quando il valore JET_bitIndexTupleLimits non viene specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="b1664-212">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="b1664-213">La specifica di un valore pari a 0 (zero) per questo campo è equivalente a:</span><span class="sxs-lookup"><span data-stu-id="b1664-213">Specifying a value of 0 (zero) for this field is equivalent to:</span></span>

  - <span data-ttu-id="b1664-214">Specifica JET_cbPrimaryKeyMost per un indice primario.</span><span class="sxs-lookup"><span data-stu-id="b1664-214">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="b1664-215">Specifica JET_cbSecondaryKeyMost per un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="b1664-215">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="b1664-216">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="b1664-216">**ptuplelimits**</span></span>

<span data-ttu-id="b1664-217">Puntatore a una struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se il valore di JET_bitIndexTupleLimits è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="b1664-217">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="b1664-218">ptuplelimits è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b1664-218">ptuplelimits was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="b1664-219">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="b1664-219">**rgconditionalcolumn**</span></span>

<span data-ttu-id="b1664-220">Parametro facoltativo di una matrice di strutture di [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , utilizzate per specificare le colonne condizionali nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-220">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="b1664-221">**cConditionalColumn**</span><span class="sxs-lookup"><span data-stu-id="b1664-221">**cConditionalColumn**</span></span>

<span data-ttu-id="b1664-222">Numero di strutture nella matrice **rgconditionalcolumn** .</span><span class="sxs-lookup"><span data-stu-id="b1664-222">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="b1664-223">**Err**</span><span class="sxs-lookup"><span data-stu-id="b1664-223">**err**</span></span>

<span data-ttu-id="b1664-224">Contiene il codice restituito per la creazione di questo indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-224">Contains the return code for creating this index.</span></span>

<span data-ttu-id="b1664-225">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="b1664-225">**cbKeyMost**</span></span>

<span data-ttu-id="b1664-226">Specifica la dimensione massima consentita, in byte, per le chiavi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-226">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="b1664-227">Questo parametro viene ignorato se il valore JET_bitIndexKeyMost non è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="b1664-227">This parameter is ignored if the JET_bitIndexKeyMost value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="b1664-228">Se questo parametro è impostato su zero e JET_bitIndexKeyMost viene specificato nel parametro *grbit* , la funzione chiamante avrà esito negativo con JET_err_InvalidDef.</span><span class="sxs-lookup"><span data-stu-id="b1664-228">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* parameter, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="b1664-229">Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero la dimensione massima della chiave legacy.</span><span class="sxs-lookup"><span data-stu-id="b1664-229">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="b1664-230">Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database (JET_paramDatabasePageSize), come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b1664-230">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize), as follows:</span></span>

  - <span data-ttu-id="b1664-231">Se JET_paramDatabasePageSize = 2048 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="b1664-231">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="b1664-232">Se JET_paramDatabasePageSize = 4096 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="b1664-232">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="b1664-233">Se JET_paramDatabasePageSize = 8192 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="b1664-233">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="b1664-234">Le dimensioni massime supportate per l'istanza possono essere lette anche dal parametro di sistema JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="b1664-234">The maximum supported key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="b1664-235">**cbKeyMost** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1664-235">**cbKeyMost** was introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="b1664-236">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1664-236">Remarks</span></span>

<span data-ttu-id="b1664-237">ESE supporta l'indicizzazione su colonne chiave contenenti più valori.</span><span class="sxs-lookup"><span data-stu-id="b1664-237">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="b1664-238">Per usare questa funzionalità, la colonna deve essere un tipo di colonna con tag (JET_bitColumnTagged) ed è necessario contrassegnarla per avere più valori indicizzati con JET_bitColumnMultiValued.</span><span class="sxs-lookup"><span data-stu-id="b1664-238">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="b1664-239">Nelle versioni di Windows precedenti a Windows Vista, solo la prima colonna chiave multivalore nell'indice avrà i valori espansi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-239">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="b1664-240">Tutte le altre colonne multivalore e con tag avranno solo i primi valori espansi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b1664-240">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="b1664-241">Supponendo che le righe seguenti siano presenti in una tabella (la colonna alfa non è multivalore, mentre le colonne beta, gamma e Delta sono multivalore) e viene creato un indice come "+ Alpha \\ 0 + Beta \\ 0 + gamma \\ 0 + Delta \\ 0 \\ 0":</span><span class="sxs-lookup"><span data-stu-id="b1664-241">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1664-242">Alfa</span><span class="sxs-lookup"><span data-stu-id="b1664-242">Alpha</span></span></p></th>
<th><p><span data-ttu-id="b1664-243">Beta</span><span class="sxs-lookup"><span data-stu-id="b1664-243">Beta</span></span></p></th>
<th><p><span data-ttu-id="b1664-244">Gamma</span><span class="sxs-lookup"><span data-stu-id="b1664-244">Gamma</span></span></p></th>
<th><p><span data-ttu-id="b1664-245">Delta</span><span class="sxs-lookup"><span data-stu-id="b1664-245">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1664-246">1</span><span class="sxs-lookup"><span data-stu-id="b1664-246">1</span></span></p></td>
<td><p><span data-ttu-id="b1664-247">ABC</span><span class="sxs-lookup"><span data-stu-id="b1664-247">ABC</span></span><br />
<span data-ttu-id="b1664-248">GHI</span><span class="sxs-lookup"><span data-stu-id="b1664-248">GHI</span></span><br />
<span data-ttu-id="b1664-249">JKL</span><span class="sxs-lookup"><span data-stu-id="b1664-249">JKL</span></span></p></td>
<td><p><span data-ttu-id="b1664-250">MNO</span><span class="sxs-lookup"><span data-stu-id="b1664-250">MNO</span></span><br />
<span data-ttu-id="b1664-251">PQR</span><span class="sxs-lookup"><span data-stu-id="b1664-251">PQR</span></span><br />
<span data-ttu-id="b1664-252">S</span><span class="sxs-lookup"><span data-stu-id="b1664-252">STU</span></span></p></td>
<td><p><span data-ttu-id="b1664-253">VWX</span><span class="sxs-lookup"><span data-stu-id="b1664-253">VWX</span></span><br />
<span data-ttu-id="b1664-254">YZ</span><span class="sxs-lookup"><span data-stu-id="b1664-254">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-255">2</span><span class="sxs-lookup"><span data-stu-id="b1664-255">2</span></span></p></td>
<td><p><span data-ttu-id="b1664-256">IL</span><span class="sxs-lookup"><span data-stu-id="b1664-256">THE</span></span></p></td>
<td><p><span data-ttu-id="b1664-257">PIOGGIA</span><span class="sxs-lookup"><span data-stu-id="b1664-257">RAIN</span></span><br />
<span data-ttu-id="b1664-258">Spagna</span><span class="sxs-lookup"><span data-stu-id="b1664-258">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="b1664-259">IN</span><span class="sxs-lookup"><span data-stu-id="b1664-259">IN</span></span><br />
<span data-ttu-id="b1664-260">RIENTRA</span><span class="sxs-lookup"><span data-stu-id="b1664-260">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1664-261">Verranno archiviate le tuple degli indici in calo:</span><span class="sxs-lookup"><span data-stu-id="b1664-261">The falling index-tuples will be stored:</span></span>

<span data-ttu-id="b1664-262">{1, ABC, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="b1664-262">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="b1664-263">{1, GHI, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="b1664-263">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="b1664-264">{1, JKL, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="b1664-264">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="b1664-265">{2,, PIOGGIA, IN}</span><span class="sxs-lookup"><span data-stu-id="b1664-265">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="b1664-266">Si noti che {2,, SPAIN, IN} non è archiviato, anche se la colonna Alpha nella seconda riga ha un singolo valore multivalore.</span><span class="sxs-lookup"><span data-stu-id="b1664-266">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="b1664-267">Nelle versioni di Windows a partire da Windows Vista, tutte le colonne multivalore possono essere espanse nell'indice specificando JET_bitIndexCrossProduct.</span><span class="sxs-lookup"><span data-stu-id="b1664-267">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="b1664-268">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1664-268">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1664-269"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b1664-269"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b1664-270">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b1664-270">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-271"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b1664-271"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b1664-272">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b1664-272">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1664-273"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b1664-273"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b1664-274">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b1664-274">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1664-275"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b1664-275"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b1664-276">Implementato come <strong>JET_ INDEXCREATE_W</strong> (Unicode) e <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b1664-276">Implemented as <strong>JET_ INDEXCREATE_W</strong> (Unicode) and <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b1664-277">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1664-277">See also</span></span>

[<span data-ttu-id="b1664-278">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="b1664-278">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="b1664-279">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="b1664-279">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="b1664-280">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b1664-280">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b1664-281">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b1664-281">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b1664-282">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="b1664-282">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="b1664-283">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="b1664-283">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="b1664-284">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="b1664-284">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="b1664-285">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="b1664-285">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="b1664-286">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="b1664-286">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="b1664-287">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b1664-287">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="b1664-288">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="b1664-288">JetUpdate</span></span>](./jetupdate-function.md)
