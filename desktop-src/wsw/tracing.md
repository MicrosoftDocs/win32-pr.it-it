---
title: Traccia
description: La traccia usa Event Tracing for Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Traccia dei servizi Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2bcd5c07c2c5ebf3a28620e39efe3034d3c2bc024ac487caaec38e3c69fca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707261"
---
# <a name="tracing"></a>Traccia

La traccia usa Event Tracing for Windows (ETW). Per sfruttare gli strumenti di traccia disponibili con Windows Server 2008 R2, installare Microsoft Windows SDK dal sito [Msdn Downloads.](https://www.microsoft.com/download/details.aspx?id=8279)


Sono supportati tre livelli di traccia:

-   Dettagliato (tutte le tracce disponibili).
-   Informazioni (tracce in informazioni).
-   Errore (tracce degli errori).

Vengono tracciati gli eventi seguenti:

-   Eventuali errori (Level=Error, Level=Info o Level=Verbose).
-   Ingresso/uscita di un'API (Level=Info o Level=Verbose).
-   Avvio e completamento di qualsiasi I/O (Level=Info o Level=Verbose)
-   Messaggi SOAP s exchanged (Level=Verbose, disponibile in Windows 2003 SP1 e versioni successive)

## <a name="generating-and-viewing-wwsapi-traces"></a>Generazione e visualizzazione di tracce WWSAPI

WWSAPI usa gli eventi basati su manifesto Windows Vista e versioni successive. Di conseguenza, l'esperienza di traccia presenta alcune differenze in base alla versione del sistema operativo. La generazione di tracce ETW può essere eseguita usando gli strumenti ETW disponibili in tutte le piattaforme supportate. Tuttavia, la visualizzazione delle tracce ETW in un formato ottimale richiede strumenti personalizzati Windows XP SP2 e Windows 2003 SP1. Esistono diversi modi per raccogliere e visualizzare le tracce degli eventi ETW WWSAPI a seconda della versione del sistema operativo.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Abilitazione e visualizzazione delle tracce WWSAPI in Visualizzatore eventi (funziona Windows Vista e versioni successive)

-   Eseguire eventvwr.msc dalla riga di comando o dal menu esegui.
-   Fare clic sul collegamento alla visualizzazione nel riquadro Azioni a destra e abilitare l'opzione Mostra log analitici e di debug.
-   Passare a Log applicazioni e servizi \\ Microsoft \\ Windows \\ WebServices provider nel riquadro sinistro.
-   Fare clic con il pulsante destro del mouse sul provider di traccia e scegliere Abilita log.
-   Eseguire lo scenario.
-   Quando si aggiorna la pagina del Visualizzatore eventi, è necessario iniziare a visualizzare le voci di traccia WWSAPI.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Abilitazione e visualizzazione delle tracce WWSAPI usando Wstrace.bat script (funziona in XPSP2 e versione precedente)

Il wstrace.bat batch consente di:

-   Creare un log di traccia
-   Eliminare un log di traccia
-   Abilitare e disabilitare la traccia
-   Aggiornare il livello di traccia (info/error/verbose)
-   Conversione dei log di traccia in file CSV

Il file batch usa logman.exe tutti i comandi, ad eccezione della conversione dei log in file CSV, che richiede uno strumento personalizzato (wstracedump.exe).

## <a name="using-tracing-commands"></a>Uso dei comandi di traccia

Il comando seguente crea un log che usa informazioni, errori o livelli dettagliati. Questo comando richiede privilegi elevati.

**wstrace.bat dettagliato \[ \| dell'errore di creazione delle \| informazioni\]**

Il comando seguente elimina il log. Questo comando richiede privilegi elevati.

**wstrace.bat eliminazione**

Il comando seguente abilita la traccia. È prima necessario creare un log.

**wstrace.bat su**

Il livello di traccia (informazioni, errore o dettagliato) può essere modificato come segue:

**wstrace.bat dettagliato \[ dell'errore \| di aggiornamento delle \| informazioni\]**

Per eseguire il dump dell'output di traccia, usare il comando seguente:

**wstrace.bat dump > temp.csv**

Gli eventi verranno scaricati nel file CSV fino a quando non viene premuto CTRL+C o non viene disabilitata la traccia.

## <a name="tracing-file-format"></a>Formato del file di traccia

I file CSV creati da wstrace.bat semplici file di testo delimitati da virgole. Questi file possono essere aperti in Excel, Blocco note e così via.

Le colonne del file sono le seguenti:

-   TimeStamp : timestamp di data e ora in cui è stato registrato l'evento
-   ProcessID : ID ULONG del processo che registra l'evento
-   ThreadID: ID ULONG del thread che registra l'evento
-   Event - Il valore enumerato del tipo di evento può essere ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message \| start" "received message stop" \| "sending message start" "sending message stop" \| \| "sending message stop"
-   Operazione: nome dell'operazione richiamata. In genere viene eseguito il mapping all'API chiamata.
-   Errore - Numero di errore HRESULT facoltativo
-   Info : informazioni facoltative sull'evento

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Raccolta del file di traccia ETW WWSAPI con gli strumenti ETW (funziona in XPSP2 e versione precedente)

Abilitazione della traccia ETW per WWSAPI

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o <EtlLogFileName> \] -ets**

per creare e avviare la sessione di traccia ETW. Logman.exe è uno strumento ETW disponibile in tutte le piattaforme supportate. Si noti che è necessario usare Microsoft Windows WebServices come \_ nome del provider in \_ XPSP2 e W2K3. È possibile eseguire provider di query logman per visualizzare l'elenco dei provider registrati. Il provider Microsoft-Windows-WebServices (o Microsoft Windows WebServices) deve essere elencato a meno che non \_ \_ sia registrato. Il provider viene in genere registrato durante l'installazione. Tuttavia, può anche essere registrato manualmente eseguendo wevtutil.exe im (in Windows Vista e versioni successive) o <ManifestFileName> mofcomp.exe <MofFileName> (in XPSP2 e W2K3).

I flag possono essere usati per filtrare le tracce in base al tipo. Può essere OR dei tipi di traccia seguenti. Se non viene specificato, tutti i tipi di traccia sono abilitati.

-   0x1- Tracce di ingresso/uscita dell'API.
-   0x2- Tracce degli errori.
-   0x4- Tracce di I/O.
-   0x8: tracce di messaggi SOAP.
-   0x10: tracce di messaggi binari.

Level può essere usato per filtrare le tracce in base al relativo livello. Deve essere uno dei valori seguenti. Se non viene specificato, tutti i livelli di traccia sono abilitati.

-   0x1: tracce irreversibili.
-   0x2- Tracce degli errori.
-   0x3- Tracce di avviso.
-   0x4: tracce in informazioni.
-   0x5: tracce dettagliate.

EtlLogFileName è il percorso del file di log eventi ETW da creare (usare l'estensione etl). Se non viene specificato, ETW sceglierà un nome casuale che può essere sottoposto a query in un secondo momento. Questo file non deve risiedere nella directory del profilo dell'utente. Il file di log eventi ETW (file con estensione etl) è in formato binario. Può essere utilizzato dalle applicazioni ETW, ma non è in formato leggibile dall'utente. Il passaggio successivo descrive come visualizzarne il contenuto.

Eseguire lo scenario

Raccolta del file di log eventi ETW.

**logman stop wstrace -ets**

per arrestare la sessione di traccia ETW. Questo è il momento in cui ETW interrompe la registrazione degli eventi. Il file di log eventi ETW (specificato nel parametro EtlLogFileName) è pronto per l'utilizzo. Può essere visualizzato in locale (le istruzioni sono riportate di seguito) o inviato al gruppo di prodotti per l'analisi.

Esempio end-to-end con strumenti ETW:

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**

**Eco.. eseguire lo scenario.**

**logman stop wstrace -ets**

**tracerpt mytrace.etl -o mytrace.xml**

**wstrace.htm**

**Eco.. usare mytrace.xml e wstrace.xsl nella pagina aperta.**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Visualizzazione delle tracce del file di traccia ETW WWSAPI wstracedump.exe strumento (funziona Windows XP e successive)

Wstracedump.exe è uno strumento consumer ETW sviluppato personalizzato che elabora gli eventi nel file di traccia ETW WWSAPI e produce output leggibile dall'utente. Può produrre output da tutte le piattaforme supportate. Per altre informazioni, vedere l'utilizzo (wstracedump.exe -?).

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Visualizzazione delle tracce del file di traccia ETW WWSAPI con gli strumenti ETW (funziona Windows Vista e versioni successive)

Tracerpt.exe è lo strumento per visualizzare il contenuto di un file di log eventi ETW e disponibile in tutte le piattaforme supportate. Può essere usato per generare file di dump CSV, EVTX o XML da un file di log eventi ETW. Tuttavia, il file di output generato ha tracce leggibili umane solo Windows Vista e versioni successive. Queste istruzioni descrivono come generare il file di dump XML e usarlo insieme a un file xsl per visualizzare le tracce in un formato corretto (il file xsl è molto semplice e può essere modificato se si desiderano formati diversi).

-   Esegui

    **tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    per creare un dump XML dal file binario ETL (tracerpt.exe il file di output in formato XML per impostazione predefinita. Eseguire tracerpt -? Per visualizzare altri formati disponibili.

-   A questo punto, è possibile visualizzare le informazioni di traccia nel file XML. È anche possibile aprire il file wstrace.htm e usare il file dump xml e il file wstrace.xsl per visualizzare le tracce in un formato più corretto. Si noti che i file devono essere nel computer locale per poter usare questo file HTML in IE.

## <a name="security"></a>Sicurezza

Quando si abilita la traccia, gli amministratori devono prendere in considerazione l'utilizzo di ulteriore spazio su disco e potenza di calcolo. Un client o un'applicazione dannosa può esaurire le risorse di sistema a meno che le impostazioni di traccia non siano configurate con limiti ragionevoli. Quando si usa la funzionalità di traccia dei messaggi, i messaggi che contengono informazioni riservate, ad esempio credenziali, informazioni personali e così via, possono essere resi persistenti sul disco o visualizzati da chiunque abbia accesso al Visualizzatore eventi di sistema. Come mitigazione di questo problema, la traccia può essere abilitata dagli utenti di sistema o amministratore Windows 2003 e versioni successive. La traccia dei messaggi è disabilitata Windows XP in cui qualsiasi utente può attivare la traccia.

L'enumerazione seguente viene utilizzata con la traccia:

-   [**API \_ DI TRACCIA WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




