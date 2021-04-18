---
description: 'Altre informazioni su: struttura JET_COLUMNCREATE'
title: Struttura JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315153"
---
# <a name="jet_columncreate-structure"></a><span data-ttu-id="4beee-103">Struttura JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="4beee-103">JET_COLUMNCREATE Structure</span></span>


<span data-ttu-id="4beee-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4beee-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columncreate-structure"></a><span data-ttu-id="4beee-105">Struttura JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="4beee-105">JET_COLUMNCREATE Structure</span></span>

<span data-ttu-id="4beee-106">La struttura **JET_COLUMNCREATE** descrive una colonna da creare in un database.</span><span class="sxs-lookup"><span data-stu-id="4beee-106">The **JET_COLUMNCREATE** structure describes a column to create in a database.</span></span>

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a><span data-ttu-id="4beee-107">Membri</span><span class="sxs-lookup"><span data-stu-id="4beee-107">Members</span></span>

<span data-ttu-id="4beee-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="4beee-108">**cbStruct**</span></span>

<span data-ttu-id="4beee-109">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="4beee-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="4beee-110">Questo campo deve essere inizializzato su **sizeof (JET_COLUMNCREATE)**.</span><span class="sxs-lookup"><span data-stu-id="4beee-110">This field must be initialized to **sizeof( JET_COLUMNCREATE )**.</span></span>

<span data-ttu-id="4beee-111">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="4beee-111">**szColumnName**</span></span>

<span data-ttu-id="4beee-112">Nome della colonna da creare.</span><span class="sxs-lookup"><span data-stu-id="4beee-112">The name of the column to create.</span></span> <span data-ttu-id="4beee-113">Il nome deve soddisfare i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4beee-113">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="4beee-114">Deve avere una lunghezza inferiore a JET_cbNameMost caratteri, escluso il carattere NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="4beee-114">It must be fewer than JET_cbNameMost characters in length, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="4beee-115">Deve contenere solo caratteri dei set seguenti: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c, 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="4beee-115">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="4beee-116">Non può iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="4beee-116">It cannot begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="4beee-117">Deve contenere almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="4beee-117">It must contain at least one non-space character.</span></span>

<span data-ttu-id="4beee-118">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="4beee-118">**coltyp**</span></span>

<span data-ttu-id="4beee-119">Tipo di colonna (ad esempio, testo, binario o numerico).</span><span class="sxs-lookup"><span data-stu-id="4beee-119">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="4beee-120">Per ulteriori informazioni, vedere [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="4beee-120">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="4beee-121">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="4beee-121">**cbMax**</span></span>

<span data-ttu-id="4beee-122">Lunghezza massima, in byte, di una colonna a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="4beee-122">The maximum length, in bytes, of a variable-length column.</span></span> <span data-ttu-id="4beee-123">Lunghezza della colonna per le colonne a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="4beee-123">The length of the column for fixed-length columns.</span></span>

<span data-ttu-id="4beee-124">**grbit**</span><span class="sxs-lookup"><span data-stu-id="4beee-124">**grbit**</span></span>

<span data-ttu-id="4beee-125">Gruppo di bit che contengono le opzioni per la struttura e che includono zero o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4beee-125">A group of bits that contain the options for this structure, and which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4beee-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4beee-126">Value</span></span></p></th>
<th><p><span data-ttu-id="4beee-127">Significato</span><span class="sxs-lookup"><span data-stu-id="4beee-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4beee-128">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="4beee-128">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="4beee-129">La colonna è fissa.</span><span class="sxs-lookup"><span data-stu-id="4beee-129">The column is fixed.</span></span> <span data-ttu-id="4beee-130">Utilizzerà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="4beee-130">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="4beee-131">Non è possibile usare JET_bitColumnFixed con JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="4beee-131">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="4beee-132">Non è possibile usare questo bit con valori Long, ad esempio <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="4beee-132">This bit cannot be used with long values such as <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-133">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="4beee-133">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="4beee-134">La colonna è contrassegnata con tag.</span><span class="sxs-lookup"><span data-stu-id="4beee-134">The column is tagged.</span></span> <span data-ttu-id="4beee-135">Se non contengono dati, le colonne con tag non utilizzano alcuno spazio nel database.</span><span class="sxs-lookup"><span data-stu-id="4beee-135">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="4beee-136">Non è possibile usare questo bit con JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="4beee-136">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4beee-137">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="4beee-137">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="4beee-138">La colonna non deve mai essere impostata su un valore NULL.</span><span class="sxs-lookup"><span data-stu-id="4beee-138">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-139">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="4beee-139">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="4beee-140">La colonna viene incrementata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4beee-140">The column is automatically incremented.</span></span> <span data-ttu-id="4beee-141">Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella.</span><span class="sxs-lookup"><span data-stu-id="4beee-141">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="4beee-142">Il numero, tuttavia, potrebbe non essere continuo.</span><span class="sxs-lookup"><span data-stu-id="4beee-142">The number, however, might not be continuous.</span></span> <span data-ttu-id="4beee-143">Se, ad esempio, vengono inserite cinque righe in una tabella, la colonna AutoIncrement potrebbe contenere i valori {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="4beee-143">For example, if five rows are inserted into a table, the autoincrement column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="4beee-144"><strong>Windows 2000:  </strong> Questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="4beee-144"><strong>Windows 2000:  </strong>This bit can be used only on columns of type <strong>JET_coltypLong</strong>.</span></span></p>
<p><span data-ttu-id="4beee-145"><strong>Windows Server 2003 e versioni successive:  </strong> Questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="4beee-145"><strong>Windows Server 2003 and later:  </strong>This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4beee-146">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="4beee-146">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="4beee-147">Questo bit è valido solo per le chiamate a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="4beee-147">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-148">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="4beee-148">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="4beee-149">Questo bit è valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="4beee-149">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4beee-150">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="4beee-150">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="4beee-151">Questo bit è valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="4beee-151">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-152">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="4beee-152">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="4beee-153">La colonna può essere multivalore.</span><span class="sxs-lookup"><span data-stu-id="4beee-153">The column can be multi-valued.</span></span> <span data-ttu-id="4beee-154">Una colonna multivalore può avere zero, uno o più valori associati.</span><span class="sxs-lookup"><span data-stu-id="4beee-154">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="4beee-155">I vari valori in una colonna multivalore sono identificati dal membro <strong>itagSequence</strong> di varie strutture, ad esempio <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="4beee-155">The various values in a multi-valued column are identified by the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="4beee-156">Le colonne multivalore devono essere contrassegnate come colonne; ovvero non possono essere colonne a lunghezza fissa o a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="4beee-156">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4beee-157">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4beee-157">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="4beee-158">La colonna è una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="4beee-158">The column is an escrow update column.</span></span> <span data-ttu-id="4beee-159">Una colonna di aggiornamento del deposito può essere aggiornata simultaneamente da diverse sessioni con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e mantenere la coerenza delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="4beee-159">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and maintain transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="4beee-160">Una colonna di aggiornamento del deposito è possibile creare solo se la tabella è vuota.</span><span class="sxs-lookup"><span data-stu-id="4beee-160">An escrow update column can be created only when the table is empty.</span></span></p></li>
<li><p><span data-ttu-id="4beee-161">Una colonna di aggiornamento del deposito vincolata deve essere di tipo <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="4beee-161">An escrow update column must be of type <strong>JET_coltypLong.</strong></span></span></p></li>
<li><p><span data-ttu-id="4beee-162">Una colonna di aggiornamento del deposito deve avere un valore predefinito, ovvero <strong>cbDefault</strong> deve essere un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="4beee-162">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
<li><p><span data-ttu-id="4beee-163">Non è possibile usare JET_bitColumnEscrowUpdate insieme alle costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4beee-163">JET_bitColumnEscrowUpdate cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="4beee-164">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="4beee-164">JET_bitColumnTagged</span></span></p></li>
<li><p><span data-ttu-id="4beee-165">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="4beee-165">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="4beee-166">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="4beee-166">JET_bitColumnAutoincrement</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-167">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="4beee-167">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="4beee-168">La colonna viene creata senza una versione.</span><span class="sxs-lookup"><span data-stu-id="4beee-168">The column is created without a version.</span></span> <span data-ttu-id="4beee-169">Le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4beee-169">Other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="4beee-170">Questo bit è utile solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="4beee-170">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="4beee-171">Non può essere utilizzato all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="4beee-171">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4beee-172">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="4beee-172">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="4beee-173">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="4beee-173">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-174">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="4beee-174">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="4beee-175">Utilizzare JET_bitColumnDeleteOnZero anziché JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="4beee-175">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="4beee-176">JET_bitColumnFinalize specifica che una colonna può essere finalizzata.</span><span class="sxs-lookup"><span data-stu-id="4beee-176">JET_bitColumnFinalize specifies that a column can be finalized.</span></span> <span data-ttu-id="4beee-177">Quando una colonna che può essere finalizzata ha una colonna di aggiornamento del deposito che raggiunge lo zero, la riga verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="4beee-177">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="4beee-178">Le versioni future possono invece richiamare una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="4beee-178">Future versions can invoke a callback function instead.</span></span> <span data-ttu-id="4beee-179">Per ulteriori informazioni, vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="4beee-179">For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="4beee-180">Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="4beee-180">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="4beee-181">Non è possibile usare JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="4beee-181">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4beee-182">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="4beee-182">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="4beee-183">Il valore predefinito per una colonna viene fornito dalla funzione di callback <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="4beee-183">The default value for a column is provided by the callback function, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="4beee-184">Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag.</span><span class="sxs-lookup"><span data-stu-id="4beee-184">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="4beee-185"><strong>pvDefault</strong> deve puntare a una struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="4beee-185"><strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p>
<p><span data-ttu-id="4beee-186">Non è possibile usare JET_bitColumnUserDefinedDefault insieme alle costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4beee-186">JET_bitColumnUserDefinedDefault cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="4beee-187">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="4beee-187">JET_bitColumnFixed</span></span></p></li>
<li><p><span data-ttu-id="4beee-188">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="4beee-188">JET_bitColumnNotNULL</span></span></p></li>
<li><p><span data-ttu-id="4beee-189">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="4beee-189">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="4beee-190">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="4beee-190">JET_bitColumnAutoincrement</span></span></p></li>
<li><p><span data-ttu-id="4beee-191">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="4beee-191">JET_bitColumnUpdatable</span></span></p></li>
<li><p><span data-ttu-id="4beee-192">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4beee-192">JET_bitColumnEscrowUpdate</span></span></p></li>
<li><p><span data-ttu-id="4beee-193">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="4beee-193">JET_bitColumnFinalize</span></span></p></li>
<li><p><span data-ttu-id="4beee-194">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="4beee-194">JET_bitColumnDeleteOnZero</span></span></p></li>
<li><p><span data-ttu-id="4beee-195">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="4beee-195">JET_bitColumnMaybeNull</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-196">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="4beee-196">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="4beee-197">La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="4beee-197">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="4beee-198">Un uso comune per una colonna che può essere finalizzata è usarlo come campo di conteggio dei riferimenti e quando il campo raggiunge lo zero, il record viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="4beee-198">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="4beee-199">JET_bitColumnDeleteOnZero è correlato JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="4beee-199">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="4beee-200">Una colonna Delete-on-zero deve essere una colonna di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="4beee-200">A delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="4beee-201">Non è possibile usare JET_bitColumnDeleteOnZero con JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="4beee-201">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="4beee-202">Impossibile utilizzare JET_bitColumnDeleteOnZero con le colonne predefinite definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4beee-202">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4beee-203">**pvDefault**</span><span class="sxs-lookup"><span data-stu-id="4beee-203">**pvDefault**</span></span>

<span data-ttu-id="4beee-204">Punta a un buffer che sarà il valore predefinito per una colonna.</span><span class="sxs-lookup"><span data-stu-id="4beee-204">Points to a buffer which will be the default value for a column.</span></span> <span data-ttu-id="4beee-205">La lunghezza del buffer è **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="4beee-205">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="4beee-206">Se non è disponibile alcun valore predefinito, **pvDefault** deve essere impostato su null e **cbDefault** deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="4beee-206">If there is no default, **pvDefault** should be set to NULL and **cbDefault** should be set to zero.</span></span> <span data-ttu-id="4beee-207">Se *grbit* ha JET_bitColumnUserDefinedDefault set, **pvDefault** verrà interpretato come un puntatore a una struttura di JET_USERDEFINEDDEFAULT.</span><span class="sxs-lookup"><span data-stu-id="4beee-207">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a JET_USERDEFINEDDEFAULT structure.</span></span> <span data-ttu-id="4beee-208">I valori predefiniti non possono essere superiori a 255 byte.</span><span class="sxs-lookup"><span data-stu-id="4beee-208">Default values cannot be larger than 255 bytes.</span></span> <span data-ttu-id="4beee-209">Se un valore predefinito è maggiore di 255 byte, verrà troncato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4beee-209">If a default value is larger than 255 bytes, it will be silently truncated.</span></span>

<span data-ttu-id="4beee-210">**cbDefault**</span><span class="sxs-lookup"><span data-stu-id="4beee-210">**cbDefault**</span></span>

<span data-ttu-id="4beee-211">Dimensione, in byte, del buffer specificato da **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="4beee-211">The size, in bytes, of the buffer specified by **pvDefault**.</span></span>

<span data-ttu-id="4beee-212">**cp**</span><span class="sxs-lookup"><span data-stu-id="4beee-212">**cp**</span></span>

<span data-ttu-id="4beee-213">Tabella codici per la colonna.</span><span class="sxs-lookup"><span data-stu-id="4beee-213">The code page for the column.</span></span> <span data-ttu-id="4beee-214">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="4beee-214">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="4beee-215">Il valore zero indica che verrà utilizzato il valore predefinito (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="4beee-215">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="4beee-216">Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.</span><span class="sxs-lookup"><span data-stu-id="4beee-216">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="4beee-217">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="4beee-217">**columnid**</span></span>

<span data-ttu-id="4beee-218">In seguito all'esito positivo, l'identificatore di colonna della colonna appena creata verrà passato nuovamente in questo campo.</span><span class="sxs-lookup"><span data-stu-id="4beee-218">On success, the column identifier of the newly-created column will be passed back in this field.</span></span> <span data-ttu-id="4beee-219">In caso di errore, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="4beee-219">On failure, the value is undefined.</span></span>

<span data-ttu-id="4beee-220">**Err**</span><span class="sxs-lookup"><span data-stu-id="4beee-220">**err**</span></span>

<span data-ttu-id="4beee-221">Il campo **Err** conterrà lo stato della creazione della colonna.</span><span class="sxs-lookup"><span data-stu-id="4beee-221">The **err** field will contain the status of creating this column.</span></span> <span data-ttu-id="4beee-222">Per un elenco dei valori restituiti probabili, vedere [JetAddColumn](./jetaddcolumn-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4beee-222">See [JetAddColumn](./jetaddcolumn-function.md) for a list of likely return values.</span></span>

### <a name="requirements"></a><span data-ttu-id="4beee-223">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4beee-223">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4beee-224"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4beee-224"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4beee-225">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4beee-225">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-226"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4beee-226"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4beee-227">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4beee-227">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4beee-228"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="4beee-228"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4beee-229">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="4beee-229">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4beee-230"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4beee-230"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4beee-231">Implementato come <strong>JET_COLUMNCREATE_W</strong> (Unicode) e <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4beee-231">Implemented as <strong>JET_COLUMNCREATE_W</strong> (Unicode) and <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4beee-232">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4beee-232">See Also</span></span>

[<span data-ttu-id="4beee-233">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="4beee-233">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="4beee-234">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4beee-234">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="4beee-235">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4beee-235">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4beee-236">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4beee-236">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4beee-237">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="4beee-237">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="4beee-238">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="4beee-238">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="4beee-239">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="4beee-239">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="4beee-240">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="4beee-240">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="4beee-241">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="4beee-241">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="4beee-242">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="4beee-242">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="4beee-243">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="4beee-243">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="4beee-244">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="4beee-244">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="4beee-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4beee-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="4beee-246">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="4beee-246">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)  
[<span data-ttu-id="4beee-247">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="4beee-247">JetSetColumns</span></span>](./jetsetcolumns-function.md)
