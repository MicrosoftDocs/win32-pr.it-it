---
description: MsiViewGetColumnInfo e la Proprietà ColumnInfo dell'oggetto View utilizzano il formato seguente per descrivere le definizioni delle colonne del database.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato della definizione di colonna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231885"
---
# <a name="column-definition-format"></a><span data-ttu-id="9ec46-103">Formato della definizione di colonna</span><span class="sxs-lookup"><span data-stu-id="9ec46-103">Column Definition Format</span></span>

<span data-ttu-id="9ec46-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) e la [**Proprietà ColumnInfo**](view-columninfo.md) dell'oggetto [**View**](view-object.md) utilizzano il formato seguente per descrivere le definizioni delle colonne del database.</span><span class="sxs-lookup"><span data-stu-id="9ec46-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) and the [**ColumnInfo Property**](view-columninfo.md) of the [**View**](view-object.md) object use the following format to describe database column definitions.</span></span> <span data-ttu-id="9ec46-105">Ogni colonna è descritta da una stringa nel campo record corrispondente restituito dalla funzione o dalla proprietà.</span><span class="sxs-lookup"><span data-stu-id="9ec46-105">Each column is described by a string in the corresponding record field returned by the function or property.</span></span> <span data-ttu-id="9ec46-106">La stringa di definizione è costituita da una singola lettera che rappresenta il tipo di dati seguito dalla larghezza della colonna (in caratteri se applicabile, in caso contrario, byte).</span><span class="sxs-lookup"><span data-stu-id="9ec46-106">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise).</span></span> <span data-ttu-id="9ec46-107">Uno spessore pari a zero indica una larghezza senza limiti (ad esempio, campi di testo lunghi e flussi).</span><span class="sxs-lookup"><span data-stu-id="9ec46-107">A width of zero designates an unbounded width (for example, long text fields and streams).</span></span> <span data-ttu-id="9ec46-108">Una lettera maiuscola indica che nella colonna sono consentiti valori null.</span><span class="sxs-lookup"><span data-stu-id="9ec46-108">An uppercase letter indicates that null values are allowed in the column.</span></span>



| <span data-ttu-id="9ec46-109">Descrittore di colonna</span><span class="sxs-lookup"><span data-stu-id="9ec46-109">Column descriptor</span></span> | <span data-ttu-id="9ec46-110">Stringa di definizione</span><span class="sxs-lookup"><span data-stu-id="9ec46-110">Definition string</span></span>                 |
|-------------------|-----------------------------------|
| <span data-ttu-id="9ec46-111">s?</span><span class="sxs-lookup"><span data-stu-id="9ec46-111">s?</span></span>                | <span data-ttu-id="9ec46-112">Stringa, lunghezza variabile (? = 1-255)</span><span class="sxs-lookup"><span data-stu-id="9ec46-112">String, variable length (?=1-255)</span></span> |
| <span data-ttu-id="9ec46-113">S0</span><span class="sxs-lookup"><span data-stu-id="9ec46-113">s0</span></span>                | <span data-ttu-id="9ec46-114">Stringa, lunghezza variabile</span><span class="sxs-lookup"><span data-stu-id="9ec46-114">String, variable length</span></span>           |
| <span data-ttu-id="9ec46-115">i2</span><span class="sxs-lookup"><span data-stu-id="9ec46-115">i2</span></span>                | <span data-ttu-id="9ec46-116">Valore short Integer</span><span class="sxs-lookup"><span data-stu-id="9ec46-116">Short integer</span></span>                     |
| <span data-ttu-id="9ec46-117">i4</span><span class="sxs-lookup"><span data-stu-id="9ec46-117">i4</span></span>                | <span data-ttu-id="9ec46-118">Long integer</span><span class="sxs-lookup"><span data-stu-id="9ec46-118">Long integer</span></span>                      |
| <span data-ttu-id="9ec46-119">V0</span><span class="sxs-lookup"><span data-stu-id="9ec46-119">v0</span></span>                | <span data-ttu-id="9ec46-120">Flusso binario</span><span class="sxs-lookup"><span data-stu-id="9ec46-120">Binary Stream</span></span>                     |
| <span data-ttu-id="9ec46-121">g?</span><span class="sxs-lookup"><span data-stu-id="9ec46-121">g?</span></span>                | <span data-ttu-id="9ec46-122">Stringa temporanea (? = 0-255)</span><span class="sxs-lookup"><span data-stu-id="9ec46-122">Temporary string (?=0-255)</span></span>        |
| <span data-ttu-id="9ec46-123">j?</span><span class="sxs-lookup"><span data-stu-id="9ec46-123">j?</span></span>                | <span data-ttu-id="9ec46-124">Integer temporaneo (? = 0, 1, 2, 4)</span><span class="sxs-lookup"><span data-stu-id="9ec46-124">Temporary integer (?=0,1,2,4)</span></span>     |
| <span data-ttu-id="9ec46-125">O0</span><span class="sxs-lookup"><span data-stu-id="9ec46-125">O0</span></span>                | <span data-ttu-id="9ec46-126">Oggetto temporaneo</span><span class="sxs-lookup"><span data-stu-id="9ec46-126">Temporary object</span></span>                  |



 

<span data-ttu-id="9ec46-127">Le stringhe utilizzate per descrivere le colonne hanno la seguente relazione con le stringhe di query SQL utilizzate da CREATE e ALTER.</span><span class="sxs-lookup"><span data-stu-id="9ec46-127">The strings used to describe columns have the following relationship to the SQL query strings used by CREATE and ALTER.</span></span> <span data-ttu-id="9ec46-128">Per altre informazioni, vedere [sintassi SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="9ec46-128">For more information, see [SQL Syntax](sql-syntax.md).</span></span>



| <span data-ttu-id="9ec46-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ec46-129">Returned value</span></span> | <span data-ttu-id="9ec46-130">Sintassi SQL</span><span class="sxs-lookup"><span data-stu-id="9ec46-130">SQL syntax</span></span>                |
|----------------|---------------------------|
| <span data-ttu-id="9ec46-131">S0</span><span class="sxs-lookup"><span data-stu-id="9ec46-131">s0</span></span>             | <span data-ttu-id="9ec46-132">LONGCHAR</span><span class="sxs-lookup"><span data-stu-id="9ec46-132">LONGCHAR</span></span>                  |
| <span data-ttu-id="9ec46-133">L0</span><span class="sxs-lookup"><span data-stu-id="9ec46-133">l0</span></span>             | <span data-ttu-id="9ec46-134">LONGCHAR LOCALIZZABILE</span><span class="sxs-lookup"><span data-stu-id="9ec46-134">LONGCHAR LOCALIZABLE</span></span>      |
| <span data-ttu-id="9ec46-135">s \#</span><span class="sxs-lookup"><span data-stu-id="9ec46-135">s \#</span></span>           | <span data-ttu-id="9ec46-136">CHAR ( \# )</span><span class="sxs-lookup"><span data-stu-id="9ec46-136">CHAR(\#)</span></span>                  |
| <span data-ttu-id="9ec46-137">s \#</span><span class="sxs-lookup"><span data-stu-id="9ec46-137">s \#</span></span>           | <span data-ttu-id="9ec46-138">CARATTERE ( \# )</span><span class="sxs-lookup"><span data-stu-id="9ec46-138">CHARACTER(\#)</span></span>             |
| <span data-ttu-id="9ec46-139">l \#</span><span class="sxs-lookup"><span data-stu-id="9ec46-139">l \#</span></span>           | <span data-ttu-id="9ec46-140">CHAR ( \# ) localizzabile</span><span class="sxs-lookup"><span data-stu-id="9ec46-140">CHAR(\#) LOCALIZABLE</span></span>      |
| <span data-ttu-id="9ec46-141">l \#</span><span class="sxs-lookup"><span data-stu-id="9ec46-141">l \#</span></span>           | <span data-ttu-id="9ec46-142">CHARACTER ( \# ) localizzabile</span><span class="sxs-lookup"><span data-stu-id="9ec46-142">CHARACTER(\#) LOCALIZABLE</span></span> |
| <span data-ttu-id="9ec46-143">i2</span><span class="sxs-lookup"><span data-stu-id="9ec46-143">i2</span></span>             | <span data-ttu-id="9ec46-144">SHORT</span><span class="sxs-lookup"><span data-stu-id="9ec46-144">SHORT</span></span>                     |
| <span data-ttu-id="9ec46-145">i2</span><span class="sxs-lookup"><span data-stu-id="9ec46-145">i2</span></span>             | <span data-ttu-id="9ec46-146">INT</span><span class="sxs-lookup"><span data-stu-id="9ec46-146">INT</span></span>                       |
| <span data-ttu-id="9ec46-147">i2</span><span class="sxs-lookup"><span data-stu-id="9ec46-147">i2</span></span>             | <span data-ttu-id="9ec46-148">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9ec46-148">INTEGER</span></span>                   |
| <span data-ttu-id="9ec46-149">i4</span><span class="sxs-lookup"><span data-stu-id="9ec46-149">i4</span></span>             | <span data-ttu-id="9ec46-150">LONG</span><span class="sxs-lookup"><span data-stu-id="9ec46-150">LONG</span></span>                      |
| <span data-ttu-id="9ec46-151">V0</span><span class="sxs-lookup"><span data-stu-id="9ec46-151">v0</span></span>             | <span data-ttu-id="9ec46-152">OBJECT</span><span class="sxs-lookup"><span data-stu-id="9ec46-152">OBJECT</span></span>                    |



 

<span data-ttu-id="9ec46-153">Se la lettera non è in maiuscolo, l'istruzione SQL deve essere aggiunta con NOT NULL.</span><span class="sxs-lookup"><span data-stu-id="9ec46-153">If the letter is not capitalized, the SQL statement should be appended with NOT NULL.</span></span>



| <span data-ttu-id="9ec46-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ec46-154">Returned value</span></span> | <span data-ttu-id="9ec46-155">Sintassi SQL</span><span class="sxs-lookup"><span data-stu-id="9ec46-155">SQL syntax</span></span>        |
|----------------|-------------------|
| <span data-ttu-id="9ec46-156">S0</span><span class="sxs-lookup"><span data-stu-id="9ec46-156">s0</span></span>             | <span data-ttu-id="9ec46-157">LONGCHAR NOT NULL</span><span class="sxs-lookup"><span data-stu-id="9ec46-157">LONGCHAR NOT NULL</span></span> |



 

<span data-ttu-id="9ec46-158">Il programma di installazione non limita internamente la lunghezza delle colonne al valore specificato dal formato di definizione della colonna.</span><span class="sxs-lookup"><span data-stu-id="9ec46-158">The installer does not internally limit the length of columns to the value specified by the column definition format.</span></span> <span data-ttu-id="9ec46-159">Se i dati immessi in un campo superano la lunghezza della colonna specificata, il pacchetto non supera la [convalida del pacchetto](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="9ec46-159">If the data entered into a field exceeds the specified column length, the package fails to pass [package validation](package-validation.md).</span></span> <span data-ttu-id="9ec46-160">Per passare la convalida in questo caso, è necessario modificare i dati o lo schema del database.</span><span class="sxs-lookup"><span data-stu-id="9ec46-160">To pass validation in this case, either the data or the database schema must be changed.</span></span> <span data-ttu-id="9ec46-161">Per modificare la lunghezza di colonna di una tabella standard è sufficiente esportare la tabella utilizzando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), modificare il file IDT esportato e quindi importare la tabella utilizzando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="9ec46-161">The only means to change the column length of a standard table is by exporting the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editing the exported .idt file, and then importing the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="9ec46-162">Gli autori non possono modificare i tipi di dati delle colonne, i valori null o gli attributi di localizzazione di tutte le colonne nelle tabelle standard.</span><span class="sxs-lookup"><span data-stu-id="9ec46-162">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="9ec46-163">Gli autori possono creare tabelle personalizzate con colonne con qualsiasi attributo di colonna.</span><span class="sxs-lookup"><span data-stu-id="9ec46-163">Authors can create custom tables with columns having any column attributes.</span></span>

<span data-ttu-id="9ec46-164">Quando si utilizza [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) per unire un database di riferimento in un database di destinazione, i nomi delle colonne, il numero di chiavi primarie e i tipi di dati di colonna devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="9ec46-164">When using [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to merge a reference database into a target database, the column names, number of primary keys, and column data types must match.</span></span> <span data-ttu-id="9ec46-165">**MsiDatabaseMerge** ignora gli attributi di localizzazione e di lunghezza della colonna.</span><span class="sxs-lookup"><span data-stu-id="9ec46-165">**MsiDatabaseMerge** ignores the localization and column length attributes.</span></span> <span data-ttu-id="9ec46-166">Se una colonna nel database di riferimento ha una lunghezza maggiore o uguale a 0 rispetto alla lunghezza della colonna nel database di destinazione, **MsiDatabaseMerge** aumenta la lunghezza della colonna nel database di destinazione fino alla lunghezza del database di riferimento.</span><span class="sxs-lookup"><span data-stu-id="9ec46-166">If a column in the reference database has a length that is 0 or greater than the that column's length in the target database, **MsiDatabaseMerge** increases the column length in the target database to the length in the reference database.</span></span>

<span data-ttu-id="9ec46-167">Quando si usa Mergmod.dll versione 2,0, l'applicazione di un modulo merge a un file con estensione msi non modifica mai la lunghezza delle colonne o i tipi di colonna di una tabella di database esistente.</span><span class="sxs-lookup"><span data-stu-id="9ec46-167">When using Mergmod.dll version 2.0, the application of a merge module to a .msi file never changes the length of columns or the column types of an existing database table.</span></span> <span data-ttu-id="9ec46-168">L'applicazione di un modulo merge può tuttavia modificare lo schema di una tabella di database esistente se il modulo aggiunge nuove colonne a una tabella per cui è valida aggiungere colonne.</span><span class="sxs-lookup"><span data-stu-id="9ec46-168">The application of a merge module can however change the schema of an existing database table if the module adds new columns to a table for which it is valid to add columns.</span></span> <span data-ttu-id="9ec46-169">Quando si utilizza una versione di Mergemod.dll inferiore alla versione 2,0, l'applicazione di un modulo merge non modifica mai la lunghezza delle colonne e non modifica mai lo schema del database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ec46-169">When using a Mergemod.dll version less than version 2.0, the application of a merge module never changes the length of columns and never changes the schema of the target database.</span></span>

 

 



