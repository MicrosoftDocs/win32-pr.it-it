---
description: È possibile aggiungere informazioni di localizzazione a un database di installazione usando un editor di tabelle di database, ad esempio Orca, fornito con l'SDK del programma di installazione di Windows o chiamando funzioni di database da un'applicazione.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Gestione delle stringhe di parametro nella tabella codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37555b905c60cb8f4727ccb723435d28b24d41d3aca1fc7026e34b799e25414a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328340"
---
# <a name="code-page-handling-of-parameter-strings"></a>Gestione delle stringhe di parametro nella tabella codici

È possibile aggiungere informazioni di localizzazione a un database di installazione usando un editor di tabelle di database, [](database-functions.md) ad esempio Orca, fornito con l'SDK del programma di installazione di Windows o chiamando funzioni di database da un'applicazione. Prestare attenzione a passare solo i parametri stringa che usano la tabella codici del database localizzato. Se un parametro stringa contiene caratteri che non possono essere rappresentati dalla tabella codici del database, il programma di installazione restituisce un errore quando si chiama [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Per un elenco di tabelle codici numeriche, vedere [Localizzazione delle tabelle Error e ActionText.](localizing-the-error-and-actiontext-tables.md)

Per altre informazioni, vedere [Determinazione della tabella codici di un database di installazione.](determining-an-installation-database-s-code-page.md)

## <a name="adding-localization-information-to-a-database"></a>Aggiunta di informazioni di localizzazione a un database

Quando si aggiungono informazioni di localizzazione a un database, la tabella codici del database deve essere supportata dal sistema operativo. Non deve essere la tabella codici corrente del sistema. [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) deve restituire **TRUE per** la tabella codici del database. Poiché il sistema converte le stringhe ANSI in Unicode, si verifica un errore se la tabella codici dell'utente corrente non corrisponde alla tabella codici del database.

La chiamata alla versione ANSI dell'API Windows Installer converte la stringa localizzata in Unicode usando la tabella codici di sistema corrente. Quando viene eseguito il commit del database, la stringa Unicode viene convertita in ANSI usando la tabella codici del database. Se la tabella codici del sistema corrente è diversa dalla tabella codici della stringa localizzata, il risultato può essere una perdita di dati e una conversione di stringa non corretta.

La procedura seguente illustra come archiviare i dati di localizzazione.

**Per archiviare i dati di localizzazione**

1.  Impostare la tabella codici del database sulla tabella codici della stringa localizzata.
2.  Convertire la stringa ANSI in Unicode usando la [**funzione MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e specificare la tabella codici dei dati localizzati.
3.  Chiamare la versione Unicode dell'API Windows Installer usando la stringa Unicode per aggiungere i dati localizzati.
4.  Eseguire il commit delle modifiche di localizzazione nel database [**usando MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

È anche possibile aggiungere informazioni di localizzazione a un database di installazione importando ed esportando file di archivio di testo ASCII. Per altre informazioni, vedere [Gestione della tabella codici delle tabelle importate ed esportate.](code-page-handling-of-imported-and-exported-tables.md)

 

 
