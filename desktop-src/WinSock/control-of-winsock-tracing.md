---
description: .
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Controllo della traccia Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b15ece4581525fddc25213c630e24d0e49110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307004"
---
# <a name="control-of-winsock-tracing"></a>Controllo della traccia Winsock

È possibile controllare la traccia Winsock utilizzando uno dei metodi seguenti:

-   Strumenti da riga di comando

    Due strumenti da riga di comando sono inclusi in Windows Vista e Windows Server 2008 utilizzati per controllare la traccia e convertire il file di log di traccia binario in testo leggibile.

    Lo strumento **logman.exe** viene utilizzato per avviare o arrestare la traccia Winsock.

    Lo strumento **tracerpt.exe** viene utilizzato per convertire il file di log di traccia binario in un file di testo leggibile.

-   Visualizzatore eventi

    Il Visualizzatore eventi in Windows Vista e versioni successive può essere utilizzato anche per abilitare la traccia Winsock. Il Visualizzatore eventi è accessibile dagli strumenti di amministrazione dal menu Start.

## <a name="using-logman-and-tracert"></a>Uso di Logman e tracert

La traccia degli eventi di rete Winsock è disabilitata per impostazione predefinita in Windows Vista e versioni successive.

Il comando seguente avvia la traccia eventi di rete Winsock in un computer, imposta il nome della sessione di traccia eventi su mywinsocksession e invia l'output a un file di log binario denominato winsocklogfile. etl:

**logman start-ETS mywinsocksession-o winsocklogfile. etl-p Microsoft-Windows-Winsock-AFD**

I file di log vengono creati nella directory corrente con nomi di file nel formato winsocklogfile \_ 000001. etl

Il seguente comando Arresta la traccia Winsock precedente in un computer per la sessione denominata mywinsocksession:

**logman stop-ETS mywinsocksession**

Un file di log binario verrà scritto nel percorso specificato dal parametro – o. Per convertire il file binario in un file di testo leggibile, viene utilizzato **tracerpt.exe** :

**tracerpt.exe <nome del file con estensione ETL> – o winsocktracelog.txt**

Se è preferibile un file di output contenente XML anziché testo normale, viene usato il comando seguente:

**tracerpt.exe <nome del file con estensione ETL> – o winsocktracelog.xml – di XML**

La traccia delle modifiche del catalogo Winsock è abilitata per impostazione predefinita in Windows Vista e versioni successive.

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

Il comando seguente avvia la traccia delle modifiche del catalogo Winsock per i provider di servizi su più livelli (LSP) in un computer, imposta il nome della sessione di traccia eventi su mywinsockcatalogsession e invia l'output a un file di log binario denominato winsockcataloglogfile. etl:

**logman start-ETS mywinsockcatalogsession-o winsockcataloglogfile. etl-p Microsoft-Windows-Winsock-WS2HELP**

I file di log vengono creati nella directory corrente con nomi di file nel formato winsockcataloglogfile \_ 000001. etl

Il seguente comando Arresta la traccia Winsock precedente in un computer per la sessione denominata sessione:

**logman stop-ETS mywinsockcatalogsession**

Un file di log binario verrà scritto nel percorso specificato dal parametro – o. Per convertire il file binario in un file di testo leggibile, viene utilizzato **tracerpt.exe** :

**tracerpt.exe <nome del file con estensione ETL> – o winsockcatalogtracelog.txt**

Se è preferibile un file di output contenente XML anziché testo normale, viene usato il comando seguente:

**tracerpt.exe <nome del file con estensione ETL> – o winsockcatalogtracelog.xml – di XML**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Utilizzo di Visualizzatore eventi per avviare la traccia degli eventi di rete Winsock

Quando si apre Visualizzatore eventi, il riquadro sinistro contiene l'elenco di eventi. Aprire **registri applicazioni e servizi** e passare all' **\\ evento di \\ rete Winsock Microsoft Windows** come origine e selezionare **operativo**.

Nel riquadro azioni selezionare **proprietà log** e selezionare la casella di controllo **Abilita registrazione** . Una volta abilitata la registrazione, è possibile modificare anche le dimensioni del file di log, se necessario.

La traccia eventi di rete Winsock è ora abilitata ed è sufficiente fare clic sull'azione Aggiorna per aggiornare l'elenco degli eventi che sono stati registrati. Per arrestare la registrazione, è sufficiente deselezionare lo stesso pulsante di opzione.

Potrebbe essere necessario aumentare le dimensioni del log a seconda del numero di eventi che si desidera visualizzare. Uno svantaggio dell'utilizzo del Visualizzatore eventi per la traccia di Winsock è che non carica tutte le risorse di stringa, in modo che i messaggi visualizzati nel campo Descrizione (dopo aver selezionato un evento) siano talvolta difficili da leggere (ad esempio, un argomento che deve essere formattato come Hex verrà visualizzato in decimale). Tuttavia, è possibile selezionare la scheda **Dettagli** nella descrizione dell'evento che mostra la voce di log XML non elaborata che in genere è più facile da comprendere.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Uso di Visualizzatore eventi per avviare la traccia delle modifiche del catalogo Winsock

Quando si apre Visualizzatore eventi, il riquadro sinistro contiene l'elenco di eventi. Aprire **registri applicazioni e servizi** e passare a **Microsoft \\ Windows \\ Winsock Catalog Change** come origine e selezionare **Operational**.

Nel riquadro azioni selezionare **proprietà log** e selezionare la casella di controllo **Abilita registrazione** . Una volta abilitata la registrazione, è possibile modificare anche le dimensioni del file di log, se necessario.

La traccia delle modifiche del catalogo Winsock è ora abilitata ed è sufficiente fare clic sull'azione Aggiorna per aggiornare l'elenco degli eventi che sono stati registrati. Per arrestare la registrazione, è sufficiente deselezionare lo stesso pulsante di opzione.

Potrebbe essere necessario aumentare le dimensioni del log a seconda del numero di eventi che si desidera visualizzare. Uno svantaggio dell'utilizzo del Visualizzatore eventi per la traccia di Winsock è che non carica tutte le risorse di stringa, in modo che i messaggi visualizzati nel campo Descrizione (dopo aver selezionato un evento) siano talvolta difficili da leggere (ad esempio, un argomento che deve essere formattato come Hex verrà visualizzato in decimale). Tuttavia, è possibile selezionare la scheda **Dettagli** nella descrizione dell'evento che mostra la voce di log XML non elaborata che in genere è più facile da comprendere.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretazione dei log di traccia Winsock

Tutti gli eventi di traccia Winsock in un log contengono due tipi di informazioni:

-   Sistema
-   EventData

Le informazioni di sistema contengono il livello di registrazione, la data e l'ora di creazione della voce di log, l'ID dell'evento che rappresenta il tipo di evento, l'ID del processo di esecuzione, l'ID del thread di esecuzione e altre informazioni di sistema. Un livello di registrazione 4 nella traccia Winsock rappresenta la registrazione degli eventi informativi. Un livello di registrazione di 5 nella traccia Winsock rappresenta la registrazione dettagliata degli eventi.

L'ID del processo di esecuzione e l'ID del thread nelle informazioni di sistema indicano il processo e il thread che era in esecuzione quando si è verificato l'evento. In molti casi, questo rappresenterà un kernel, un thread di lavoro e un processo, non un thread in modalità utente e o il processo dell'applicazione. Questo campo non è in genere molto utile.

Ogni tipo di evento di traccia Winsock dispone di un ID evento univoco nella sezione sistema dei dati registrati. Questi ID evento possono essere facilmente utilizzati per filtrare un file di log per eventi di traccia Winsock specifici.

EVENTDATA contiene informazioni specifiche per il tipo di evento.

Il parametro Process nelle informazioni EventData è l'indirizzo della struttura EPROCESS del kernel per il processo, non il PID effettivo. Per associare un evento al PID in modalità utente, prendere il valore del processo dalle informazioni EventData da qualsiasi voce di log e cercare in precedenza nel log un evento di creazione del socket con il valore del processo. Una volta trovata una corrispondenza, l'ultimo parametro nei dati dell'evento di creazione del socket è l'ID del processo in modalità utente che ha creato il socket.

Un parametro address nelle informazioni EVENTDATA viene restituito in alcuni eventi di traccia Winsock. Un parametro address rappresenta un indirizzo IP, ma viene visualizzato nel file di testo creato dallo strumento **tracerpt.exe** o in Visualizzatore eventi come byte non elaborati o un numero. Gli indirizzi IPv6 vengono visualizzati in formato esadecimale, quindi sono più facilmente comprensibili. Gli indirizzi IPv4 vengono visualizzati come numero decimale grande. Gli sviluppatori dovranno convertire manualmente i byte non elaborati di un indirizzo IPv4 nella notazione di indirizzo decimale punteggiata IPv4 più familiare per poter interpretare il valore in modo più efficace.

In alcuni eventi di traccia Winsock viene restituito un parametro error in EventData. Un parametro di errore è formato da un codice di errore NTSTATUS o HRESULT. Questo parametro di errore viene visualizzato nel file di testo creato dallo strumento **tracerpt.exe** o in Visualizzatore eventi come numero decimale. Gli sviluppatori dovranno convertire manualmente il numero decimale in un numero esadecimale per interpretare meglio il codice di errore in alcuni casi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Dettagli traccia eventi di rete Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Livelli di traccia Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
