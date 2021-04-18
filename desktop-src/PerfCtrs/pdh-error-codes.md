---
description: Tutte le funzioni PDH (Performance Data Helper) restituiscono un valore di tipo PDH \_ status.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Codici di errore dell'helper Dati di prestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0417801b4f7a23e48a74201aa48193987a0edee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312155"
---
# <a name="performance-data-helper-error-codes"></a>Codici di errore dell'helper Dati di prestazione

Tutte le funzioni PDH (Performance Data Helper) restituiscono un valore di tipo **PDH \_ status**. Se la funzione ha esito positivo, il valore restituito è `ERROR_SUCCESS` . In caso contrario, la funzione restituisce un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di errore PDH. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) , come illustrato nell'esempio seguente.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD_PTR pArgs[] = { (DWORD_PTR)L"<collectionname>" };
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE
                       FORMAT_MESSAGE_ALLOCATE_BUFFER
                       FORMAT_MESSAGE_IGNORE_INSERTS,
                       hPdhLibrary,
                       dwErrorCode,
                       0,
                       (LPWSTR)&pMessage,
                       0,
                       NULL))
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
        return;
    }

    wprintf(L"Formatted message: %ls\n", pMessage);
    LocalFree(pMessage);
}
```

Per le funzioni di raccolta e formattazione dei dati, è importante ricordare che il valore restituito della funzione indica l'esito positivo o negativo della chiamata di funzione e non necessariamente quella dei dati del contatore. Controllare sempre il membro **CStatus** del valore del contatore restituito per verificare che i dati restituiti siano validi prima di usarli. Se il valore del membro **CStatus** non indica esito positivo, non usare i dati.

Nella tabella seguente viene fornito un elenco di codici di errore specifici per PDH. Questi valori vengono definiti nel `pdhmsg.h` file di intestazione.

| Codice di errore                                                   | Descrizione
|--------------------------------------------------------------|------------
| 0x00000000 (PDH \_ CSTATUS \_ \_ dati validi)                       | I dati restituiti sono validi.
| 0x00000001 (PDH \_ CSTATUS \_ New \_ Data)                         | Il valore dei dati restituiti è valido e diverso dall'ultimo campione.
| 0x800007D0 (PDH \_ CSTATUS \_ No \_ Machine)                       | Impossibile connettersi al computer specificato oppure il computer è offline.
| 0x800007D1 (PDH \_ CSTATUS \_ Nessuna \_ istanza)                      | L'istanza specificata non è presente.
| 0x800007D2 ( \_ altri dati di PDH \_ )                                 | Sono presenti più dati da restituire rispetto al buffer fornito. Allocare un buffer più grande e chiamare di nuovo la funzione.
| 0x800007D3 ( \_ elemento CSTATUS \_ PDH \_ non \_ convalidato)              | L'elemento dati è stato aggiunto alla query ma non è stato convalidato né accessibile. Non sono disponibili altre informazioni sullo stato dell'elemento dati.
| 0x800007D4 ( \_ nuovo tentativo PDH)                                      | È necessario ritentare l'operazione selezionata.
| 0x800007D5 (PDH \_ nessun \_ dato)                                   | Nessun dato da restituire.
| 0x800007D6 ( \_ \_ denominatore PDH calcolo negativo \_ )                | Rilevato un contatore con un valore denominatore negativo.
| 0x800007D7 (PDH \_ Calc \_ negative \_ TIMEBASE)                   | È stato rilevato un contatore con un valore di base temporale negativo.
| 0x800007D8 ( \_ valore PDH Calc \_ negativo \_ )                      | È stato rilevato un contatore con un valore negativo.
| 0x800007D9 ( \_ finestra di dialogo PDH \_ annullata)                          | L'utente ha annullato la finestra di dialogo.
| 0x800007DA ( \_ fine \_ del file di log di PDH \_ \_ )                         | È stata raggiunta la fine del file di log.
| 0x800007DB ( \_ \_ timeout query asincrono PDH \_ )                      | Si è verificato un timeout durante l'attesa della fine del thread di raccolta del contatore asincrono.
| 0x800007DC (PDH \_ non può \_ impostare l' \_ \_ origine dati in tempo reale predefinita \_ ) | Impossibile modificare l'impostazione dell'origine dati in tempo reale predefinita. Sono disponibili sessioni di query in tempo reale per la raccolta di dati del contatore.
| 0xC0000BB8 (PDH \_ CSTATUS \_ nessun \_ oggetto)                        | L'oggetto specificato non è stato trovato nel sistema.
| 0xC0000BB9 (PDH \_ CSTATUS \_ senza \_ contatore)                       | Impossibile trovare il contatore specificato.
| 0xC0000BBA (PDH \_ CSTATUS \_ dati non validi \_ )                     | I dati restituiti non sono validi.
| 0xC0000BBB ( \_ errore di \_ allocazione della memoria PDH \_ )                | Una funzione PDH non è in grado di allocare memoria temporanea sufficiente per completare l'operazione. Chiudere alcune applicazioni o estendere il file di paging e riprovare la funzione.
| 0xC0000BBC ( \_ handle non valido PDH \_ )                            | L'handle non è un oggetto PDH valido.
| 0xC0000BBD ( \_ argomento non valido PDH \_ )                          | Argomento obbligatorio mancante o non corretto.
| 0xC0000BBE ( \_ funzione PDH \_ non \_ trovata)                       | Impossibile trovare la funzione specificata.
| 0xC0000BBF (PDH \_ CSTATUS \_ No \_ counterName)                   | Non è stato specificato alcun contatore.
| 0xC0000BC0 (PDH \_ CSTATUS \_ Bad \_ counterName)                  | Impossibile analizzare il percorso del contatore. Controllare il formato e la sintassi del percorso specificato.
| 0xC0000BC1 ( \_ buffer non valido PDH \_ )                            | Il buffer passato dal chiamante non è valido.
| 0xC0000BC2 ( \_ buffer insufficiente PDH \_ )                       | I dati richiesti sono maggiori del buffer fornito. Impossibile restituire i dati richiesti.
| 0xC0000BC3 (PDH \_ non è in grado di \_ connettere il \_ computer)                   | Impossibile connettersi al computer richiesto.
| 0xC0000BC4 ( \_ percorso non valido di PDH \_ )                              | Impossibile interpretare il percorso del contatore specificato.
| 0xC0000BC5 ( \_ istanza non valida di PDH \_ )                          | Impossibile leggere il nome dell'istanza dal percorso del contatore specificato.
| 0xC0000BC6 (PDH \_ dati non validi \_ )                              | I dati non sono validi.
| 0xC0000BC7 (PDH \_ senza \_ dati della finestra di dialogo \_ )                           | Il blocco di dati della finestra di dialogo manca o non è valido.
| 0xC0000BC8 (PDH \_ non è in grado di \_ leggere \_ \_ stringhe nome)                | Impossibile leggere il contatore e/o il testo della guida dal computer specificato.
| 0xC0000BC9 ( \_ errore di creazione del file di log PDH \_ \_ \_ )                   | Impossibile creare il file di log specificato.
| 0xC0000BCA ( \_ errore di apertura del file di log PDH \_ \_ \_ )                     | Impossibile aprire il file di log specificato.
| 0xC0000BCB ( \_ tipo di log PDH \_ \_ non \_ trovato)                      | Il tipo di file di log specificato non è stato installato nel sistema.
| 0xC0000BCC (PDH \_ nessun \_ altro \_ dato)                             | Dati disponibili esauriti.
| 0xC0000BCD ( \_ voce PDH \_ non presente \_ nel \_ file di log \_ )                  | Il record specificato non è stato trovato nel file di log.
| 0xC0000BCE ( \_ origine dati \_ PDH \_ è un \_ file di log \_ )                | L'origine dati specificata è un file di log.
| 0xC0000BCF (l' \_ origine dati PDH \_ \_ è in \_ \_ tempo reale)               | L'origine dati specificata è l'attività corrente.
| 0xC0000BD0 (PDH \_ non è in grado di leggere l'intestazione del \_ \_ log \_ )                  | Impossibile leggere l'intestazione del file di log.
| 0xC0000BD1 ( \_ file PDH \_ non \_ trovato)                           | Impossibile trovare il file specificato.
| 0xC0000BD2 (il \_ file \_ PDH \_ esiste già)                      | Esiste già un file con il nome file specificato.
| 0xC0000BD3 (PDH \_ non \_ implementato)                           | La funzione a cui si fa riferimento non è stata implementata.
| 0xC0000BD4 ( \_ stringa PDH \_ non \_ trovata)                         | Impossibile trovare la stringa specificata nell'elenco delle stringhe di testo della guida e del nome delle prestazioni.
| 0x80000BD5 (PDH \_ non è possibile \_ eseguire il mapping dei file dei \_ nomi \_ )                   | Impossibile eseguire il mapping ai file di dati del nome del contatore delle prestazioni. I dati verranno letti dal registro di sistema e archiviati localmente.
| 0xC0000BD6 ( \_ formato di \_ log PDH sconosciuto \_ )                       | Il formato del file di log specificato non è riconosciuto dalla DLL PDH.
| 0xC0000BD7 ( \_ comando PDH Unknown \_ LOGSVC \_ )                   | Il valore del comando del servizio di log specificato non è riconosciuto.
| 0xC0000BD8 ( \_ query PDH \_ LOGSVC \_ non \_ trovata)                  | Impossibile trovare o aprire la query specificata dal servizio log.
| 0xC0000BD9 (PDH \_ LOGSVC \_ non \_ aperto)                        | Non è stato possibile aprire la chiave del servizio di log dei dati sulle prestazioni. Il problema potrebbe essere dovuto a privilegi insufficienti o perché il servizio non è stato installato.
| 0xC0000BDA ( \_ Errore WBEM PDH \_ )                                | Si è verificato un errore durante l'accesso all'archivio dati WBEM.
| 0xC0000BDB ( \_ accesso PDH \_ negato)                             | Impossibile accedere al computer o al servizio desiderato. Controllare le autorizzazioni e l'autenticazione del servizio log o della sessione utente interattiva rispetto a quelle del computer o del servizio monitorato.
| 0xC0000BDC ( \_ file di log PDH \_ \_ troppo \_ piccolo)                      | La dimensione massima del file di log specificata è troppo piccola per la registrazione dei contatori selezionati. Nessun dato verrà registrato in questo file di log. Specificare un set più piccolo di contatori da registrare o una dimensione di file più grande e ripetere la chiamata.
| 0xC0000BDD ( \_ origine dati non valida PDH \_ )                        | Impossibile connettersi al nome dell'origine dati ODBC.
| 0xC0000BDE (PDH \_ non valido \_ SQLDB)                             | Il database SQL non contiene un set di tabelle valido per PerfMon.
| 0xC0000BDF (PDH \_ senza \_ contatori)                               | Nessun contatore trovato per questo set di log SQL di Perfmon.
| 0xC0000BE0 (PDH \_ SQL \_ Alloc \_ non riuscita)                         | La chiamata a SQLAllocStmt non è riuscita con %1.
| 0xC0000BE1 (PDH \_ SQL \_ ALLOCCON \_ non riuscito)                      | La chiamata a SQLAllocConnect non è riuscita con %1.
| 0xC0000BE2 (PDH \_ SQL \_ Exec \_ Direct \_ non riuscita)                  | Chiamata a SQLExecDirect non riuscita con %1.
| 0xC0000BE3 ( \_ recupero SQL \_ PDH \_ non riuscito)                         | Chiamata a SQLFetch non riuscita con %1.
| 0xC0000BE4 (PDH \_ SQL \_ RowCount \_ non riuscito)                      | Chiamata a SQLRowCount non riuscita con %1.
| 0xC0000BE5 (PDH \_ SQL \_ more \_ results \_ Failed)                 | La chiamata a SQLMoreResults non è riuscita con %1.
| 0xC0000BE6 (PDH \_ SQL \_ Connect \_ non riuscita)                       | Chiamata a SQLConnect non riuscita con %1.
| 0xC0000BE7 ( \_ associazione SQL \_ PDH \_ non riuscita)                          | La chiamata a SQLBindCol non è riuscita con %1.
| 0xC0000BE8 (PDH \_ non è in grado di \_ connettere il \_ \_ server WMI)               | Impossibile connettersi al server WMI sul computer richiesto.
| 0xC0000BE9 ( \_ raccolta di PLA PDH \_ \_ già \_ in esecuzione)          | Raccolta "%1! s!" è già in esecuzione.
| 0xC0000BEA ( \_ \_ pianificazione errore PDH \_ PLA \_ sovrapposizione)              | L'ora di inizio specificata è successiva all'ora di fine.
| 0xC0000BEB ( \_ raccolta PLA \_ PDH \_ non \_ trovata)                | Raccolta "%1! s!" non esiste.
| 0xC0000BEC ( \_ \_ pianificazione errori PDH \_ PLA \_ )              | L'ora di fine specificata è già trascorsa.
| 0xC0000BED ( \_ errore di PLA PDH \_ \_ nostart)                        | Raccolta "%1! s!" non avviata; controllare se nel registro eventi dell'applicazione sono presenti errori.
| 0xC0000BEE ( \_ errore PLA \_ PDH \_ già \_ esistente)                | Raccolta "%1! s!" esiste già.
| 0xC0000BEF ( \_ tipo di errore PDH PLA non \_ \_ \_ corrispondente)                 | Il tipo di impostazioni non corrisponde.
| 0xC0000BF0 ( \_ \_ filePath errore PDH PLA \_ )                       | Le informazioni specificate non vengono risolte in un nome di percorso valido.
| 0xC0000BF1 ( \_ errore del \_ servizio PDH PLA \_ )                        | Il servizio "registri di prestazioni & avvisi" non ha risposto.
| 0xC0000BF2 (errore di convalida di PDH \_ PLA \_ \_ )                     | Le informazioni passate non sono valide.
| 0x80000BF3 ( \_ avviso di \_ convalida PDH PLA \_ )                   | Le informazioni passate non sono valide.
| 0xC0000BF4 ( \_ \_ nome errore PDH \_ PLA \_ troppo \_ lungo)                | Il nome specificato è troppo lungo.
| 0xC0000BF5 ( \_ formato di \_ log SQL non valido PDH \_ \_ )                  | Il formato del log SQL non è corretto. Il formato corretto è `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 ( \_ contatore PDH \_ già presente \_ nella \_ query)                | Il contatore delle prestazioni nella chiamata [**chiamata PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) è già stato aggiunto nella query sulle prestazioni. Questo contatore viene ignorato.
| 0xC0000BF7 ( \_ log binario \_ PDH \_ danneggiato)                       | Impossibile leggere le informazioni sui contatori e i dati dai file di log binari di input.
| 0xC0000BF8 ( \_ esempio di log PDH \_ \_ troppo \_ piccolo)                    | Almeno uno dei file di log binari di input contiene meno di due campioni di dati.
| 0xC0000BF9 (PDH \_ OS \_ \_ versione successiva)                         | La versione del sistema operativo nel computer denominato %1 è successiva a quella del computer locale. Questa operazione non è disponibile dal computer locale.
| 0xC0000BFA (PDH \_ OS \_ \_ versione precedente)                       | %1 supporta %2 o versione successiva. Controllare la versione del sistema operativo nel computer denominato %3.
| 0xC0000BFB ( \_ ora di \_ Accodamento non corretta PDH \_ )                    | Il file di output deve contenere dati precedenti rispetto al file da accodare.
| 0xC0000BFC (PDH del \_ contatore di \_ Accodamento non corrispondente \_ )                 | Per aggiungere entrambi i file devono essere presenti contatori identici.
| 0xC0000BFD (PDH \_ SQL \_ ALTER \_ detail \_ non riuscita)                 | Non è possibile modificare il layout della tabella CounterDetail nel database SQL.
| 0xC0000BFE ( \_ \_ timeout dati prestazioni query PDH \_ \_ )                 | Il sistema è occupato. Si è verificato un timeout durante la raccolta dei dati del contatore. Riprovare più tardi o aumentare il valore del registro di sistema **CollectTime** .
