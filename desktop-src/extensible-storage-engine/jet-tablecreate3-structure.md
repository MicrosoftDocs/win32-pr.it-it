---
description: 'Altre informazioni su: struttura JET_TABLECREATE3'
title: Struttura JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
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
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305746"
---
# <a name="jet_tablecreate3-structure"></a><span data-ttu-id="da2ea-103">Struttura JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="da2ea-103">JET_TABLECREATE3 Structure</span></span>


<span data-ttu-id="da2ea-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="da2ea-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="da2ea-105">La struttura **JET_TABLECREATE3** contiene le informazioni necessarie per creare una tabella popolata con colonne e indici in un database Extensible Storage Engine (ESE) e che designa una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="da2ea-105">The **JET_TABLECREATE3** structure contains the information that is needed to create a table populated with columns and indexes in an Extensible Storage Engine (ESE) database, and that designates a callback function.</span></span> <span data-ttu-id="da2ea-106">La struttura **JET_TABLECREATE3** viene utilizzata dalla funzione [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) .</span><span class="sxs-lookup"><span data-stu-id="da2ea-106">The **JET_TABLECREATE3** structure is used by the [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) function.</span></span>

<span data-ttu-id="da2ea-107">La struttura **JET_TABLECREATE3** è stata introdotta nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da2ea-107">The **JET_TABLECREATE3** structure was introduced in the Windows 7 operating system.</span></span>

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a><span data-ttu-id="da2ea-108">Membri</span><span class="sxs-lookup"><span data-stu-id="da2ea-108">Members</span></span>

<span data-ttu-id="da2ea-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="da2ea-109">**cbStruct**</span></span>

<span data-ttu-id="da2ea-110">Dimensioni in byte della struttura (per l'espansione futura).</span><span class="sxs-lookup"><span data-stu-id="da2ea-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="da2ea-111">Deve essere impostato su sizeof (JET_TABLECREATE3) in byte.</span><span class="sxs-lookup"><span data-stu-id="da2ea-111">It must be set to sizeof( JET_TABLECREATE3 ) in bytes.</span></span>

<span data-ttu-id="da2ea-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="da2ea-112">**szTableName**</span></span>

<span data-ttu-id="da2ea-113">Nome della tabella da creare.</span><span class="sxs-lookup"><span data-stu-id="da2ea-113">The name of the table to create.</span></span>

<span data-ttu-id="da2ea-114">Il nome deve soddisfare le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="da2ea-114">The name must meet the following conditions:</span></span>

  - <span data-ttu-id="da2ea-115">Deve avere un valore minore di JET_cbNameMost, escluso il valore null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="da2ea-115">It must have a value that is less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="da2ea-116">Deve essere costituito dal set di caratteri seguente: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D.</span><span class="sxs-lookup"><span data-stu-id="da2ea-116">It must consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]); that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="da2ea-117">Non deve iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="da2ea-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="da2ea-118">Deve essere costituito da almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="da2ea-118">It must consist of at least one non-space character.</span></span>

<span data-ttu-id="da2ea-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="da2ea-119">**szTemplateTableName**</span></span>

<span data-ttu-id="da2ea-120">Nome di una tabella esistente da cui ereditare il Data Definition Language di base (DDL).</span><span class="sxs-lookup"><span data-stu-id="da2ea-120">The name of an existing table from which to inherit the base data definition language (DDL).</span></span> <span data-ttu-id="da2ea-121">L'utilizzo di una tabella modello consente la creazione semplificata di molte tabelle con colonne e indici identici.</span><span class="sxs-lookup"><span data-stu-id="da2ea-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="da2ea-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="da2ea-122">**ulPages**</span></span>

<span data-ttu-id="da2ea-123">Numero iniziale di pagine del database da allocare per la tabella.</span><span class="sxs-lookup"><span data-stu-id="da2ea-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="da2ea-124">La specifica di un numero maggiore di uno può ridurre la frammentazione se nella tabella vengono inserite molte righe.</span><span class="sxs-lookup"><span data-stu-id="da2ea-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="da2ea-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="da2ea-125">**ulDensity**</span></span>

<span data-ttu-id="da2ea-126">Densità della tabella, in punti percentuali.</span><span class="sxs-lookup"><span data-stu-id="da2ea-126">The table density, in percentage points.</span></span> <span data-ttu-id="da2ea-127">Il numero deve essere 0 o compreso tra 20 e 100.</span><span class="sxs-lookup"><span data-stu-id="da2ea-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="da2ea-128">Il valore 0 indica che deve essere utilizzato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="da2ea-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="da2ea-129">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="da2ea-129">The default value is 80.</span></span>

<span data-ttu-id="da2ea-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="da2ea-130">**rgcolumncreate**</span></span>

<span data-ttu-id="da2ea-131">Matrice di strutture di [JET_COLUMNCREATE](./jet-columncreate-structure.md) , ciascuna delle quali corrisponde a una colonna da creare nella nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="da2ea-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="da2ea-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="da2ea-132">**cColumns**</span></span>

<span data-ttu-id="da2ea-133">Numero di elementi [JET_COLUMNCREATE](./jet-columncreate-structure.md) nel parametro *rgcolumncreate* .</span><span class="sxs-lookup"><span data-stu-id="da2ea-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in the *rgcolumncreate* parameter.</span></span>

<span data-ttu-id="da2ea-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="da2ea-134">**rgindexcreate**</span></span>

<span data-ttu-id="da2ea-135">Matrice di strutture di [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , ciascuna delle quali corrisponde a un indice da creare nella nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="da2ea-135">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="da2ea-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="da2ea-136">**cIndexes**</span></span>

<span data-ttu-id="da2ea-137">Numero di elementi [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) nel parametro *rgindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="da2ea-137">The number of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) elements in the *rgindexcreate* parameter.</span></span>

<span data-ttu-id="da2ea-138">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="da2ea-138">**szCallback**</span></span>

<span data-ttu-id="da2ea-139">Funzione che viene chiamata durante alcuni eventi.</span><span class="sxs-lookup"><span data-stu-id="da2ea-139">The function that gets called during certain events.</span></span> <span data-ttu-id="da2ea-140">**cbtyp** determina quando verrà chiamata la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="da2ea-140">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="da2ea-141">Il formato di **szCallback** deve essere " \! function module", ad esempio "Alpha \! beta" si riferisce alla funzione beta nel modulo denominato "Alpha".</span><span class="sxs-lookup"><span data-stu-id="da2ea-141">The format of **szCallback** must be "module\!function" — for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span>

<span data-ttu-id="da2ea-142">Il prototipo della funzione deve corrispondere alla funzione di callback [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="da2ea-142">The prototype of the function must match the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span>

<span data-ttu-id="da2ea-143">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="da2ea-143">**cbtyp**</span></span>

<span data-ttu-id="da2ea-144">Descrive il tipo di funzione di callback designato da **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="da2ea-144">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="da2ea-145">Per ulteriori informazioni, vedere [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="da2ea-145">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span>

<span data-ttu-id="da2ea-146">Questo bit è costituito da uno o più valori di bit elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="da2ea-146">This bitfield is composed of one or more of the bit values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da2ea-147">Valore</span><span class="sxs-lookup"><span data-stu-id="da2ea-147">Value</span></span></p></th>
<th><p><span data-ttu-id="da2ea-148">Significato</span><span class="sxs-lookup"><span data-stu-id="da2ea-148">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-149">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="da2ea-149">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="da2ea-150">La funzione di callback verrà chiamata quando una colonna che può essere finalizzata è scesa a zero.</span><span class="sxs-lookup"><span data-stu-id="da2ea-150">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-151">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="da2ea-151">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="da2ea-152">La funzione di callback verrà chiamata prima dell'inserimento del record.</span><span class="sxs-lookup"><span data-stu-id="da2ea-152">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-153">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="da2ea-153">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="da2ea-154">La funzione di callback verrà chiamata dopo che il motore di database ha completato l'inserimento di un record.</span><span class="sxs-lookup"><span data-stu-id="da2ea-154">The callback function will be called after the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-155">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="da2ea-155">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="da2ea-156">La funzione di callback verrà chiamata prima della modifica di un record.</span><span class="sxs-lookup"><span data-stu-id="da2ea-156">The callback function will be called prior to the modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-157">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="da2ea-157">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="da2ea-158">La funzione di callback verrà chiamata dopo aver completato la modifica di un record.</span><span class="sxs-lookup"><span data-stu-id="da2ea-158">The callback function will be called after finishing the modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-159">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="da2ea-159">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="da2ea-160">La funzione di callback verrà chiamata prima dell'eliminazione di un record.</span><span class="sxs-lookup"><span data-stu-id="da2ea-160">The callback function will be called prior to the deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-161">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="da2ea-161">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="da2ea-162">La funzione di callback verrà chiamata dopo l'eliminazione di un record.</span><span class="sxs-lookup"><span data-stu-id="da2ea-162">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-163">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="da2ea-163">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="da2ea-164">La funzione di callback verrà chiamata per calcolare un valore predefinito definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="da2ea-164">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-165">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="da2ea-165">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="da2ea-166">La funzione di callback verrà chiamata quando è necessario liberare l'archivio locale associato a un cursore.</span><span class="sxs-lookup"><span data-stu-id="da2ea-166">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-167">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="da2ea-167">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="da2ea-168">La funzione di callback verrà chiamata quando l'archiviazione locale associata a una tabella deve essere liberata.</span><span class="sxs-lookup"><span data-stu-id="da2ea-168">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="da2ea-169">**grbit**</span><span class="sxs-lookup"><span data-stu-id="da2ea-169">**grbit**</span></span>

<span data-ttu-id="da2ea-170">Gruppo di bit che contiene zero o più valori dell'opzione di chiamata elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="da2ea-170">A group of bits that contains zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da2ea-171">Valore</span><span class="sxs-lookup"><span data-stu-id="da2ea-171">Value</span></span></p></th>
<th><p><span data-ttu-id="da2ea-172">Significato</span><span class="sxs-lookup"><span data-stu-id="da2ea-172">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-173">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="da2ea-173">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="da2ea-174">Impedisce operazioni DDL sulla tabella, ad esempio l'aggiunta o la rimozione di colonne.</span><span class="sxs-lookup"><span data-stu-id="da2ea-174">Prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-175">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="da2ea-175">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="da2ea-176">Fa in modo che la tabella sia una tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="da2ea-176">Causes the table to be a template table.</span></span> <span data-ttu-id="da2ea-177">Le nuove tabelle possono quindi specificare il nome della tabella come tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="da2ea-177">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="da2ea-178">L'impostazione JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="da2ea-178">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="da2ea-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="da2ea-180">Deve essere utilizzato insieme a JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="da2ea-180">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="da2ea-181">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="da2ea-181">Deprecated.</span></span> <span data-ttu-id="da2ea-182">Non usare.</span><span class="sxs-lookup"><span data-stu-id="da2ea-182">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="da2ea-183">**pSeqSpacehints**</span><span class="sxs-lookup"><span data-stu-id="da2ea-183">**pSeqSpacehints**</span></span>

<span data-ttu-id="da2ea-184">Puntatore a una struttura [JET_SPACEHINTS](./jet-spacehints-structure.md) per l'indice sequenziale predefinito.</span><span class="sxs-lookup"><span data-stu-id="da2ea-184">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for default sequential index.</span></span>

<span data-ttu-id="da2ea-185">**pSeqSpacehints** è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da2ea-185">**pSeqSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="da2ea-186">**pLVSpacehints**</span><span class="sxs-lookup"><span data-stu-id="da2ea-186">**pLVSpacehints**</span></span>

<span data-ttu-id="da2ea-187">Puntatore a una struttura [JET_SPACEHINTS](./jet-spacehints-structure.md) per un albero di valori Long separato.</span><span class="sxs-lookup"><span data-stu-id="da2ea-187">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for a Separated Long Value tree.</span></span>

<span data-ttu-id="da2ea-188">**pLVSpacehints** è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da2ea-188">**pLVSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="da2ea-189">**cbSeparateLV**</span><span class="sxs-lookup"><span data-stu-id="da2ea-189">**cbSeparateLV**</span></span>

<span data-ttu-id="da2ea-190">Dimensioni per separare un valore LV intrinseco dal record primario.</span><span class="sxs-lookup"><span data-stu-id="da2ea-190">The size to separate an intrinsic LV from the primary record.</span></span> <span data-ttu-id="da2ea-191">Qualsiasi struttura c di valore Long per un albero BT separato.</span><span class="sxs-lookup"><span data-stu-id="da2ea-191">Any long-value c structure for a Separated LV tree.</span></span> <span data-ttu-id="da2ea-192">Per ulteriori informazioni, vedere ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span><span class="sxs-lookup"><span data-stu-id="da2ea-192">For more information, see ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span></span> <span data-ttu-id="da2ea-193">Le colonne con valori di grandi dimensioni minori di questo valore possono essere separate se il record diventa troppo grande.</span><span class="sxs-lookup"><span data-stu-id="da2ea-193">Long-value columns smaller than this value may be separated if the record becomes too large.</span></span>

<span data-ttu-id="da2ea-194">**cbSeparateLV** è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da2ea-194">**cbSeparateLV** was introduced in Windows 7.</span></span>

<span data-ttu-id="da2ea-195">**TableID**</span><span class="sxs-lookup"><span data-stu-id="da2ea-195">**tableid**</span></span>

<span data-ttu-id="da2ea-196">Un campo di output che include il [JET_TABLEID](./jet-tableid.md) della nuova tabella se la chiamata API ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="da2ea-196">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="da2ea-197">Se la chiamata API ha esito negativo, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="da2ea-197">If the API call fails, the value is undefined.</span></span> <span data-ttu-id="da2ea-198">Questa tabella viene aperta in modo esclusivo.</span><span class="sxs-lookup"><span data-stu-id="da2ea-198">This table is opened exclusively.</span></span>

<span data-ttu-id="da2ea-199">**Creata**</span><span class="sxs-lookup"><span data-stu-id="da2ea-199">**cCreated**</span></span>

<span data-ttu-id="da2ea-200">Un campo di output che contiene il numero di oggetti creati se la chiamata API ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="da2ea-200">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="da2ea-201">Se la chiamata API ha esito negativo, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="da2ea-201">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="da2ea-202">Il numero di oggetti creati è uguale alla somma di colonne, tabelle e indici creati correttamente.</span><span class="sxs-lookup"><span data-stu-id="da2ea-202">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="da2ea-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da2ea-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="da2ea-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="da2ea-205">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="da2ea-205">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="da2ea-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="da2ea-207">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="da2ea-207">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da2ea-208"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="da2ea-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="da2ea-209">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="da2ea-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da2ea-210"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="da2ea-210"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="da2ea-211">Implementato come <strong>JET_TABLECREATE3_W</strong> (Unicode) e <strong>JET_TABLECREATE3_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="da2ea-211">Implemented as <strong>JET_TABLECREATE3_W</strong> (Unicode) and <strong>JET_TABLECREATE3_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="da2ea-212">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da2ea-212">See also</span></span>

[<span data-ttu-id="da2ea-213">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="da2ea-213">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="da2ea-214">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="da2ea-214">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="da2ea-215">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="da2ea-215">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="da2ea-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="da2ea-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="da2ea-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="da2ea-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="da2ea-218">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="da2ea-218">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="da2ea-219">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="da2ea-219">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="da2ea-220">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="da2ea-220">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="da2ea-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="da2ea-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="da2ea-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="da2ea-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="da2ea-223">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="da2ea-223">JetDefragment2</span></span>](./jetdefragment2-function.md)
