---
description: Un file di archivio di testo per un database di Windows Installer contiene un'estensione del nome di file. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato file di archivio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881114"
---
# <a name="archive-file-format"></a><span data-ttu-id="0830a-103">Formato file di archivio</span><span class="sxs-lookup"><span data-stu-id="0830a-103">Archive File Format</span></span>

<span data-ttu-id="0830a-104">Un [file di archivio di testo](text-archive-files.md) per un database di Windows Installer contiene un'estensione del nome di file. IDT.</span><span class="sxs-lookup"><span data-stu-id="0830a-104">A [text archive file](text-archive-files.md) for a Windows Installer database carries an .idt file name extension.</span></span> <span data-ttu-id="0830a-105">Quando viene esportato un intero database nei file di archivio, ogni tabella nel database dispone di un file con estensione IDT separato.</span><span class="sxs-lookup"><span data-stu-id="0830a-105">When an entire database is exported to archive files, each table in the database has a separate .idt file.</span></span> <span data-ttu-id="0830a-106">Se una tabella contiene una colonna di flusso, ogni flusso della tabella è rappresentato da un file con estensione IBD.</span><span class="sxs-lookup"><span data-stu-id="0830a-106">If a table contains a stream column, each stream in the table is represented by a file with an .ibd file name extension.</span></span> <span data-ttu-id="0830a-107">I file con estensione IBD vengono archiviati in una cartella con lo stesso nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="0830a-107">The .ibd files are stored in a folder with the same name as the table.</span></span>

## <a name="idt-file-format"></a><span data-ttu-id="0830a-108">Formato file. IDT</span><span class="sxs-lookup"><span data-stu-id="0830a-108">.idt File Format</span></span>

<span data-ttu-id="0830a-109">Il file con estensione IDT di una tabella di database esportata contenente solo caratteri ASCII presenta il formato di base seguente.</span><span class="sxs-lookup"><span data-stu-id="0830a-109">The .idt file of an exported database table that contains only ASCII characters has the following basic format.</span></span>

-   <span data-ttu-id="0830a-110">La prima riga contiene i nomi delle colonne di tabella separati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="0830a-110">The first row contains the table column names separated by tabs.</span></span>
-   <span data-ttu-id="0830a-111">La seconda riga contiene le definizioni di colonna separate da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="0830a-111">The second row contains the column definitions separated by tabs.</span></span>
-   <span data-ttu-id="0830a-112">Se il file contiene solo dati ASCII, la terza riga è il nome della tabella e i nomi delle colonne chiave primaria separati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="0830a-112">If the file contain only ASCII data, the third row is table name and primary key column names separated by tabs.</span></span>
-   <span data-ttu-id="0830a-113">Le righe rimanenti nel file rappresentano le righe della tabella, con colonne separate da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="0830a-113">The remaining rows in the file represent rows in the table, with columns separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="0830a-114">Se il file contiene dati non ASCII, la terza riga è la tabella codici numerica seguita dal nome della tabella e dai nomi delle colonne di chiave primaria separati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="0830a-114">If the file contains non-ASCII data, the third row is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span> <span data-ttu-id="0830a-115">Un file con estensione IDT che contiene informazioni non ASCII deve essere salvato nel formato ASCII.</span><span class="sxs-lookup"><span data-stu-id="0830a-115">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="0830a-116">Un file di archivio di testo, ad esempio, può contenere i nomi di colonna e di tabella codificati come UTF-8, ma il file di archivio deve essere ASCII.</span><span class="sxs-lookup"><span data-stu-id="0830a-116">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span> <span data-ttu-id="0830a-117">Vedere la sezione [dati ASCII in file di archivio di testo](ascii-data-in-text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="0830a-117">See the section [ASCII Data in Text Archive Files](ascii-data-in-text-archive-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="0830a-118">I file [ \_ ForceCodepage](-forcecodepage.md) e [ \_ SummaryInformation](-summaryinformation.md) . IDT speciali utilizzano i formati estesi.</span><span class="sxs-lookup"><span data-stu-id="0830a-118">The special [\_ForceCodepage](-forcecodepage.md) and [\_SummaryInformation](-summaryinformation.md) .idt files use extended formats.</span></span> <span data-ttu-id="0830a-119">Per le \_ \_ descrizioni dei formati, vedere le sezioni ForceCodepage e SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="0830a-119">See the \_ForceCodepage and \_SummaryInformation sections for descriptions of their formats.</span></span>

 

## <a name="column-definitions"></a><span data-ttu-id="0830a-120">Definizioni di colonna</span><span class="sxs-lookup"><span data-stu-id="0830a-120">Column Definitions</span></span>

<span data-ttu-id="0830a-121">Le definizioni delle colonne sono indicate da caratteri.</span><span class="sxs-lookup"><span data-stu-id="0830a-121">Column definitions are indicated by characters.</span></span>

-   <span data-ttu-id="0830a-122">Il primo carattere indica il tipo di colonna.</span><span class="sxs-lookup"><span data-stu-id="0830a-122">The first character indicates the column type.</span></span> <span data-ttu-id="0830a-123">Una lettera minuscola indica una colonna che non ammette i valori null e una lettera maiuscola indica che la colonna può contenere valori null.</span><span class="sxs-lookup"><span data-stu-id="0830a-123">A lowercase letter indicates a non-nullable column and an uppercase letter indicates that the column can contain null values.</span></span>

    | <span data-ttu-id="0830a-124">Carattere</span><span class="sxs-lookup"><span data-stu-id="0830a-124">Character</span></span> | <span data-ttu-id="0830a-125">Significato</span><span class="sxs-lookup"><span data-stu-id="0830a-125">Meaning</span></span>                   |
    |-----------|---------------------------|
    | <span data-ttu-id="0830a-126">s, S</span><span class="sxs-lookup"><span data-stu-id="0830a-126">s, S</span></span>      | <span data-ttu-id="0830a-127">Colonna stringa</span><span class="sxs-lookup"><span data-stu-id="0830a-127">String Column</span></span>             |
    | <span data-ttu-id="0830a-128">l, L</span><span class="sxs-lookup"><span data-stu-id="0830a-128">l, L</span></span>      | <span data-ttu-id="0830a-129">Colonna stringa localizzabile</span><span class="sxs-lookup"><span data-stu-id="0830a-129">Localizable String Column</span></span> |
    | <span data-ttu-id="0830a-130">v, V</span><span class="sxs-lookup"><span data-stu-id="0830a-130">v, V</span></span>      | <span data-ttu-id="0830a-131">Colonna binaria</span><span class="sxs-lookup"><span data-stu-id="0830a-131">Binary Column</span></span>             |
    | <span data-ttu-id="0830a-132">i,</span><span class="sxs-lookup"><span data-stu-id="0830a-132">i, I</span></span>      | <span data-ttu-id="0830a-133">Colonna integer</span><span class="sxs-lookup"><span data-stu-id="0830a-133">Integer Column</span></span>            |

    

     

-   <span data-ttu-id="0830a-134">Il secondo carattere indica le dimensioni dei dati della colonna.</span><span class="sxs-lookup"><span data-stu-id="0830a-134">The second character indicates the column data size.</span></span>

    > [!Note]  
    > <span data-ttu-id="0830a-135">Il Windows Installer non utilizza effettivamente la dimensione della colonna specificata per limitare le dimensioni della stringa che è possibile immettere in un campo di colonna stringa.</span><span class="sxs-lookup"><span data-stu-id="0830a-135">The Windows Installer does not actually use the specified column size to limit the size of the string that can be entered into a string column field.</span></span> <span data-ttu-id="0830a-136">Tuttavia, alcuni strumenti di creazione utilizzano le dimensioni di colonna specificate per limitare le dimensioni di una stringa valida.</span><span class="sxs-lookup"><span data-stu-id="0830a-136">However, some authoring tools do use the specified column size to limit the size of a valid string.</span></span> <span data-ttu-id="0830a-137">È consigliabile che le stringhe immesse in una colonna soddisfino il requisito di dimensione specificato.</span><span class="sxs-lookup"><span data-stu-id="0830a-137">It is recommended that strings entered into any column meet the specified size requirement.</span></span>

     

    

    | <span data-ttu-id="0830a-138">Definizione di colonna</span><span class="sxs-lookup"><span data-stu-id="0830a-138">Column Definition</span></span> | <span data-ttu-id="0830a-139">Significato</span><span class="sxs-lookup"><span data-stu-id="0830a-139">Meaning</span></span>                                    |
    |-------------------|--------------------------------------------|
    | <span data-ttu-id="0830a-140">s255</span><span class="sxs-lookup"><span data-stu-id="0830a-140">s255</span></span>              | <span data-ttu-id="0830a-141">Lunghezza della colonna stringa non nullable 255</span><span class="sxs-lookup"><span data-stu-id="0830a-141">Non-Nullable String Column 255 long</span></span>        |
    | <span data-ttu-id="0830a-142">L50</span><span class="sxs-lookup"><span data-stu-id="0830a-142">L50</span></span>               | <span data-ttu-id="0830a-143">Lunghezza della colonna stringa localizzabile Nullable 50</span><span class="sxs-lookup"><span data-stu-id="0830a-143">Nullable Localizable String Column 50 long</span></span> |
    | <span data-ttu-id="0830a-144">I2, I2</span><span class="sxs-lookup"><span data-stu-id="0830a-144">i2, I2</span></span>            | <span data-ttu-id="0830a-145">Colonna short Integer</span><span class="sxs-lookup"><span data-stu-id="0830a-145">Short Integer Column</span></span>                       |
    | <span data-ttu-id="0830a-146">I4, I4</span><span class="sxs-lookup"><span data-stu-id="0830a-146">i4, I4</span></span>            | <span data-ttu-id="0830a-147">Colonna Long Integer</span><span class="sxs-lookup"><span data-stu-id="0830a-147">Long Integer Column</span></span>                        |

    

     

## <a name="control-character-translation"></a><span data-ttu-id="0830a-148">Conversione di caratteri di controllo</span><span class="sxs-lookup"><span data-stu-id="0830a-148">Control Character Translation</span></span>

<span data-ttu-id="0830a-149">L'esportazione di una tabella in un file di archivio di testo converte i caratteri di controllo in modo da evitare conflitti con i delimitatori di file.</span><span class="sxs-lookup"><span data-stu-id="0830a-149">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span> <span data-ttu-id="0830a-150">Durante la scrittura nel file con estensione IDT, i caratteri di controllo vengono convertiti come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0830a-150">While writing into the .idt file, the control characters are translated as follows.</span></span>



| <span data-ttu-id="0830a-151">Carattere di controllo</span><span class="sxs-lookup"><span data-stu-id="0830a-151">Control Character</span></span> | <span data-ttu-id="0830a-152">Traduzione in. IDT</span><span class="sxs-lookup"><span data-stu-id="0830a-152">Translation in .idt</span></span> | <span data-ttu-id="0830a-153">Significato</span><span class="sxs-lookup"><span data-stu-id="0830a-153">Meaning</span></span>         |
|-------------------|---------------------|-----------------|
| <span data-ttu-id="0830a-154">NULL</span><span class="sxs-lookup"><span data-stu-id="0830a-154">NULL</span></span>              | <span data-ttu-id="0830a-155">21</span><span class="sxs-lookup"><span data-stu-id="0830a-155">21</span></span>                  | <span data-ttu-id="0830a-156">Null</span><span class="sxs-lookup"><span data-stu-id="0830a-156">Null</span></span>            |
| <span data-ttu-id="0830a-157">BS</span><span class="sxs-lookup"><span data-stu-id="0830a-157">BS</span></span>                | <span data-ttu-id="0830a-158">27</span><span class="sxs-lookup"><span data-stu-id="0830a-158">27</span></span>                  | <span data-ttu-id="0830a-159">Spazio indietro</span><span class="sxs-lookup"><span data-stu-id="0830a-159">Back Space</span></span>      |
| <span data-ttu-id="0830a-160">HT</span><span class="sxs-lookup"><span data-stu-id="0830a-160">HT</span></span>                | <span data-ttu-id="0830a-161">16</span><span class="sxs-lookup"><span data-stu-id="0830a-161">16</span></span>                  | <span data-ttu-id="0830a-162">Scheda</span><span class="sxs-lookup"><span data-stu-id="0830a-162">Tab</span></span>             |
| <span data-ttu-id="0830a-163">Se</span><span class="sxs-lookup"><span data-stu-id="0830a-163">LF</span></span>                | <span data-ttu-id="0830a-164">25</span><span class="sxs-lookup"><span data-stu-id="0830a-164">25</span></span>                  | <span data-ttu-id="0830a-165">avanzamento riga</span><span class="sxs-lookup"><span data-stu-id="0830a-165">Line Feed</span></span>       |
| <span data-ttu-id="0830a-166">FF</span><span class="sxs-lookup"><span data-stu-id="0830a-166">FF</span></span>                | <span data-ttu-id="0830a-167">24</span><span class="sxs-lookup"><span data-stu-id="0830a-167">24</span></span>                  | <span data-ttu-id="0830a-168">Feed form</span><span class="sxs-lookup"><span data-stu-id="0830a-168">Form Feed</span></span>       |
| <span data-ttu-id="0830a-169">CR</span><span class="sxs-lookup"><span data-stu-id="0830a-169">CR</span></span>                | <span data-ttu-id="0830a-170">17</span><span class="sxs-lookup"><span data-stu-id="0830a-170">17</span></span>                  | <span data-ttu-id="0830a-171">ritorno a capo</span><span class="sxs-lookup"><span data-stu-id="0830a-171">Carriage Return</span></span> |



 

 

 



