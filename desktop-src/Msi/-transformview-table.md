---
description: Si tratta di una tabella temporanea di sola lettura utilizzata per visualizzare le trasformazioni con la modalità di visualizzazione trasforma. Questa tabella non viene mai resa permanente dal programma di installazione.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: Tabella _TransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528884"
---
# <a name="_transformview-table"></a><span data-ttu-id="dd283-104">\_Tabella transformview</span><span class="sxs-lookup"><span data-stu-id="dd283-104">\_TransformView Table</span></span>

<span data-ttu-id="dd283-105">Si tratta di una tabella temporanea di sola lettura utilizzata per visualizzare le trasformazioni con la modalità di visualizzazione trasforma.</span><span class="sxs-lookup"><span data-stu-id="dd283-105">This is a read-only temporary table used to view transforms with the transform view mode.</span></span> <span data-ttu-id="dd283-106">Questa tabella non viene mai resa permanente dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="dd283-106">This table is never persisted by the installer.</span></span>

<span data-ttu-id="dd283-107">Per richiamare la modalità di visualizzazione trasformazione, ottenere un handle e aprire il database di riferimento.</span><span class="sxs-lookup"><span data-stu-id="dd283-107">To invoke the transform view mode, obtain a handle and open the reference database.</span></span> <span data-ttu-id="dd283-108">Vedere [recupero di un handle di database](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="dd283-108">See [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span> <span data-ttu-id="dd283-109">Chiamare [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) con \_ errore MSITRANSFORM \_ VIEWTRANSFORM.</span><span class="sxs-lookup"><span data-stu-id="dd283-109">Call [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) with MSITRANSFORM\_ERROR\_VIEWTRANSFORM.</span></span> <span data-ttu-id="dd283-110">In questo modo viene arrestata l'applicazione della trasformazione al database e viene eseguito il dump del contenuto della trasformazione nella \_ tabella transformview.</span><span class="sxs-lookup"><span data-stu-id="dd283-110">This stops the transform from being applied to the database and dumps the transform contents into the \_TransformView table.</span></span> <span data-ttu-id="dd283-111">È possibile accedere ai dati nella tabella tramite query SQL.</span><span class="sxs-lookup"><span data-stu-id="dd283-111">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="dd283-112">Vedere [utilizzo delle query](working-with-queries.md).</span><span class="sxs-lookup"><span data-stu-id="dd283-112">See [Working with Queries](working-with-queries.md).</span></span>

<span data-ttu-id="dd283-113">La \_ tabella transformview non viene cancellata quando viene applicata un'altra trasformazione.</span><span class="sxs-lookup"><span data-stu-id="dd283-113">The \_TransformView table is not cleared when another transform is applied.</span></span> <span data-ttu-id="dd283-114">La tabella riflette l'effetto cumulativo delle applicazioni successive.</span><span class="sxs-lookup"><span data-stu-id="dd283-114">The table reflects the cumulative effect of successive applications.</span></span> <span data-ttu-id="dd283-115">Per visualizzare le trasformazioni separatamente è necessario rilasciare la tabella.</span><span class="sxs-lookup"><span data-stu-id="dd283-115">To view the transforms separately you must release the table.</span></span>

<span data-ttu-id="dd283-116">La \_ tabella transformview include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd283-116">The \_TransformView Table has the following columns.</span></span>



| <span data-ttu-id="dd283-117">Colonna</span><span class="sxs-lookup"><span data-stu-id="dd283-117">Column</span></span>  | <span data-ttu-id="dd283-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd283-118">Type</span></span>                         | <span data-ttu-id="dd283-119">Chiave</span><span class="sxs-lookup"><span data-stu-id="dd283-119">Key</span></span> | <span data-ttu-id="dd283-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="dd283-120">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="dd283-121">Tabella</span><span class="sxs-lookup"><span data-stu-id="dd283-121">Table</span></span>   | [<span data-ttu-id="dd283-122">Identificatore</span><span class="sxs-lookup"><span data-stu-id="dd283-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="dd283-123">S</span><span class="sxs-lookup"><span data-stu-id="dd283-123">Y</span></span>   | <span data-ttu-id="dd283-124">N</span><span class="sxs-lookup"><span data-stu-id="dd283-124">N</span></span>        |
| <span data-ttu-id="dd283-125">Colonna</span><span class="sxs-lookup"><span data-stu-id="dd283-125">Column</span></span>  | [<span data-ttu-id="dd283-126">Text</span><span class="sxs-lookup"><span data-stu-id="dd283-126">Text</span></span>](text.md)             | <span data-ttu-id="dd283-127">S</span><span class="sxs-lookup"><span data-stu-id="dd283-127">Y</span></span>   | <span data-ttu-id="dd283-128">N</span><span class="sxs-lookup"><span data-stu-id="dd283-128">N</span></span>        |
| <span data-ttu-id="dd283-129">Riga</span><span class="sxs-lookup"><span data-stu-id="dd283-129">Row</span></span>     | [<span data-ttu-id="dd283-130">Text</span><span class="sxs-lookup"><span data-stu-id="dd283-130">Text</span></span>](text.md)             | <span data-ttu-id="dd283-131">S</span><span class="sxs-lookup"><span data-stu-id="dd283-131">Y</span></span>   | <span data-ttu-id="dd283-132">S</span><span class="sxs-lookup"><span data-stu-id="dd283-132">Y</span></span>        |
| <span data-ttu-id="dd283-133">Data</span><span class="sxs-lookup"><span data-stu-id="dd283-133">Data</span></span>    | [<span data-ttu-id="dd283-134">Text</span><span class="sxs-lookup"><span data-stu-id="dd283-134">Text</span></span>](text.md)             | <span data-ttu-id="dd283-135">N</span><span class="sxs-lookup"><span data-stu-id="dd283-135">N</span></span>   | <span data-ttu-id="dd283-136">S</span><span class="sxs-lookup"><span data-stu-id="dd283-136">Y</span></span>        |
| <span data-ttu-id="dd283-137">Corrente</span><span class="sxs-lookup"><span data-stu-id="dd283-137">Current</span></span> | [<span data-ttu-id="dd283-138">Text</span><span class="sxs-lookup"><span data-stu-id="dd283-138">Text</span></span>](text.md)             | <span data-ttu-id="dd283-139">N</span><span class="sxs-lookup"><span data-stu-id="dd283-139">N</span></span>   | <span data-ttu-id="dd283-140">S</span><span class="sxs-lookup"><span data-stu-id="dd283-140">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="dd283-141">Colonna</span><span class="sxs-lookup"><span data-stu-id="dd283-141">Column</span></span>

<dl> <dt>

<span data-ttu-id="dd283-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="dd283-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="dd283-143">Nome di una tabella di database modificata.</span><span class="sxs-lookup"><span data-stu-id="dd283-143">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="dd283-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna</span><span class="sxs-lookup"><span data-stu-id="dd283-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="dd283-145">Nome di una colonna di tabella modificata o di inserimento, eliminazione, creazione o eliminazione.</span><span class="sxs-lookup"><span data-stu-id="dd283-145">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="dd283-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga</span><span class="sxs-lookup"><span data-stu-id="dd283-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="dd283-147">Elenco dei valori di chiave primaria separati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="dd283-147">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="dd283-148">I valori di chiave primaria null sono rappresentati da un singolo carattere di spazio.</span><span class="sxs-lookup"><span data-stu-id="dd283-148">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="dd283-149">Un valore null in questa colonna indica una modifica dello schema.</span><span class="sxs-lookup"><span data-stu-id="dd283-149">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="dd283-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati</span><span class="sxs-lookup"><span data-stu-id="dd283-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="dd283-151">Dati, nome di un flusso di dati o definizione di colonna.</span><span class="sxs-lookup"><span data-stu-id="dd283-151">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="dd283-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrente</span><span class="sxs-lookup"><span data-stu-id="dd283-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="dd283-153">Valore corrente dal database di riferimento o da un numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="dd283-153">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd283-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd283-154">Remarks</span></span>

<span data-ttu-id="dd283-155">La \_ transformview viene mantenuta in memoria da un conteggio dei blocchi, che può essere rilasciato con il comando SQL seguente.</span><span class="sxs-lookup"><span data-stu-id="dd283-155">The \_TransformView is held in memory by a lock count, that can be released with the following SQL command.</span></span>

<span data-ttu-id="dd283-156">"ALTER TABLE \_ Transformview Free".</span><span class="sxs-lookup"><span data-stu-id="dd283-156">"ALTER TABLE \_TransformView FREE".</span></span>

<span data-ttu-id="dd283-157">È possibile accedere ai dati nella tabella tramite query SQL.</span><span class="sxs-lookup"><span data-stu-id="dd283-157">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="dd283-158">Il linguaggio SQL è costituito da due divisioni principali: DDL (Data Definition Language) utilizzato per definire tutti gli oggetti in un database SQL e DML (Data Manipulation Language) utilizzato per selezionare, inserire, aggiornare ed eliminare dati negli oggetti definiti mediante DDL.</span><span class="sxs-lookup"><span data-stu-id="dd283-158">The SQL language has two main divisions: Data Definition Language (DDL) that is used to define all the objects in an SQL database, and Data Manipulation Language (DML) that is used to select, insert, update, and delete data in the objects defined using DDL.</span></span>

<span data-ttu-id="dd283-159">Le operazioni di trasformazione DML (Data Manipulation Language) sono indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="dd283-159">The Data Manipulation Language (DML) transform operations are indicated as follows.</span></span> <span data-ttu-id="dd283-160">I dati DML (Data Manipulation Language) sono istruzioni in SQL che consentono di modificare, anziché definire i dati.</span><span class="sxs-lookup"><span data-stu-id="dd283-160">Data Manipulation Language (DML) are those statements in SQL that manipulate, as opposed to define, data.</span></span>



| <span data-ttu-id="dd283-161">Operazione di trasformazione</span><span class="sxs-lookup"><span data-stu-id="dd283-161">Transform operation</span></span> | <span data-ttu-id="dd283-162">Risultato SQL</span><span class="sxs-lookup"><span data-stu-id="dd283-162">SQL result</span></span>                                    |
|---------------------|-----------------------------------------------|
| <span data-ttu-id="dd283-163">Modificare i dati</span><span class="sxs-lookup"><span data-stu-id="dd283-163">Modify data</span></span>         | <span data-ttu-id="dd283-164">tabella colonna riga dati {valore corrente}</span><span class="sxs-lookup"><span data-stu-id="dd283-164">{table} {column} {row} {data} {current value}</span></span> |
| <span data-ttu-id="dd283-165">Inserimento di una riga</span><span class="sxs-lookup"><span data-stu-id="dd283-165">Insert row</span></span>          | <span data-ttu-id="dd283-166">tabella "INSERT" {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="dd283-166">{table} "INSERT" {row} NULL NULL</span></span>              |
| <span data-ttu-id="dd283-167">Elimina riga</span><span class="sxs-lookup"><span data-stu-id="dd283-167">Delete row</span></span>          | <span data-ttu-id="dd283-168">tabella "DELETE" {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="dd283-168">{table} "DELETE" {row} NULL NULL</span></span>              |



 

<span data-ttu-id="dd283-169">Le operazioni di trasformazione DDL (Data Definition Language) sono indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="dd283-169">The Data Definition Language (DDL) transform operations are indicated as follows.</span></span> <span data-ttu-id="dd283-170">I dati DDL (Data Definition Language) sono istruzioni in SQL che definiscono, anziché modificare, i dati.</span><span class="sxs-lookup"><span data-stu-id="dd283-170">Data Definition Language (DDL) are those statements in SQL that define, as opposed to manipulate, data.</span></span>



| <span data-ttu-id="dd283-171">Operazione di trasformazione</span><span class="sxs-lookup"><span data-stu-id="dd283-171">Transform operation</span></span> | <span data-ttu-id="dd283-172">Risultato SQL</span><span class="sxs-lookup"><span data-stu-id="dd283-172">SQL result</span></span>                                   |
|---------------------|----------------------------------------------|
| <span data-ttu-id="dd283-173">Aggiungere una colonna</span><span class="sxs-lookup"><span data-stu-id="dd283-173">Add column</span></span>          | <span data-ttu-id="dd283-174">tabella colonna NULL {defn} {numero di colonna}</span><span class="sxs-lookup"><span data-stu-id="dd283-174">{table} {column} NULL {defn} {column number}</span></span> |
| <span data-ttu-id="dd283-175">Aggiungi tabella</span><span class="sxs-lookup"><span data-stu-id="dd283-175">Add table</span></span>           | <span data-ttu-id="dd283-176">tabella "CREATE" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="dd283-176">{table} "CREATE" NULL NULL NULL</span></span>              |
| <span data-ttu-id="dd283-177">Eliminare una tabella</span><span class="sxs-lookup"><span data-stu-id="dd283-177">Drop table</span></span>          | <span data-ttu-id="dd283-178">tabella "DROP" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="dd283-178">{table} "DROP" NULL NULL NULL</span></span>                |



 

<span data-ttu-id="dd283-179">Quando l'applicazione di una trasformazione aggiunge questa tabella, il campo dati riceve testo che può essere interpretato come valore integer a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="dd283-179">When the application of a transform adds this table, the Data field receives text that can be interpreted as a 16-bit integer value.</span></span> <span data-ttu-id="dd283-180">Il valore descrive la colonna denominata nel campo colonna.</span><span class="sxs-lookup"><span data-stu-id="dd283-180">The value describes the column named in the Column field.</span></span> <span data-ttu-id="dd283-181">È possibile confrontare il valore integer con le costanti nella tabella seguente per determinare la definizione della colonna modificata.</span><span class="sxs-lookup"><span data-stu-id="dd283-181">You can compare the integer value to the constants in the following table to determine the definition of the altered column.</span></span>



| <span data-ttu-id="dd283-182">bit</span><span class="sxs-lookup"><span data-stu-id="dd283-182">Bit</span></span>                                                                                                       | <span data-ttu-id="dd283-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd283-183">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd283-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>BITS 0 7</span><span class="sxs-lookup"><span data-stu-id="dd283-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span></span><br/>         | <span data-ttu-id="dd283-185">Esadecimale: 0x0000 0x0100</span><span class="sxs-lookup"><span data-stu-id="dd283-185">Hexadecimal: 0x0000 0x0100</span></span><br/> <span data-ttu-id="dd283-186">Decimale: 0 255</span><span class="sxs-lookup"><span data-stu-id="dd283-186">Decimal: 0 255</span></span><br/> <span data-ttu-id="dd283-187">Larghezza colonna</span><span class="sxs-lookup"><span data-stu-id="dd283-187">Column width</span></span><br/>                                                                                                                                                                                                                                  |
| <span data-ttu-id="dd283-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span><span class="sxs-lookup"><span data-stu-id="dd283-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span></span><br/>                  | <span data-ttu-id="dd283-189">Esadecimale: 0x0100</span><span class="sxs-lookup"><span data-stu-id="dd283-189">Hexadecimal: 0x0100</span></span><br/> <span data-ttu-id="dd283-190">Decimale: 256</span><span class="sxs-lookup"><span data-stu-id="dd283-190">Decimal: 256</span></span><br/> <span data-ttu-id="dd283-191">Una colonna persistente.</span><span class="sxs-lookup"><span data-stu-id="dd283-191">A persistent column.</span></span> <span data-ttu-id="dd283-192">Zero indica una colonna temporanea.</span><span class="sxs-lookup"><span data-stu-id="dd283-192">Zero means a temporary column.</span></span> <br/>                                                                                                                                                                                                   |
| <span data-ttu-id="dd283-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span><span class="sxs-lookup"><span data-stu-id="dd283-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span></span><br/>                  | <span data-ttu-id="dd283-194">Esadecimale: 0x0200</span><span class="sxs-lookup"><span data-stu-id="dd283-194">Hexadecimal: 0x0200</span></span><br/> <span data-ttu-id="dd283-195">Decimale: 1023</span><span class="sxs-lookup"><span data-stu-id="dd283-195">Decimal: 1023</span></span><br/> <span data-ttu-id="dd283-196">Colonna localizzabile.</span><span class="sxs-lookup"><span data-stu-id="dd283-196">A localizable column.</span></span> <span data-ttu-id="dd283-197">Zero indica che la colonna non può essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="dd283-197">Zero means the column cannot be localized.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="dd283-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span><span class="sxs-lookup"><span data-stu-id="dd283-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span></span><br/> | <span data-ttu-id="dd283-199">Esadecimale: 0x0000</span><span class="sxs-lookup"><span data-stu-id="dd283-199">Hexadecimal: 0x0000</span></span><br/> <span data-ttu-id="dd283-200">Decimale: 0</span><span class="sxs-lookup"><span data-stu-id="dd283-200">Decimal: 0</span></span><br/> <span data-ttu-id="dd283-201">Long integer</span><span class="sxs-lookup"><span data-stu-id="dd283-201">Long integer</span></span><br/> <span data-ttu-id="dd283-202">Esadecimale: 0x0400</span><span class="sxs-lookup"><span data-stu-id="dd283-202">Hexadecimal: 0x0400</span></span><br/> <span data-ttu-id="dd283-203">Decimale: 1024</span><span class="sxs-lookup"><span data-stu-id="dd283-203">Decimal: 1024</span></span><br/> <span data-ttu-id="dd283-204">Valore short Integer</span><span class="sxs-lookup"><span data-stu-id="dd283-204">Short integer</span></span><br/> <span data-ttu-id="dd283-205">Esadecimale: 0x0800</span><span class="sxs-lookup"><span data-stu-id="dd283-205">Hexadecimal: 0x0800</span></span><br/> <span data-ttu-id="dd283-206">Decimale: 2048</span><span class="sxs-lookup"><span data-stu-id="dd283-206">Decimal: 2048</span></span><br/> <span data-ttu-id="dd283-207">Oggetto binario</span><span class="sxs-lookup"><span data-stu-id="dd283-207">Binary object</span></span><br/> <span data-ttu-id="dd283-208">Esadecimale: 0x0C00</span><span class="sxs-lookup"><span data-stu-id="dd283-208">Hexadecimal: 0x0C00</span></span><br/> <span data-ttu-id="dd283-209">Decimale: 3072</span><span class="sxs-lookup"><span data-stu-id="dd283-209">Decimal: 3072</span></span><br/> <span data-ttu-id="dd283-210">string</span><span class="sxs-lookup"><span data-stu-id="dd283-210">String</span></span><br/> |
| <span data-ttu-id="dd283-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span><span class="sxs-lookup"><span data-stu-id="dd283-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span></span><br/>              | <span data-ttu-id="dd283-212">Esadecimale: 0x1000</span><span class="sxs-lookup"><span data-stu-id="dd283-212">Hexadecimal: 0x1000</span></span><br/> <span data-ttu-id="dd283-213">Decimale: 4096</span><span class="sxs-lookup"><span data-stu-id="dd283-213">Decimal: 4096</span></span><br/> <span data-ttu-id="dd283-214">Colonna nullable.</span><span class="sxs-lookup"><span data-stu-id="dd283-214">Nullable column.</span></span> <span data-ttu-id="dd283-215">Zero indica che la colonna è non nullable.</span><span class="sxs-lookup"><span data-stu-id="dd283-215">Zero means the column is non-nullable.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="dd283-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span><span class="sxs-lookup"><span data-stu-id="dd283-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span></span><br/>              | <span data-ttu-id="dd283-217">Esadecimale: 0x2000</span><span class="sxs-lookup"><span data-stu-id="dd283-217">Hexadecimal: 0x2000</span></span><br/> <span data-ttu-id="dd283-218">Decimale: 8192</span><span class="sxs-lookup"><span data-stu-id="dd283-218">Decimal: 8192</span></span><br/> <span data-ttu-id="dd283-219">Colonna chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="dd283-219">Primary key column.</span></span> <span data-ttu-id="dd283-220">Zero indica che questa colonna non è una chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="dd283-220">Zero means this column is not a primary key.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="dd283-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>BITS 14 15</span><span class="sxs-lookup"><span data-stu-id="dd283-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span></span><br/> | <span data-ttu-id="dd283-222">Esadecimale: 0x4000 0x8000</span><span class="sxs-lookup"><span data-stu-id="dd283-222">Hexadecimal: 0x4000 0x8000</span></span><br/> <span data-ttu-id="dd283-223">Decimale: 16384 32768</span><span class="sxs-lookup"><span data-stu-id="dd283-223">Decimal: 16384 32768</span></span><br/> <span data-ttu-id="dd283-224">Riservato</span><span class="sxs-lookup"><span data-stu-id="dd283-224">Reserved</span></span><br/>                                                                                                                                                                                                                                |



 

<span data-ttu-id="dd283-225">Per uno script di esempio che illustra la \_ tabella transformview, vedere [visualizzare una trasformazione](view-a-transform.md).</span><span class="sxs-lookup"><span data-stu-id="dd283-225">For a script sample that demonstrates the \_TransformView table, see [View a Transform](view-a-transform.md).</span></span>

 

 




