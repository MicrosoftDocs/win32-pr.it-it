---
description: Il Windows di installazione archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: String-Pool convalida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e895a9e9032cb0cf5d94b5a8c3c9070c46fe79041dee41e4ea10366043b4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627361"
---
# <a name="string-pool-validation"></a>String-Pool convalida

Il Windows di installazione archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni. L'unico modo per convalidare il pool di stringhe è usare lo strumento MsiInfo disponibile in Windows Installer SDK.

La verifica del pool di stringhe è costituita da due controlli principali:

-   [Test delle stringhe DBCS](#dbcs-string-tests)
-   [Verifica del conteggio dei riferimenti](#reference-count-verification)

## <a name="dbcs-string-tests"></a>Test delle stringhe DBCS

I test della stringa DBCS analizzano ogni stringa nel database per due criteri: per i pacchetti con una tabella codici neutra contrassegnata, se un carattere è un carattere esteso (maggiore di 127), la stringa viene contrassegnata e viene visualizzato un messaggio che indica che la tabella codici del database non è valida perché questi caratteri richiedono che il rendering di una tabella codici specifica sia coerente in tutti i sistemi.

Se il database include una tabella codici, viene eseguita l'analisi di ogni stringa alla ricerca di un indicatore DBCS non valido. Se una stringa non neutra è stata contrassegnata in modo non corretto, il rendering dei caratteri non verrà eseguito correttamente. Questo errore si verifica in genere forzando la tabella codici a un valore specifico usando \_ Tabella ForceCodepage con stringhe non neutre già presenti nel database. Si noti che questo controllo richiede che la tabella codici del database sia installata nel sistema.

Se si verifica un problema della tabella codici, l'utente può correggere l'errore usando la tabella ForceCodepage per forzare la tabella codici \_ del database al valore appropriato. Per altre informazioni, vedere [Gestione della tabella codici.](code-page-handling-windows-installer-.md)

## <a name="reference-count-verification"></a>Verifica del conteggio dei riferimenti

Per verificare i conteggi dei riferimenti di tutte le stringhe, in ogni tabella viene eseguita l'analisi dei valori stringa, viene mantenuto il conteggio di ogni stringa distinta e il risultato viene confrontato con il conteggio dei riferimenti archiviati nel pool di stringhe di database.

Se si verifica un problema di conteggio dei riferimenti alle stringhe, l'utente deve esportare immediatamente ogni tabella del database usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), creare un nuovo database e importare le tabelle nel nuovo database usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Il nuovo database ha quindi lo stesso contenuto del database precedente, ma i conteggi dei riferimenti alle stringhe sono corretti. L'aggiunta o l'eliminazione di dati da un database con un pool di stringhe danneggiato può aumentare il danneggiamento del database e la perdita di dati, quindi eseguire rapidamente questi passaggi è importante per evitare ulteriori perdite di dati.

Quando si ricompilano i database, ricordarsi di incorporare le risorse di archiviazione e i flussi necessari nel nuovo database (vedere tabella [ \_ Flussi](-streams-table.md) e tabella di [ \_ archiviazione)](-storages-table.md)e di essere a conoscenza dei problemi della tabella codici. Ricordarsi anche di impostare ognuna delle proprietà [del flusso di informazioni di riepilogo](summary-information-stream.md) necessarie.

 

 



