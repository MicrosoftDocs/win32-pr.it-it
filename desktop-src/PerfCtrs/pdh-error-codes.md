---
description: Tutte le funzioni PDH (Performance Data Helper) restituiscono un valore di tipo PDH \_ STATUS.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Codici di errore dell'helper Dati di prestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16367cb3cd2c0ed83c69067e82fe180a6930910b1c45e76d3e01b75a6832d89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033811"
---
# <a name="performance-data-helper-error-codes"></a>Codici di errore dell'helper Dati di prestazione

Tutte le funzioni PDH (Performance Data Helper) restituiscono un valore di **tipo PDH \_ STATUS**. Se la funzione ha esito positivo, il valore restituito è `ERROR_SUCCESS` . In caso contrario, la funzione restituisce un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di errore PDH. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la [**funzione FormatMessage,**](/windows/desktop/api/winbase/nf-winbase-formatmessage) come illustrato nell'esempio seguente.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE |
                       FORMAT_MESSAGE_ALLOCATE_BUFFER |
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

Per le funzioni di raccolta e formattazione dei dati, è importante ricordare che il valore restituito della funzione indica l'esito positivo o negativo della chiamata di funzione e non necessariamente quello dei dati del contatore. Controllare sempre il **membro CStatus** del valore del contatore restituito per assicurarsi che i dati restituiti siano validi prima di usarli. Se il valore del **membro CStatus** non indica l'esito positivo, non usare i dati.

Nella tabella seguente viene fornito un elenco di codici di errore specifici di PDH. Questi valori sono definiti nel `pdhmsg.h` file di intestazione.

| Codice di errore                                                   | Descrizione
|--------------------------------------------------------------|------------
| 0x00000000 (PDH \_ CSTATUS \_ DATI \_ VALIDI)                       | I dati restituiti sono validi.
| 0x00000001 (PDH \_ CSTATUS \_ NUOVI \_ DATI)                         | Il valore dei dati restituiti è valido e diverso dall'ultimo esempio.
| 0x800007D0 (PDH \_ CSTATUS \_ NO \_ MACHINE)                       | Impossibile connettersi al computer specificato oppure il computer è offline.
| 0x800007D1 (PDH \_ CSTATUS \_ NO \_ INSTANCE)                      | L'istanza specificata non è presente.
| 0x800007D2 (PDH \_ MORE \_ DATA)                                 | È necessario restituire più dati di quelli che verrebbero memorizzati nel buffer fornito. Allocare un buffer più grande e chiamare di nuovo la funzione .
| 0x800007D3 (ELEMENTO CSTATUS PDH \_ \_ NON \_ \_ CONVALIDATO)              | L'elemento dati è stato aggiunto alla query, ma non è stato convalidato né è stato eseguito l'accesso. Non sono disponibili altre informazioni sullo stato per questo elemento di dati.
| 0x800007D4 (TENTATIVO \_ PDH)                                      | L'operazione selezionata deve essere ritentata.
| 0x800007D5 (PDH \_ NO \_ DATA)                                   | Nessun dato da restituire.
| 0x800007D6 (PDH \_ CALC \_ NEGATIVE \_ DENOMINATOR)                | È stato rilevato un contatore con un valore denominatore negativo.
| 0x800007D7 (PDH \_ CALC \_ NEGATIVE \_ TIMEBASE)                   | È stato rilevato un contatore con un valore di base temporale negativo.
| 0x800007D8 (PDH \_ CALC \_ NEGATIVE \_ VALUE)                      | È stato rilevato un contatore con un valore negativo.
| 0x800007D9 (FINESTRA DI DIALOGO PDH \_ \_ ANNULLATA)                          | L'utente ha annullato la finestra di dialogo.
| 0x800007DA (PDH \_ END \_ OF LOG \_ \_ FILE)                         | È stata raggiunta la fine del file di log.
| 0x800007DB (TIMEOUT QUERY \_ ASINCRONA \_ PDH) \_                      | Si è verificato un timeout durante l'attesa della fine del thread di raccolta contatori asincrono.
| 0x800007DC (PDH \_ NON PUÒ IMPOSTARE \_ \_ \_ L'ORIGINE DATI IN TEMPO REALE \_ PREDEFINITA) | Impossibile modificare l'origine dati predefinita in tempo reale del set di modifiche. Sono presenti sessioni di query in tempo reale che raccolgono i dati dei contatori.
| 0xC0000BB8 (PDH \_ CSTATUS \_ NO \_ OBJECT)                        | L'oggetto specificato non è stato trovato nel sistema.
| 0xC0000BB9 (PDH \_ CSTATUS \_ NO \_ COUNTER)                       | Impossibile trovare il contatore specificato.
| 0xC0000BBA (PDH \_ CSTATUS \_ DATI NON \_ VALIDI)                     | I dati restituiti non sono validi.
| 0xC0000BBB (ERRORE DI ALLOCAZIONE \_ MEMORIA PDH) \_ \_                | Una funzione PDH non è stata in grado di allocare memoria temporanea sufficiente per completare l'operazione. Chiudere alcune applicazioni o estendere il file di pagina e ripetere la funzione.
| 0xC0000BBC (HANDLE PDH \_ NON \_ VALIDO)                            | L'handle non è un oggetto PDH valido.
| 0xC0000BBD (ARGOMENTO PDH \_ NON \_ VALIDO)                          | Un argomento obbligatorio manca o non è corretto.
| 0xC0000BBE (FUNZIONE PDH \_ \_ NON \_ TROVATA)                       | Impossibile trovare la funzione specificata.
| 0xC0000BBF (PDH \_ CSTATUS \_ NO \_ COUNTERNAME)                   | Non è stato specificato alcun contatore.
| 0xC0000BC0 (PDH \_ CSTATUS \_ BAD \_ COUNTERNAME)                  | Impossibile analizzare il percorso del contatore. Controllare il formato e la sintassi del percorso specificato.
| 0xC0000BC1 (BUFFER PDH \_ NON \_ VALIDO)                            | Il buffer passato dal chiamante non è valido.
| 0xC0000BC2 (PDH \_ INSUFFICIENT \_ BUFFER)                       | I dati richiesti sono maggiori del buffer fornito. Impossibile restituire i dati richiesti.
| 0xC0000BC3 (PDH \_ CANNOT \_ CONNECT \_ MACHINE)                   | Impossibile connettersi al computer richiesto.
| 0xC0000BC4 (PERCORSO PDH \_ NON \_ VALIDO)                              | Impossibile interpretare il percorso del contatore specificato.
| 0xC0000BC5 (ISTANZA PDH \_ NON \_ VALIDA)                          | Impossibile leggere il nome dell'istanza dal percorso del contatore specificato.
| 0xC0000BC6 (DATI PDH \_ NON \_ VALIDI)                              | I dati non sono validi.
| 0xC0000BC7 (PDH \_ NO \_ DIALOG \_ DATA)                           | Blocco di dati della finestra di dialogo mancante o non valido.
| 0xC0000BC8 (PDH \_ NON È IN GRADO DI LEGGERE STRINGHE DI \_ \_ \_ NOMI)                | Impossibile leggere il contatore e/o il testo della Guida dal computer specificato.
| 0xC0000BC9 (ERRORE DI CREAZIONE \_ FILE DI LOG PDH) \_ \_ \_                   | Impossibile creare il file di log specificato.
| 0xC0000BCA (ERRORE DI APERTURA \_ FILE DI LOG PDH) \_ \_ \_                     | Impossibile aprire il file di log specificato.
| 0xC0000BCB (TIPO DI LOG PDH \_ \_ NON \_ \_ TROVATO)                      | Il tipo di file di log specificato non è stato installato in questo sistema.
| 0xC0000BCC (PDH \_ NO \_ MORE \_ DATA)                             | Dati disponibili esauriti.
| 0xC0000BCD (VOCE PDH \_ \_ NON NEL FILE \_ DI \_ \_ LOG)                  | Il record specificato non è stato trovato nel file di log.
| 0xC0000BCE (L'ORIGINE DATI PDH \_ È IL FILE DI \_ \_ \_ \_ LOG)                | L'origine dati specificata è un file di log.
| 0xC0000BCF (L'ORIGINE DATI PDH \_ \_ È IN TEMPO \_ \_ \_ REALE)               | L'origine dati specificata è l'attività corrente.
| 0xC0000BD0 (PDH \_ UNABLE \_ READ LOG \_ \_ HEADER)                  | Impossibile leggere l'intestazione del file di log.
| 0xC0000BD1 (FILE PDH \_ \_ NON \_ TROVATO)                           | Impossibile trovare il file specificato.
| 0xC0000BD2 (FILE PDH \_ \_ GIÀ \_ ESISTENTE)                      | Esiste già un file con il nome file specificato.
| 0xC0000BD3 (PDH \_ NON \_ IMPLEMENTATO)                           | La funzione a cui si fa riferimento non è stata implementata.
| 0xC0000BD4 (STRINGA PDH \_ \_ NON \_ TROVATA)                         | Impossibile trovare la stringa specificata nell'elenco di stringhe di testo della Guida e del nome delle prestazioni.
| 0x80000BD5 (PDH \_ UNABLE \_ MAP NAME \_ \_ FILES)                   | Impossibile eseguire il mapping ai file di dati del nome del contatore delle prestazioni. I dati verranno letti dal Registro di sistema e archiviati in locale.
| 0xC0000BD6 (PDH \_ UNKNOWN \_ LOG \_ FORMAT)                       | Il formato del file di log specificato non è riconosciuto dalla DLL PDH.
| 0xC0000BD7 (COMANDO PDH \_ UNKNOWN \_ \_ LOGSVC)                   | Il valore del comando del servizio di log specificato non è riconosciuto.
| 0xC0000BD8 (QUERY LOGSVC PDH \_ \_ NON \_ \_ TROVATA)                  | La query specificata dal servizio di log non è stata trovata o non è stata aperta.
| 0xC0000BD9 (PDH \_ LOGSVC \_ NON \_ APERTO)                        | Impossibile aprire la chiave del servizio Log dati prestazioni. Ciò potrebbe essere dovuto a privilegi insufficienti o perché il servizio non è stato installato.
| 0xC0000BDA (ERRORE \_ WBEM \_ PDH)                                | Si è verificato un errore durante l'accesso all'archivio dati WBEM.
| 0xC0000BDB (ACCESSO PDH \_ \_ NEGATO)                             | Impossibile accedere al computer o al servizio desiderato. Controllare le autorizzazioni e l'autenticazione del servizio di log o della sessione utente interattiva rispetto a quelle del computer o del servizio monitorato.
| 0xC0000BDC (FILE DI LOG PDH \_ \_ TROPPO \_ \_ PICCOLO)                      | Le dimensioni massime del file di log specificate sono troppo piccole per registrare i contatori selezionati. In questo file di log non verrà registrato alcun dato. Specificare un set più piccolo di contatori da registrare o dimensioni di file maggiori e ripetere questa chiamata.
| 0xC0000BDD (ORIGINE DATI NON \_ VALIDA PDH) \_                        | Impossibile connettersi al nome origine dati ODBC.
| 0xC0000BDE (PDH \_ INVALID \_ SQLDB)                             | database SQL non contiene un set valido di tabelle per Perfmon.
| 0xC0000BDF (PDH \_ NESSUN \_ CONTATORE)                               | Non sono stati trovati contatori per questo set di SQL Perfmon.
| 0xC0000BE0 (PDH SQL \_ \_ ALLOC \_ FAILED)                         | Chiamata a SQLAllocStmt non riuscita con %1.
| 0xC0000BE1 (PDH \_ SQL \_ ALLOCCON \_ FAILED)                      | Chiamata a SQLAllocConnect non riuscita con %1.
| 0xC0000BE2 (PDH SQL \_ \_ EXEC DIRECT \_ \_ FAILED)                  | Chiamata a SQLExecDirect non riuscita con %1.
| 0xC0000BE3 (PDH SQL \_ \_ FETCH \_ FAILED)                         | Chiamata a SQLFetch non riuscita con %1.
| 0xC0000BE4 (PDH SQL \_ \_ ROWCOUNT \_ FAILED)                      | Chiamata a SQLRowCount non riuscita con %1.
| 0xC0000BE5 (PDH SQL \_ RISULTATI \_ NON \_ \_ RIUSCITI)                 | Chiamata a SQLMoreResults non riuscita con %1.
| 0xC0000BE6 (PDH SQL \_ CONNECT \_ \_ FAILED)                       | Chiamata a SQLConnect non riuscita con %1.
| 0xC0000BE7 (PDH SQL \_ \_ BIND \_ FAILED)                          | Chiamata a SQLBindCol non riuscita con %1.
| 0xC0000BE8 (PDH \_ NON PUÒ CONNETTERE IL SERVER \_ \_ \_ WMI)               | Impossibile connettersi al server WMI nel computer richiesto.
| 0xC0000BE9 (PDH \_ PLA \_ COLLECTION ALREADY \_ \_ RUNNING)          | Raccolta "%1!s!" è già in esecuzione.
| 0xC0000BEA (SOVRAPPOSIZIONE PIANIFICAZIONE ERRORI \_ PDH \_ \_ \_ PLA)              | L'ora di inizio specificata è dopo l'ora di fine.
| 0xC0000BEB (PDH \_ PLA \_ COLLECTION NOT \_ \_ FOUND)                | Raccolta "%1!s!" non esiste.
| 0xC0000BEC (PIANIFICAZIONE DEGLI ERRORI \_ PDH \_ PLA \_ \_ TRASCORSO)              | L'ora di fine specificata è già trascorsa.
| 0xC0000BED (PDH \_ PLA \_ ERROR \_ NOSTART)                        | Raccolta "%1!s!" non è stato avviato; controllare il registro eventi dell'applicazione per eventuali errori.
| 0xC0000BEE (L'ERRORE PDH \_ PLA \_ ESISTE \_ \_ GIÀ)                | Raccolta "%1!s!" esiste già.
| 0xC0000BEF (TIPO DI ERRORE \_ PDH PLA NON \_ \_ \_ CORRISPONDENTE)                 | Mancata corrispondenza nel tipo di impostazioni.
| 0xC0000BF0 (PDH \_ PLA \_ ERROR \_ FILEPATH)                       | Le informazioni specificate non vengono risolte in un nome di percorso valido.
| 0xC0000BF1 (ERRORE DEL SERVIZIO \_ PDH \_ \_ PLA)                        | Il servizio "Avvisi & prestazioni" non ha risposto.
| 0xC0000BF2 (ERRORE DI CONVALIDA \_ DELLA PLA PDH) \_ \_                     | Le informazioni passate non sono valide.
| 0x80000BF3 (AVVISO DI CONVALIDA \_ DELLA PLA PDH) \_ \_                   | Le informazioni passate non sono valide.
| 0xC0000BF4 (PDH \_ PLA \_ ERROR NAME TOO \_ \_ \_ LONG)                | Il nome specificato è troppo lungo.
| 0xC0000BF5 (PDH \_ INVALID \_ SQL LOG \_ \_ FORMAT)                  | SQL formato del log non è corretto. Il formato corretto è `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 (CONTATORE PDH \_ \_ GIÀ IN \_ \_ QUERY)                | Il contatore delle prestazioni nella chiamata [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) è già stato aggiunto nella query sulle prestazioni. Questo contatore viene ignorato.
| 0xC0000BF7 (LOG BINARIO PDH \_ \_ \_ DANNEGGIATO)                       | Impossibile leggere le informazioni sui contatori e i dati dai file di log binari di input.
| 0xC0000BF8 (ESEMPIO DI LOG PDH \_ \_ TROPPO \_ \_ PICCOLO)                    | Almeno uno dei file di log binari di input contiene meno di due esempi di dati.
| 0xC0000BF9 (PDH \_ OS \_ VERSIONE \_ SUCCESSIVA)                         | La versione del sistema operativo nel computer denominato %1 è successiva a quella del computer locale. Questa operazione non è disponibile nel computer locale.
| 0xC0000BFA (VERSIONE PRECEDENTE del SISTEMA OPERATIVO \_ PDH) \_ \_                       | %1 supporta %2 o versione successiva. Controllare la versione del sistema operativo nel computer denominato %3.
| 0xC0000BFB (PDH \_ TEMPO DI \_ ACCODAMENTO NON \_ CORRETTO)                    | Il file di output deve contenere dati precedenti rispetto al file da aggiungere.
| 0xC0000BFC (PDH \_ UNMATCHED \_ APPEND \_ COUNTER)                 | Entrambi i file devono avere contatori identici per poter essere aggiunti.
| 0xC0000BFD (PDH SQL \_ ALTER \_ \_ DETAIL \_ FAILED)                 | Impossibile modificare il layout della tabella CounterDetail SQL database.
| 0xC0000BFE (PDH \_ QUERY \_ PERF \_ DATA \_ TIMEOUT)                 | Il sistema è occupato. Si è verificato un timeout durante la raccolta dei dati del contatore. Riprovare più tardi o aumentare il **valore del Registro di sistema CollectTime.**
