---
description: Guida per gli sviluppatori per la versione ridistribuibile di XAudio 2,9
ms.assetid: ''
title: Guida per gli sviluppatori per la versione ridistribuibile di XAudio 2,9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a87c2dc44179f2c189270dfa91d2cf2696ea98a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103969008"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Guida per gli sviluppatori per la versione ridistribuibile di XAudio 2,9

Una versione di XAudio 2,9 è disponibile come [pacchetto NuGet](/nuget/what-is-nuget). Gli sviluppatori possono ridistribuire questa versione di XAudio 2,9 con le proprie app. Questo consente a un'app di usare XAudio 2,9 nelle versioni precedenti di Windows che non includono XAudio 2,9 come parte dell'immagine del sistema operativo. L'uso di questo ridistribuibile è preferibile rispetto alla ridistribuzione di XAudio 2,7 da DirectX SDK, perché XAudio 2,7 non è stato aggiornato da 2010.

## <a name="supported-platforms"></a>Piattaforme supportate

Pacchetto NuGet XAudio 2,9 (*Microsoft. XAudio2. Redist. \* . nupkg*) include una versione a 32 bit e una versione a 64 bit di una dll che implementa l'API XAudio 2,9. La DLL è denominata XAUDIO2 \_9REDIST.DLL. Questa DLL funzionerà in Windows 7 SP1, Windows 8, Windows 8.1 e Windows 10.

Quando la DLL viene usata in un sistema Windows 10, controlla il numero di versione di XAUDIO2 \_9.DLL che fa parte del sistema operativo e, se il sistema operativo è più recente, delegherà tutte le chiamate API a XAUDIO2 \_9.DLL nel sistema operativo. Ciò garantisce che le app usino sempre la versione più recente di XAudio 2,9 disponibile nella piattaforma corrente.

La DLL non è destinata a Xbox One. Se usato su Xbox One, la DLL delega sempre tutte le chiamate API a XAUDIO2 \_9.DLL nel sistema operativo Xbox One.

La DLL non è destinata alle app UWP. Le app UWP devono usare la \_9.DLL XAUDIO2 che fa parte del sistema operativo.

## <a name="installing-the-nuget-package"></a>Installazione del pacchetto NuGet

Il modo più semplice per installare il pacchetto NuGet consiste nell'usare [Gestione pacchetti NuGet](/nuget/consume-packages/install-use-packages-visual-studio) in Microsoft Visual Studio. In tal caso, il file di progetto di Visual Studio verrà aggiornato automaticamente per includere *Microsoft. XAudio2. Redist. targets*. Il file con *estensione targets* aggiunge la cartella di inclusione con i file di intestazione per XAudio2 alla raccolta di percorsi di inclusione del progetto. Il file con *estensione targets* renderà anche il. DLL o. Collegamento EXE con XAUDIO2REDIST. LIB e XAPOBASEREDIST. LIB.

XAPOBASEREDIST della libreria. LIB è necessario solo se si intende impement un oggetto di elaborazione XAudio personalizzato (XAPO) ed è possibile rimuoverlo da *Microsoft. XAudio2. Redist. targets* se non è usato.

È anche possibile usare altri strumenti per estrarre il contenuto del pacchetto NuGet o persino rinominare l'estensione di file in. zip ed estrarre i file con qualsiasi strumento di estrazione ZIP.

## <a name="compiling-your-app"></a>Compilazione dell'app

### <a name="choosing-which-headers-to-include"></a>Scelta delle intestazioni da includere

Il pacchetto NuGet XAudio 2,9 include gli stessi file di intestazione XAudio2 inclusi in Windows 10 SDK. Tuttavia, i file di intestazione hanno apportato alcune modifiche per assicurarsi che sia possibile usarli in modo esplicito per tutte le [piattaforme supportate](#supported-platforms), incluse le versioni precedenti di Windows.

Se si [installa il pacchetto NuGet](#installing-the-nuget-package) usando Gestione pacchetti nuget in Microsoft Visual Studio, il percorso dei file di intestazione viene inserito davanti al percorso dei file di intestazione Windows SDK. Ciò significa che se il codice nel progetto include XAUDIO2. Intestazione H, prenderà l'intestazione multipiattaforma dal pacchetto NuGet. Si tratta in genere del comportamento desiderato.

È necessario prestare attenzione se si aggiunge manualmente il percorso alle intestazioni di inclusione al progetto, perché specificarle nell'ordine errato può causare la XAUDIO2 specifica della versione del sistema operativo [. H](/windows/win32/api/xaudio2/) da includere dalla Windows SDK, anziché dalla versione multipiattaforma di XAUDIO2. H.

Per fare in modo che l'inclusione delle intestazioni sia meno soggetta a errori, il pacchetto NuGet contiene una versione di ogni intestazione con "REDIST" aggiunta. Ad esempio, oltre a XAUDIO2. H, il pacchetto NuGet include anche XAUDIO2REDIST. H. Se si preferisce, il codice può includere direttamente XAUDIO2REDIST. H per eliminare qualsiasi ambiguità sul file di intestazione utilizzato. Quando si include-REDIST. Versione H di un file di intestazione. l'ordine in cui sono elencate le directory dei file di inclusione nel file di progetto non è rilevante.

Si noti che se l'app viene compilata anche per Xbox One, è necessario continuare a includere XAUDIO2. H quando si esegue la compilazione per Xbox One, perché alcune API specifiche di Xbox sono escluse da XAUDIO2REDIST. H. Questo pacchetto NuGet non è destinato a Xbox One.

### <a name="loading-the-dll"></a>Caricamento della DLL

È consigliabile collegare l'app a XAUDIO2REDIST. LIB e install XAUDIO2 \_9REDIST.DLL nella stessa cartella dell'eseguibile dell'app. Questo comporterà il \_ caricamento di XAUDIO29REDIST.DLL non appena viene avviato il file eseguibile. Tuttavia, se si preferisce, è possibile usare [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) e [**GETPROCADDRESS**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per caricare XAUDIO2 \_9REDIST.DLL su richiesta. Si tratta di una soluzione efficace se l'app non deve sempre usare le API XAudio2. Tuttavia, se si esegue questa operazione, è consigliabile mantenere il XAUDIO2 \_9REDIST.DLL caricato fino alla chiusura dell'app, perché il tentativo di scaricare la dll può causare un arresto anomalo se un thread in background sta ancora eseguendo codice nella dll.

Diversamente dalla versione precedente di XAudio 2,7, non è possibile usare CoCreateInstance per caricare la DLL.

### <a name="verifying-the-dll-signature"></a>Verifica della firma della DLL

Il \_ file binario9REDIST.DLL XAUDIO2 è firmato da Microsoft utilizzando una firma SHA-2. Il codice che tenta di convalidare la firma, ad esempio i moduli anti-cheat per i giochi, deve quindi supportare SHA-2. Si noti che Windows 7 SP1 non supporta originariamente SHA-2 e richiede un aggiornamento per aggiungere tale funzionalità. L'aggiornamento è disponibile come [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update).

## <a name="testing"></a>Test

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Audio spaziale nelle versioni più recenti di Windows 10

A partire dall'aggiornamento di Windows 10 1903, XAudio 2,9 USA automaticamente il [suono surround virtuale](#spatial-sound-and-virtual-surround), se vengono soddisfatte determinate condizioni. Si consiglia di testare il gioco che genera un suono multicanale in Windows 10 1903 (o versione successiva) per verificare che il gioco suoni come previsto.

#### <a name="enabling-spatial-sound"></a>Abilitazione del suono spaziale

L'utente può abilitare un formato audio spaziale facendo clic con il pulsante destro del mouse sull'icona dell'altoparlante nella barra di sistema di Windows. 

XAudio 2,9 userà solo il formato audio spaziale selezionato dall'utente solo se il processo che usa l'API XAudio2 è riconosciuto come gioco dalla barra dei giochi di Windows. Durante lo sviluppo, è possibile che il processo non sia ancora riconosciuto come gioco dalla barra del gioco. Per modificare questa operazione, usare il tasto di scelta rapida Win + G per visualizzare la barra del gioco mentre il gioco è in esecuzione. Quindi, fare clic sull'icona "Settings" (impostazioni) e selezionare la casella di controllo "tenere presente che si tratta di un gioco".

#### <a name="opting-out-from-spatial-sound"></a>Esclusione dal suono spaziale

È possibile rifiutare esplicitamente a XAudio2 di usare il codificatore audio spaziale specificando determinati valori per il parametro [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) in [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice). 

Il suono spaziale è abilitato per le categorie seguenti:

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

Il suono spaziale non è abilitato se viene specificata una delle seguenti categorie:

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>Gestione degli errori

È importante verificare che il gioco possa gestire una modifica nel dispositivo audio, ad esempio quando le cuffie sono collegate o scollegate. Questa operazione deve essere testata con le cuffie che supportano solo la frequenza di campionamento di 44,1 kHz. Molte cuffie USB di fascia bassa e auricolari Bluetooth supportano solo 44,1 kHz. La transizione tra la frequenza di campionamento di 48 kHz e la frequenza di campionamento di 44,1 kHz può causare un errore anche quando viene usata la funzionalità dell' [endpoint audio virtuale](#virtual-audio-endpoint) . L'errore non si verifica se le cuffie supportano anche 48 kHz. Si noti che la funzionalità endpoint audio virtuale non è disponibile in Windows 7 SP1.

Il codice di errore restituito da XAudio 2,9 quando non è possibile eseguire il ripristino automatico da una modifica nell'endpoint audio è [XAUDIO2 \_ E il dispositivo è \_ \_ invalidato](xaudio2-error-codes.md). Tuttavia, è consigliabile che le app non codifichino a livello di codice una dipendenza dal codice di errore con un valore specifico.

Per ricevere una notifica dell'errore, l'app deve implementare l'interfaccia [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) e fornire un puntatore a tale interfaccia richiamando il metodo [**IXAudio2:: RegisterForCallbacks**](xaudio2-callbacks.md) . L'implementazione dell'app di [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) verrà richiamata dall'API XAudio2 se si verifica un errore durante la riproduzione.

Si noti che [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) non viene necessariamente richiamato se la pipeline audio è sospesa. Ad esempio, se l'utente riduce al minimo l'app o l'app viene sospesa per qualsiasi motivo, la riproduzione audio potrebbe essere sospesa. Se la modifica apportata al dispositivo audio si verifica durante questo periodo di tempo, l'errore viene restituito solo quando l'app richiama [**IXAudio2:: avvio**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) e/o richiama [**IXAudio2SourceVoice:: Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start). Se la riproduzione può essere sospesa con l'app, è necessario testare la modifica del dispositivo audio mentre la riproduzione viene sospesa, per verificare che l'app possa ancora eseguire il ripristino da questa situazione.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Differenze dell'API XAudio 2,9 rispetto a XAudio 2,7

Questa sezione fornisce un riepilogo delle differenze tra le API tra XAudio 2,7 e la versione ridistribuibile di XAudio 2,9.

### <a name="supported-formats"></a>Formati supportati

XAudio 2,9 supporta questi formati di input nel PC:

* PCM lineare a 16 bit
* PCM a virgola mobile a 32 bit lineare
* ADPCM a 16 bit
* xWMA

Il formato XMA è supportato solo su Xbox One.

### <a name="preferred-cpu-core"></a>Core CPU preferito

È possibile specificare quale core CPU XAudio 2,9 deve usare per il thread di elaborazione audio. Tuttavia, in genere è preferibile consentire a XAudio 2,9 di scegliere questo valore in modo autonomo. Questa operazione viene eseguita impostando il parametro **XAudio2Processor** nella chiamata a [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) su XAUDIO2 \_ usare \_ il \_ processore predefinito. 

XAudio 2,9 sceglierà un core CPU diverso su Xbox One rispetto al computer. Il metodo IXAudio2Extension:: getprocessor può essere usato per determinare il XAudio2 di core CPU scelto.

### <a name="virtual-audio-endpoint"></a>Endpoint audio virtuale

Per impostazione predefinita, XAudio 2,9 userà un endpoint audio virtuale quando viene eseguito in Windows 8 o versione successiva. Ciò significa che se l'endpoint audio predefinito viene modificato mentre viene usato XAudio 2,9, viene eseguito un tentativo di passare automaticamente al nuovo endpoint audio. Un esempio di quando questo può verificarsi quando l'endpoint audio predefinito è una coppia di cuffie connesse tramite USB e quindi l'utente scollega le cuffie. In questo modo, i relatori saranno il nuovo endpoint audio predefinito.

Se l'app specifica un formato audio specifico quando si richiama [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice), potrebbe non essere possibile per xaudio 2,9 eseguire questa opzione. Se, ad esempio, l'app ha specificato che la voce di mastering deve usare una frequenza di campionamento di 48 kHz e il nuovo dispositivo audio supporta solo 44,1 kHz, l'opzione automatica avrà esito negativo e XAudio 2,9 segnalerà l'errore di [ \_ dispositivo XAUDIO2 e \_ \_ invalidato](xaudio2-error-codes.md) .

L'app può rifiutare esplicitamente l'uso dell'endpoint audio virtuale passando il flag [**XAUDIO2 \_ No \_ virtual \_ audio \_ client**](xaudio2-boundary-values-and-flags.md) a [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

Gli endpoint audio virtuali non sono disponibili in Windows 7 SP1. Il flag **XAUDIO2 \_ No \_ virtual \_ audio \_ client** non ha alcun effetto su Windows 7 SP1.

### <a name="audio-categories"></a>Categorie audio

L'app deve specificare una categoria per il flusso audio. Questa operazione viene eseguita fornendo un valore dall'enumerazione AudioCategory quando si richiama il metodo [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) . Ad esempio, AudioCategory_GameEffects. La categoria audio può influenzare il modo in cui Windows elabora il suono o il modo in cui rappresenta il flusso audio nel pannello di controllo del volume. La categoria audio ha effetto anche se il [suono surround virtuale](#spatial-sound-and-virtual-surround) viene abilitato automaticamente.

### <a name="duration-of-audio-processing-quantum"></a>Durata del quantum di elaborazione audio

Nella maggior parte dei PC, XAudio 2,9 elabora l'audio in blocchi di 10 millisecondi. Questa operazione è denominata Quantum di elaborazione. Tuttavia, la durata di questo quantum può essere diversa da 10 millisecondi in alcuni componenti hardware. Le app che devono essere a conoscenza del quantum esatto possono richiamare il metodo IXAudio2Extension:: GetProcessingQuantum per recuperare il valore.

### <a name="spatial-sound-and-virtual-surround"></a>Audio spaziale e surround virtuale

A partire dall'aggiornamento di Windows 10 1903, XAudio 2,9 USA automaticamente il suono surround virtuale, se vengono soddisfatte determinate condizioni. Si consiglia di testare il gioco che genera un suono multicanale in Windows 10 1903 (o versione successiva) per verificare che il gioco suoni come previsto. Per una discussione su come testare questa funzionalità, vedere la sezione [test del suono spaziale](#spatial-sound-in-newer-versions-of-windows-10) .

In genere, XAudio 2,9 esegue un riduzioni di qualsiasi audio multicanale in modo che corrisponda al numero "fisico" di canali audio supportati dall'endpoint audio. Ad esempio, se il gioco fornisce un'origine audio del canale 7,1, ma il suono viene riprodotto in cuffia, XAudio 2,9 ridurrà l'audio del canale 7,1 in stereo, usando una matrice di riduzioni standard del settore. Se il PC è connesso a un endpoint audio HDMI, l'audio del canale 7,1 verrà trasmesso così com'è attraverso la connessione HDMI.

Windows 10 aggiunge il supporto per l'audio spaziale, usando un codificatore centralizzato che codifica l'audio in un formato [audio spaziale](../coreaudio/spatial-sound.md) selezionato dall'utente. Windows 10 è incluso in un formato audio spaziale denominato Windows Sonic. È possibile scaricare altri formati, ad esempio Dolby Atmos per le cuffie, dal Microsoft Store. Alcuni formati audio spaziali, ad esempio Windows Sonic e Dolby Atmos per le cuffie, sono progettati per essere usati in endpoint audio stereo. Questi formati ripiegano il suono surround in stereo usando algoritmi proprietari che raggiungono un effetto audio surround "virtuale". In altre parole, il listener può percepire un suono da posizioni diverse nello spazio 3D anche quando si indossano solo le cuffie o quando si è in ascolto su una singola coppia di altoparlanti stereo.

È possibile ottenere effetti simili usando le API [X3DAudio](x3daudio.md) incluse in xaudio 2,9. La differenza principale consiste nel fatto che X3DAudio richiede allo sviluppatore di app di programmare in modo esplicito l'audio 3D, mentre il suono surround virtuale viene applicato automaticamente a qualsiasi origine audio basata sul canale tradional.

In Windows 10 1903 e versioni successive, i giochi che usano XAudio 2,9 utilizzeranno il formato audio spaziale a livello di sistema che l'utente ha abilitato sull'endpoint audio, se disponibile. Ciò significa che XAudio 2,9 non eseguirà la normale riduzione del suono surround a stereo. Al contrario, il segnale audio surround verrà recapitato al codificatore audio spaziale (ad esempio, Windows Sonic) per ottenere un effetto audio surround virtuale.

### <a name="createhrtfapo"></a>CreateHrtfApo

La funzione [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) è disponibile solo in Windows 10. Non è implementato in XAudio 2,9 Redistributable.
