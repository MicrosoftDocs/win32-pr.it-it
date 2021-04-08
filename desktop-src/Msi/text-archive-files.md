---
description: Le tabelle di database Windows Installer possono essere esportate in file di testo ASCII utilizzando MsiDatabaseExport o il metodo Export dell'oggetto di database.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: File di archivio di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882389"
---
# <a name="text-archive-files"></a><span data-ttu-id="713b2-103">File di archivio di testo</span><span class="sxs-lookup"><span data-stu-id="713b2-103">Text Archive Files</span></span>

<span data-ttu-id="713b2-104">Le tabelle di database Windows Installer possono essere esportate in file di testo ASCII utilizzando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) o il metodo [**Export**](database-export.md) dell'oggetto di [**database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="713b2-104">The Windows Installer database tables can be exported to ASCII text files by using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) or the [**Export**](database-export.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="713b2-105">Le informazioni contenute in questi file di archivio di testo possono quindi essere importate di nuovo in un database di Windows Installer utilizzando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o il metodo di [importazione](database-import.md) dell'oggetto di **database** .</span><span class="sxs-lookup"><span data-stu-id="713b2-105">The information in these text archive files can then be imported back into a Windows Installer database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the **Database** object.</span></span>

<span data-ttu-id="713b2-106">Strumenti come [msidb.exe](msidb-exe.md) sono in grado di esportare e importare file di archivio di testo.</span><span class="sxs-lookup"><span data-stu-id="713b2-106">Tools such as [msidb.exe](msidb-exe.md) are capable of exporting and importing text archive files.</span></span> <span data-ttu-id="713b2-107">Vedere [esportare file](export-files.md) e [importare file](import-files.md) per [Windows Installer esempi di script](windows-installer-scripting-examples.md) in grado di esportare e importare file di archivio di testo da un database.</span><span class="sxs-lookup"><span data-stu-id="713b2-107">See [Export Files](export-files.md) and [Import Files](import-files.md) for [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) that can export and import text archive files from a database.</span></span>

> [!Note]  
> <span data-ttu-id="713b2-108">I file di archivio di testo non sono intesi come mezzo per modificare il database di installazione.</span><span class="sxs-lookup"><span data-stu-id="713b2-108">Text archive files are not intended as a means to edit the installation database.</span></span> <span data-ttu-id="713b2-109">Per creare e modificare un pacchetto di installazione, è necessario utilizzare uno strumento di modifica della tabella Windows Installer, ad esempio [Orca](orca-exe.md) o uno strumento di terze parti.</span><span class="sxs-lookup"><span data-stu-id="713b2-109">You should use a Windows Installer table editing tool, such as [Orca](orca-exe.md) or a third-party tool, to create and modify an installation package.</span></span>

 

<span data-ttu-id="713b2-110">I file di archivio di testo possono essere utilizzati per gli scopi seguenti.</span><span class="sxs-lookup"><span data-stu-id="713b2-110">Text archive files can be used for the following purposes.</span></span>

-   <span data-ttu-id="713b2-111">I file di archivio di testo possono essere utilizzati con i sistemi di controllo della versione.</span><span class="sxs-lookup"><span data-stu-id="713b2-111">Text archive files can be used with version control systems.</span></span>
-   <span data-ttu-id="713b2-112">Per rimuovere lo spazio di archiviazione sprecato e ridurre le dimensioni finali dei file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="713b2-112">To remove wasted storage space and reduce the final size of .msi files.</span></span> <span data-ttu-id="713b2-113">Vedere [riduzione delle dimensioni di un file con estensione msi](reducing-the-size-of-an--msi-file.md).</span><span class="sxs-lookup"><span data-stu-id="713b2-113">See [Reducing the Size of an .msi File](reducing-the-size-of-an--msi-file.md).</span></span>
-   <span data-ttu-id="713b2-114">Per aggiungere informazioni di localizzazione a un database di installazione.</span><span class="sxs-lookup"><span data-stu-id="713b2-114">To add localization information to an installation database.</span></span> <span data-ttu-id="713b2-115">Per ulteriori informazioni, vedere [gestione di tabelle codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="713b2-115">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

-   <span data-ttu-id="713b2-116">Per determinare la tabella codici di un database.</span><span class="sxs-lookup"><span data-stu-id="713b2-116">To determine the code page of a database.</span></span> <span data-ttu-id="713b2-117">Vedere [la pagina relativa alla determinazione della tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="713b2-117">See [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>
-   <span data-ttu-id="713b2-118">Per impostare la tabella codici di un database.</span><span class="sxs-lookup"><span data-stu-id="713b2-118">To set the code page of a database.</span></span> <span data-ttu-id="713b2-119">Vedere [impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="713b2-119">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="713b2-120">Per aumentare il limite di una colonna di database.</span><span class="sxs-lookup"><span data-stu-id="713b2-120">To increase the limit of a database column.</span></span> <span data-ttu-id="713b2-121">Esportare la tabella usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), modificare il file IDT esportato e quindi importare la tabella usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="713b2-121">Export the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edit the exported .idt file, and then import the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="713b2-122">Gli autori non possono modificare i tipi di dati delle colonne, i valori null o gli attributi di localizzazione di tutte le colonne nelle tabelle standard.</span><span class="sxs-lookup"><span data-stu-id="713b2-122">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="713b2-123">Vedere anche [creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="713b2-123">See also [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="713b2-124">Nelle pagine seguenti vengono descritte le pagine di archivio del testo e i relativi formati.</span><span class="sxs-lookup"><span data-stu-id="713b2-124">The following pages describe text archive pages and their formats.</span></span>

-   [<span data-ttu-id="713b2-125">Formato file di archivio</span><span class="sxs-lookup"><span data-stu-id="713b2-125">Archive File Format</span></span>](archive-file-format.md)
-   [<span data-ttu-id="713b2-126">Dati ASCII nei file di archivio di testo</span><span class="sxs-lookup"><span data-stu-id="713b2-126">ASCII Data in Text Archive Files</span></span>](ascii-data-in-text-archive-files.md)
-   [<span data-ttu-id="713b2-127">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="713b2-127">\_ForceCodepage</span></span>](-forcecodepage.md)
-   [<span data-ttu-id="713b2-128">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="713b2-128">\_SummaryInformation</span></span>](-summaryinformation.md)

 

 



