---
description: 'Altre informazioni su: struttura JET_TABLECREATE2'
title: Struttura JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885781"
---
# <a name="jet_tablecreate2-structure"></a><span data-ttu-id="c5d32-103">Struttura JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="c5d32-103">JET_TABLECREATE2 Structure</span></span>


<span data-ttu-id="c5d32-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c5d32-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate2-structure"></a><span data-ttu-id="c5d32-105">Struttura JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="c5d32-105">JET_TABLECREATE2 Structure</span></span>

<span data-ttu-id="c5d32-106">La struttura **JET_TABLECREATE2** contiene le informazioni necessarie per creare una tabella popolata con colonne e indici in un database ESE e che designa una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="c5d32-106">The **JET_TABLECREATE2** structure contains the information that is needed to create a table populated with columns and indexes in an ESE database, and that designates a callback function.</span></span> <span data-ttu-id="c5d32-107">La struttura **JET_TABLECREATE2** viene utilizzata da [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5d32-107">The **JET_TABLECREATE2** structure is used by [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span>

<span data-ttu-id="c5d32-108">**Windows XP:** La struttura **JET_TABLECREATE2** è stata introdotta in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5d32-108">**Windows XP:** The **JET_TABLECREATE2** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a><span data-ttu-id="c5d32-109">Membri</span><span class="sxs-lookup"><span data-stu-id="c5d32-109">Members</span></span>

<span data-ttu-id="c5d32-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="c5d32-110">**cbStruct**</span></span>

<span data-ttu-id="c5d32-111">Dimensioni in byte della struttura (per l'espansione futura).</span><span class="sxs-lookup"><span data-stu-id="c5d32-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="c5d32-112">Deve essere impostato su sizeof (JET_TABLECREATE2) in byte.</span><span class="sxs-lookup"><span data-stu-id="c5d32-112">It must be set to sizeof( JET_TABLECREATE2 ) in bytes.</span></span>

<span data-ttu-id="c5d32-113">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="c5d32-113">**szTableName**</span></span>

<span data-ttu-id="c5d32-114">Nome della tabella da creare.</span><span class="sxs-lookup"><span data-stu-id="c5d32-114">The name of table to create.</span></span>

<span data-ttu-id="c5d32-115">Il nome deve essere utilizzato per soddisfare le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5d32-115">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="c5d32-116">Hanno un valore minore di JET_cbNameMost, escluso il valore NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c5d32-116">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5d32-117">Sono costituiti dal set di caratteri seguente: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="c5d32-117">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5d32-118">Non iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="c5d32-118">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5d32-119">Sono costituiti da almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="c5d32-119">Consist of at least one non-space character.</span></span>

<span data-ttu-id="c5d32-120">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="c5d32-120">**szTemplateTableName**</span></span>

<span data-ttu-id="c5d32-121">Nome di una tabella già esistente da cui ereditare DDL di base (Data Definition Language).</span><span class="sxs-lookup"><span data-stu-id="c5d32-121">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="c5d32-122">L'utilizzo di una tabella modello consente la creazione semplificata di molte tabelle con colonne e indici identici.</span><span class="sxs-lookup"><span data-stu-id="c5d32-122">Using a template table allows easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="c5d32-123">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="c5d32-123">**ulPages**</span></span>

<span data-ttu-id="c5d32-124">Numero iniziale di pagine del database da allocare per la tabella.</span><span class="sxs-lookup"><span data-stu-id="c5d32-124">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="c5d32-125">La specifica di un numero maggiore di uno può ridurre la frammentazione se nella tabella vengono inserite molte righe.</span><span class="sxs-lookup"><span data-stu-id="c5d32-125">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="c5d32-126">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="c5d32-126">**ulDensity**</span></span>

<span data-ttu-id="c5d32-127">Densità della tabella, in punti percentuali.</span><span class="sxs-lookup"><span data-stu-id="c5d32-127">The table density, in percentage points.</span></span> <span data-ttu-id="c5d32-128">Il numero deve essere 0 o compreso tra 20 e 100.</span><span class="sxs-lookup"><span data-stu-id="c5d32-128">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="c5d32-129">Il valore 0 indica che deve essere utilizzato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c5d32-129">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="c5d32-130">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="c5d32-130">The default is 80.</span></span>

<span data-ttu-id="c5d32-131">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="c5d32-131">**rgcolumncreate**</span></span>

<span data-ttu-id="c5d32-132">Matrice di strutture di [JET_COLUMNCREATE](./jet-columncreate-structure.md) , ciascuna delle quali corrisponde a una colonna da creare nella nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="c5d32-132">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="c5d32-133">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="c5d32-133">**cColumns**</span></span>

<span data-ttu-id="c5d32-134">numero di elementi [JET_COLUMNCREATE](./jet-columncreate-structure.md) in **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="c5d32-134">the number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="c5d32-135">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="c5d32-135">**rgindexcreate**</span></span>

<span data-ttu-id="c5d32-136">Matrice di strutture di [JET_INDEXCREATE](./jet-indexcreate-structure.md) , ciascuna delle quali corrisponde a un indice da creare nella nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="c5d32-136">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="c5d32-137">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="c5d32-137">**cIndexes**</span></span>

<span data-ttu-id="c5d32-138">Numero di elementi [JET_INDEXCREATE](./jet-indexcreate-structure.md) in **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="c5d32-138">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="c5d32-139">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="c5d32-139">**szCallback**</span></span>

<span data-ttu-id="c5d32-140">Funzione che viene chiamata durante alcuni eventi.</span><span class="sxs-lookup"><span data-stu-id="c5d32-140">The function that gets called during certain events.</span></span> <span data-ttu-id="c5d32-141">**cbtyp** determina quando verrà chiamata la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="c5d32-141">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="c5d32-142">Il formato di **szCallback** deve essere " \! function module", ad esempio "Alpha \! beta" si riferisce alla funzione beta nel modulo denominato "Alpha".</span><span class="sxs-lookup"><span data-stu-id="c5d32-142">The format of **szCallback** must be "module\!function"—for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span> <span data-ttu-id="c5d32-143">Il prototipo della funzione deve corrispondere [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5d32-143">The prototype of the function must match [JET_CALLBACK](./jet-callback-callback-function.md).</span></span> <span data-ttu-id="c5d32-144">Per ulteriori informazioni, vedere [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5d32-144">For more information, see [JET_CALLBACK](./jet-callback-callback-function.md).</span></span>

<span data-ttu-id="c5d32-145">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="c5d32-145">**cbtyp**</span></span>

<span data-ttu-id="c5d32-146">Descrive il tipo di funzione di callback designato da **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="c5d32-146">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="c5d32-147">Per ulteriori informazioni, vedere [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="c5d32-147">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span> <span data-ttu-id="c5d32-148">Questo bit è costituito da uno o più dei seguenti bit.</span><span class="sxs-lookup"><span data-stu-id="c5d32-148">This bitfield is composed of one or more of the following bits.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5d32-149">Valore</span><span class="sxs-lookup"><span data-stu-id="c5d32-149">Value</span></span></p></th>
<th><p><span data-ttu-id="c5d32-150">Significato</span><span class="sxs-lookup"><span data-stu-id="c5d32-150">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-151">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="c5d32-151">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="c5d32-152">La funzione di callback verrà chiamata quando una colonna che può essere finalizzata è scesa a zero.</span><span class="sxs-lookup"><span data-stu-id="c5d32-152">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-153">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="c5d32-153">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="c5d32-154">La funzione di callback verrà chiamata prima dell'inserimento del record.</span><span class="sxs-lookup"><span data-stu-id="c5d32-154">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-155">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="c5d32-155">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="c5d32-156">La funzione di callback verrà chiamata al termine dell'inserimento di un record da parte del motore di database.</span><span class="sxs-lookup"><span data-stu-id="c5d32-156">The callback function will be called once the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-157">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="c5d32-157">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="c5d32-158">La funzione di callback verrà chiamata prima della modifica di un record.</span><span class="sxs-lookup"><span data-stu-id="c5d32-158">The callback function will be called prior to modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-159">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="c5d32-159">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="c5d32-160">La funzione di callback verrà chiamata dopo il completamento della modifica di un record.</span><span class="sxs-lookup"><span data-stu-id="c5d32-160">The callback function will be called after finishing modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-161">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="c5d32-161">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="c5d32-162">La funzione di callback verrà chiamata prima dell'eliminazione di un record.</span><span class="sxs-lookup"><span data-stu-id="c5d32-162">The callback function will be called prior to deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-163">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="c5d32-163">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="c5d32-164">La funzione di callback verrà chiamata dopo l'eliminazione di un record.</span><span class="sxs-lookup"><span data-stu-id="c5d32-164">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-165">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="c5d32-165">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="c5d32-166">La funzione di callback verrà chiamata per calcolare un valore predefinito definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c5d32-166">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-167">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="c5d32-167">JET_cbtypOnlineDefragCompleted</span></span></p></td>
<td><p><span data-ttu-id="c5d32-168">La funzione di callback verrà chiamata dopo il completamento di una chiamata a <a href="gg294095(v=exchg.10).md">JetDefragment2</a> .</span><span class="sxs-lookup"><span data-stu-id="c5d32-168">The callback function will be called after a call to <a href="gg294095(v=exchg.10).md">JetDefragment2</a> has completed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-169">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="c5d32-169">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="c5d32-170">La funzione di callback verrà chiamata quando è necessario liberare l'archivio locale associato a un cursore.</span><span class="sxs-lookup"><span data-stu-id="c5d32-170">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-171">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="c5d32-171">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="c5d32-172">La funzione di callback verrà chiamata quando l'archiviazione locale associata a una tabella deve essere liberata.</span><span class="sxs-lookup"><span data-stu-id="c5d32-172">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5d32-173">**grbit**</span><span class="sxs-lookup"><span data-stu-id="c5d32-173">**grbit**</span></span>

<span data-ttu-id="c5d32-174">Gruppo di bit che contiene le opzioni per la chiamata, che includono zero o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5d32-174">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5d32-175">Valore</span><span class="sxs-lookup"><span data-stu-id="c5d32-175">Value</span></span></p></th>
<th><p><span data-ttu-id="c5d32-176">Significato</span><span class="sxs-lookup"><span data-stu-id="c5d32-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-177">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="c5d32-177">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="c5d32-178">L'impostazione di JET_bitTableCreateFixedDDL impedisce operazioni DDL nella tabella, ad esempio l'aggiunta o la rimozione di colonne.</span><span class="sxs-lookup"><span data-stu-id="c5d32-178">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-179">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="c5d32-179">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="c5d32-180">Impostando JET_bitTableCreateTemplateTable la tabella è una tabella modello.</span><span class="sxs-lookup"><span data-stu-id="c5d32-180">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="c5d32-181">Le nuove tabelle possono quindi specificare il nome della tabella come tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="c5d32-181">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="c5d32-182">L'impostazione JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="c5d32-182">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="c5d32-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="c5d32-184">Deve essere utilizzato insieme a JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="c5d32-184">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="c5d32-185">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c5d32-185">Deprecated.</span></span> <span data-ttu-id="c5d32-186">Non usare.</span><span class="sxs-lookup"><span data-stu-id="c5d32-186">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5d32-187">**TableID**</span><span class="sxs-lookup"><span data-stu-id="c5d32-187">**tableid**</span></span>

<span data-ttu-id="c5d32-188">Un campo di output che include il [JET_TABLEID](./jet-tableid.md) della nuova tabella se la chiamata API ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c5d32-188">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="c5d32-189">Se la chiamata API ha esito negativo, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="c5d32-189">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="c5d32-190">**Creata**</span><span class="sxs-lookup"><span data-stu-id="c5d32-190">**cCreated**</span></span>

<span data-ttu-id="c5d32-191">Un campo di output che contiene il numero di oggetti creati se la chiamata API ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c5d32-191">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="c5d32-192">Se la chiamata API ha esito negativo, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="c5d32-192">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="c5d32-193">Il numero di oggetti creati è uguale alla somma di colonne, tabelle e indici creati correttamente.</span><span class="sxs-lookup"><span data-stu-id="c5d32-193">The count of objects that is created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="c5d32-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5d32-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-195"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c5d32-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c5d32-196">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5d32-196">Requires Windows  Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c5d32-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c5d32-198">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c5d32-198">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5d32-199"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c5d32-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c5d32-200">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c5d32-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5d32-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c5d32-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c5d32-202">Implementato come <strong>JET_TABLECREATE2_W</strong> (Unicode) e <strong>JET_TABLECREATE2_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c5d32-202">Implemented as <strong>JET_TABLECREATE2_W</strong> (Unicode) and <strong>JET_TABLECREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c5d32-203">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c5d32-203">See Also</span></span>

[<span data-ttu-id="c5d32-204">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="c5d32-204">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="c5d32-205">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="c5d32-205">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="c5d32-206">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c5d32-206">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="c5d32-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c5d32-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c5d32-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c5d32-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c5d32-209">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="c5d32-209">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="c5d32-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c5d32-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c5d32-211">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="c5d32-211">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="c5d32-212">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="c5d32-212">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="c5d32-213">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="c5d32-213">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="c5d32-214">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="c5d32-214">JetDefragment2</span></span>](./jetdefragment2-function.md)
