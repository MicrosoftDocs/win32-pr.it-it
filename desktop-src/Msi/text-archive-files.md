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
# <a name="text-archive-files"></a>File di archivio di testo

Le tabelle di database Windows Installer possono essere esportate in file di testo ASCII utilizzando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) o il metodo [**Export**](database-export.md) dell'oggetto di [**database**](database-object.md) . Le informazioni contenute in questi file di archivio di testo possono quindi essere importate di nuovo in un database di Windows Installer utilizzando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o il metodo di [importazione](database-import.md) dell'oggetto di **database** .

Strumenti come [msidb.exe](msidb-exe.md) sono in grado di esportare e importare file di archivio di testo. Vedere [esportare file](export-files.md) e [importare file](import-files.md) per [Windows Installer esempi di script](windows-installer-scripting-examples.md) in grado di esportare e importare file di archivio di testo da un database.

> [!Note]  
> I file di archivio di testo non sono intesi come mezzo per modificare il database di installazione. Per creare e modificare un pacchetto di installazione, è necessario utilizzare uno strumento di modifica della tabella Windows Installer, ad esempio [Orca](orca-exe.md) o uno strumento di terze parti.

 

I file di archivio di testo possono essere utilizzati per gli scopi seguenti.

-   I file di archivio di testo possono essere utilizzati con i sistemi di controllo della versione.
-   Per rimuovere lo spazio di archiviazione sprecato e ridurre le dimensioni finali dei file con estensione msi. Vedere [riduzione delle dimensioni di un file con estensione msi](reducing-the-size-of-an--msi-file.md).
-   Per aggiungere informazioni di localizzazione a un database di installazione. Per ulteriori informazioni, vedere [gestione di tabelle codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).

-   Per determinare la tabella codici di un database. Vedere [la pagina relativa alla determinazione della tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md).
-   Per impostare la tabella codici di un database. Vedere [impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).
-   Per aumentare il limite di una colonna di database. Esportare la tabella usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), modificare il file IDT esportato e quindi importare la tabella usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Gli autori non possono modificare i tipi di dati delle colonne, i valori null o gli attributi di localizzazione di tutte le colonne nelle tabelle standard. Vedere anche [creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md).

Nelle pagine seguenti vengono descritte le pagine di archivio del testo e i relativi formati.

-   [Formato file di archivio](archive-file-format.md)
-   [Dati ASCII nei file di archivio di testo](ascii-data-in-text-archive-files.md)
-   [\_ForceCodepage](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



