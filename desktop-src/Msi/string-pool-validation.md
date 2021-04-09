---
description: Il Windows Installer archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: Convalida String-Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130278"
---
# <a name="string-pool-validation"></a>Convalida String-Pool

Il Windows Installer archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni. L'unico mezzo per convalidare il pool di stringhe consiste nell'usare lo strumento MsiInfo disponibile in Windows Installer SDK.

La verifica del pool di stringhe è costituita da due controlli principali:

-   [Test di stringhe DBCS](#dbcs-string-tests)
-   [Verifica conteggio riferimenti](#reference-count-verification)

## <a name="dbcs-string-tests"></a>Test di stringhe DBCS

I test delle stringhe DBCS analizzano ogni stringa del database per due criteri: per i pacchetti con una tabella codici neutra contrassegnata, se un carattere è un carattere esteso (maggiore di 127), la stringa viene contrassegnata e viene visualizzato un messaggio che indica che la tabella codici del database non è valida perché questi caratteri richiedono che venga eseguito il rendering coerente di una tabella codici in tutti i sistemi

Se il database include una tabella codici, viene eseguita l'analisi di ogni stringa per un indicatore DBCS non valido. Se una stringa non neutra è stata contrassegnata in modo errato, i caratteri non vengono visualizzati correttamente. Questo problema si verifica in genere forzando la tabella codici su un valore specifico usando il \_ Tabella ForceCodepage con stringhe non neutre già presenti nel database. Si noti che questo controllo richiede che la tabella codici del database sia installata nel sistema.

Se si verifica un problema nella tabella codici, l'utente può correggere l'errore usando la \_ tabella ForceCodepage per forzare il valore appropriato della tabella codici del database. Per ulteriori informazioni, vedere la pagina relativa alla [gestione della tabella codici](code-page-handling-windows-installer-.md).

## <a name="reference-count-verification"></a>Verifica conteggio riferimenti

Per verificare i conteggi dei riferimenti di tutte le stringhe, viene eseguita l'analisi di ogni tabella per i valori stringa, viene mantenuto il conteggio di ogni stringa distinta e il risultato viene confrontato con il conteggio dei riferimenti archiviati nel pool di stringhe del database.

Se si verifica un problema di conteggio dei riferimenti di stringa, l'utente deve esportare immediatamente ogni tabella del database usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), creare un nuovo database e importare le tabelle nel nuovo database usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Il nuovo database dispone quindi dello stesso contenuto del vecchio database, ma i conteggi dei riferimenti di stringa sono corretti. L'aggiunta o l'eliminazione di dati da un database con un pool di stringhe danneggiato può aumentare il danneggiamento del database e la perdita di dati, quindi è importante eseguire rapidamente questi passaggi per evitare ulteriori perdite di dati.

Quando si ricompilano i database, ricordarsi di incorporare le archiviazioni e i flussi necessari nel nuovo database (vedere la tabella [ \_ flussi](-streams-table.md) tabella e [ \_ archiviazione](-storages-table.md)) e tenere presente i problemi della tabella codici. Ricordarsi inoltre di impostare tutte le proprietà del [flusso di informazioni di riepilogo](summary-information-stream.md) necessarie.

 

 



