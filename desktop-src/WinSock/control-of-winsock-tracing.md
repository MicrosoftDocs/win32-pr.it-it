---
description: Controllo della traccia winsock
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Controllo della traccia Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f256c4e3927672bc13b14bfb72ca3b02c22bde
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110549"
---
# <a name="control-of-winsock-tracing"></a>Controllo della traccia winsock

La traccia winsock può essere controllata usando uno dei metodi seguenti:

-   Strumenti da riga di comando

    In Windows Vista e Windows Server 2008 sono inclusi due strumenti da riga di comando usati per controllare la traccia e convertire il file di log di traccia binario in testo leggibile.

    Lo **logman.exe** viene usato per avviare o arrestare la traccia winsock.

    Lo **tracerpt.exe** viene usato per convertire il file di log di traccia binario in un file di testo leggibile.

-   Visualizzatore eventi

    Il Visualizzatore eventi in Windows Vista e versioni successive può essere usato anche per abilitare la traccia Winsock. Il Visualizzatore eventi è accessibile in Strumenti di amministrazione dal menu Start.

## <a name="using-logman-and-tracert"></a>Uso di logman e tracert

La traccia eventi di rete Winsock è disabilitata per impostazione predefinita in Windows Vista e versioni successive.

Il comando seguente avvia winsock network event tracing on a computer, imposta il nome della sessione di traccia eventi su mywinsocksession e invia l'output a un file di log binario denominato winsocklogfile.etl:

**logman start -ets mywinsocksession -o winsocklogfile.etl -p Microsoft-Windows-Winsock-AFD**

I file di log vengono creati nella directory corrente con nomi file nel formato winsocklogfile \_ 000001.etl

Il comando seguente arresta la traccia winsock precedente in un computer per la sessione denominata mywinsocksession:

**logman stop -ets mywinsocksession**

Un file di log binario verrà scritto nel percorso specificato dal parametro -o. Per convertire il file binario in un file di testo leggibile, **tracerpt.exe** viene usato:

**tracerpt.exe <nome del file con estensione etl> –o winsocktracelog.txt**

Se si preferisce un file di output contenente xml anziché testo normale, viene usato il comando seguente:

**tracerpt.exe <nome del file con estensione etl> –o winsocktracelog.xml –of xml**

La traccia delle modifiche del catalogo Winsock è abilitata per impostazione predefinita in Windows Vista e versioni successive.

> [!Note]  
> I provider di servizi a più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

Il comando seguente avvia l'analisi delle modifiche del catalogo Winsock per provider di servizi a più livelli (LSP) in un computer, imposta il nome della sessione di traccia eventi su mywinsockcatalogsession e invia l'output a un file di log binario denominato winsockcataloglogfile.etl:

**logman start -ets mywinsockcatalogsession -o winsockcataloglogfile.etl -p Microsoft-Windows-Winsock-WS2HELP**

I file di log vengono creati nella directory corrente con nomi di file nel formato winsockcataloglogfile \_ 000001.etl

Il comando seguente arresta la traccia Winsock precedente in un computer per la sessione denominata mysession:

**logman stop -ets mywinsockcatalogsession**

Un file di log binario verrà scritto nel percorso specificato dal parametro –o. Per convertire il file binario in un file di testo leggibile, **tracerpt.exe** viene usato:

**tracerpt.exe <nome del file con estensione etl> –o winsockcatalogtracelog.txt**

Se si preferisce un file di output contenente xml anziché testo normale, viene usato il comando seguente:

**tracerpt.exe <nome del file con estensione etl> –o winsockcatalogtracelog.xml –of xml**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Uso Visualizzatore eventi per avviare Winsock Network Event Tracing

Quando si apre Visualizzatore eventi, il riquadro sinistro contiene l'elenco di eventi. Aprire **Registri applicazioni e servizi** e passare a Microsoft Windows Winsock Network Event (Evento di rete Microsoft Windows **\\ \\ Winsock)** come origine e selezionare **Operational (Operativo).**

Nel riquadro Azione selezionare Proprietà **log e** selezionare la casella di **controllo Abilita** registrazione. Dopo aver abilitato la registrazione, è anche possibile modificare le dimensioni del file di log, se necessario.

La traccia degli eventi di rete Winsock è ora abilitata e tutto quello che è necessario fare è premere l'azione Aggiorna per aggiornare l'elenco di eventi registrati. Per arrestare la registrazione, è sufficiente deselezionare lo stesso pulsante di opzione.

Potrebbe essere necessario aumentare le dimensioni del log a seconda del numero di eventi che si desidera visualizzare. Uno svantaggio dell'uso di Visualizzatore eventi per la traccia Winsock è che non carica tutte le risorse di tipo stringa, quindi i messaggi visualizzati nel campo Descrizione (dopo aver selezionato un evento) sono talvolta difficili da leggere (ad esempio, un argomento che deve essere formattato come esadecimale verrà visualizzato in formato decimale). Tuttavia, è possibile selezionare la **scheda Dettagli nella descrizione** dell'evento che mostra la voce di log XML non elaborata che in genere è più facile comprendere gli argomenti.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Uso Visualizzatore eventi avviare La traccia delle modifiche del catalogo Winsock

Quando si apre Visualizzatore eventi, il riquadro sinistro contiene l'elenco degli eventi. Aprire **Registri applicazioni e servizi,** passare a Microsoft Windows Winsock Catalog Change (Modifica catalogo Di Microsoft Windows **\\ \\ Winsock)** come origine e selezionare **Operational (Operativo).**

Nel riquadro Azione selezionare Proprietà **log e selezionare** la casella di controllo **Abilita** registrazione. Dopo aver abilitato la registrazione, è anche possibile modificare le dimensioni del file di log, se necessario.

La traccia delle modifiche del catalogo Winsock è ora abilitata e è necessario solo eseguire l'azione Aggiorna per aggiornare l'elenco di eventi registrati. Per arrestare la registrazione, è sufficiente deselezionare lo stesso pulsante di opzione.

Potrebbe essere necessario aumentare le dimensioni del log a seconda del numero di eventi che si desidera visualizzare. Uno svantaggio dell'uso di Visualizzatore eventi per la traccia Winsock è che non carica tutte le risorse di tipo stringa, quindi i messaggi visualizzati nel campo Descrizione (dopo aver selezionato un evento) sono talvolta difficili da leggere(ad esempio, un argomento che deve essere formattato come esadecimale verrà visualizzato in formato decimale). Tuttavia, è possibile selezionare la **scheda Dettagli nella descrizione** dell'evento che mostra la voce di log XML non elaborata che in genere è più facile comprendere gli argomenti.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretazione dei log di traccia di Winsock

Tutti gli eventi di traccia di Winsock in un log contengono due tipi di informazioni:

-   Sistema
-   EventData

Le informazioni di sistema contengono il livello di registrazione, l'ora di creazione della voce di log, l'ID evento che rappresenta il tipo di evento, l'ID processo di esecuzione, l'ID thread di esecuzione e altre informazioni di sistema. Un livello di log 4 nella traccia Winsock rappresenta la registrazione degli eventi di informazioni. Un livello di log 5 nella traccia Winsock rappresenta la registrazione dettagliata degli eventi.

L'ID del processo di esecuzione e l'ID thread nelle informazioni di sistema indicano il processo e il thread in esecuzione quando si è verificato l'evento. In molti casi, rappresenta un kernel o un thread di lavoro e un processo, non un thread in modalità utente e o il processo dell'applicazione. Questo campo non è quindi in genere molto utile.

Ogni tipo di evento di traccia Winsock ha un ID evento univoco nella sezione di sistema dei dati registrati. Questi ID evento possono essere facilmente usati per filtrare un file di log per eventi di traccia Winsock specifici.

Eventdata contiene informazioni specifiche per il tipo di evento.

Il parametro Process nelle informazioni eventdata è l'indirizzo della struttura EPROCESS del kernel per il processo, non il PID effettivo. Per associare un evento al PID in modalità utente, prendere il valore Process dalle informazioni eventdata da qualsiasi voce di log e cercare in precedenza nel log un evento di creazione socket con il valore Process. Una volta trovata una corrispondenza, l'ultimo parametro nei dati dell'evento di creazione del socket è l'ID processo in modalità utente che ha creato il socket.

Un parametro Address nelle informazioni eventdata viene restituito in alcuni eventi di traccia Winsock. Un parametro Address rappresenta un indirizzo IP, ma viene visualizzato nel file di testo creato dallo strumento **tracerpt.exe** o in Visualizzatore eventi come byte non elaborati o un numero. Gli indirizzi IPv6 vengono visualizzati in formato esadecimale, quindi sono più facilmente comprensibili. Gli indirizzi IPv4 vengono visualizzati come numero decimale di grandi dimensioni. Gli sviluppatori dovranno convertire manualmente i byte non elaborati di un indirizzo IPv4 nella notazione di indirizzi decimali con punti IPv4 più nota per poter interpretare meglio il valore.

In alcuni eventi di traccia Winsock viene restituito un parametro Error in eventdata. Un parametro Error è nel formato di codice di errore NTSTATUS o HRESULT. Questo parametro di errore viene visualizzato nel file di testo creato dallo strumento **tracerpt.exe** o in Visualizzatore eventi come numero decimale. Gli sviluppatori dovranno convertire manualmente il numero decimale in un numero esadecimale per interpretare meglio il codice di errore in alcuni casi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> <dt>

[Dettagli traccia modifiche catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Dettagli di Traccia eventi di rete Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Livelli di traccia di Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
