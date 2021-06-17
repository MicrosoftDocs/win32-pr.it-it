---
description: Guida per gli sviluppatori per la versione ridistribuibile di XAudio 2.9
ms.assetid: ''
title: Guida per gli sviluppatori per la versione ridistribuibile di XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a73ebd01d599446dc96e1e6735d8af572203a23b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262593"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Guida per gli sviluppatori per la versione ridistribuibile di XAudio 2.9

Una versione di XAudio 2.9 è disponibile come [pacchetto NuGet.](/nuget/what-is-nuget) Gli sviluppatori possono ridistribuire questa versione di XAudio 2.9 con le proprie app. In questo modo un'app può usare XAudio 2.9 in versioni precedenti di Windows che non includono XAudio 2.9 come parte dell'immagine del sistema operativo. L'uso di questo ridistribuibile è preferibile rispetto alla ridistribuzione di XAudio 2.7 da DirectX SDK, perché XAudio 2.7 non è stato aggiornato dal 2010.

Assicurarsi di visitare la pagina di destinazione [di DirectX](https://devblogs.microsoft.com/directx/landing-page/) per altre risorse per gli sviluppatori DirectX.

## <a name="supported-platforms"></a>Piattaforme supportate

Pacchetto NuGet XAudio 2.9 (*Microsoft.XAudio2.Redist. \* . nupkg*) include una versione a 32 bit e una versione a 64 bit di una DLL che implementa l'API XAudio 2.9. La DLL è denominata XAUDIO2 \_9REDIST.DLL. Questa DLL funzionerà in Windows 7 SP1, Windows 8, Windows 8.1 e Windows 10.

Quando la DLL viene usata in un sistema Windows 10, controlla il numero di versione del9.DLL XAUDIO2 che fa parte del sistema operativo e, se il sistema operativo è più recente, delega tutte le chiamate API a \_ XAUDIO2 \_9.DLL nel sistema operativo. Ciò garantisce che le app usino sempre la versione più recente di XAudio 2.9 disponibile nella piattaforma corrente.

La DLL non è destinata a Xbox One. Se usata in Xbox One, la DLL delega sempre tutte le chiamate API a XAUDIO29.DLL nel Xbox One \_ operativo.

La DLL non è destinata alle app UWP. Le app UWP devono usare il9.DLL XAUDIO2 \_ che fa parte del sistema operativo.

## <a name="installing-the-nuget-package"></a>Installazione del pacchetto NuGet

Il modo più semplice per installare il pacchetto NuGet è usare le Gestione pacchetti [NuGet](/nuget/consume-packages/install-use-packages-visual-studio) in Microsoft Visual Studio. In questo caso, il file Visual Studio di progetto verrà aggiornato automaticamente per includere *Microsoft.XAudio2.Redist.targets*. Il file *con estensione targets* aggiunge la cartella Include con i file di intestazione per XAudio2 alla raccolta di percorsi di inclusione del progetto. Il file *con estensione targets* creerà anche il .DLL o .EXE collegamento con XAUDIO2REDIST. LIB e XAPOBASEREDIST. Lib.

Libreria XAPOBASEREDIST. LIB è necessario solo se si intende impementare un oggetto XAudio Processing Object (XAPO) personalizzato ed è possibile rimuoverlo da *Microsoft.XAudio2.Redist.targets* se non è usato.

È anche possibile usare altri strumenti per estrarre il contenuto del pacchetto NuGet o persino rinominare l'estensione di file in .zip ed estrarre i file con qualsiasi strumento di estrazione ZIP.

> È disponibile anche una ``xaudio2redist`` porta per [vc++ Gestione pacchetti](https://github.com/microsoft/vcpkg).

## <a name="compiling-your-app"></a>Compilazione dell'app

### <a name="choosing-which-headers-to-include"></a>Scelta delle intestazioni da includere

Il pacchetto NuGet XAudio 2.9 include gli stessi file di intestazione XAudio2 inclusi in Windows 10 SDK. Tuttavia, i file di intestazione hanno apportato alcune modifiche per assicurarsi che sia possibile usarli mentre si usano in modo esplicito tutte le piattaforme [supportate,](#supported-platforms)incluse le versioni precedenti di Windows.

Se si installa il pacchetto [NuGet](#installing-the-nuget-package) usando il Gestione pacchetti NuGet in Microsoft Visual Studio, il percorso dei file di intestazione viene posizionato davanti al percorso dei Windows SDK di intestazione. Ciò significa che se il codice nel progetto include XAUDIO2. L'intestazione H preleverà l'intestazione multipiattaforma dal pacchetto NuGet. Questo è in genere il comportamento desiderato.

È consigliabile prestare attenzione se si aggiunge manualmente il percorso alle intestazioni di inclusione al progetto, perché specificarle nell'ordine errato può causare XAUDIO2 specifico della versione del sistema [operativo. H](/windows/win32/api/xaudio2/) da includere dal Windows SDK, anziché dalla versione multipiattaforma di XAUDIO2.H.

Per rendere meno ergasto l'inclusione delle intestazioni, il pacchetto NuGet contiene una versione di ogni intestazione a cui viene aggiunto "REDIST". Ad esempio, oltre a XAUDIO2. H, il pacchetto NuGet include anche XAUDIO2REDIST.H. Se si preferisce, il codice può includere direttamente XAUDIO2REDIST. H per eliminare eventuali ambiguità sul file di intestazione in uso. Quando si include -REDIST. Versione H di un file di intestazione, l'ordine in cui le directory dei file di inclusione sono elencate nel file di progetto non è importante.

Si noti che se l'app viene compilata anche per Xbox One, è consigliabile continuare a includere XAUDIO2. H durante la compilazione per Xbox One, perché alcune API specifiche Xbox One sono escluse da XAUDIO2REDIST.H. Questo pacchetto NuGet non è destinato a Xbox One.

### <a name="loading-the-dll"></a>Caricamento della DLL

È consigliabile collegare l'app a XAUDIO2REDIST. LIB e installare XAUDIO2 \_9REDIST.DLL nella stessa cartella del file eseguibile dell'app. Ciò causerà il caricamento9REDIST.DLL XAUDIO2 non appena viene avviato \_ l'eseguibile. Tuttavia, se si preferisce, è possibile usare [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per caricare XAUDIO29REDIST.DLL \_ su richiesta. Si tratta di una soluzione ottimale se l'app non deve sempre usare le API XAudio2. In questo caso, tuttavia, è necessario mantenere il9REDIST.DLL XAUDIO2 caricato fino alla chiusura dell'app, poiché il tentativo di scaricare la DLL può causare un arresto anomalo se un thread in background sta ancora eseguendo codice nella \_ DLL.

A differenza della versione precedente di XAudio 2.7, non è possibile usare CoCreateInstance per caricare la DLL.

### <a name="verifying-the-dll-signature"></a>Verifica della firma dll

Il file binario9REDIST.DLL XAUDIO2 \_ è firmato da Microsoft usando una firma SHA-2. Qualsiasi codice che tenta di convalidare la firma, ad esempio i moduli anti-cheat per i giochi, deve pertanto supportare SHA-2. Si noti che Windows 7 SP1 non supportava originariamente SHA-2 e richiede un aggiornamento per aggiungere tale funzionalità. L'aggiornamento è disponibile come [KB4474419.](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update)

## <a name="testing"></a>Test

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Suono spaziale nelle versioni più recenti di Windows 10

A partire dall'Windows 10 1903, XAudio 2.9 usa automaticamente il suono [surround](#spatial-sound-and-virtual-surround)virtuale, se vengono soddisfatte determinate condizioni. È consigliabile testare il gioco che genera audio multicanale Windows 10 1903 (o versione più recente) per verificare che il gioco suoni come previsto.

#### <a name="enabling-spatial-sound"></a>Abilitazione del suono spaziale

L'utente può abilitare un formato audio spaziale facendo clic con il pulsante destro del mouse sull'icona del parlante nella barra delle applicazioni di Windows. 

XAudio 2.9 userà il formato audio spaziale selezionato dall'utente solo se il processo che usa l'API XAudio2 viene riconosciuto come gioco da Windows Game Bar. Durante lo sviluppo, è possibile che il processo non sia ancora riconosciuto come gioco dal Game Bar. Per modificare questa impostazione, usare la combinazione di tasti Win+G per visualizzare il Game Bar mentre il gioco è in esecuzione. Fare quindi clic sull'icona "Impostazioni" e selezionare la casella di controllo "Ricorda che si tratta di un gioco".

#### <a name="opting-out-from-spatial-sound"></a>Rifiuto esplicito dal suono spaziale

È possibile rifiutare esplicitamente l'uso del codificatore audio spaziale da parte di XAudio2 specificando determinati valori per il parametro [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) in [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice). 

Il suono spaziale è abilitato per queste categorie:

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

L'audio spaziale non è abilitato se viene specificata una delle categorie seguenti:

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>Gestione degli errori

È importante verificare che il gioco sia in grado di gestire una modifica nel dispositivo audio, ad esempio quando le cuffia sono collegate o scollegate. Deve essere testato con le cuffia che supportano solo la frequenza di campionamento di 44,1 kHz. Molte cuffia USB di fascia bassa e visori Bluetooth supportano solo 44,1 kHz. La transizione tra la frequenza di campionamento di 48 kHz e la frequenza di campionamento di 44,1 kHz può causare un errore anche quando viene usata la funzionalità [dell'endpoint audio](#virtual-audio-endpoint) virtuale. L'errore non si verifica se le cuffia supportano anche 48 kHz. Si noti che la funzionalità endpoint audio virtuale non è disponibile in Windows 7 SP1.

Il codice di errore restituito da XAudio 2.9 quando non è in grado di eseguire automaticamente il ripristino da una modifica dell'endpoint audio è [XAUDIO2 \_ E \_ DEVICE \_ INVALIDATED](xaudio2-error-codes.md). Tuttavia, è consigliabile che le app non hard-code una dipendenza dal codice di errore con un valore specifico.

Per ricevere una notifica dell'errore, l'app deve implementare l'interfaccia [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) e fornire un puntatore a tale interfaccia richiamando il metodo [**IXAudio2::RegisterForCallbacks.**](xaudio2-callbacks.md) L'implementazione dell'app [**di IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) verrà richiamata dall'API XAudio2 se si verifica un errore durante la riproduzione.

Si noti [**che IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) non viene necessariamente richiamato se la pipeline audio viene sospesa. Ad esempio, se l'utente riduce al minimo l'app o l'app viene sospesa per qualsiasi motivo, la riproduzione audio potrebbe essere sospesa. Se la modifica nel dispositivo audio si verifica durante questo periodo di tempo, l'errore viene restituito solo quando l'app richiama [**IXAudio2::StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) e/o richiama [**IXAudio2SourceVoice::Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start). Se la riproduzione può essere sospesa con l'app, è necessario testare la modifica del dispositivo audio mentre la riproduzione è sospesa, per verificare che l'app possa ancora recuperare da questa situazione.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Differenze dell'API XAudio 2.9 rispetto a XAudio 2.7

In questa sezione viene fornito un riepilogo di alcune differenze delle API tra XAudio 2.7 e la versione ridistribuibile di XAudio 2.9.

### <a name="supported-formats"></a>Formati supportati

XAudio 2.9 supporta questi formati di input nel PC:

* PCM lineare a 16 bit
* PCM float a 32 bit lineare
* ADPCM a 16 bit
* xWMA

Il formato XMA è supportato solo in Xbox One.

### <a name="preferred-cpu-core"></a>Core CPU preferito

È possibile specificare quale core CPU XAudio 2.9 deve usare per il thread di elaborazione audio. Tuttavia, è in genere preferibile consentire a XAudio 2.9 di scegliere questo valore da solo. Questa operazione viene eseguita impostando il **parametro XAudio2Processor** nella chiamata a [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) su XAUDIO2 \_ USE DEFAULT \_ \_ PROCESSOR. 

XAudio 2.9 sceglierà un core CPU diverso Xbox One su PC. Il metodo IXAudio2Extension::GetProcessor può essere usato per determinare quale core della CPU XAudio2 ha scelto.

### <a name="virtual-audio-endpoint"></a>Endpoint audio virtuale

XAudio 2.9 userà un endpoint audio virtuale per impostazione predefinita, quando è in Windows 8 o versioni successive. Ciò significa che se l'endpoint audio predefinito cambia mentre viene usato XAudio 2.9, tenterà di passare automaticamente al nuovo endpoint audio. Un esempio di quando ciò può verificarsi quando l'endpoint audio predefinito è una coppia di cuffia connesse tramite USB e quindi l'utente scollega le cuffia. In questo modo gli altoparlanti saranno il nuovo endpoint audio predefinito.

Se l'app specifica un formato audio specifico quando richiama [**IXAudio2::CreateMasteringVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)potrebbe non essere possibile per XAudio 2.9 eseguire questa opzione. Ad esempio, se l'app ha specificato che Mastering Voice deve usare una frequenza di campionamento di 48 kHz e il nuovo dispositivo audio supporta solo 44,1 kHz, il commutatore automatico avrà esito negativo e XAudio 2.9 segnalerà l'errore [XAUDIO2 \_ E \_ DEVICE \_ INVALIDATED.](xaudio2-error-codes.md)

L'app può rifiutare esplicitamente l'uso dell'endpoint audio virtuale passando il flag [**XAUDIO2 \_ NO VIRTUAL AUDIO \_ \_ \_ CLIENT**](xaudio2-boundary-values-and-flags.md) a [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

Gli endpoint audio virtuali non sono disponibili in Windows 7 SP1. Il flag **XAUDIO2 \_ NO VIRTUAL AUDIO \_ \_ \_ CLIENT** non ha alcun effetto su Windows 7 SP1.

### <a name="audio-categories"></a>Categorie audio

L'app deve specificare una categoria per il flusso audio. Questa operazione viene eseguita specificando un valore dall'enumerazione AudioCategory quando si richiama il [**metodo IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) Ad esempio, AudioCategory_GameEffects. La categoria audio può influire sul modo in cui Windows elabora il suono o come rappresenta il flusso audio nel pannello di controllo del volume. La categoria audio influisce anche se [l'audio surround virtuale](#spatial-sound-and-virtual-surround) viene abilitato automaticamente.

### <a name="duration-of-audio-processing-quantum"></a>Durata del quantum di elaborazione audio

Nella maggior parte dei PC, XAudio 2.9 elabora l'audio in blocchi di 10 millisecondi. Si tratta del quantum di elaborazione. Tuttavia, la durata di questo quantistico può essere diversa da 10 millisecondi in alcuni componenti hardware. Le app che devono conoscere il quantum esatto possono richiamare il metodo IXAudio2Extension::GetProcessingQuantum per recuperare il valore.

### <a name="spatial-sound-and-virtual-surround"></a>Suono spaziale e surround virtuale

A partire dall'Windows 10 1903, XAudio 2.9 usa automaticamente il suono surround virtuale, se vengono soddisfatte determinate condizioni. È consigliabile testare il gioco che genera audio multicanale Windows 10 1903 (o versione più recente) per verificare che il gioco suoni come previsto. Per una discussione [su come testare questa](#spatial-sound-in-newer-versions-of-windows-10) funzionalità, vedere la sezione test del suono spaziale.

In genere, XAudio 2.9 esegue un folds down qualsiasi audio multicanale in modo che corrisponda al numero "fisico" di canali audio supportati dall'endpoint audio. Ad esempio, se il gioco fornisce un'origine audio a 7,1 canali, ma il suono viene riprodotto sulle cuffia, XAudio 2.9 ridurà l'audio del canale 7.1 in stereo, usando una matrice di fold-down standard del settore. Se il PC è connesso a un endpoint audio HDMI, l'audio del canale 7.1 verrà trasmesso così come è tramite la connessione HDMI.

Windows 10 aggiunge il supporto per l'audio spaziale, usando un codificatore centralizzato che codifica l'audio in un formato audio [spaziale selezionato dall'utente.](../coreaudio/spatial-sound.md) Windows 10 è incluso in un formato audio spaziale denominato Windows Sonic. Altri formati, ad esempio Dolby Atmos for Headphones, possono essere scaricati dal Microsoft Store. Alcuni dei formati audio spaziali, ad esempio Windows Sonic e Dolby Atmos for Headphones, sono progettati per l'uso su endpoint audio stereo. Questi formati ri fold down surround sound to stereo using proprietary algorithms that achieve a "virtual" surround sound effect(Effetti sonori surround "virtuali"). In altre parole, l'ascoltatore può percepire il suono che appare da posizioni diverse nello spazio 3D anche quando indossa solo le cuffia o durante l'ascolto su una singola coppia di altoparlanti stereo.

Effetti simili possono essere ottenuti [usando le API X3DAudio](x3daudio.md) incluse in XAudio 2.9. La differenza principale è che X3DAudio richiede allo sviluppatore di app di programmare in modo esplicito l'audio 3D, mentre il suono surround virtuale viene applicato automaticamente a qualsiasi origine audio basata su canale tradionale.

In Windows 10 1903 e versioni più nuove, i giochi che usano XAudio 2.9 useranno il formato audio spaziale a livello di sistema abilitato dall'utente nell'endpoint audio, se presente. Questo significa che XAudio 2.9 non eseguirà il consueto fold-down del suono surround in stereo. Il segnale sonoro surround verrà invece recapitato al codificatore di suoni spaziali (ad esempio, Windows Sonic) per ottenere un effetto sonoro surround virtuale.

### <a name="createhrtfapo"></a>CreateHrtfApo

La [**funzione CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) è disponibile solo in Windows 10. Non viene implementato in XAudio 2.9 Redistributable.
