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
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Gestione delle tabelle codici per le tabelle importate ed esportate

È possibile aggiungere informazioni di localizzazione a un database di installazione importando ed esportando i file di archivio di testo ASCII utilizzando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) e [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Poiché il pool di stringhe del database utilizza una tabella codici ANSI, il database e i [file di archivio di testo](text-archive-files.md) esportati dispongono di tabelle codici.

Quando un [file di archivio di testo](text-archive-files.md) viene esportato da un database, la tabella codici del file di archivio corrisponde al database padre. Per un elenco di tabelle codici numeriche, vedere [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md).

> [!Note]  
> L'esportazione di una tabella in un file di archivio di testo converte i caratteri di controllo in modo da evitare conflitti con i delimitatori di file.

 

## <a name="ascii-text-archive-files"></a>File di archivio di testo ASCII

I [file di archivio di testo](text-archive-files.md) ASCII esportati da [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) vengono illustrati nel formato seguente:

-   I nomi delle colonne della tabella vengono scritti nella prima riga.
-   I formati di colonna vengono scritti sulla seconda riga.
-   Se la tabella contiene solo dati ASCII, la terza riga del file di testo è il nome della tabella seguito da un elenco delle chiavi primarie.
-   Se la tabella contiene dati non ASCII e il database viene contrassegnato con una tabella codici numerica, il numero della tabella codici viene visualizzato all'inizio della terza riga.
-   Se il database contiene dati non ASCII, ma il database non è contrassegnato con la tabella codici numerici, il numero della tabella codici di sistema corrente viene scritto all'inizio della terza riga.
-   Le righe rimanenti del file di testo sono i dati nella tabella codici specificata.
-   Se una tabella contiene flussi, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) esporta ogni flusso della tabella in un file separato.

### <a name="neutral-and-non-neutral-code-pages"></a>Tabelle codici neutre e non neutre

È possibile semplificare la localizzazione iniziando con un database con una tabella codici neutra:

-   In un database vuoto è presente una tabella codici non associata ad alcun paese.
-   Un database che non contiene caratteri estesi che richiedono la rappresentazione di una tabella codici in ASCII presenta una tabella codici non associata ad alcun paese.

Per ulteriori informazioni, vedere [la pagina relativa alla creazione di un database con una tabella codici indipendente](creating-a-database-with-a-neutral-code-page.md).

Le tabelle codici neutre e non neutre hanno le caratteristiche seguenti:

-   Se un [file di archivio di testo](text-archive-files.md) con una tabella codici non neutra viene importato in un database con una tabella codici diversa da neutro, il programma di installazione restituisce un errore quando viene chiamato [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .
-   Un [file di archivio di testo](text-archive-files.md) con una tabella codici neutra può essere importato in un database in cui è presente una tabella codici.
-   Un [file di archivio di testo](text-archive-files.md) contenente una tabella codici può essere importato in un database con una tabella codici neutra.
-   L'importazione di un [file di archivio di testo](text-archive-files.md) in un database con una tabella codici neutra imposta la tabella codici del database sulla tabella codici del file di archivio. Tutti i file di archivio importati successivamente nel database devono avere la stessa tabella codici del primo file.

Per ulteriori informazioni, vedere la pagina relativa alla [determinazione di una tabella codici del database di installazione](determining-an-installation-database-s-code-page.md) e [l'impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).

I [file di archivio di testo](text-archive-files.md) esportati da [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) possono essere usati con i sistemi di controllo della versione. Utilizzare le [funzioni di database](database-functions.md) o un editor tabella di database per modificare il database.

È possibile aggiungere informazioni di localizzazione a un database di installazione utilizzando un editor tabelle di database o l'API Windows Installer. Per ulteriori informazioni, vedere la pagina relativa alla [gestione della tabella codici delle stringhe dei parametri](code-page-handling-of-parameter-strings.md).

 

 



