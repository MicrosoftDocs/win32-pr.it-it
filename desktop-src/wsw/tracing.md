---
title: Traccia
description: La traccia utilizza Event Tracing for Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Traccia dei servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399946"
---
# <a name="tracing"></a>Traccia

La traccia utilizza Event Tracing for Windows (ETW). Per sfruttare i vantaggi degli strumenti di traccia disponibili con Windows Server 2008 R2, installare il Microsoft Windows SDK dal sito di [download di MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .


Sono supportati tre livelli di traccia:

-   Verbose (tutte le tracce disponibili).
-   Informazioni (tracce informative).
-   Errore (tracce di errore).

Vengono tracciati gli eventi seguenti:

-   Eventuali errori (Level = Error, Level = info o level = verbose).
-   Ingresso/uscita di un'API (Level = info o level = verbose).
-   Inizio e completamento di qualsiasi IO (Level = info o level = verbose)
-   Messaggi SOAP scambiati (level = verbose, disponibile in Windows 2003 SP1 e versioni successive)

## <a name="generating-and-viewing-wwsapi-traces"></a>Generazione e visualizzazione di tracce WWSAPI

WWSAPI utilizza gli eventi basati su manifesto in Windows Vista e versioni successive. Di conseguenza, l'esperienza di traccia presenta alcune differenze in base alla versione del sistema operativo. La generazione di tracce ETW può essere eseguita tramite gli strumenti ETW predefiniti in tutte le piattaforme supportate. Tuttavia, la visualizzazione delle tracce ETW in un formato gradevole richiede strumenti personalizzati in Windows XP SP2 e Windows 2003 SP1. Esistono diversi modi per raccogliere e visualizzare le tracce degli eventi ETW WWSAPI a seconda della versione del sistema operativo.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Abilitazione e visualizzazione di tracce WWSAPI in Visualizzatore eventi (funziona in Windows Vista e versioni successive)

-   Eseguire eventvwr. msc dalla riga di comando o dal menu Esegui.
-   Fare clic sul collegamento Visualizza nel riquadro azioni a destra e abilitare l'opzione Mostra log analitici e debug.
-   Passare a registri applicazioni e servizi \\ \\ \\ provider di servizi di Microsoft Windows nel riquadro sinistro.
-   Fare clic con il pulsante destro del mouse sul provider di traccia e selezionare Abilita log.
-   Eseguire lo scenario.
-   Quando si aggiorna la pagina Visualizzatore eventi, è necessario iniziare a visualizzare le voci di traccia WWSAPI.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Abilitazione e visualizzazione di tracce WWSAPI usando Wstrace.bat script (funziona in XPSP2 e versioni successive)

Il file batch wstrace.bat offre un modo pratico per:

-   Creazione di un registro di traccia
-   Eliminare un registro di traccia
-   Abilitare e disabilitare la traccia
-   Aggiornare il livello di traccia (info/Error/verbose)
-   Conversione dei log di traccia in file CSV

Il file batch USA logman.exe per tutti i comandi, ad eccezione della conversione dei log in un file CSV, che richiede uno strumento personalizzato (wstracedump.exe).

## <a name="using-tracing-commands"></a>Uso di comandi di traccia

Il comando che segue crea un log che usa il livello info, Error o Verbose. Questo comando richiede privilegi elevati.

**wstrace.bat crea \[ informazioni \| \| dettagliate errore\]**

Il comando che segue elimina il log. Questo comando richiede privilegi elevati.

**Eliminazionewstrace.bat**

Il comando seguente abilita la traccia. È necessario innanzitutto creare un log.

**wstrace.bat**

Il livello di traccia (info, Error o verbose) può essere modificato come segue:

**wstrace.bat \[ \| Dettagli errore informazioni \| aggiornamento\]**

Per eseguire il dump dell'output della traccia, utilizzare il comando seguente:

**wstrace.bat dump > temp.csv**

Gli eventi verranno scaricati nel file CSV fino a quando non viene premuto CTRL + C o la traccia è disabilitata.

## <a name="tracing-file-format"></a>Formato file di traccia

I file CSV creati da wstrace.bat sono semplici file di testo con variabili separate da virgole. Questi file possono essere aperti in Excel, blocco note e così via.

Le colonne del file sono le seguenti:

-   TimeStamp: TimeStamp del momento in cui è stato registrato l'evento
-   ProcessID-ID ULONG del processo che registra l'evento
-   ThreadID-ID ULONG del thread che registra l'evento
-   Il valore enumerato per l'evento del tipo di evento può essere ("API Enter" " \| API Pending" \| "API ExitSyncSuccess" \| "API ExitSyncFailure" \| "API ExitAsyncSuccess" \| "API ExitAsyncFailure" " \| io Started" \| "io completed" \| "io failed" \| "Error" \| "received message Start" \| "received message" \| "received message stop" "invio del messaggio" "invio del messaggio" \| \| \| "invio del messaggio STOP")
-   Operation: il nome dell'operazione richiamata. In genere viene eseguito il mapping all'API chiamata.
-   Errore-numero di errore HRESULT facoltativo
-   Info: informazioni facoltative sull'evento

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Raccolta del file di traccia WWSAPI ETW mediante gli strumenti ETW (funziona in XPSP2 e versioni successive)

Abilitazione della traccia ETW per WWSAPI

**logman start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o <EtlLogFileName> \] -ETS**

per creare e avviare la sessione di traccia ETW. Logman.exe è uno strumento ETW interno disponibile su tutte le piattaforme supportate. Si noti che è necessario usare \_ \_ i servizi WebService di Microsoft Windows come nome del provider in xpsp2 e W2K3. È possibile eseguire Logman query providers per visualizzare l'elenco dei provider registrati. È necessario elencare il provider Microsoft-Windows-WebServices (o Microsoft \_ Windows \_ WebServices), a meno che non sia registrato. Il provider viene normalmente registrato durante l'installazione. Tuttavia, può anche essere registrato manualmente eseguendo wevtutil.exe im <ManifestFileName> (in Windows Vista e versioni successive) o mofcomp.exe <MofFileName> (in xpsp2 e W2K3).

I flag possono essere utilizzati per filtrare le tracce in base al tipo. Può essere o un valore dei seguenti tipi di traccia. Se non è specificato, tutti i tipi di traccia sono abilitati.

-   0x1: tracce di ingresso/uscita API.
-   0x2-tracce di errore.
-   tracce di 0x4-IO.
-   0x8: tracce di messaggi SOAP.
-   0x10: tracce di messaggi binari.

Il livello può essere utilizzato per filtrare le tracce in base al relativo livello. Deve essere uno dei valori seguenti. Se non è specificato, tutti i livelli di traccia sono abilitati.

-   0x1-tracce irreversibili.
-   0x2-tracce di errore.
-   0x3-tracce di avviso.
-   0x4-tracce informative.
-   0x5-tracce dettagliate.

EtlLogFileName è il percorso del file di log eventi ETW da creare (usare l'estensione ETL). Se non viene specificato, ETW sceglie un nome casuale su cui è possibile eseguire query in un secondo momento. Il file non deve trovarsi nella directory del profilo dell'utente. Il file di registro eventi ETW (file con estensione ETL) è in formato binario. Può essere utilizzato dalle applicazioni ETW, ma non è in formato leggibile. Il passaggio successivo descrive come visualizzarne il contenuto.

Eseguire lo scenario

Raccolta del file di registro eventi ETW.

**logman stop wstrace-ETS**

per arrestare la sessione di traccia ETW. Questo è il momento in cui ETW interrompe la registrazione degli eventi. Il file di registro eventi ETW (specificato nel parametro EtlLogFileName) è pronto per essere utilizzato. Può essere visualizzato localmente (le istruzioni sono fornite di seguito) o inviato al gruppo di prodotti per l'analisi.

Esempio end-to-end con gli strumenti ETW:

**logman start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-WebServices-o Trace. etl-ETS**

**Echo... eseguire lo scenario.**

**logman stop wstrace-ETS**

**tracerpt di traccia. etl-o mytrace.xml**

**wstrace.htm**

**Echo... utilizzare mytrace.xml e wstrace. xsl nella pagina aperta.**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Visualizzazione delle tracce del file di traccia WWSAPI ETW mediante lo strumento wstracedump.exe (funziona in Windows XP e versioni successive)

Wstracedump.exe è uno strumento di consumer ETW sviluppato personalizzato che elabora gli eventi nel file di traccia WWSAPI ETW e produce un output leggibile. Può produrre output da tutte le piattaforme supportate. Per ulteriori informazioni, vedere l'utilizzo (wstracedump.exe-?).

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Visualizzazione delle tracce del file di traccia di WWSAPI ETW mediante gli strumenti ETW (funziona in Windows Vista e versioni successive)

Tracerpt.exe è lo strumento per visualizzare il contenuto di un file di log eventi ETW e disponibile in tutte le piattaforme supportate. Può essere utilizzato per generare file di dump CSV, EVTX o XML da un file di log eventi ETW. Tuttavia, il file di output generato ha tracce leggibili solo in Windows Vista e versioni successive. Queste istruzioni illustrano come generare il file di dump XML e usarlo insieme a un file XSL per visualizzare le tracce in un formato gradevole (il file XSL è molto semplice e può essere modificato se si desiderano formati diversi).

-   Esegui

    **tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    per creare un dump XML dal file ETL binario (tracerpt.exe crea il file di output in formato XML per impostazione predefinita. Eseguire tracerpt-? Per visualizzare altri formati disponibili).

-   A questo punto, è possibile visualizzare le informazioni di traccia nel file XML. Inoltre, è possibile aprire il file di wstrace.htm e utilizzare il file di dump XML e il file wstrace. xsl per visualizzare le tracce in un formato più gradevole. Si noti che i file devono trovarsi nel computer locale per poter usare questo file HTML in IE.

## <a name="security"></a>Sicurezza

Quando si Abilita la funzionalità di traccia, gli amministratori devono tenere in considerazione il consumo di spazio su disco e la potenza di calcolo. Un'applicazione o un client dannoso può esaurire le risorse di sistema a meno che le impostazioni di traccia non siano configurate con limiti Quando si utilizza la funzionalità di traccia dei messaggi, i messaggi che contengono informazioni riservate, ad esempio credenziali, informazioni personali e così via, possono essere salvati in modo permanente sul disco o essere visualizzati da chiunque abbia accesso al Visualizzatore eventi di sistema. Per ovviare a questo problema, la traccia può essere abilitata dagli utenti di sistema o amministratore in Windows 2003 e versioni successive. La traccia dei messaggi è disabilitata in Windows XP su cui qualsiasi utente può attivare la traccia.

La seguente enumerazione viene utilizzata con la traccia:

-   [**\_API di traccia WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




