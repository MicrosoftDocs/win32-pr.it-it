---
description: È possibile aggiungere informazioni di localizzazione a un database di installazione utilizzando un editor tabelle di database, ad esempio ORCA fornito con l'SDK di Windows Installer o chiamando le funzioni di database da un'applicazione.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Gestione della tabella codici delle stringhe di parametro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a52872472d5509e1abdf35aa12be5afb6a8d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226357"
---
# <a name="code-page-handling-of-parameter-strings"></a>Gestione della tabella codici delle stringhe di parametro

È possibile aggiungere informazioni di localizzazione a un database di installazione utilizzando un editor tabelle di database, ad esempio ORCA fornito con l'SDK di Windows Installer o chiamando le [funzioni di database](database-functions.md) da un'applicazione. Prestare attenzione a passare solo i parametri di stringa che usano la tabella codici del database in fase di localizzazione. Se un parametro di stringa contiene caratteri che non possono essere rappresentati dalla tabella codici del database, il programma di installazione restituisce un errore durante la chiamata a [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Per un elenco di tabelle codici numeriche, vedere [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md).

Per ulteriori informazioni, vedere la pagina relativa alla [determinazione della tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md).

## <a name="adding-localization-information-to-a-database"></a>Aggiunta di informazioni di localizzazione a un database

Quando si aggiungono informazioni di localizzazione a un database, la tabella codici del database deve essere supportata dal sistema operativo. Non è necessario che sia la tabella codici corrente del sistema. [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) deve restituire **true** per la tabella codici del database. Poiché il sistema converte le stringhe ANSI in Unicode, si verifica un errore se la tabella codici dell'utente corrente non corrisponde alla tabella codici del database.

La chiamata della versione ANSI dell'API Windows Installer converte la stringa localizzata in Unicode usando la tabella codici di sistema corrente. Quando viene eseguito il commit del database, la stringa Unicode viene convertita in ANSI utilizzando la tabella codici del database. Se la tabella codici di sistema corrente è diversa dalla tabella codici della stringa localizzata, il risultato può essere una perdita di dati e una conversione di stringa non corretta.

Nella procedura riportata di seguito viene illustrato come archiviare i dati di localizzazione.

**Per archiviare i dati di localizzazione**

1.  Impostare la tabella codici del database sulla tabella codici della stringa localizzata.
2.  Convertire la stringa ANSI in Unicode usando la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e specificare la tabella codici dei dati localizzati.
3.  Chiamare la versione Unicode dell'API Windows Installer usando la stringa Unicode per aggiungere i dati localizzati.
4.  Eseguire il commit delle modifiche di localizzazione nel database tramite [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

È inoltre possibile aggiungere informazioni di localizzazione a un database di installazione importando ed esportando i file di archivio di testo ASCII. Per ulteriori informazioni, vedere [gestione di tabelle codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).

 

 
