---
description: Il Windows Installer archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni. Per un elenco di tabelle codici numeriche, vedere localizzazione delle tabelle Error e ActionText.
ms.assetid: 5d413fb7-99da-49f3-ace3-ec285df2e634
title: Gestione della tabella codici (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db2788a1bfc6bdb49ec1402d5bba8a1a2594b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308332"
---
# <a name="code-page-handling-windows-installer"></a>Gestione della tabella codici (Windows Installer)

Il Windows Installer archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni. Per un elenco di tabelle codici numeriche, vedere [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md).

Per ulteriori informazioni, [determinare la tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md).

Windows Installer utilizza [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) per determinare se la tabella codici è valida.

### <a name="localizing-a-windows-installer-package"></a>Localizzazione di un pacchetto di Windows Installer

Se si localizza un pacchetto di Windows Installer, è possibile che si verifichi la modifica delle informazioni nelle tabelle di database, l'esportazione delle tabelle nei file di archivio di testo ANSI e la successiva importazione dei file di archivio nel database in fase di localizzazione. È inoltre possibile aggiungere modifiche di localizzazione a un database utilizzando un editor tabelle di database o le [funzioni di database](database-functions.md). È importante impostare la tabella codici del database che viene localizzato prima di apportare eventuali modifiche di localizzazione al database. Non impostare la tabella codici del database dopo la localizzazione del database, perché ciò può danneggiare i caratteri estesi. Per ulteriori informazioni, vedere [impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).

L'approccio consigliato per la gestione delle tabelle codici consiste nel creare un database neutro che contenga solo caratteri che possono essere convertiti in qualsiasi tabella codici. Per ulteriori informazioni, vedere [la pagina relativa alla creazione di un database con una tabella codici indipendente](creating-a-database-with-a-neutral-code-page.md).

Se si aggiungono informazioni di localizzazione con i file di archivio del database, è possibile utilizzare [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) per esportare tabelle da un database che contiene le modifiche di localizzazione nei file di archivio di testo ANSI, quindi importarli nel database localizzato con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). La tabella codici di un file di archivio esportato è sempre uguale al relativo database padre. Le tabelle codici di un file importato e del database che riceve il file devono essere identiche oppure è necessario che almeno una delle due tabelle codici sia neutra. Per ulteriori informazioni, vedere [gestione di tabelle codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).

Se si aggiungono informazioni di localizzazione con un editor di testo o se le [funzioni di database](database-functions.md) fanno attenzione a passare solo parametri di stringa all'API Windows Installer che utilizza la tabella codici del database che si sta localizzando. Se un parametro di stringa contiene caratteri non rappresentati dalla tabella codici del database, si verifica un errore durante la chiamata a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Per ulteriori informazioni, vedere la pagina relativa alla [gestione della tabella codici delle stringhe dei parametri](code-page-handling-of-parameter-strings.md).

Se un pacchetto viene utilizzato per installare versioni in più lingue di un prodotto, la trasformazione utilizzata per localizzare le stringhe può anche modificare la tabella codici del database.

 

 
