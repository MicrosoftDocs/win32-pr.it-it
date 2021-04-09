---
description: 'Altre informazioni su: struttura JET_INDEXCREATE2'
title: Struttura JET_INDEXCREATE2
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968719"
---
# <a name="jet_indexcreate2-structure"></a><span data-ttu-id="e487a-103">Struttura JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="e487a-103">JET_INDEXCREATE2 Structure</span></span>


<span data-ttu-id="e487a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e487a-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="e487a-105">La struttura **JET_INDEXCREATE2** contiene le informazioni necessarie per creare un indice sui dati in un database Extensible Storage Engine (ESE).</span><span class="sxs-lookup"><span data-stu-id="e487a-105">The **JET_INDEXCREATE2** structure contains the information that is required to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="e487a-106">La struttura viene utilizzata da funzioni quali [JetCreateIndex2](./jetcreateindex2-function.md)e in strutture quali [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e487a-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

<span data-ttu-id="e487a-107">La struttura **JET_INDEXCREATE2** è stata introdotta nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e487a-107">The **JET_INDEXCREATE2** structure was introduced in the Windows 7 operating system.</span></span>

```cpp
typedef struct tagJET_INDEXCREATE2 {
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
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="e487a-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e487a-108">Members</span></span>

<span data-ttu-id="e487a-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e487a-109">**cbStruct**</span></span>

<span data-ttu-id="e487a-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="e487a-110">The size, in bytes, of this structure.</span></span> <span data-ttu-id="e487a-111">Impostare questo membro su sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="e487a-111">Set this member to sizeof( JET_INDEXCREATE2 ).</span></span>

<span data-ttu-id="e487a-112">**szIndexName**</span><span class="sxs-lookup"><span data-stu-id="e487a-112">**szIndexName**</span></span>

<span data-ttu-id="e487a-113">Nome dell'indice da creare.</span><span class="sxs-lookup"><span data-stu-id="e487a-113">The name of the index to create.</span></span>

<span data-ttu-id="e487a-114">Il nome deve soddisfare le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e487a-114">The name should meet the following conditions:</span></span>

  - <span data-ttu-id="e487a-115">Deve essere minore di JET_cbNameMost, escluso il valore null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e487a-115">It should be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="e487a-116">Deve essere costituito dal set di caratteri seguente: 0 (zero) a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di " \! "</span><span class="sxs-lookup"><span data-stu-id="e487a-116">It must consist of the following set of characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="e487a-117">(punto esclamativo), "," (virgola), " \[ " (parentesi di apertura) e " \] " (parentesi di chiusura), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="e487a-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="e487a-118">Non deve iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="e487a-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="e487a-119">Deve contenere almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="e487a-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="e487a-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="e487a-120">**szKey**</span></span>

<span data-ttu-id="e487a-121">Puntatore a una stringa con terminazione null di token delimitati da null.</span><span class="sxs-lookup"><span data-stu-id="e487a-121">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="e487a-122">Ogni token è nel formato " \<direction-specifier\> \<column-name\> ", dove Direction-Specification è "+" o "-".</span><span class="sxs-lookup"><span data-stu-id="e487a-122">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="e487a-123">Ad esempio, un **szKey** di "+ ABC \\ 0-def \\ 0 + ghi \\ 0" effettuerà l'indice sulle tre colonne "ABC" (in ordine crescente), "def" (in ordine decrescente) e "ghi" (in ordine crescente).</span><span class="sxs-lookup"><span data-stu-id="e487a-123">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="e487a-124">Nel linguaggio C i valori letterali stringa hanno un carattere di terminazione **null** implicito, quindi la stringa precedente verrà terminata da un valore null doppio.</span><span class="sxs-lookup"><span data-stu-id="e487a-124">In the C language, string literals have an implied **NULL** terminator, so the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="e487a-125">Il numero di colonne specificato in **szKey** non deve superare JET_ccolKeyMost (una costante dipendente dalla versione).</span><span class="sxs-lookup"><span data-stu-id="e487a-125">The number of columns specified in **szKey** must not exceed JET_ccolKeyMost (a version-dependent constant).</span></span>

<span data-ttu-id="e487a-126">Almeno una colonna deve essere denominata in **szKey**.</span><span class="sxs-lookup"><span data-stu-id="e487a-126">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="e487a-127">Comportamento obsoleto: dopo il carattere di terminazione doppio NULL, è possibile specificare un ID lingua (una parola che viene passata in MAKELCID (LangID, SORT_DEFAULT)) come metodo per specificare l'LCID per l'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-127">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="e487a-128">Non è consentito specificare sia un ID lingua in **szKey** che un LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) , impostando JET_bitIndexUnicode in *grbit*.</span><span class="sxs-lookup"><span data-stu-id="e487a-128">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="e487a-129">Deprecato: dopo l'ID lingua, è possibile passare **cbVarSegMac** come tipo di dati **ushort** .</span><span class="sxs-lookup"><span data-stu-id="e487a-129">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a **USHORT** data type.</span></span> <span data-ttu-id="e487a-130">Il comportamento non è definito se USHORT è impostato in **szKey** e se **cbVarSegMac** è impostato nella struttura.</span><span class="sxs-lookup"><span data-stu-id="e487a-130">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="e487a-131">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="e487a-131">**cbKey**</span></span>

<span data-ttu-id="e487a-132">Lunghezza, in byte, di **szKey**, inclusi i due valori null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e487a-132">The length, in bytes, of **szKey**, including the two terminating nulls.</span></span>

<span data-ttu-id="e487a-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="e487a-133">**grbit**</span></span>

<span data-ttu-id="e487a-134">Gruppo di bit che contiene zero o più opzioni di valore elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e487a-134">A group of bits that contain zero or more of the value options that are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e487a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e487a-135">Value</span></span></p></th>
<th><p><span data-ttu-id="e487a-136">Significato</span><span class="sxs-lookup"><span data-stu-id="e487a-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e487a-137">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="e487a-137">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="e487a-138">Le voci di indice (chiavi) duplicate non sono consentite.</span><span class="sxs-lookup"><span data-stu-id="e487a-138">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="e487a-139">Questa operazione viene applicata quando viene chiamato <a href="gg269288(v=exchg.10).md">JetUpdate</a> , non quando viene chiamato <a href="gg294137(v=exchg.10).md">JetSetColumn</a> .</span><span class="sxs-lookup"><span data-stu-id="e487a-139">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-140">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="e487a-140">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="e487a-141">L'indice è un indice primario (cluster).</span><span class="sxs-lookup"><span data-stu-id="e487a-141">The index is a primary (clustered) index.</span></span> <span data-ttu-id="e487a-142">Ogni tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="e487a-142">Every table must have exactly one primary index.</span></span> <span data-ttu-id="e487a-143">Se nessun indice primario viene definito in modo esplicito su una tabella, il motore di database creerà il proprio indice primario.</span><span class="sxs-lookup"><span data-stu-id="e487a-143">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-144">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="e487a-144">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="e487a-145">Nessuna delle colonne in cui viene creato l'indice può contenere un valore <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="e487a-145">None of the columns over which the index is created may contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-146">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="e487a-146">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="e487a-147">Non aggiungere una voce di indice per una riga se tutte le colonne indicizzate sono <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e487a-147">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-148">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="e487a-148">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="e487a-149">Non aggiungere una voce di indice per una riga se una delle colonne indicizzate è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e487a-149">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-150">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="e487a-150">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="e487a-151">Non aggiungere una voce di indice per una riga se la prima colonna indicizzata è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e487a-151">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-152">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="e487a-152">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="e487a-153">Specifica che le operazioni sugli indici verranno registrate in modalità differita.</span><span class="sxs-lookup"><span data-stu-id="e487a-153">Specifies that the index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="e487a-154">JET_bitIndexLazyFlush non influisce sulla pigrizia degli aggiornamenti dei dati.</span><span class="sxs-lookup"><span data-stu-id="e487a-154">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="e487a-155">Se l'operazione di indicizzazione viene interrotta dalla terminazione del processo, il ripristino soft sarà comunque in grado di ottenere il database in uno stato coerente, ma l'indice potrebbe non essere presente.</span><span class="sxs-lookup"><span data-stu-id="e487a-155">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-156">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="e487a-156">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="e487a-157">Non provare a compilare l'indice perché tutte le voci restituiscono <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e487a-157">Do not try to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="e487a-158"><strong>grbit</strong> È inoltre necessario specificare JET_bitIgnoreAnyNull quando viene passato JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="e487a-158"><strong>grbit</strong> MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="e487a-159">Si tratta di un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e487a-159">This is a performance enhancement.</span></span> <span data-ttu-id="e487a-160">Se, ad esempio, viene aggiunta una nuova colonna a una tabella e quindi viene creato un indice sulla colonna appena aggiunta, tutti i record della tabella verranno analizzati anche se non vengono aggiunti all'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-160">For example, if a new column is added to a table, and then an index is created over this newly added column, all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="e487a-161">La specifica di JET_bitIndexEmpty ignora l'analisi della tabella, che potrebbe richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="e487a-161">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-162">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="e487a-162">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="e487a-163">JET_bitIndexUnversioned fa in modo che la creazione dell'indice sia visibile ad altre transazioni.</span><span class="sxs-lookup"><span data-stu-id="e487a-163">JET_bitIndexUnversioned causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="e487a-164">In genere, una sessione in una transazione non sarà in grado di visualizzare un'operazione di creazione dell'indice in un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="e487a-164">Ordinarily, a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="e487a-165">Questo flag può essere utile se è probabile che un'altra transazione crei lo stesso indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-165">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="e487a-166">Il secondo indice-creazione avrà semplicemente esito negativo anziché causare numerose operazioni di database non necessarie.</span><span class="sxs-lookup"><span data-stu-id="e487a-166">The second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="e487a-167">La seconda transazione potrebbe non essere in grado di utilizzare immediatamente l'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-167">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="e487a-168">L'operazione di creazione dell'indice deve essere completata prima che sia utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="e487a-168">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="e487a-169">La sessione non deve attualmente trovarsi in una transazione per creare un indice senza informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="e487a-169">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-170">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="e487a-170">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="e487a-171">Se si specifica questo flag, i valori <strong>null</strong> verranno ordinati dopo i dati per tutte le colonne dell'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-171">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-172">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="e487a-172">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="e487a-173">L'impostazione di questo flag influiscono sull'interpretazione del campo di Unione LCID/pidxunicde nella struttura.</span><span class="sxs-lookup"><span data-stu-id="e487a-173">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="e487a-174">L'impostazione del bit significa che il campo pidxunicode punta effettivamente a una struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> .</span><span class="sxs-lookup"><span data-stu-id="e487a-174">Setting the bit means that the pidxunicode field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="e487a-175">JET_bitIndexUnicode non è necessario per indicizzare i dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="e487a-175">JET_bitIndexUnicode is not required to index Unicode data.</span></span> <span data-ttu-id="e487a-176">È necessario solo per personalizzare la normalizzazione dei dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="e487a-176">It is only needed to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-177">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="e487a-177">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="e487a-178">Specifica che l'indice è un indice della tupla.</span><span class="sxs-lookup"><span data-stu-id="e487a-178">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="e487a-179">Per una descrizione di un indice di tupla, vedere <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="e487a-179">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="e487a-180">Il valore JET_bitIndexTuples è stato introdotto nel sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e487a-180">The JET_bitIndexTuples value was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-181">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="e487a-181">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="e487a-182">L'impostazione di questo flag influiscono sull'interpretazione del campo di Unione <strong>cbVarSegMac/ptuplelimits</strong> nella struttura.</span><span class="sxs-lookup"><span data-stu-id="e487a-182">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="e487a-183">L'impostazione di questo bit significa che il campo <strong>ptuplelimits</strong> punta effettivamente a una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> per consentire limiti di indice di tupla personalizzati (implica JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="e487a-183">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="e487a-184">Il valore <strong>JET_bitIndexTupleLimits</strong> è stato introdotto nel sistema operativo Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e487a-184">The <strong>JET_bitIndexTupleLimits</strong> value was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-185">JET_bitIndexCrossProduct</span><span class="sxs-lookup"><span data-stu-id="e487a-185">JET_bitIndexCrossProduct</span></span><br />
<span data-ttu-id="e487a-186">0x00004000</span><span class="sxs-lookup"><span data-stu-id="e487a-186">0x00004000</span></span></p></td>
<td><p><span data-ttu-id="e487a-187">Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave.</span><span class="sxs-lookup"><span data-stu-id="e487a-187">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="e487a-188">In caso contrario, l'indice avrà una sola voce per ogni valore multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice utilizzerà il primo valore multivalore di qualsiasi altra colonna chiave con più colonne con valori.</span><span class="sxs-lookup"><span data-stu-id="e487a-188">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multi valued columns.</span></span></p>
<p><span data-ttu-id="e487a-189">Se, ad esempio, si specifica questo flag per un indice sulla colonna A con i valori &quot; rosso &quot; e &quot; blu &quot; e sulla colonna B con i valori &quot; 1 &quot; e &quot; 2 &quot; , verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; rosso &quot; , &quot; 2 &quot; ; &quot; blu &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="e487a-189">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot;, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="e487a-190">In caso contrario, verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="e487a-190">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="e487a-191">Il valore <strong>JET_bitIndexCrossProduct</strong> è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e487a-191">The <strong>JET_bitIndexCrossProduct</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-192">JET_bitIndexKeyMost</span><span class="sxs-lookup"><span data-stu-id="e487a-192">JET_bitIndexKeyMost</span></span><br />
<span data-ttu-id="e487a-193">0x00008000</span><span class="sxs-lookup"><span data-stu-id="e487a-193">0x00008000</span></span></p></td>
<td><p><span data-ttu-id="e487a-194">Se si specifica questo flag, l'indice utilizzerà la dimensione massima della chiave specificata nel campo <strong>cbKeyMost</strong> della struttura.</span><span class="sxs-lookup"><span data-stu-id="e487a-194">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="e487a-195">In caso contrario, l'indice utilizzerà JET_cbKeyMost (255) come dimensione massima della chiave.</span><span class="sxs-lookup"><span data-stu-id="e487a-195">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="e487a-196">Il valore <strong>JET_bitIndexKeyMost</strong> è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e487a-196">The <strong>JET_bitIndexKeyMost</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-197">JET_bitIndexDisallowTruncation</span><span class="sxs-lookup"><span data-stu-id="e487a-197">JET_bitIndexDisallowTruncation</span></span><br />
<span data-ttu-id="e487a-198">0x00010000</span><span class="sxs-lookup"><span data-stu-id="e487a-198">0x00010000</span></span></p></td>
<td><p><span data-ttu-id="e487a-199">Se si specifica questo flag, eventuali aggiornamenti all'indice che comporteranno la mancata riuscita di una chiave troncata con il codice di risposta JET_errKeyTruncated.</span><span class="sxs-lookup"><span data-stu-id="e487a-199">Specifying this flag will cause any update to the index that would result in a truncated key to fail with the JET_errKeyTruncated response code.</span></span> <span data-ttu-id="e487a-200">In caso contrario, le chiavi verranno troncate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e487a-200">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="e487a-201">Per ulteriori informazioni sul troncamento delle chiavi, vedere <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="e487a-201">For more information about key truncation, see <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p>
<p><span data-ttu-id="e487a-202">Il valore <strong>JET_bitIndexDisallowTruncation</strong> è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e487a-202">The <strong>JET_bitIndexDisallowTruncation</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e487a-203">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="e487a-203">**ulDensity**</span></span>

<span data-ttu-id="e487a-204">Densità percentuale dell'albero iniziale B + dell'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-204">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="e487a-205">Se si specifica un numero inferiore a 100, viene utilizzato un maggior numero di spazio per la creazione iniziale dell'indice, ma è possibile applicare una crescita futura dell'indice, evitando così la frammentazione interna.</span><span class="sxs-lookup"><span data-stu-id="e487a-205">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="e487a-206">**lcid**</span><span class="sxs-lookup"><span data-stu-id="e487a-206">**lcid**</span></span>

<span data-ttu-id="e487a-207">Identificatore delle impostazioni locali (LCID) da usare per la normalizzazione dei dati quando il valore di JET_bitIndexUnicode non è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="e487a-207">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="e487a-208">L'LCID influiscono sulla normalizzazione se l'indice è sovrascrivendo le colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="e487a-208">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="e487a-209">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="e487a-209">**pidxunicode**</span></span>

<span data-ttu-id="e487a-210">Puntatore a una struttura [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se il valore di JET_bitIndexUnicode è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="e487a-210">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="e487a-211">Ciò consente all'utente di specificare i flag personalizzati che vengono passati alla funzione [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante la normalizzazione Unicode.</span><span class="sxs-lookup"><span data-stu-id="e487a-211">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="e487a-212">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="e487a-212">**cbVarSegMac**</span></span>

<span data-ttu-id="e487a-213">Lunghezza massima, in byte, di ogni colonna da archiviare nell'indice quando il valore JET_bitIndexTupleLimits non viene specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="e487a-213">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="e487a-214">La specifica di un valore pari a 0 (zero) per questo campo equivale a quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e487a-214">Specifying a value of 0 (zero) for this field is equivalent to the following:</span></span>

  - <span data-ttu-id="e487a-215">Specifica JET_cbPrimaryKeyMost per un indice primario.</span><span class="sxs-lookup"><span data-stu-id="e487a-215">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="e487a-216">Specifica JET_cbSecondaryKeyMost per un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="e487a-216">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="e487a-217">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="e487a-217">**ptuplelimits**</span></span>

<span data-ttu-id="e487a-218">Puntatore a una struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se il valore di JET_bitIndexTupleLimits è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="e487a-218">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="e487a-219">**ptuplelimits** è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e487a-219">**ptuplelimits** was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="e487a-220">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="e487a-220">**rgconditionalcolumn**</span></span>

<span data-ttu-id="e487a-221">Parametro facoltativo di una matrice di strutture di [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , utilizzate per specificare le colonne condizionali nell'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-221">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="e487a-222">**cConditionalColumn**</span><span class="sxs-lookup"><span data-stu-id="e487a-222">**cConditionalColumn**</span></span>

<span data-ttu-id="e487a-223">Numero di strutture nella matrice **rgconditionalcolumn** .</span><span class="sxs-lookup"><span data-stu-id="e487a-223">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="e487a-224">**Err**</span><span class="sxs-lookup"><span data-stu-id="e487a-224">**err**</span></span>

<span data-ttu-id="e487a-225">Contiene il codice restituito per la creazione di questo indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-225">Contains the return code for creating this index.</span></span>

<span data-ttu-id="e487a-226">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="e487a-226">**cbKeyMost**</span></span>

<span data-ttu-id="e487a-227">Specifica la dimensione massima consentita, in byte, per le chiavi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-227">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="e487a-228">Questo parametro viene ignorato se JET_bitIndexKeyMost non è specificato nel parametro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="e487a-228">This parameter is ignored if JET_bitIndexKeyMost is not specified in *grbit* parameter.</span></span> <span data-ttu-id="e487a-229">Se questo parametro è impostato su zero e JET_bitIndexKeyMost viene specificato nel membro *grbit* , la funzione chiamante avrà esito negativo con JET_err_InvalidDef.</span><span class="sxs-lookup"><span data-stu-id="e487a-229">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* member, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="e487a-230">Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero la dimensione massima della chiave legacy.</span><span class="sxs-lookup"><span data-stu-id="e487a-230">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="e487a-231">Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database (JET_paramDatabasePageSize) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e487a-231">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize) as follows:</span></span>

  - <span data-ttu-id="e487a-232">Se JET_paramDatabasePageSize = 2048 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="e487a-232">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="e487a-233">Se JET_paramDatabasePageSize = 4096 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="e487a-233">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="e487a-234">Se JET_paramDatabasePageSize = 8192 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="e487a-234">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="e487a-235">La dimensione massima supportata per la chiave per l'istanza può essere letta anche dal parametro di sistema JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="e487a-235">The maximum supported maximum key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="e487a-236">**cbKeyMost** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e487a-236">**cbKeyMost** was introduced in Windows Vista.</span></span>

<span data-ttu-id="e487a-237">**pSpacehints**</span><span class="sxs-lookup"><span data-stu-id="e487a-237">**pSpacehints**</span></span>

<span data-ttu-id="e487a-238">Puntatore a una struttura [JET_SPACEHINTS](./jet-spacehints-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e487a-238">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure.</span></span>

<span data-ttu-id="e487a-239">**pSpacehints** è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e487a-239">**pSpacehints** was introduced in Windows 7.</span></span>

### <a name="remarks"></a><span data-ttu-id="e487a-240">Commenti</span><span class="sxs-lookup"><span data-stu-id="e487a-240">Remarks</span></span>

<span data-ttu-id="e487a-241">ESE supporta l'indicizzazione su colonne chiave contenenti più valori.</span><span class="sxs-lookup"><span data-stu-id="e487a-241">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="e487a-242">Per usare questa funzionalità, la colonna deve essere un tipo di colonna con tag (JET_bitColumnTagged) ed è necessario contrassegnarla per avere più valori indicizzati con JET_bitColumnMultiValued.</span><span class="sxs-lookup"><span data-stu-id="e487a-242">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="e487a-243">Nelle versioni di Windows precedenti a Windows Vista, solo la prima colonna chiave multivalore nell'indice avrà i valori espansi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-243">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="e487a-244">Tutte le altre colonne multivalore e con tag avranno solo i primi valori espansi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="e487a-244">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="e487a-245">Supponendo che le righe seguenti siano presenti in una tabella (la colonna alfa non è multivalore, mentre le colonne beta, gamma e Delta sono multivalore) e viene creato un indice come "+ Alpha \\ 0 + Beta \\ 0 + gamma \\ 0 + Delta \\ 0 \\ 0":</span><span class="sxs-lookup"><span data-stu-id="e487a-245">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e487a-246">Alfa</span><span class="sxs-lookup"><span data-stu-id="e487a-246">Alpha</span></span></p></th>
<th><p><span data-ttu-id="e487a-247">Beta</span><span class="sxs-lookup"><span data-stu-id="e487a-247">Beta</span></span></p></th>
<th><p><span data-ttu-id="e487a-248">Gamma</span><span class="sxs-lookup"><span data-stu-id="e487a-248">Gamma</span></span></p></th>
<th><p><span data-ttu-id="e487a-249">Delta</span><span class="sxs-lookup"><span data-stu-id="e487a-249">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e487a-250">1</span><span class="sxs-lookup"><span data-stu-id="e487a-250">1</span></span></p></td>
<td><p><span data-ttu-id="e487a-251">ABC</span><span class="sxs-lookup"><span data-stu-id="e487a-251">ABC</span></span><br />
<span data-ttu-id="e487a-252">GHI</span><span class="sxs-lookup"><span data-stu-id="e487a-252">GHI</span></span><br />
<span data-ttu-id="e487a-253">JKL</span><span class="sxs-lookup"><span data-stu-id="e487a-253">JKL</span></span></p></td>
<td><p><span data-ttu-id="e487a-254">MNO</span><span class="sxs-lookup"><span data-stu-id="e487a-254">MNO</span></span><br />
<span data-ttu-id="e487a-255">PQR</span><span class="sxs-lookup"><span data-stu-id="e487a-255">PQR</span></span><br />
<span data-ttu-id="e487a-256">S</span><span class="sxs-lookup"><span data-stu-id="e487a-256">STU</span></span></p></td>
<td><p><span data-ttu-id="e487a-257">VWX</span><span class="sxs-lookup"><span data-stu-id="e487a-257">VWX</span></span><br />
<span data-ttu-id="e487a-258">YZ</span><span class="sxs-lookup"><span data-stu-id="e487a-258">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-259">2</span><span class="sxs-lookup"><span data-stu-id="e487a-259">2</span></span></p></td>
<td><p><span data-ttu-id="e487a-260">IL</span><span class="sxs-lookup"><span data-stu-id="e487a-260">THE</span></span></p></td>
<td><p><span data-ttu-id="e487a-261">PIOGGIA</span><span class="sxs-lookup"><span data-stu-id="e487a-261">RAIN</span></span><br />
<span data-ttu-id="e487a-262">Spagna</span><span class="sxs-lookup"><span data-stu-id="e487a-262">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="e487a-263">IN</span><span class="sxs-lookup"><span data-stu-id="e487a-263">IN</span></span><br />
<span data-ttu-id="e487a-264">RIENTRA</span><span class="sxs-lookup"><span data-stu-id="e487a-264">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e487a-265">Verranno archiviate le tuple degli indici seguenti:</span><span class="sxs-lookup"><span data-stu-id="e487a-265">The following index-tuples will be stored:</span></span>

<span data-ttu-id="e487a-266">{1, ABC, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="e487a-266">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="e487a-267">{1, GHI, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="e487a-267">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="e487a-268">{1, JKL, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="e487a-268">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="e487a-269">{2,, PIOGGIA, IN}</span><span class="sxs-lookup"><span data-stu-id="e487a-269">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="e487a-270">Si noti che {2,, SPAIN, IN} non è archiviato, anche se la colonna Alpha nella seconda riga ha un singolo valore multivalore.</span><span class="sxs-lookup"><span data-stu-id="e487a-270">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="e487a-271">Nelle versioni di Windows a partire da Windows Vista, tutte le colonne multivalore possono essere espanse nell'indice specificando JET_bitIndexCrossProduct.</span><span class="sxs-lookup"><span data-stu-id="e487a-271">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="e487a-272">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e487a-272">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e487a-273"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e487a-273"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e487a-274">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e487a-274">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-275"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e487a-275"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e487a-276">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e487a-276">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e487a-277"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e487a-277"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e487a-278">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e487a-278">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e487a-279"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e487a-279"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e487a-280">Implementato come <strong>JET_ INDEXCREATE2_W</strong> (Unicode) e <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e487a-280">Implemented as <strong>JET_ INDEXCREATE2_W</strong> (Unicode) and <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e487a-281">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e487a-281">See also</span></span>

[<span data-ttu-id="e487a-282">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="e487a-282">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="e487a-283">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="e487a-283">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="e487a-284">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e487a-284">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e487a-285">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e487a-285">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e487a-286">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="e487a-286">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="e487a-287">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="e487a-287">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="e487a-288">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="e487a-288">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="e487a-289">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="e487a-289">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="e487a-290">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="e487a-290">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="e487a-291">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="e487a-291">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="e487a-292">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="e487a-292">JetUpdate</span></span>](./jetupdate-function.md)
