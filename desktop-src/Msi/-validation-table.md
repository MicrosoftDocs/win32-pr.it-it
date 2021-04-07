---
description: La \_ tabella di convalida è una tabella di sistema che contiene i nomi delle colonne e i valori delle colonne per tutte le tabelle del database.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: Tabella _Validation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881186"
---
# <a name="_validation-table"></a><span data-ttu-id="3e328-103">\_Tabella di convalida</span><span class="sxs-lookup"><span data-stu-id="3e328-103">\_Validation Table</span></span>

<span data-ttu-id="3e328-104">La \_ tabella di convalida è una tabella di sistema che contiene i nomi delle colonne e i valori delle colonne per tutte le tabelle del database.</span><span class="sxs-lookup"><span data-stu-id="3e328-104">The \_Validation table is a system table that contains the column names and the column values for all of the tables in the database.</span></span> <span data-ttu-id="3e328-105">Viene utilizzato durante il processo di convalida del database per garantire che tutte le colonne siano contabilizzate e dispongano dei valori corretti.</span><span class="sxs-lookup"><span data-stu-id="3e328-105">It is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="3e328-106">Questa tabella non è inclusa nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="3e328-106">This table is not shipped with the installer database.</span></span>

<span data-ttu-id="3e328-107">La \_ tabella di convalida include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e328-107">The \_Validation table has the following columns.</span></span>



| <span data-ttu-id="3e328-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="3e328-108">Column</span></span>      | <span data-ttu-id="3e328-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e328-109">Type</span></span>                               | <span data-ttu-id="3e328-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="3e328-110">Key</span></span> | <span data-ttu-id="3e328-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="3e328-111">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="3e328-112">Tabella</span><span class="sxs-lookup"><span data-stu-id="3e328-112">Table</span></span>       | [<span data-ttu-id="3e328-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3e328-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3e328-114">S</span><span class="sxs-lookup"><span data-stu-id="3e328-114">Y</span></span>   | <span data-ttu-id="3e328-115">N</span><span class="sxs-lookup"><span data-stu-id="3e328-115">N</span></span>        |
| <span data-ttu-id="3e328-116">Colonna</span><span class="sxs-lookup"><span data-stu-id="3e328-116">Column</span></span>      | [<span data-ttu-id="3e328-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3e328-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3e328-118">S</span><span class="sxs-lookup"><span data-stu-id="3e328-118">Y</span></span>   | <span data-ttu-id="3e328-119">N</span><span class="sxs-lookup"><span data-stu-id="3e328-119">N</span></span>        |
| <span data-ttu-id="3e328-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="3e328-120">Nullable</span></span>    | [<span data-ttu-id="3e328-121">Text</span><span class="sxs-lookup"><span data-stu-id="3e328-121">Text</span></span>](text.md)                   | <span data-ttu-id="3e328-122">N</span><span class="sxs-lookup"><span data-stu-id="3e328-122">N</span></span>   | <span data-ttu-id="3e328-123">N</span><span class="sxs-lookup"><span data-stu-id="3e328-123">N</span></span>        |
| <span data-ttu-id="3e328-124">MinValue</span><span class="sxs-lookup"><span data-stu-id="3e328-124">MinValue</span></span>    | [<span data-ttu-id="3e328-125">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="3e328-125">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="3e328-126">N</span><span class="sxs-lookup"><span data-stu-id="3e328-126">N</span></span>   | <span data-ttu-id="3e328-127">S</span><span class="sxs-lookup"><span data-stu-id="3e328-127">Y</span></span>        |
| <span data-ttu-id="3e328-128">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3e328-128">MaxValue</span></span>    | [<span data-ttu-id="3e328-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="3e328-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="3e328-130">N</span><span class="sxs-lookup"><span data-stu-id="3e328-130">N</span></span>   | <span data-ttu-id="3e328-131">S</span><span class="sxs-lookup"><span data-stu-id="3e328-131">Y</span></span>        |
| <span data-ttu-id="3e328-132">KeyTable</span><span class="sxs-lookup"><span data-stu-id="3e328-132">KeyTable</span></span>    | [<span data-ttu-id="3e328-133">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3e328-133">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3e328-134">N</span><span class="sxs-lookup"><span data-stu-id="3e328-134">N</span></span>   | <span data-ttu-id="3e328-135">S</span><span class="sxs-lookup"><span data-stu-id="3e328-135">Y</span></span>        |
| <span data-ttu-id="3e328-136">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="3e328-136">KeyColumn</span></span>   | [<span data-ttu-id="3e328-137">Integer</span><span class="sxs-lookup"><span data-stu-id="3e328-137">Integer</span></span>](integer.md)             | <span data-ttu-id="3e328-138">N</span><span class="sxs-lookup"><span data-stu-id="3e328-138">N</span></span>   | <span data-ttu-id="3e328-139">S</span><span class="sxs-lookup"><span data-stu-id="3e328-139">Y</span></span>        |
| <span data-ttu-id="3e328-140">Category</span><span class="sxs-lookup"><span data-stu-id="3e328-140">Category</span></span>    | [<span data-ttu-id="3e328-141">Text</span><span class="sxs-lookup"><span data-stu-id="3e328-141">Text</span></span>](text.md)                   | <span data-ttu-id="3e328-142">N</span><span class="sxs-lookup"><span data-stu-id="3e328-142">N</span></span>   | <span data-ttu-id="3e328-143">S</span><span class="sxs-lookup"><span data-stu-id="3e328-143">Y</span></span>        |
| <span data-ttu-id="3e328-144">Set</span><span class="sxs-lookup"><span data-stu-id="3e328-144">Set</span></span>         | [<span data-ttu-id="3e328-145">Text</span><span class="sxs-lookup"><span data-stu-id="3e328-145">Text</span></span>](text.md)                   | <span data-ttu-id="3e328-146">N</span><span class="sxs-lookup"><span data-stu-id="3e328-146">N</span></span>   | <span data-ttu-id="3e328-147">S</span><span class="sxs-lookup"><span data-stu-id="3e328-147">Y</span></span>        |
| <span data-ttu-id="3e328-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e328-148">Description</span></span> | [<span data-ttu-id="3e328-149">Text</span><span class="sxs-lookup"><span data-stu-id="3e328-149">Text</span></span>](text.md)                   | <span data-ttu-id="3e328-150">N</span><span class="sxs-lookup"><span data-stu-id="3e328-150">N</span></span>   | <span data-ttu-id="3e328-151">S</span><span class="sxs-lookup"><span data-stu-id="3e328-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3e328-152">Colonne</span><span class="sxs-lookup"><span data-stu-id="3e328-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3e328-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="3e328-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="3e328-154">Utilizzato per identificare una tabella specifica.</span><span class="sxs-lookup"><span data-stu-id="3e328-154">Used to identify a particular table.</span></span> <span data-ttu-id="3e328-155">Questa chiave e la chiave della colonna formano la chiave primaria della \_ tabella di convalida.</span><span class="sxs-lookup"><span data-stu-id="3e328-155">This key and the Column key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="3e328-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna</span><span class="sxs-lookup"><span data-stu-id="3e328-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="3e328-157">Utilizzato per identificare una colonna specifica della tabella.</span><span class="sxs-lookup"><span data-stu-id="3e328-157">Used to identify a particular column of the table.</span></span> <span data-ttu-id="3e328-158">Questa chiave e la chiave della tabella formano la chiave primaria della \_ tabella di convalida.</span><span class="sxs-lookup"><span data-stu-id="3e328-158">This key and the Table key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="3e328-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span><span class="sxs-lookup"><span data-stu-id="3e328-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span></span>
</dt> <dd>

<span data-ttu-id="3e328-160">Indica se la colonna può contenere un valore null.</span><span class="sxs-lookup"><span data-stu-id="3e328-160">Identifies whether the column may contain a Null value.</span></span>

<span data-ttu-id="3e328-161">Questa colonna può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e328-161">This column may have one of the following values.</span></span>



| <span data-ttu-id="3e328-162">string</span><span class="sxs-lookup"><span data-stu-id="3e328-162">String</span></span> | <span data-ttu-id="3e328-163">Significato</span><span class="sxs-lookup"><span data-stu-id="3e328-163">Meaning</span></span>                                   |
|--------|-------------------------------------------|
| <span data-ttu-id="3e328-164">S</span><span class="sxs-lookup"><span data-stu-id="3e328-164">Y</span></span>      | <span data-ttu-id="3e328-165">Sì, la colonna potrebbe avere un valore null.</span><span class="sxs-lookup"><span data-stu-id="3e328-165">Yes, the column may have a Null value.</span></span>    |
| <span data-ttu-id="3e328-166">N</span><span class="sxs-lookup"><span data-stu-id="3e328-166">N</span></span>      | <span data-ttu-id="3e328-167">No, la colonna non può avere un valore null.</span><span class="sxs-lookup"><span data-stu-id="3e328-167">No, the column may not have a Null value.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3e328-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span><span class="sxs-lookup"><span data-stu-id="3e328-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span></span>
</dt> <dd>

<span data-ttu-id="3e328-169">Questo campo si applica alle colonne con valore numerico.</span><span class="sxs-lookup"><span data-stu-id="3e328-169">This field applies to columns having numeric value.</span></span> <span data-ttu-id="3e328-170">Il campo contiene il valore minimo consentito.</span><span class="sxs-lookup"><span data-stu-id="3e328-170">The field contains the minimum permissible value.</span></span> <span data-ttu-id="3e328-171">Può trattarsi del valore minimo per un numero intero o del valore minimo per una stringa di data o di versione.</span><span class="sxs-lookup"><span data-stu-id="3e328-171">This can be the minimum value for an integer or the minimum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="3e328-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span><span class="sxs-lookup"><span data-stu-id="3e328-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span></span>
</dt> <dd>

<span data-ttu-id="3e328-173">Questo campo si applica alle colonne con valore numerico.</span><span class="sxs-lookup"><span data-stu-id="3e328-173">This field applies to columns having numeric value.</span></span> <span data-ttu-id="3e328-174">Il campo è il valore massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="3e328-174">The field is the maximum permissible value.</span></span> <span data-ttu-id="3e328-175">Può trattarsi del valore massimo per un numero intero o del valore massimo per una stringa di data o di versione.</span><span class="sxs-lookup"><span data-stu-id="3e328-175">This may be the maximum value for an integer or the maximum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="3e328-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span><span class="sxs-lookup"><span data-stu-id="3e328-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span></span>
</dt> <dd>

<span data-ttu-id="3e328-177">Questo campo si applica alle colonne che sono chiavi esterne.</span><span class="sxs-lookup"><span data-stu-id="3e328-177">This field applies to columns that are external keys.</span></span> <span data-ttu-id="3e328-178">Il campo identificato nella colonna deve essere collegato al numero di colonna specificato da colonna colonna nella tabella denominata in tabella.</span><span class="sxs-lookup"><span data-stu-id="3e328-178">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="3e328-179">Può trattarsi di un elenco di tabelle separate da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="3e328-179">This can be a list of tables separated by semicolons.</span></span>

</dd> <dt>

<span data-ttu-id="3e328-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span><span class="sxs-lookup"><span data-stu-id="3e328-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span></span>
</dt> <dd>

<span data-ttu-id="3e328-181">Questo campo si applica alle colonne della tabella che sono chiavi esterne.</span><span class="sxs-lookup"><span data-stu-id="3e328-181">This field applies to table columns that are external keys.</span></span> <span data-ttu-id="3e328-182">Il campo identificato nella colonna deve essere collegato al numero di colonna specificato da colonna colonna nella tabella denominata in tabella.</span><span class="sxs-lookup"><span data-stu-id="3e328-182">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="3e328-183">L'intervallo consentito del campo colonna colonna è 1-32.</span><span class="sxs-lookup"><span data-stu-id="3e328-183">The permissible range of the KeyColumn field is 1-32.</span></span>

</dd> <dt>

<span data-ttu-id="3e328-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria</span><span class="sxs-lookup"><span data-stu-id="3e328-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="3e328-185">Questo è il tipo di dati contenuti nel campo del database specificato dalle colonne della tabella e della colonna della \_ tabella di convalida.</span><span class="sxs-lookup"><span data-stu-id="3e328-185">This is the type of data contained by the database field specified by the Table and Column columns of the \_Validation table.</span></span> <span data-ttu-id="3e328-186">Se si tratta di un tipo con un valore numerico, ad esempio [Integer](integer.md), [DoubleInteger](doubleinteger.md) o [time/date](time-date.md), immettere null in questo campo e specificare l'intervallo del valore utilizzando le colonne MinValue e MaxValue.</span><span class="sxs-lookup"><span data-stu-id="3e328-186">If this is a type having a numeric value, such as [Integer](integer.md), [DoubleInteger](doubleinteger.md) or [Time/Date](time-date.md), then enter null into this field and specify the value's range using the MinValue and MaxValue columns.</span></span> <span data-ttu-id="3e328-187">Utilizzare la colonna Categoria per specificare i tipi di dati non numerici descritti in [tipi di dati di colonna](column-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="3e328-187">Use the Category column to specify the non-numeric data types described in [Column Data Types](column-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e328-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span><span class="sxs-lookup"><span data-stu-id="3e328-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span></span>
</dt> <dd>

<span data-ttu-id="3e328-189">Si tratta di un elenco di valori consentiti per questo campo separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="3e328-189">This is a list of permissible values for this field separated by semicolons.</span></span> <span data-ttu-id="3e328-190">Questo campo viene in genere usato per le enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="3e328-190">This field is usually used for enumerations.</span></span>

</dd> <dt>

<span data-ttu-id="3e328-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e328-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="3e328-192">Descrizione dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="3e328-192">A description of the data that is stored in the column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="3e328-193">Convalida</span><span class="sxs-lookup"><span data-stu-id="3e328-193">Validation</span></span>

<dl>

[<span data-ttu-id="3e328-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="3e328-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3e328-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="3e328-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3e328-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="3e328-196">ICE32</span></span>](ice32.md)  
</dl>

## <a name="remarks"></a><span data-ttu-id="3e328-197">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e328-197">Remarks</span></span>

<span data-ttu-id="3e328-198">Il campo categoria di questa tabella si applica solo ai dati stringa.</span><span class="sxs-lookup"><span data-stu-id="3e328-198">The Category field of this table only applies to string data.</span></span> <span data-ttu-id="3e328-199">Se il campo colonna fa riferimento a una colonna con dati binari, è necessario specificare il tipo di dati binario nel campo categoria.</span><span class="sxs-lookup"><span data-stu-id="3e328-199">If the Column field refers to a column with binary data, the binary data type must be specified in the Category field.</span></span> <span data-ttu-id="3e328-200">I tipi di colonna di dati Integer ignorano il campo categoria durante la convalida.</span><span class="sxs-lookup"><span data-stu-id="3e328-200">Integer data Column types ignore the Category field during validation.</span></span>

 

 



