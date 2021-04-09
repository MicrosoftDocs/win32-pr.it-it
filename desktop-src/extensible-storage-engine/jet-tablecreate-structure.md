---
description: 'Altre informazioni su: struttura JET_TABLECREATE'
title: Struttura JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128183"
---
# <a name="jet_tablecreate-structure"></a><span data-ttu-id="26c01-103">Struttura JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="26c01-103">JET_TABLECREATE Structure</span></span>


<span data-ttu-id="26c01-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="26c01-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate-structure"></a><span data-ttu-id="26c01-105">Struttura JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="26c01-105">JET_TABLECREATE Structure</span></span>

<span data-ttu-id="26c01-106">La struttura **JET_TABLECREATE** contiene le informazioni necessarie per creare una tabella popolata con colonne e indici in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="26c01-106">The **JET_TABLECREATE** structure contains the information that is necessary to create a table populated with columns and indexes in an ESE database.</span></span> <span data-ttu-id="26c01-107">La struttura **JET_TABLECREATE** viene utilizzata da [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span><span class="sxs-lookup"><span data-stu-id="26c01-107">The **JET_TABLECREATE** structure is used by [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span></span>

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a><span data-ttu-id="26c01-108">Membri</span><span class="sxs-lookup"><span data-stu-id="26c01-108">Members</span></span>

<span data-ttu-id="26c01-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="26c01-109">**cbStruct**</span></span>

<span data-ttu-id="26c01-110">Dimensioni in byte della struttura (per l'espansione futura).</span><span class="sxs-lookup"><span data-stu-id="26c01-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="26c01-111">Deve essere impostato su sizeof (JET_TABLECREATE) in byte.</span><span class="sxs-lookup"><span data-stu-id="26c01-111">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="26c01-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="26c01-112">**szTableName**</span></span>

<span data-ttu-id="26c01-113">Nome della tabella da creare.</span><span class="sxs-lookup"><span data-stu-id="26c01-113">The name of the table to create.</span></span>

<span data-ttu-id="26c01-114">Il nome deve essere utilizzato per soddisfare le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="26c01-114">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="26c01-115">Hanno un valore minore di JET_cbNameMost, escluso il valore NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="26c01-115">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="26c01-116">Sono costituiti dal set di caratteri seguente: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="26c01-116">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="26c01-117">Non iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="26c01-117">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="26c01-118">Sono costituiti da almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="26c01-118">Consist of at least one non-space character.</span></span>

<span data-ttu-id="26c01-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="26c01-119">**szTemplateTableName**</span></span>

<span data-ttu-id="26c01-120">Nome di una tabella già esistente da cui ereditare DDL di base (Data Definition Language).</span><span class="sxs-lookup"><span data-stu-id="26c01-120">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="26c01-121">L'utilizzo di una tabella modello consente la creazione semplificata di molte tabelle con colonne e indici identici.</span><span class="sxs-lookup"><span data-stu-id="26c01-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="26c01-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="26c01-122">**ulPages**</span></span>

<span data-ttu-id="26c01-123">Numero iniziale di pagine del database da allocare per la tabella.</span><span class="sxs-lookup"><span data-stu-id="26c01-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="26c01-124">La specifica di un numero maggiore di uno può ridurre la frammentazione se nella tabella vengono inserite molte righe.</span><span class="sxs-lookup"><span data-stu-id="26c01-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="26c01-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="26c01-125">**ulDensity**</span></span>

<span data-ttu-id="26c01-126">Densità della tabella, in punti percentuali.</span><span class="sxs-lookup"><span data-stu-id="26c01-126">The table density, in percentage points.</span></span> <span data-ttu-id="26c01-127">Il numero deve essere 0 o compreso tra 20 e 100.</span><span class="sxs-lookup"><span data-stu-id="26c01-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="26c01-128">Il valore 0 indica che deve essere utilizzato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="26c01-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="26c01-129">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="26c01-129">The default is 80.</span></span>

<span data-ttu-id="26c01-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="26c01-130">**rgcolumncreate**</span></span>

<span data-ttu-id="26c01-131">Matrice di strutture di [JET_COLUMNCREATE](./jet-columncreate-structure.md) , ciascuna delle quali corrisponde a una colonna da creare nella nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="26c01-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="26c01-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="26c01-132">**cColumns**</span></span>

<span data-ttu-id="26c01-133">Numero di elementi [JET_COLUMNCREATE](./jet-columncreate-structure.md) in **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="26c01-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="26c01-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="26c01-134">**rgindexcreate**</span></span>

<span data-ttu-id="26c01-135">Matrice di strutture di [JET_INDEXCREATE](./jet-indexcreate-structure.md) , ciascuna delle quali corrisponde a un indice da creare nella nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="26c01-135">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="26c01-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="26c01-136">**cIndexes**</span></span>

<span data-ttu-id="26c01-137">Numero di elementi [JET_INDEXCREATE](./jet-indexcreate-structure.md) in **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="26c01-137">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="26c01-138">**grbit**</span><span class="sxs-lookup"><span data-stu-id="26c01-138">**grbit**</span></span>

<span data-ttu-id="26c01-139">Gruppo di bit che contiene le opzioni per la chiamata, che includono zero o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="26c01-139">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26c01-140">Valore</span><span class="sxs-lookup"><span data-stu-id="26c01-140">Value</span></span></p></th>
<th><p><span data-ttu-id="26c01-141">Significato</span><span class="sxs-lookup"><span data-stu-id="26c01-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26c01-142">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="26c01-142">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="26c01-143">L'impostazione di JET_bitTableCreateFixedDDL impedisce operazioni DDL nella tabella, ad esempio l'aggiunta o la rimozione di colonne.</span><span class="sxs-lookup"><span data-stu-id="26c01-143">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26c01-144">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="26c01-144">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="26c01-145">Impostando JET_bitTableCreateTemplateTable la tabella è una tabella modello.</span><span class="sxs-lookup"><span data-stu-id="26c01-145">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="26c01-146">Le nuove tabelle possono quindi specificare il nome della tabella come tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="26c01-146">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="26c01-147">L'impostazione JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="26c01-147">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26c01-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="26c01-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="26c01-149">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="26c01-149">Deprecated.</span></span> <span data-ttu-id="26c01-150">Non usare.</span><span class="sxs-lookup"><span data-stu-id="26c01-150">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26c01-151">**TableID**</span><span class="sxs-lookup"><span data-stu-id="26c01-151">**tableid**</span></span>

<span data-ttu-id="26c01-152">Un campo di output che include il [JET_TABLEID](./jet-tableid.md) della nuova tabella se la chiamata API ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="26c01-152">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="26c01-153">Se la chiamata API ha esito negativo, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="26c01-153">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="26c01-154">**Creata**</span><span class="sxs-lookup"><span data-stu-id="26c01-154">**cCreated**</span></span>

<span data-ttu-id="26c01-155">Un campo di output che contiene il numero di oggetti creati se la chiamata API ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="26c01-155">An output field that contains the count of objects created if the API call succeeds.</span></span> <span data-ttu-id="26c01-156">Se la chiamata API ha esito negativo, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="26c01-156">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="26c01-157">Il numero di oggetti creati è uguale alla somma di colonne, tabelle e indici creati correttamente.</span><span class="sxs-lookup"><span data-stu-id="26c01-157">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="26c01-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26c01-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26c01-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="26c01-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="26c01-160">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="26c01-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26c01-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="26c01-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="26c01-162">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="26c01-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26c01-163"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="26c01-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="26c01-164">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="26c01-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26c01-165"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="26c01-165"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="26c01-166">Implementato come <strong>JET_TABLECREATE_W</strong> (Unicode) e <strong>JET_TABLECREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="26c01-166">Implemented as <strong>JET_TABLECREATE_W</strong> (Unicode) and <strong>JET_TABLECREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="26c01-167">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="26c01-167">See Also</span></span>

[<span data-ttu-id="26c01-168">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="26c01-168">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="26c01-169">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="26c01-169">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="26c01-170">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="26c01-170">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="26c01-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="26c01-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="26c01-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="26c01-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="26c01-173">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="26c01-173">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="26c01-174">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="26c01-174">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="26c01-175">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="26c01-175">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="26c01-176">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="26c01-176">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="26c01-177">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="26c01-177">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
