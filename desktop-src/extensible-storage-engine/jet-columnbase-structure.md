---
description: 'Altre informazioni su: struttura JET_COLUMNBASE'
title: Struttura JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319210"
---
# <a name="jet_columnbase-structure"></a><span data-ttu-id="03e75-103">Struttura JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="03e75-103">JET_COLUMNBASE Structure</span></span>


<span data-ttu-id="03e75-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="03e75-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnbase-structure"></a><span data-ttu-id="03e75-105">Struttura JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="03e75-105">JET_COLUMNBASE Structure</span></span>

<span data-ttu-id="03e75-106">La struttura **JET_COLUMNBASE** descrive i parametri di una colonna di base.</span><span class="sxs-lookup"><span data-stu-id="03e75-106">The **JET_COLUMNBASE** structure describes the parameters of a base column.</span></span> <span data-ttu-id="03e75-107">Le funzioni [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usano la struttura **JET_COLUMNBASE** .</span><span class="sxs-lookup"><span data-stu-id="03e75-107">The [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions use the **JET_COLUMNBASE** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a><span data-ttu-id="03e75-108">Membri</span><span class="sxs-lookup"><span data-stu-id="03e75-108">Members</span></span>

<span data-ttu-id="03e75-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="03e75-109">**cbStruct**</span></span>

<span data-ttu-id="03e75-110">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="03e75-110">The size of this structure, in bytes.</span></span> <span data-ttu-id="03e75-111">Impostare **cbStruct** su sizeof (JET_COLUMNBASE).</span><span class="sxs-lookup"><span data-stu-id="03e75-111">Set **cbStruct** to sizeof( JET_COLUMNBASE ).</span></span>

<span data-ttu-id="03e75-112">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="03e75-112">**columnid**</span></span>

<span data-ttu-id="03e75-113">Riservato.</span><span class="sxs-lookup"><span data-stu-id="03e75-113">Reserved.</span></span> <span data-ttu-id="03e75-114">Impostare **ColumnID** su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03e75-114">Set **columnid** to 0 (zero).</span></span>

<span data-ttu-id="03e75-115">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="03e75-115">**coltyp**</span></span>

<span data-ttu-id="03e75-116">Tipo di colonna (ad esempio, testo, binario o numerico).</span><span class="sxs-lookup"><span data-stu-id="03e75-116">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="03e75-117">Per ulteriori informazioni, vedere [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="03e75-117">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="03e75-118">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="03e75-118">**wCountry**</span></span>

<span data-ttu-id="03e75-119">Riservato.</span><span class="sxs-lookup"><span data-stu-id="03e75-119">Reserved.</span></span> <span data-ttu-id="03e75-120">Impostare su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03e75-120">Set to 0 (zero).</span></span>

<span data-ttu-id="03e75-121">**langid**</span><span class="sxs-lookup"><span data-stu-id="03e75-121">**langid**</span></span>

<span data-ttu-id="03e75-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="03e75-122">Reserved.</span></span> <span data-ttu-id="03e75-123">Impostare su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03e75-123">Set to 0 (zero).</span></span>

<span data-ttu-id="03e75-124">**cp**</span><span class="sxs-lookup"><span data-stu-id="03e75-124">**cp**</span></span>

<span data-ttu-id="03e75-125">Tabella codici per la colonna.</span><span class="sxs-lookup"><span data-stu-id="03e75-125">The code page for the column.</span></span> <span data-ttu-id="03e75-126">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="03e75-126">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="03e75-127">Il valore zero indica che verrà utilizzato il valore predefinito (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="03e75-127">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="03e75-128">Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.</span><span class="sxs-lookup"><span data-stu-id="03e75-128">If the column is not a text column, the code page is automatically set to zero.</span></span>

<span data-ttu-id="03e75-129">**wFiller**</span><span class="sxs-lookup"><span data-stu-id="03e75-129">**wFiller**</span></span>

<span data-ttu-id="03e75-130">Riservato.</span><span class="sxs-lookup"><span data-stu-id="03e75-130">Reserved.</span></span> <span data-ttu-id="03e75-131">Impostare su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03e75-131">Set to 0 (zero).</span></span>

<span data-ttu-id="03e75-132">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="03e75-132">**cbMax**</span></span>

<span data-ttu-id="03e75-133">Lunghezza massima, in byte, di una colonna a lunghezza variabile o lunghezza effettiva, in byte, di una colonna a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="03e75-133">The maximum length, in bytes, of a variable-length column, or the actual length, in bytes, of a fixed-length column.</span></span>

<span data-ttu-id="03e75-134">**grbit**</span><span class="sxs-lookup"><span data-stu-id="03e75-134">**grbit**</span></span>

<span data-ttu-id="03e75-135">Opzioni per la colonna, inclusi zero o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="03e75-135">Options for the column, including zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03e75-136">Valore</span><span class="sxs-lookup"><span data-stu-id="03e75-136">Value</span></span></p></th>
<th><p><span data-ttu-id="03e75-137">Significato</span><span class="sxs-lookup"><span data-stu-id="03e75-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03e75-138">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="03e75-138">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="03e75-139">La colonna è fissa e occupa la stessa quantità di spazio in una riga indipendentemente dalla quantità di dati in essa contenuti.</span><span class="sxs-lookup"><span data-stu-id="03e75-139">The column is fixed and occupies the same amount of space in a row regardless of how much data it contains.</span></span> <span data-ttu-id="03e75-140">JET_bitColumnFixed non possono essere combinati con JET_bitColumnTagged e non possono essere usati quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLongText</strong> o <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="03e75-140">JET_bitColumnFixed cannot be combined with JET_bitColumnTagged, and cannot be used when the <strong>coltyp</strong> member is set to <strong>JET_coltypLongText</strong> or <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-141">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="03e75-141">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="03e75-142">La colonna è contrassegnata e occupa lo spazio nel database solo se contiene dati.</span><span class="sxs-lookup"><span data-stu-id="03e75-142">The column is tagged and occupies space in the database only if it contains data.</span></span> <span data-ttu-id="03e75-143">Non è possibile combinare JET_bitColumnTagged con JET_bitColumnFixed, JET_bitColumnVersion o JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="03e75-143">JET_bitColumnTagged cannot be combined with JET_bitColumnFixed, JET_bitColumnVersion, or JET_bitColumnEscrowUpdate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-144">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="03e75-144">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="03e75-145">La colonna non deve essere impostata su un valore <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="03e75-145">The column must not be set to a <strong>NULL</strong> value.</span></span></p>
<p><span data-ttu-id="03e75-146">Non è possibile combinare JET_bitColumnNotNULL con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="03e75-146">JET_bitColumnNotNULL cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-147">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="03e75-147">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="03e75-148">La colonna è una colonna della versione che specifica la versione della riga.</span><span class="sxs-lookup"><span data-stu-id="03e75-148">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="03e75-149">Il valore di questa colonna inizia da zero e viene incrementato automaticamente per ogni aggiornamento della riga.</span><span class="sxs-lookup"><span data-stu-id="03e75-149">The value of this column starts at zero and is automatically incremented for each update of the row.</span></span></p>
<p><span data-ttu-id="03e75-150">JET_bitColumnVersion può essere utilizzato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong> e non può essere combinato con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged o JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="03e75-150">JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> and cannot be combined with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged, or JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-151">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="03e75-151">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="03e75-152">La colonna viene incrementata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="03e75-152">The column is automatically incremented.</span></span> <span data-ttu-id="03e75-153">Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella.</span><span class="sxs-lookup"><span data-stu-id="03e75-153">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="03e75-154">I numeri, tuttavia, non possono essere sequenziali.</span><span class="sxs-lookup"><span data-stu-id="03e75-154">The numbers, however, may not be sequential.</span></span> <span data-ttu-id="03e75-155">Se, ad esempio, vengono inserite cinque righe in una tabella, la colonna incrementata automaticamente potrebbe contenere i valori {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="03e75-155">For example, if five rows are inserted into a table, the automatically incremented column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="03e75-156">JET_bitColumnAutoincrement può essere utilizzato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong> e non può essere combinato con JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault o JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="03e75-156">JET_bitColumnAutoincrement can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong> and cannot be combined with JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault, or JET_bitColumnVersion.</span></span></p>
<p><span data-ttu-id="03e75-157"><strong>Windows 2000:  </strong> JET_bitColumnVersion può essere utilizzato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="03e75-157"><strong>Windows 2000:  </strong>JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-158">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="03e75-158">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="03e75-159">Valido solo per le chiamate a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="03e75-159">Valid only for calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span> <span data-ttu-id="03e75-160">Non è possibile combinare JET_bitColumnUpdatable con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="03e75-160">JET_bitColumnUpdatable cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-161">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="03e75-161">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="03e75-162">Valido solo per le chiamate a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="03e75-162">Valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-163">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="03e75-163">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="03e75-164">Valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="03e75-164">Valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-165">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="03e75-165">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="03e75-166">La colonna può essere multivalore.</span><span class="sxs-lookup"><span data-stu-id="03e75-166">The column can be multi-valued.</span></span> <span data-ttu-id="03e75-167">Una colonna multivalore può avere zero, uno o più valori associati.</span><span class="sxs-lookup"><span data-stu-id="03e75-167">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="03e75-168">I vari valori in una colonna multivalore sono identificati da un numero nel membro <strong>itagSequence</strong> di varie strutture, ad esempio <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="03e75-168">The various values in a multi-valued column are identified by a number in the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="03e75-169">Le colonne multivalore devono essere contrassegnate come colonne; ovvero, non possono essere colonne a lunghezza fissa o a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="03e75-169">Multi-valued columns must be tagged columns; that is, they may not be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-170">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="03e75-170">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="03e75-171">Specifica che una colonna è una colonna di aggiornamento del deposito che può essere aggiornata simultaneamente da sessioni diverse con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e che avrà coerenza transazionale.</span><span class="sxs-lookup"><span data-stu-id="03e75-171">Specifies that a column is an escrow update column that can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will have transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="03e75-172">Una colonna di aggiornamento del deposito è possibile creare solo se la tabella è vuota.</span><span class="sxs-lookup"><span data-stu-id="03e75-172">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="03e75-173">Per una colonna di aggiornamento del deposito, il membro <strong>coltyp</strong> deve essere impostato su <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="03e75-173">For an escrow update column, the <strong>coltyp</strong> member must be set to <strong>JET_coltypLong.</strong></span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="03e75-174">Una colonna di aggiornamento del deposito deve avere un valore predefinito, ovvero <strong>cbDefault</strong> deve essere un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="03e75-174">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="03e75-175">Non è possibile combinare JET_bitColumnEscrowUpdate con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="03e75-175">JET_bitColumnEscrowUpdate cannot be combined with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-176">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="03e75-176">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="03e75-177">La colonna viene creata senza un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="03e75-177">The column is created without a version number.</span></span> <span data-ttu-id="03e75-178">Ciò significa che altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="03e75-178">This means that other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="03e75-179">JET_bitColumnUnversioned viene utilizzata solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="03e75-179">JET_bitColumnUnversioned is used only with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="03e75-180">Non può essere utilizzato all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="03e75-180">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-181">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="03e75-181">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="03e75-182">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="03e75-182">Reserved for future use.</span></span></p>
<p><span data-ttu-id="03e75-183">Non è possibile combinare JET_bitColumnMaybeNull con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="03e75-183">JET_bitColumnMaybeNull cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-184">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="03e75-184">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="03e75-185">Non usare.</span><span class="sxs-lookup"><span data-stu-id="03e75-185">Do not use.</span></span> <span data-ttu-id="03e75-186">In alternativa, usare JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="03e75-186">Use JET_bitColumnDeleteOnZero instead.</span></span></p>
<p><span data-ttu-id="03e75-187">La colonna può essere finalizzata.</span><span class="sxs-lookup"><span data-stu-id="03e75-187">The column can be finalized.</span></span> <span data-ttu-id="03e75-188">Una colonna che può essere finalizzata è una colonna di aggiornamento del deposito che causa l'eliminazione della riga quando la colonna raggiunge lo zero.</span><span class="sxs-lookup"><span data-stu-id="03e75-188">A column that can be finalized is an escrow update column that causes the row to be deleted when the column reaches zero.</span></span> <span data-ttu-id="03e75-189">Le versioni future possono invece richiamare una funzione di callback (vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="03e75-189">Future versions may invoke a callback function instead (See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="03e75-190">Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="03e75-190">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="03e75-191">Non è possibile combinare JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="03e75-191">JET_bitColumnFinalize cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-192">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="03e75-192">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="03e75-193">Il valore predefinito per una colonna verrà fornito da una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="03e75-193">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="03e75-194">Vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="03e75-194">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="03e75-195">Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag.</span><span class="sxs-lookup"><span data-stu-id="03e75-195">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="03e75-196">Se JET_bitColumnUserDefinedDefault è specificato, <strong>pvDefault</strong> deve puntare a una struttura di <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof (JET_USERDEFINEDDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="03e75-196">If JET_bitColumnUserDefinedDefault is specified, the <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></p>
<p><span data-ttu-id="03e75-197">Non è possibile combinare JET_bitColumnUserDefinedDefault con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="03e75-197">JET_bitColumnUserDefinedDefault cannot be combined with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-198">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="03e75-198">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="03e75-199">La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="03e75-199">The column is an escrow update column and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="03e75-200">Un uso comune per le colonne Delete-on-zero è come campi del conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="03e75-200">A common use for delete-on-zero columns is as reference count fields.</span></span> <span data-ttu-id="03e75-201">Quando il numero di riferimenti è pari a zero, il record viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="03e75-201">When the number of references fall to zero, the record is deleted.</span></span> <span data-ttu-id="03e75-202">Una colonna Delete-on-zero deve essere una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="03e75-202">A delete-on-zero column must be an escrow update column.</span></span></p>
<p><span data-ttu-id="03e75-203">JET_bitColumnDeleteOnZero sostituisce JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="03e75-203">JET_bitColumnDeleteOnZero replaces JET_bitColumnFinalize.</span></span></p>
<p><span data-ttu-id="03e75-204">Non è possibile combinare JET_bitColumnDeleteOnZero con JET_bitColumnFinalize o JET_bitColumnUserDefinedDefault né usare le colonne predefinite definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="03e75-204">JET_bitColumnDeleteOnZero cannot be combined with JET_bitColumnFinalize or JET_bitColumnUserDefinedDefault, and cannot be used with user-defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03e75-205">**szBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="03e75-205">**szBaseTableName**</span></span>

<span data-ttu-id="03e75-206">Tabella da cui la tabella corrente eredita la DDL.</span><span class="sxs-lookup"><span data-stu-id="03e75-206">The table from which the current table inherits its DDL.</span></span>

<span data-ttu-id="03e75-207">**szBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="03e75-207">**szBaseColumnName**</span></span>

<span data-ttu-id="03e75-208">Nome della colonna nella tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="03e75-208">The name of the column in the template table.</span></span>

### <a name="remarks"></a><span data-ttu-id="03e75-209">Commenti</span><span class="sxs-lookup"><span data-stu-id="03e75-209">Remarks</span></span>

<span data-ttu-id="03e75-210">**JET_COLUMNBASE** contiene gran parte delle stesse informazioni [JET_COLUMNDEF](./jet-columndef-structure.md), ma aggiunge campi stringa per descrivere la tabella di base (se è stata usata una DDL gerarchica).</span><span class="sxs-lookup"><span data-stu-id="03e75-210">**JET_COLUMNBASE** contains much of the same information as [JET_COLUMNDEF](./jet-columndef-structure.md), but it adds string fields to describe the base table (if a hierarchical DDL was used).</span></span>

### <a name="requirements"></a><span data-ttu-id="03e75-211">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03e75-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03e75-212"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="03e75-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="03e75-213">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="03e75-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="03e75-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="03e75-215">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="03e75-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e75-216"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="03e75-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="03e75-217">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="03e75-217">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e75-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="03e75-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="03e75-219">Implementato come <strong>JET_COLUMNBASE_W</strong> (Unicode) e <strong>JET_COLUMNBASE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="03e75-219">Implemented as <strong>JET_COLUMNBASE_W</strong> (Unicode) and <strong>JET_COLUMNBASE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="03e75-220">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03e75-220">See Also</span></span>

[<span data-ttu-id="03e75-221">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="03e75-221">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="03e75-222">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="03e75-222">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="03e75-223">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="03e75-223">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="03e75-224">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="03e75-224">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="03e75-225">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="03e75-225">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="03e75-226">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="03e75-226">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="03e75-227">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="03e75-227">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="03e75-228">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="03e75-228">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="03e75-229">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="03e75-229">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="03e75-230">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="03e75-230">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="03e75-231">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="03e75-231">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
