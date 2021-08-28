---
description: Quando Shell rileva l'inserimento di nuovi supporti o l'allegato di un dispositivo hot-plug, viene determinato il contenuto del dispositivo o del supporto. AutoPlay, a seconda delle impostazioni correnti, esegue una delle operazioni seguenti.
title: Uso e configurazione di AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 35de48ee77cde7c598088b3f3877083efc2151f5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481487"
---
# <a name="using-and-configuring-autoplay"></a>Uso e configurazione di AutoPlay

Quando Shell rileva l'inserimento di nuovi supporti o l'allegato di un dispositivo hot-plug, viene determinato il contenuto del dispositivo o del supporto. AutoPlay, a seconda delle impostazioni correnti, esegue una delle operazioni seguenti.

-   Riproduce automaticamente il contenuto.
-   Visualizza una finestra di dialogo che richiede all'utente di scegliere un gestore predefinito per un singolo tipo di contenuto.
-   Presenta, nel caso di contenuto misto, un elenco di applicazioni del gestore disponibili da avviare. Il gestore scelto riproduce quindi automaticamente il tipo di contenuto associato.
-   Visualizza una visualizzazione cartella standard dei file.
-   Non esegue alcuna operazione se,  in precedenza, l'utente aveva scelto Non eseguire alcuna azione per tale tipo di contenuto, nonché se è stato **specificato Eseguire sempre l'azione selezionata.**

Se il contenuto non soddisfa i criteri per AutoPlay, l'evento viene quindi passato a Windows Image Acquisition (WIA).

Negli argomenti seguenti viene illustrata la configurazione e l'uso di AutoPlay.

-   [Preparazione di hardware e software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay)
-   [Modalità di ricerca dei contenuti multimediali in AutoPlay](#how-autoplay-searches-media)
-   [Definizione di tipi di contenuto singolo e misto](#defining-single-and-mixed-content-types)
-   [Scenari di esempio](#sample-scenarios)
    -   [Riproduzione automatica per Archiviazione dispositivi con picture media](#autoplay-for-storage-devices-with-picture-media)
    -   [Riproduzione automatica per Musica di riproduzione di file e Archiviazione dispositivi contenenti Musica multimediali](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [Riproduzione automatica per la riproduzione di video alla prima presentazione](#autoplay-for-video-playback-on-first-presentation)
-   [Assegnazione di applicazioni del gestore predefinite](#assigning-default-handler-applications)
-   [Gestione di supporti contenenti tipi di contenuto misti](#handling-media-containing-mixed-content-types)
-   [Interfacce utente di AutoPlay](#autoplay-user-interfaces)
    -   [Finestra di dialogo Tipo di contenuto singolo](#single-content-type-dialog-box)
    -   [Finestra di dialogo Supporto misto](#mixed-media-dialog-box)
    -   [Pagina Proprietà](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Preparazione di hardware e software per l'uso con AutoPlay

Per il funzionamento di AutoPlay, nel Registro di sistema devono essere visualizzate diverse informazioni. Queste informazioni interagiscono e fanno riferimento tra loro per formare l'ambiente AutoPlay completo. Questo documento presenta la configurazione di ognuna di queste informazioni come una singola procedura autonoma.

Per istruzioni aggiuntive, vedere gli argomenti seguenti.

-   [Come assegnare un gestore di dispositivi a un dispositivo](how-to-assign-a-device-handler-to-a-device.md)
-   [Come specificare un'icona, un'etichetta o un gestore di dispositivi per un dispositivo usando un gruppo di dispositivi](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Come specificare un'icona, un'etichetta o un gestore di dispositivi per un dispositivo usando una classe di dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Come impedire la riproduzione automatica per un componente](how-to-prevent-autoplay-for-a-component.md)
-   [Come registrare un gestore per un evento del dispositivo](how-to-register-a-handler-for-a-device-event.md)
-   [Come usare gli eventi AutoPlay nelle applicazioni in esecuzione](how-to-use-autoplay-events-in-running-applications.md)
-   [Come registrare un gestore eventi](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>Modalità di ricerca dei contenuti multimediali in AutoPlay

AutoPlay cerca i quattro livelli di directory multimediali sotto la directory radice per trovare i tipi di file noti. Usa il valore PerceivedType associato a un'estensione di file nel Registro di sistema per determinare la categoria di file, se si tratta di un'immagine, un file audio o un file video. Con queste informazioni, AutoPlay avvia il gestore appropriato per il dispositivo e il tipo di file. Per altre informazioni, vedere [Tipi percepiti e Registrazione dell'applicazione.](fa-perceivedtypes.md)

## <a name="defining-single-and-mixed-content-types"></a>Definizione di tipi di contenuto singolo e misto

AutoPlay definisce tre categorie di contenuto principali.

-   Immagini
-   Musica
-   Video

Un supporto è considerato contenente un singolo tipo di contenuto se tutti i file sul supporto rientrano in una sola di queste tre categorie. Si noti che ciò non significa che i file devono essere dello stesso tipo *di file.* .jpg, .gif e .bmp sono tipi di file diversi, ma un tipo di contenuto (immagini).

Se i tipi di contenuto supportati sono presenti sul supporto, ma nessun singolo tipo di contenuto può considerare il 100% del totale, il supporto viene considerato come un tipo di contenuto misto e viene gestito di conseguenza. Per altre informazioni, vedere [Gestione di supporti contenenti tipi di contenuto misto.](#handling-media-containing-mixed-content-types)

## <a name="sample-scenarios"></a>Scenari di esempio

Gli scenari seguenti forniscono una conoscenza di base di cosa aspettarsi da AutoPlay.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>Riproduzione automatica per Archiviazione dispositivi con picture media

1.  L'utente collega un dispositivo lettore USB SanDisk CompactFlash in cui sono già stati inseriti supporti contenenti il tipo di contenuto immagine al 100% sotto forma di .jpg file.
2.  Viene visualizzata la notifica Found New Hardware - SanDisk ImageMate ( Trovato nuovo **hardware - SanDisk ImageMate).**
3.  AutoPlay avvia l'applicazione immagine appropriata.

Analogamente, quando l'utente inserisce lo stesso supporto CompactFlash nel lettore quando il lettore è già collegato al sistema, l'evento di inserimento del contenuto multimediale determina anche l'avvio dell'applicazione per la presentazione di immagini da parte di AutoPlay. L'utente ha la possibilità di passare alla pagina Proprietà del dispositivo multimediale SanDisk per modificare l'impostazione predefinita in un'altra applicazione AutoPlay registrata, ad esempio la Creazione guidata scanner e fotocamera o Picture It!.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>Riproduzione automatica per Musica di riproduzione di file e Archiviazione dispositivi contenenti Musica multimediali

1.  L'utente collega un lettore MP3 Diamond Rio USB.
2.  La notifica visualizza **Found New Hardware - Diamond Rio MP3 Player**( Trovato nuovo hardware - Diamond Rio MP3 Player ).
3.  AutoPlay riproduce i file usando il gestore predefinito registrato, ad esempio Windows Media Player.

Analogamente, se l'utente inserisce supporti contenenti file .mp3 (ad esempio, CompactFlash, SmartMedia, Memory Stick o CD-ROM) che contengono il 100% del contenuto totale supportato in un dispositivo di archiviazione, l'evento di inserimento multimediale causerebbe anche la riproduzione dei file usando il Windows Media Player. L'utente può accedere alla finestra delle proprietà del dispositivo di archiviazione e modificare l'azione predefinita in un'altra applicazione AutoPlay registrata, ad esempio WinAmp o Real Player.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>Riproduzione automatica per la riproduzione di video alla prima presentazione

1.  L'utente collega per la prima volta una videocamera digitale 1394.
2.  All'utente viene visualizzata una semplice finestra di dialogo che chiede quale applicazione eseguire. È possibile eseguire una delle applicazioni AutoPlay registrate o aprire una cartella per visualizzare i file. L'utente può impostare il comportamento selezionato come azione predefinita per gli eventi hot-plug della videocamera digitale successivi.

## <a name="assigning-default-handler-applications"></a>Assegnazione di applicazioni del gestore predefinite

Una nuova installazione di Windows trova AutoPlay con un set di applicazioni del gestore registrate. Le applicazioni registrate per impostazione predefinita durante un Windows installazione sono le seguenti.




| Tipo supporto | Applicazioni | 
|------------|--------------|
| Immagini | <ul><li>Presentazione (impostazione predefinita)</li><li>Procedura guidata fotocamera e scanner</li><li>Stampa guidata</li><li>Aprire la cartella</li></ul> | 
| Musica | <ul><li>Windows Media Player (impostazione predefinita)</li><li>Aprire la cartella</li></ul> | 
| Video | <ul><li>Windows Media Player (impostazione predefinita)</li><li>Aprire la cartella</li></ul> | 




 

Nel caso di tipi non supportati, agli utenti viene chiesto di assegnare l'impostazione predefinita per l'azione AutoPlay associata a ogni dispositivo di archiviazione alla prima introduzione al sistema. A quel punto, all'utente viene richiesto di scegliere un'azione da un elenco fornito di applicazioni registrate o di visualizzare una visualizzazione cartella che elenca il contenuto multimediale. L'utente ha anche la possibilità di scegliere di essere richiesto ogni volta che viene rilevato il tipo di supporto anziché salvare qualsiasi applicazione specifica come predefinita.

> [!Note]  
> I produttori di dispositivi hanno la possibilità di registrare e assegnare applicazioni predefinite da usare con i propri prodotti specifici. In questi casi, la finestra di dialogo che offre una scelta all'utente non viene visualizzata.

 

Per essere offerte come opzione del gestore da AutoPlay, le applicazioni appena installate devono registrarsi nel Registro di sistema. Per informazioni dettagliate, vedere [Preparazione di hardware e software per l'uso con AutoPlay.](#preparing-hardware-and-software-for-use-with-autoplay)

Gli utenti possono sempre modificare il gestore AutoPlay predefinito per qualsiasi dispositivo di archiviazione o tipo di contenuto. La pagina delle proprietà AutoPlay è accessibile per la modifica nella finestra delle proprietà del dispositivo di archiviazione in **Computer locale**.

Per esempi di richieste utente e pagine delle proprietà, vedere [Interfacce utente di AutoPlay](#autoplay-user-interfaces).

## <a name="handling-media-containing-mixed-content-types"></a>Gestione di supporti contenenti tipi di contenuto misti

Quando AutoPlay viene presentato con un supporto di contenuto misto, richiede l'input dell'utente prima di poter intervenire. In questo caso, all'utente viene visualizzata una finestra di dialogo contenente un elenco filtrato di tutte le applicazioni registrate appropriate disponibili per i tipi di contenuto presenti nel supporto. L'utente può scegliere una di queste applicazioni per la riproduzione automatica di quel particolare tipo di contenuto, mentre le altre rimangono invariate. Poiché la composizione del contenuto multimediale misto varia in base a ogni singolo disco, non è possibile salvare questa scelta come predefinita.

Per esempi di richieste dell'utente, vedere [Interfacce utente di AutoPlay.](#autoplay-user-interfaces)

## <a name="autoplay-user-interfaces"></a>Interfacce utente di AutoPlay

Sono disponibili tre interfacce utente possibili.

-   Finestra di dialogo che richiede all'utente di immettere un'azione per un singolo tipo di contenuto
-   Finestra di dialogo che richiede all'utente di immettere un'azione per tipi di contenuto misti
-   Una pagina delle proprietà

### <a name="single-content-type-dialog-box"></a>Finestra di dialogo Tipo di contenuto singolo

Quando al sistema viene presentata un'azione AutoPlay predefinita, viene visualizzata una finestra di dialogo simile alla seguente.

![Screenshot della finestra di dialogo tipo di contenuto singolo](images/pix.png)

Gli utenti possono eseguire una delle operazioni seguenti.

-   Scegliere un'azione dall'elenco delle applicazioni registrate.
-   Elencare i file sul supporto in una visualizzazione cartella normale.
-   Non eseguire alcuna azione.

Un utente può anche salvare una scelta come azione predefinita per questo supporto facendo clic sulla **casella Eseguire sempre l'azione** selezionata. Dopo aver scelto questa opzione, la finestra di dialogo non viene più visualizzata. Tuttavia, in Windows XP Service Pack 1 (SP1), se una nuova applicazione in grado di gestire un particolare tipo di supporto viene aggiunta al computer, la finestra di dialogo viene nuovamente visualizzata all'utente, offrendo la possibilità di selezionare la nuova applicazione come azione AutoPlay predefinita. Le applicazioni possono anche impostare se stesse come selezione predefinita quando vengono installate.

Windows XP SP1 aggiunge anche una funzionalità che mantiene la scelta dell'utente per l'azione AutoPlay se non fa clic sulla casella Sempre **l'azione** selezionata. Se un utente sceglie un'azione AutoPlay per una singola istanza, la volta successiva che viene visualizzata la finestra di dialogo per quel tipo di file multimediale, la stessa azione è la selezione predefinita.

Perché un'applicazione sia inclusa nell'elenco delle azioni possibili, deve essere registrata con AutoPlay. Per altre informazioni, vedere [Preparazione di hardware e software per l'uso con AutoPlay.](#preparing-hardware-and-software-for-use-with-autoplay)

### <a name="mixed-media-dialog-box"></a>Finestra di dialogo Supporto misto

La finestra di dialogo seguente viene visualizzata quando qualsiasi supporto contenente una combinazione di tipi di file supportati viene presentato al sistema. Si tratta essenzialmente della stessa finestra di dialogo con un singolo supporto del contenuto, ma con due differenze significative. In primo luogo, le opzioni di azione disponibili sono costituite da un elenco filtrato di applicazioni rilevanti per tutti i tipi di contenuto presenti nel supporto. In secondo momento, non è possibile scegliere un'azione predefinita permanente perché i tipi di contenuto e le percentuali di contenuti multimediali misti sono troppo imprevedibili.

![Screenshot della finestra di dialogo supporto misto](images/mix.png)

Perché un'applicazione sia inclusa nell'elenco delle azioni possibili, deve essere registrata con AutoPlay. Per altre informazioni, vedere [Preparazione di hardware e software per l'uso con AutoPlay.](#preparing-hardware-and-software-for-use-with-autoplay)

### <a name="property-page"></a>Pagina Proprietà

Di seguito è riportata una pagina delle proprietà AutoPlay di esempio per un dispositivo DVD/CD-ROM.

![Screenshot della pagina delle proprietà](images/apdlg.png)

Ogni tipo di dispositivo offre un subset appropriato di tipi di contenuto per la configurazione di AutoPlay. A sua volta, ogni tipo di contenuto, se selezionato, offre un elenco appropriato di opzioni di azione nella casella di riepilogo. È possibile scegliere un'azione diversa per ogni tipo di contenuto.

 

 



