---
description: È possibile aggiungere informazioni di localizzazione a un database di installazione importando ed esportando file di archivio di testo ASCII usando MsiDatabaseExport e MsiDatabaseImport.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Gestione delle tabelle codici delle tabelle importate ed esportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9a64617ccfda25380076d62e6dd4ad8c18c55f68afd0236b3258638c899f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066001"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Gestione delle tabelle codici delle tabelle importate ed esportate

È possibile aggiungere informazioni di localizzazione a un database di installazione importando ed esportando file di archivio di testo ASCII usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) [**e MsiDatabaseImport.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) Poiché il pool di stringhe di database usa una tabella codici ANSI, sia il database che i file di archivio di testo [esportati](text-archive-files.md) dispongono di tabelle codici.

Quando un [file di archivio](text-archive-files.md) di testo viene esportato da un database, la tabella codici del file di archivio corrisponde al database padre. Per un elenco di tabelle codici numeriche, vedere [Localizzazione delle tabelle Error e ActionText.](localizing-the-error-and-actiontext-tables.md)

> [!Note]  
> L'esportazione di una tabella in un file di archivio di testo converte i caratteri di controllo per evitare conflitti con i delimitatori di file.

 

## <a name="ascii-text-archive-files"></a>File di archivio di testo ASCII

I file [di archivio di testo](text-archive-files.md) ASCII esportati da [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) sono illustrati nel formato seguente:

-   I nomi delle colonne della tabella vengono scritti nella prima riga.
-   I formati di colonna vengono scritti nella seconda riga.
-   Se la tabella contiene solo dati ASCII, la terza riga del file di testo è il nome della tabella seguito da un elenco di chiavi primarie.
-   Se la tabella contiene dati non ASCII e il database è contrassegnato con una tabella codici numerica, il numero della tabella codici viene visualizzato all'inizio della terza riga.
-   Se il database contiene dati non ASCII, ma il database non è contrassegnato con la tabella codici numerica, il numero della tabella codici di sistema corrente viene scritto all'inizio della terza riga.
-   Le righe rimanenti del file di testo sono i dati nella tabella codici specificata.
-   Se una tabella contiene flussi, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) esporta ogni flusso della tabella in un file separato.

### <a name="neutral-and-non-neutral-code-pages"></a>Tabella codici neutra e non neutra

È possibile semplificare la localizzazione iniziando con un database con una tabella codici neutra:

-   Un database vuoto ha una tabella codici neutra.
-   Un database che non contiene caratteri estesi che richiedono una tabella codici da rappresentare in ASCII ha una tabella codici neutra.

Per altre informazioni, vedere [Creazione di un database con una tabella codici neutra.](creating-a-database-with-a-neutral-code-page.md)

Le tabelle codici neutre e non neutre hanno le caratteristiche seguenti:

-   Se un [file](text-archive-files.md) di archivio di testo con una tabella codici non neutra viene importato in un database con una tabella codici diversa da quella non neutra, il programma di installazione restituisce un errore quando viene chiamato [**MsiDatabaseImport.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   Un [file di archivio di](text-archive-files.md) testo con una tabella codici neutra può essere importato in un database con qualsiasi tabella codici.
-   Un [file di archivio di](text-archive-files.md) testo con qualsiasi tabella codici può essere importato in un database con una tabella codici neutra.
-   L'importazione [di un file di](text-archive-files.md) archivio di testo in un database con una tabella codici neutra imposta la tabella codici del database sulla tabella codici del file di archivio. Tutti i file di archivio successivamente importati nel database devono avere la stessa tabella codici del primo file.

Per altre informazioni, vedere [Determinazione di una tabella codici del database di installazione](determining-an-installation-database-s-code-page.md) e Impostazione della tabella codici di un [database.](setting-the-code-page-of-a-database.md)

I [file di archivio di](text-archive-files.md) testo esportati da [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) possono essere usati con i sistemi di controllo della versione. Usare Funzioni [di database o](database-functions.md) un editor di tabelle di database per modificare il database.

È possibile aggiungere informazioni di localizzazione a un database di installazione usando un editor di tabelle di database o l'API Windows Installer. Per altre informazioni, vedere [Gestione della tabella codici delle stringhe di parametro.](code-page-handling-of-parameter-strings.md)

 

 



