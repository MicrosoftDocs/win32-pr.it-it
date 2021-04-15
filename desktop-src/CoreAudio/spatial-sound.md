---
description: Microsoft Spatial Sound è la soluzione a livello di piattaforma Microsoft per il supporto di suoni spaziali in Xbox, Windows e HoloLens 2, che consente di racchiudere i segnali audio sia per l'elevazione (sopra o sotto il listener).
ms.assetid: 4F962F1A-CA4A-4018-BA97-516EA3519650
title: 'Audio spaziale per sviluppatori '
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/18/2020
ms.openlocfilehash: 9db3614ea7932af874da351e7a92980d51b90011
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/04/2021
ms.locfileid: "104555533"
---
# <a name="spatial-sound-for-developers"></a>Audio spaziale per sviluppatori 
> [!Note] 
> Questa documentazione è destinata a un pubblico di sviluppatori. Per il supporto degli utenti finali per l'abilitazione di un suono spaziale nel dispositivo, vedere [come attivare il suono spaziale in Windows 10](https://support.microsoft.com/help/4563140/how-to-turn-on-spatial-sound-in-windows-10).

Microsoft Spatial Sound è la soluzione a livello di piattaforma Microsoft per il supporto di suoni spaziali in Xbox, Windows e HoloLens 2, che consente di racchiudere i segnali audio sia per l'elevazione (sopra o sotto il listener). Il suono spaziale può essere sfruttato dalle app desktop di Windows (Win32) e dalle app piattaforma UWP (Universal Windows Platform) (UWP) sulle piattaforme supportate. Le API audio spaziali consentono agli sviluppatori di creare oggetti audio che emettono audio dalle posizioni nello spazio 3D. Gli oggetti audio dinamici consentono di emettere audio da una posizione arbitraria nello spazio, che può cambiare nel tempo. È anche possibile specificare che gli oggetti audio emettono un suono da uno dei 17 canali statici predefiniti (8.1.4.4) che possono rappresentare altoparlanti reali o virtualizzati. Il formato di output effettivo viene selezionato dall'utente e può essere sottratto dalle implementazioni di suoni spaziali Microsoft; l'audio verrà presentato a altoparlanti, cuffie e ricevitori Home Theater esistenti senza che sia necessario apportare modifiche al codice o al contenuto. La piattaforma supporta completamente la codifica Dolby Atmos in tempo reale per l'output di cuffie HDMI e stereo, DTS: X per le cuffie e Windows Sonic per la codifica delle cuffie stereo. Infine, le app audio spaziali Microsoft rispettano i criteri di combinazione del sistema e il loro audio verrà combinato anche con app non compatibili con lo spazio. Il supporto tecnico Microsoft Spatial è inoltre integrato in Media Foundation; le app che usano Media Foundation possono riprodurre il contenuto Dolby Atmos senza alcuna implementazione aggiuntiva.

Il suono spaziale con audio spaziale Microsoft supporta TV, teatri domestici e barre audio che supportano Dolby Atmos. Il suono spaziale può essere usato anche con qualsiasi coppia di cuffie che il consumer può possedere, con il rendering audio della piattaforma usando Windows Sonic per le cuffie, Dolby Atmos per le cuffie o DTS Headphone: X.


## <a name="enabling-microsoft-spatial-sound"></a>Abilitazione del suono spaziale Microsoft

Sia che si tratti di uno sviluppatore o di un consumer, un utente deve abilitare il suono spaziale Microsoft sul dispositivo per ascoltare il suono spaziale.

### <a name="windows"></a>Windows
Nei PC Windows, questa operazione viene eseguita tramite la pagina delle proprietà per un determinato dispositivo di output audio. Dal pannello di controllo **audio** selezionare un dispositivo di output e fare clic su **proprietà del dispositivo**. Nella sezione relativa al **suono spaziale** della pagina, se il dispositivo supporta il suono spaziale, è possibile selezionare uno dei formati disponibili nell'elenco a discesa **formato audio spaziale** .

![abilitare l'audio spaziale nel pannello di controllo audio](images/spatialsoundsettingswindows1.png)

È anche possibile abilitare il suono spaziale Microsoft facendo clic con il pulsante destro del mouse sull'icona del **volume** nella barra delle applicazioni.

![abilitare l'audio spaziale dalla barra delle applicazioni](images/spatialsoundsettingswindows2.png)

### <a name="xbox-one"></a>Xbox One
Su Xbox One, le funzionalità audio spaziali Microsoft sono sempre disponibili per il consumer e vengono abilitate tramite l'app impostazioni in **Volume > generale & output audio**.


![abilitare l'audio spaziale su Xbox One nell'app impostazioni ](images/audiosettingsbitstream.png)

Dopo aver selezionato Dolby Atmos per Home Theater come "formato bitstream", il supporto per questo formato viene controllato tramite i dati di identificazione di visualizzazione estesa HDMI (EDID). Se il dispositivo HDMI non supporta il formato, viene visualizzato un messaggio di errore all'utente. Si noti che la prima volta che si seleziona questa opzione, l'utente deve scaricare l'app Dolby Access.

Se per l' **audio HDMI** è selezionato un formato diverso da "bitstream out", l'elenco a discesa **formato bitstream** è disabilitato.

![Audio spaziale disabilitato in Xbox One nell'app impostazioni ](images/audiosettingsplain.png)

Selezionare Dolby Atmos per le cuffie, DTS Headphone: X o Windows Sonic per le cuffie dall'elenco a discesa **formato auricolare** in **audio cuffia**

![abilitare l'audio spaziale per le cuffie su Xbox One nell'app impostazioni ](images/audiosettingsheadphone.png)

Quando il suono spaziale Microsoft non è disponibile (ad esempio, quando si esegue la riproduzione in altoparlanti stereo del portatile incorporato o se l'utente non ha abilitato in modo esplicito il suono spaziale Microsoft per la prima volta), il numero di oggetti dinamici disponibili restituiti da [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) a un'applicazione sarà 0.

### <a name="hololens-2"></a>HoloLens 2

In HoloLens 2, Microsoft spatial audio è abilitato per impostazione predefinita e usa l'offload DSP hardware progettato specificamente per Windows Sonic per le cuffie.

## <a name="microsoft-spatial-sound-and-audio-middleware"></a>Middleware audio e audio Microsoft spaziali

Molti sviluppatori di app e giochi usano soluzioni di motore per il rendering audio di terze parti, che spesso includono strumenti sofisticati per la creazione e l'ascolto. Microsoft ha collaborato con diversi provider di soluzioni per implementare il suono spaziale Microsoft negli ambienti di creazione esistenti. Questo significa spesso che le API illustrate in questa sezione sono astratte dalla visualizzazione dell'app; vengono sottoposti a incapsulamento come plug-in di elaborazione dei segnali digitali (DSP) che l'app può creare un'istanza e che l'implementatore audio dell'app può usare per combinare un canale audio Microsoft spaziale, submix o inviare singole voci ai plug-in dell'istanza dinamica dell'oggetto in base alle esigenze. Consultare il provider di soluzioni middleware audio per il proprio livello di supporto per il suono spaziale Microsoft.

## <a name="microsoft-spatial-sound-for-audio-renderers"></a>Audio spaziale Microsoft per renderer audio

Molti renderer audio sono destinati a un endpoint [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) dell'API di sessione audio (WASAPI) di Windows, in cui l'applicazione inserisce i buffer di dati audio misti e con formato conforme a un sink audio WASAPI; i buffer recapitati vengono quindi utilizzati per la combinazione con altri client, l'elaborazione finale a livello di sistema e il rendering.

Gli endpoint spaziali Microsoft spaziali sono implementati come [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), che presenta molte analogie con **IAudioClient**. Supporta oggetti acustici *statici* che formano un canale letto, con supporto per un massimo di 8.1.4.4 canali (8 canali intorno al listener, a sinistra, a destra, al centro, a sinistra, a destra, a destra, a sinistra, a destra e indietro al centro; 1 canale degli effetti a frequenza ridotta; 4 canali al di sopra del listener; 4 canali sotto il listener). E supporta oggetti *dinamici dinamici* , che possono essere posizionati in modo arbitrario nello spazio 3D.

Il modello di codifica di implementazione generale per **ISpatialAudioClient** è:

-   Creare oggetti audio statici e/o dinamici.
-   Inserire il buffer audio di ogni oggetto per ogni fotogramma, in modo che il sistema possa eseguirne il rendering.
-   Aggiornare le posizioni 3D degli oggetti dinamici su richiesta: con la frequenza, o raramente, in cui si desidera l'app.

Si noti che il formato di output corrente (altoparlanti o cuffie; Windows Sonic per le cuffie, Dolby Atmos o DTS Headphone: X) viene sottratto dall'implementazione precedente, lo sviluppatore dell'app può concentrarsi sul suono spaziale senza dover eseguire il pivot in base al formato. Le app che preferiscono il comportamento per la divergenza in base al formato di output possono eseguire query sul formato in uso, ma l'astrazione significa che un'app non è necessaria per gestire questi formati.

## <a name="microsoft-spatial-sound-integration-with-audio-renderers"></a>Integrazione di Microsoft Spatial Sound con renderer audio

Poiché [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) è un sink audio che usa i dati, un renderer audio offre diverse opzioni per interagire con i dati audio e distribuirli. Sono disponibili tre tecniche di integrazione di uso comune e per i titoli che usano il middleware audio, è possibile che siano disponibili plug-in equivalenti basati su queste opzioni:

-   **7.1.4 Panner e mastering Voice**: i renderer che già supportano gli endpoint 7,1 possono scegliere di aggiungere semplicemente il supporto per i quattro canali di altezza aggiuntivi supportati dal canale statico di **ISpatialAudioClient** . Qualsiasi Panoramica del canale eseguita in precedenza (probabilmente già sfruttando le coordinate x, y, z) può essere aggiornata per includere questi canali di altezza. Questa operazione spesso offre una minor interferenza per il renderer e i flussi di lavoro audio delle app, Signal, Flow e mix. Tramite le cuffie, si noti che la combinazione di app completa verrà spazializzazione, quindi anche la musica stereo può essere percepita come "esternalizzata" dal listener.
-   **Gestire un endpoint esistente, oltre ad aggiungere un bus 7.1.4 (e Panner)**: alcuni titoli possono scegliere di mantenere due endpoint: il relativo endpoint WASAPI stereo esistente (per il contenuto "diretto alle orecchie" non destinato alla spazializzazione) insieme a un canale **ISpatialAudioClient** statico che supporta 7.1.4 (o anche fino a 8.1.4.4). Naturalmente, la gestione delle interazioni tra due miscele presenta ulteriori problemi ai creatori di contenuto, sebbene la sincronizzazione venga mantenuta, perché le istanze WASAPI e ISAC attive in un determinato momento utilizzano le stesse dimensioni del buffer e Clock per l'elaborazione.
-   **Usare oggetti dinamici dinamici per determinate voci o sottocombinazioni**: offrendo forse il posizionamento più dettagliato o accurato, ma potenzialmente creando un'opacità di combinazione, questa tecnica comporta l'uso di oggetti audio dinamici **ISpatialAudioClient** . Si noti che i metadati e il buffer audio vengono recapitati al renderer, quindi questi suoni saranno opachi per il resto della combinazione di app. Inoltre, dal momento che è presente un numero limitato di oggetti dinamici dinamici disponibili, il renderer dovrà prendere in considerazione l'implementazione di tecniche di assegnazione delle priorità, ovvero l'eliminazione, la condivisione di risorse audio, la fusione con il canale statico e così via. I giochi hanno usato spesso questa tecnica per i singoli suoni "Hero", ad esempio un elicottero che si sposta sopra il listener.

I renderer possono anche combinare e trovare la corrispondenza tra questi approcci.

## <a name="microsoft-spatial-sound-runtime-resource-implications"></a>Implicazioni delle risorse di runtime di Microsoft Spatial Sound

In Windows e Xbox il numero di voci disponibili varia in base al formato in uso. I formati Dolby Atmos supportano 32 oggetti attivi totali (pertanto, se è in uso un letto canale 7.1.4, possono essere attivi 20 oggetti audio dinamici aggiuntivi). Windows Sonic per le cuffie supporta 128 oggetti attivi totali, con il canale LFE (Low Frequency Effects) che non viene effettivamente conteggiato come oggetto. Pertanto, quando un canale 8.1.4.4 è in uso, gli oggetti dinamici di 112 possono essere attivi.

Per piattaforma UWP (Universal Windows Platform) app eseguite su console di gioco Xbox One, la codifica in tempo reale (per Dolby Atmos per Home Theater, Dolby Atmos per cuffie, DTS Headphone: X e Windows Sonic per le cuffie) viene eseguita in hardware senza costi della CPU.

| Formato                       | Numero massimo oggetti statici (canale letto) | Numero massimo oggetti dinamici <br> Xbox One | Numero massimo oggetti dinamici <br> Windows | Numero massimo oggetti dinamici <br> HoloLens 2
|------------------------------|----------------------------------|-------------------------------------------|------------------------------------------|------------------------------------------|
| Dolby Atmos (HDMI)           | 12 (7.1.4)                       | 20                                        | 20                                       | N/D |
| Dolby Atmos (cuffie & altoparlanti predefiniti)     | 17 (8.1.4.4)                     | 16                                        | 16                                       | N/D |
| Cuffia DTS: X (cuffie) | 17 (8.1.4.4)        | 16                                        | 32                                      | N/D |
| Windows Sonic per le cuffie | 17 (8.1.4.4)        | 15                                        | 112                                      | 31 |


Le app devono considerare anche le implicazioni delle risorse seguenti:

-   **Larghezza di banda di archiviazione/disco**: il contenuto lineare pre-creato in 7.1.4 sarà in genere superiore a 7,1 di contenuto lineare (anche se i codec percettivi già sfruttano spesso i vantaggi della correlazione dei canali per rendere questo molto meno del 50% dei canali effettivi dei dati audio)
-   **Altri costi di elaborazione dei segnali digitali**: alcuni effetti globali precedenti potrebbero ora diventare istanze per ogni oggetto audio dinamico. Inoltre, alcuni autori di contenuti potrebbero voler aggiornare alcuni effetti DSP per supportare canali aggiuntivi o usarli in modo univoco.

## <a name="microsoft-spatial-sound-and-sound-spatialization-cues"></a>Suggerimenti per la spazializzazione di audio e suoni spaziali Microsoft

Il suono spaziale Microsoft si concentra sulla simulazione del posizionamento del suono su una sfera idealizzata intorno al listener. Windows Sonic per le cuffie, DTS Headphone: X e Dolby Atmos implementano il mapping degli speaker e la virtualizzazione per le cuffie, ma si noti che molti altri aspetti della simulazione spaziale sonora, già implementata in modalità abilitata per l'autore del contenuto, vengono lasciati ai motori esistenti. I creatori di contenuti continuano a usare gli strumenti e i processi di gioco esistenti che in precedenza avevano per tali indicazioni spaziali come Doppler, attenuazione basata sulla distanza e filtro, occlusione e ostruzione e riverberazione ambientale.

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Repository GitHub degli esempi di suoni spaziali Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)
-   Dolby offre una serie di risorse di supporto correlate a Dolby Atmos e all'app Dolby Access all'indirizzo <https://developer.dolby.com> .

## <a name="spatial-sound-interfaces"></a>Interfacce audio spaziali



| Interfaccia                                                                              | Descrizione                                                                                                                    |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)                                     | Consente a un client di creare flussi audio che emettono audio da una posizione nello spazio 3D.                                          |
| [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)                                     | Rappresenta un oggetto che fornisce dati audio di cui eseguire il rendering da una posizione nello spazio 3D rispetto all'utente.                |
| [**ISpatialAudioObjectRenderStream**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)             | Fornisce metodi per il controllo di un flusso di rendering dell'oggetto audio spaziale, incluso l'avvio, l'arresto e la reimpostazione del flusso. |
| [**ISpatialAudioObjectRenderStreamNotify**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify) | Fornisce notifiche per i client audio spaziali per rispondere alle modifiche nello stato di un ISpatialAudioObjectRenderStream.     |



 

> [!Note]  
> Quando si usano le interfacce [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) in un titolo XDK (Xbox One Development Kit), è necessario chiamare prima **EnableSpatialAudio** prima di chiamare [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) o [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). In caso contrario, verrà restituito un errore E \_ nointerface dalla chiamata a Activate. **EnableSpatialAudio** è disponibile solo per i titoli XDK e non deve essere chiamato per piattaforma UWP (Universal Windows Platform) app eseguite su Xbox One, né per i dispositivi non Xbox One.

 

## <a name="spatial-sound-structures"></a>Strutture audio spaziali



| Struttura                                                                                                 | Descrizione                                                                  |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) | Rappresenta i parametri di attivazione per un flusso di rendering audio spaziale.          |
| [**SpatialAudioClientActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams)                          | Rappresenta i parametri di attivazione facoltativi per un flusso di rendering audio spaziale. |



 

## <a name="spatial-sound-enumerations"></a>Enumerazioni di suoni spaziali



| Enumerazione                                | Descrizione                                   |
|--------------------------------------------|-----------------------------------------------|
| [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) | Specifica il tipo di un ISpatialAudioObject. |



 

 

 



