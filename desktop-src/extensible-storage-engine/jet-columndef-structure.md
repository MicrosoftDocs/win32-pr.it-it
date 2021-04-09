---
description: 'Altre informazioni su: struttura JET_COLUMNDEF'
title: Struttura JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968621"
---
# <a name="jet_columndef-structure"></a><span data-ttu-id="61da7-103">Struttura JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="61da7-103">JET_COLUMNDEF Structure</span></span>


<span data-ttu-id="61da7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="61da7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columndef-structure"></a><span data-ttu-id="61da7-105">Struttura JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="61da7-105">JET_COLUMNDEF Structure</span></span>

<span data-ttu-id="61da7-106">La struttura **JET_COLUMNDEF** definisce i dati che possono essere archiviati in una colonna.</span><span class="sxs-lookup"><span data-stu-id="61da7-106">The **JET_COLUMNDEF** structure defines the data that can be stored in a column.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a><span data-ttu-id="61da7-107">Membri</span><span class="sxs-lookup"><span data-stu-id="61da7-107">Members</span></span>

<span data-ttu-id="61da7-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="61da7-108">**cbStruct**</span></span>

<span data-ttu-id="61da7-109">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="61da7-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="61da7-110">Deve essere impostato su sizeof (JET_COLUMNDEF).</span><span class="sxs-lookup"><span data-stu-id="61da7-110">It must be set to sizeof( JET_COLUMNDEF).</span></span>

<span data-ttu-id="61da7-111">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="61da7-111">**columnid**</span></span>

<span data-ttu-id="61da7-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="61da7-112">Reserved.</span></span> <span data-ttu-id="61da7-113">**ColumnID** deve essere impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="61da7-113">**columnid** must be set to 0 (zero).</span></span>

<span data-ttu-id="61da7-114">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="61da7-114">**coltyp**</span></span>

<span data-ttu-id="61da7-115">Tipo di colonna (ad esempio, testo, binario o numerico).</span><span class="sxs-lookup"><span data-stu-id="61da7-115">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="61da7-116">Per ulteriori informazioni, vedere [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="61da7-116">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="61da7-117">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="61da7-117">**wCountry**</span></span>

<span data-ttu-id="61da7-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="61da7-118">Reserved.</span></span> <span data-ttu-id="61da7-119">**wCountry** deve essere impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="61da7-119">**wCountry** must be set to 0 (zero).</span></span>

<span data-ttu-id="61da7-120">**langid**</span><span class="sxs-lookup"><span data-stu-id="61da7-120">**langid**</span></span>

<span data-ttu-id="61da7-121">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="61da7-121">Obsolete.</span></span> <span data-ttu-id="61da7-122">**LangID** deve essere impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="61da7-122">**langid** should be set to 0 (zero).</span></span>

<span data-ttu-id="61da7-123">**cp**</span><span class="sxs-lookup"><span data-stu-id="61da7-123">**cp**</span></span>

<span data-ttu-id="61da7-124">Tabella codici per la colonna.</span><span class="sxs-lookup"><span data-stu-id="61da7-124">The code page for the column.</span></span> <span data-ttu-id="61da7-125">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="61da7-125">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="61da7-126">Il valore zero indica che verrà utilizzato il valore predefinito (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="61da7-126">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="61da7-127">Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.</span><span class="sxs-lookup"><span data-stu-id="61da7-127">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="61da7-128">**wCollate**</span><span class="sxs-lookup"><span data-stu-id="61da7-128">**wCollate**</span></span>

<span data-ttu-id="61da7-129">Riservato.</span><span class="sxs-lookup"><span data-stu-id="61da7-129">Reserved.</span></span> <span data-ttu-id="61da7-130">**wCollate** deve essere impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="61da7-130">**wCollate** must be set to 0 (zero).</span></span>

<span data-ttu-id="61da7-131">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="61da7-131">**cbMax**</span></span>

<span data-ttu-id="61da7-132">Lunghezza massima, in byte, di una colonna a lunghezza variabile o lunghezza di una colonna a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="61da7-132">The maximum length, in bytes, of a variable-length column, or the length of a fixed-length column.</span></span>

<span data-ttu-id="61da7-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="61da7-133">**grbit**</span></span>

<span data-ttu-id="61da7-134">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="61da7-134">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61da7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="61da7-135">Value</span></span></p></th>
<th><p><span data-ttu-id="61da7-136">Significato</span><span class="sxs-lookup"><span data-stu-id="61da7-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61da7-137">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="61da7-137">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="61da7-138">La colonna verrà corretta.</span><span class="sxs-lookup"><span data-stu-id="61da7-138">The column will be fixed.</span></span> <span data-ttu-id="61da7-139">Utilizzerà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="61da7-139">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="61da7-140">Non è possibile usare JET_bitColumnFixed con JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="61da7-140">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="61da7-141">Non è possibile usare questo bit con valori Long (ovvero <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="61da7-141">This bit cannot be used with long values (that is <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-142">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="61da7-142">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="61da7-143">La colonna verrà contrassegnata con tag.</span><span class="sxs-lookup"><span data-stu-id="61da7-143">The column will be tagged.</span></span> <span data-ttu-id="61da7-144">Se non contengono dati, le colonne con tag non utilizzano alcuno spazio nel database.</span><span class="sxs-lookup"><span data-stu-id="61da7-144">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="61da7-145">Non è possibile usare questo bit con JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="61da7-145">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-146">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="61da7-146">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="61da7-147">La colonna non deve mai essere impostata su un valore NULL.</span><span class="sxs-lookup"><span data-stu-id="61da7-147">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-148">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="61da7-148">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="61da7-149">La colonna è una colonna della versione che specifica la versione della riga.</span><span class="sxs-lookup"><span data-stu-id="61da7-149">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="61da7-150">Il valore di questa colonna inizia da zero e verrà incrementato automaticamente per ogni aggiornamento nella riga.</span><span class="sxs-lookup"><span data-stu-id="61da7-150">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span></p>
<p><span data-ttu-id="61da7-151">Questo bit può essere applicato solo a colonne <strong>JET_coltypLong</strong> .</span><span class="sxs-lookup"><span data-stu-id="61da7-151">This bit can only be applied to <strong>JET_coltypLong</strong> columns.</span></span> <span data-ttu-id="61da7-152">Non è possibile usare questo bit con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate o JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="61da7-152">This bit cannot be used with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, or JET_bitColumnTagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-153">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="61da7-153">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="61da7-154">La colonna verrà incrementata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="61da7-154">The column will automatically be incremented.</span></span> <span data-ttu-id="61da7-155">Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella.</span><span class="sxs-lookup"><span data-stu-id="61da7-155">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="61da7-156">I numeri, tuttavia, potrebbero non essere continui.</span><span class="sxs-lookup"><span data-stu-id="61da7-156">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="61da7-157">Se, ad esempio, vengono inserite cinque righe in una tabella, la &quot; colonna AutoIncrement &quot; potrebbe contenere i valori {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="61da7-157">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="61da7-158">Questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="61da7-158">This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p>
<p><span data-ttu-id="61da7-159"><strong>Windows 2000:  </strong> In Windows 2000, questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="61da7-159"><strong>Windows 2000:  </strong>In Windows 2000, this bit can only be used on columns of type <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-160">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="61da7-160">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="61da7-161">Questo bit è valido solo per le chiamate a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="61da7-161">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-162">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="61da7-162">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="61da7-163">Questo bit è valido solo per le chiamate a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="61da7-163">This bit is valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-164">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="61da7-164">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="61da7-165">Questo bit è valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="61da7-165">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-166">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="61da7-166">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="61da7-167">La colonna può essere multivalore.</span><span class="sxs-lookup"><span data-stu-id="61da7-167">The column can be multi-valued.</span></span> <span data-ttu-id="61da7-168">Una colonna multivalore può avere zero, uno o più valori associati.</span><span class="sxs-lookup"><span data-stu-id="61da7-168">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="61da7-169">I vari valori in una colonna multivalore sono identificati da un numero denominato membro <strong>itagSequence</strong> , che appartiene a diverse strutture, tra cui: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>e <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="61da7-169">The various values in a multi-valued column are identified by a number called the <strong>itagSequence</strong> member, which belongs to various structures, including: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, and <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="61da7-170">Le colonne multivalore devono essere contrassegnate come colonne; ovvero non possono essere colonne a lunghezza fissa o a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="61da7-170">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-171">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="61da7-171">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="61da7-172">Specifica che una colonna è una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="61da7-172">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="61da7-173">Una colonna di aggiornamento del deposito può essere aggiornata simultaneamente da diverse sessioni con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manterrà la coerenza transazionale.</span><span class="sxs-lookup"><span data-stu-id="61da7-173">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will maintain transactional consistency.</span></span> <span data-ttu-id="61da7-174">Una colonna di aggiornamento del deposito deve soddisfare anche le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="61da7-174">An escrow update column must also meet the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="61da7-175">Una colonna di aggiornamento del deposito è possibile creare solo se la tabella è vuota.</span><span class="sxs-lookup"><span data-stu-id="61da7-175">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="61da7-176">Una colonna di aggiornamento del deposito vincolata deve essere di tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="61da7-176">An escrow update column must be of type <strong>JET_coltypLong</strong>.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="61da7-177">Una colonna di aggiornamento del deposito deve avere un valore predefinito, ovvero <strong>cbDefault</strong> deve essere un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="61da7-177">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="61da7-178">Non è possibile usare JET_bitColumnEscrowUpdate in combinazione con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="61da7-178">JET_bitColumnEscrowUpdate cannot be used in conjunction with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-179">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="61da7-179">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="61da7-180">La colonna verrà creata in un oggetto senza informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="61da7-180">The column will be created in an without version information.</span></span> <span data-ttu-id="61da7-181">Ciò significa che le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="61da7-181">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="61da7-182">Questo bit è utile solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="61da7-182">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="61da7-183">Non può essere utilizzato all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="61da7-183">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-184">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="61da7-184">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="61da7-185">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="61da7-185">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-186">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="61da7-186">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="61da7-187">Utilizzare JET_bitColumnDeleteOnZero anziché JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="61da7-187">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="61da7-188">JET_bitColumnFinalize che una colonna può essere finalizzata.</span><span class="sxs-lookup"><span data-stu-id="61da7-188">JET_bitColumnFinalize that a column can be finalized.</span></span> <span data-ttu-id="61da7-189">Quando una colonna che può essere finalizzata ha una colonna di aggiornamento del deposito che raggiunge lo zero, la riga verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="61da7-189">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="61da7-190">Le versioni future possono richiamare invece una funzione di callback. per ulteriori informazioni, vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="61da7-190">Future versions might invoke a callback function instead (For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="61da7-191">Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="61da7-191">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="61da7-192">Non è possibile usare JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="61da7-192">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-193">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="61da7-193">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="61da7-194">Il valore predefinito per una colonna verrà fornito da una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="61da7-194">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="61da7-195">Vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="61da7-195">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="61da7-196">Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag.</span><span class="sxs-lookup"><span data-stu-id="61da7-196">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="61da7-197">Specificando JET_bitColumnUserDefinedDefault significa che <strong>pvDefault</strong> deve puntare a una struttura di <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span><span class="sxs-lookup"><span data-stu-id="61da7-197">Specifying JET_bitColumnUserDefinedDefault means that <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span></span></p>
<ul>
<li><p><span data-ttu-id="61da7-198">Non è possibile usare JET_bitColumnUserDefinedDefault in combinazione con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="61da7-198">JET_bitColumnUserDefinedDefault cannot be used in conjunction with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-199">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="61da7-199">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="61da7-200">La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="61da7-200">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="61da7-201">Un uso comune per una colonna che può essere finalizzata è usarlo come campo di conteggio dei riferimenti e quando il campo raggiunge lo zero, il record viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="61da7-201">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="61da7-202">JET_bitColumnDeleteOnZero è correlato JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="61da7-202">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="61da7-203">Una colonna Delete-on-zero deve essere una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="61da7-203">A Delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="61da7-204">Non è possibile usare JET_bitColumnDeleteOnZero con JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="61da7-204">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="61da7-205">Impossibile utilizzare JET_bitColumnDeleteOnZero con le colonne predefinite definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="61da7-205">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="61da7-206">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61da7-206">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61da7-207"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="61da7-207"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="61da7-208">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="61da7-208">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61da7-209"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="61da7-209"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="61da7-210">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="61da7-210">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61da7-211"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="61da7-211"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="61da7-212">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="61da7-212">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="61da7-213">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="61da7-213">See Also</span></span>

[<span data-ttu-id="61da7-214">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="61da7-214">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="61da7-215">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="61da7-215">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="61da7-216">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="61da7-216">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="61da7-217">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="61da7-217">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="61da7-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="61da7-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="61da7-219">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="61da7-219">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="61da7-220">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="61da7-220">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="61da7-221">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="61da7-221">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="61da7-222">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="61da7-222">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="61da7-223">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="61da7-223">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="61da7-224">JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="61da7-224">JetOpenTempTable2</span></span>](./jetopentemptable2-function.md)  
[<span data-ttu-id="61da7-225">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="61da7-225">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)  
[<span data-ttu-id="61da7-226">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="61da7-226">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
