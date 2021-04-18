---
description: È possibile aggiungere informazioni di localizzazione a un database di installazione importando ed esportando i file di archivio di testo ASCII utilizzando MsiDatabaseExport e MsiDatabaseImport.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Gestione delle tabelle codici per le tabelle importate ed esportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308333"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a><span data-ttu-id="00d80-103">Gestione delle tabelle codici per le tabelle importate ed esportate</span><span class="sxs-lookup"><span data-stu-id="00d80-103">Code Page Handling of Imported and Exported Tables</span></span>

<span data-ttu-id="00d80-104">È possibile aggiungere informazioni di localizzazione a un database di installazione importando ed esportando i file di archivio di testo ASCII utilizzando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) e [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="00d80-104">You can add localization information to an installation database by importing and exporting ASCII text archive files using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) and [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="00d80-105">Poiché il pool di stringhe del database utilizza una tabella codici ANSI, il database e i [file di archivio di testo](text-archive-files.md) esportati dispongono di tabelle codici.</span><span class="sxs-lookup"><span data-stu-id="00d80-105">Because the database string pool uses an ANSI code page, both the database and exported [Text Archive Files](text-archive-files.md) have code pages.</span></span>

<span data-ttu-id="00d80-106">Quando un [file di archivio di testo](text-archive-files.md) viene esportato da un database, la tabella codici del file di archivio corrisponde al database padre.</span><span class="sxs-lookup"><span data-stu-id="00d80-106">When a [Text Archive File](text-archive-files.md) is exported from a database, the code page of the archive file is the same as the parent database.</span></span> <span data-ttu-id="00d80-107">Per un elenco di tabelle codici numeriche, vedere [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="00d80-107">For a list of numeric code pages, see [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).</span></span>

> [!Note]  
> <span data-ttu-id="00d80-108">L'esportazione di una tabella in un file di archivio di testo converte i caratteri di controllo in modo da evitare conflitti con i delimitatori di file.</span><span class="sxs-lookup"><span data-stu-id="00d80-108">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span>

 

## <a name="ascii-text-archive-files"></a><span data-ttu-id="00d80-109">File di archivio di testo ASCII</span><span class="sxs-lookup"><span data-stu-id="00d80-109">ASCII Text Archive Files</span></span>

<span data-ttu-id="00d80-110">I [file di archivio di testo](text-archive-files.md) ASCII esportati da [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) vengono illustrati nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="00d80-110">The ASCII [Text Archive Files](text-archive-files.md) exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) are explained in the following format:</span></span>

-   <span data-ttu-id="00d80-111">I nomi delle colonne della tabella vengono scritti nella prima riga.</span><span class="sxs-lookup"><span data-stu-id="00d80-111">The names of the table columns are written on the first line.</span></span>
-   <span data-ttu-id="00d80-112">I formati di colonna vengono scritti sulla seconda riga.</span><span class="sxs-lookup"><span data-stu-id="00d80-112">The column formats are written on the second line.</span></span>
-   <span data-ttu-id="00d80-113">Se la tabella contiene solo dati ASCII, la terza riga del file di testo è il nome della tabella seguito da un elenco delle chiavi primarie.</span><span class="sxs-lookup"><span data-stu-id="00d80-113">If the table contains only ASCII data, the third line of the text file is the table name followed by a list of the primary keys.</span></span>
-   <span data-ttu-id="00d80-114">Se la tabella contiene dati non ASCII e il database viene contrassegnato con una tabella codici numerica, il numero della tabella codici viene visualizzato all'inizio della terza riga.</span><span class="sxs-lookup"><span data-stu-id="00d80-114">If the table contains non-ASCII data and the database is stamped with a numeric code page, the code page number appears at the beginning of the third line.</span></span>
-   <span data-ttu-id="00d80-115">Se il database contiene dati non ASCII, ma il database non è contrassegnato con la tabella codici numerici, il numero della tabella codici di sistema corrente viene scritto all'inizio della terza riga.</span><span class="sxs-lookup"><span data-stu-id="00d80-115">If the database contains non-ASCII data, but the database is not stamped with the numeric code page, the current system code page number is written at the beginning of the third line.</span></span>
-   <span data-ttu-id="00d80-116">Le righe rimanenti del file di testo sono i dati nella tabella codici specificata.</span><span class="sxs-lookup"><span data-stu-id="00d80-116">The remaining lines of the text file are the data in the specified code page.</span></span>
-   <span data-ttu-id="00d80-117">Se una tabella contiene flussi, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) esporta ogni flusso della tabella in un file separato.</span><span class="sxs-lookup"><span data-stu-id="00d80-117">If a table contains streams, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exports each stream in the table to a separate file.</span></span>

### <a name="neutral-and-non-neutral-code-pages"></a><span data-ttu-id="00d80-118">Tabelle codici neutre e non neutre</span><span class="sxs-lookup"><span data-stu-id="00d80-118">Neutral and Non-Neutral Code Pages</span></span>

<span data-ttu-id="00d80-119">È possibile semplificare la localizzazione iniziando con un database con una tabella codici neutra:</span><span class="sxs-lookup"><span data-stu-id="00d80-119">You can facilitate localization by starting with a database that has a neutral code page:</span></span>

-   <span data-ttu-id="00d80-120">In un database vuoto è presente una tabella codici non associata ad alcun paese.</span><span class="sxs-lookup"><span data-stu-id="00d80-120">A blank database has a neutral code page.</span></span>
-   <span data-ttu-id="00d80-121">Un database che non contiene caratteri estesi che richiedono la rappresentazione di una tabella codici in ASCII presenta una tabella codici non associata ad alcun paese.</span><span class="sxs-lookup"><span data-stu-id="00d80-121">A database that does not contain extended characters that require a code page to be represented in ASCII has a neutral code page.</span></span>

<span data-ttu-id="00d80-122">Per ulteriori informazioni, vedere [la pagina relativa alla creazione di un database con una tabella codici indipendente](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="00d80-122">For more information, see [Creating a Database with a Neutral Code Page](creating-a-database-with-a-neutral-code-page.md).</span></span>

<span data-ttu-id="00d80-123">Le tabelle codici neutre e non neutre hanno le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="00d80-123">Neutral and non-neutral code pages have the following characteristics:</span></span>

-   <span data-ttu-id="00d80-124">Se un [file di archivio di testo](text-archive-files.md) con una tabella codici non neutra viene importato in un database con una tabella codici diversa da neutro, il programma di installazione restituisce un errore quando viene chiamato [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .</span><span class="sxs-lookup"><span data-stu-id="00d80-124">If a [Text Archive File](text-archive-files.md) with a non-neutral code page is imported into a database that has a different non-neutral code page, the Installer returns an error when [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) is called.</span></span>
-   <span data-ttu-id="00d80-125">Un [file di archivio di testo](text-archive-files.md) con una tabella codici neutra può essere importato in un database in cui è presente una tabella codici.</span><span class="sxs-lookup"><span data-stu-id="00d80-125">A [Text Archive File](text-archive-files.md) that has a neutral code page can be imported into a database that has any code page.</span></span>
-   <span data-ttu-id="00d80-126">Un [file di archivio di testo](text-archive-files.md) contenente una tabella codici può essere importato in un database con una tabella codici neutra.</span><span class="sxs-lookup"><span data-stu-id="00d80-126">A [Text Archive File](text-archive-files.md) that has any code page can be imported into a database that has a neutral code page.</span></span>
-   <span data-ttu-id="00d80-127">L'importazione di un [file di archivio di testo](text-archive-files.md) in un database con una tabella codici neutra imposta la tabella codici del database sulla tabella codici del file di archivio.</span><span class="sxs-lookup"><span data-stu-id="00d80-127">Importing a [Text Archive File](text-archive-files.md) into a database with a neutral code page sets the code page of the database to the archive file code page.</span></span> <span data-ttu-id="00d80-128">Tutti i file di archivio importati successivamente nel database devono avere la stessa tabella codici del primo file.</span><span class="sxs-lookup"><span data-stu-id="00d80-128">All archive files subsequently imported into the database must have the same code page as the first file.</span></span>

<span data-ttu-id="00d80-129">Per ulteriori informazioni, vedere la pagina relativa alla [determinazione di una tabella codici del database di installazione](determining-an-installation-database-s-code-page.md) e [l'impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="00d80-129">For more information, see [Determining an Installation Database Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

<span data-ttu-id="00d80-130">I [file di archivio di testo](text-archive-files.md) esportati da [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) possono essere usati con i sistemi di controllo della versione.</span><span class="sxs-lookup"><span data-stu-id="00d80-130">The [Text Archive Files](text-archive-files.md) that are exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) can be used with version control systems.</span></span> <span data-ttu-id="00d80-131">Utilizzare le [funzioni di database](database-functions.md) o un editor tabella di database per modificare il database.</span><span class="sxs-lookup"><span data-stu-id="00d80-131">Use the [Database Functions](database-functions.md) or a database table editor to edit the database.</span></span>

<span data-ttu-id="00d80-132">È possibile aggiungere informazioni di localizzazione a un database di installazione utilizzando un editor tabelle di database o l'API Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="00d80-132">You can add localization information to an installation database by using a database table editor or the Windows Installer API.</span></span> <span data-ttu-id="00d80-133">Per ulteriori informazioni, vedere la pagina relativa alla [gestione della tabella codici delle stringhe dei parametri](code-page-handling-of-parameter-strings.md).</span><span class="sxs-lookup"><span data-stu-id="00d80-133">For more information, see [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).</span></span>

 

 



