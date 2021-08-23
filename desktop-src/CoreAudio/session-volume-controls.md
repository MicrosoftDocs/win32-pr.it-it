---
description: Controlli del volume di sessione
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Controlli del volume di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe45dce825dedd116c8f9c65684ac665eb6483f95dec3d247071f66408e8ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758891"
---
# <a name="session-volume-controls"></a>Controlli del volume di sessione

Come spiegato in precedenza, i client WASAPI possono controllare singolarmente il livello del volume di ogni [sessione audio.](audio-sessions.md) WASAPI applica l'impostazione del volume per una sessione in modo uniforme a tutti i flussi nella sessione. Ogni livello di volume è un valore compreso nell'intervallo da 0,0 a 1,0, dove 0,0 indica il silenzio e 1,0 indica il volume completo (nessuna attenuazione).

Un client crea in modo implicito una sessione assegnando il primo flusso a tale sessione. Il livello di volume predefinito della nuova sessione è 1.0. Come illustrato in precedenza, l'utente può regolare il livello del volume della sessione tramite l'interfaccia utente di un programma di controllo (ad esempio, Sndvol) che è un client WASAPI. Le impostazioni del controllo sono persistenti.

Oltre alle impostazioni del volume controllato dal client, il sistema applica le proprie impostazioni del volume alle sessioni. Queste impostazioni sono basate sui criteri audio e cambiano in modo dinamico in risposta alle modifiche nei flussi che costituiscono la combinazione audio globale. Per altre informazioni sui criteri audio, vedere [Componenti audio in modalità utente.](user-mode-audio-components.md)

Il software di sistema che implementa il controllo del volume per ogni flusso moltiplica gli esempi PCM nel flusso per il livello di volume effettivo. Il livello di volume effettivo è il risultato della moltiplicazione delle impostazioni del volume del client e del volume di sistema. Di conseguenza, la modifica risultante nell'ampiezza del segnale è una combinazione lineare dei livelli di volume del client e del sistema. Ad esempio, se il livello del volume client è 0,8 e il livello del volume di sistema<sup></sup> è 0,5, il livello di volume effettivo è (0,8). (0,5) = 0,4.

Si noti che la sonorità percepita non è lineare rispetto all'ampiezza del segnale. Al contrario, la sonorità varia approssimativamente come logaritmo del livello di volume v:

sonorità in decibel = 20<sup>.</sup> log₁₀(v)

Pertanto, impostando v = 0,5 si attenua la sonorità del segnale originale (il segnale prima dell'applicazione del livello del volume) di 6 decibel, impostando v = 0,25 si attenua il segnale di 12 decibel e così via. Un livello di volume v = 1.0, corrispondente a 0 decibel, non modifica il livello di segnale originale.

Le applicazioni audio con interfacce utente per il controllo del livello del volume visualizzano in genere i dispositivi di scorrimento che generano variazioni della sonorità percepita che sono proporzionali in modo lineare alle variazioni della posizione del dispositivo di scorrimento. Per produrre una relazione lineare tra la voce percepita e la posizione del dispositivo di scorrimento, l'applicazione deve definire una relazione non lineare tra il livello di volume v e la posizione del dispositivo di scorrimento. Per altre informazioni, vedere [Audio-Tapered Volume Controls](audio-tapered-volume-controls.md).

Come spiegato in precedenza, il programma di controllo del volume di sistema, Sndvol, visualizza i dispositivi di scorrimento del volume per le sessioni audio in riproduzione in ogni dispositivo di rendering audio. Questi dispositivi di scorrimento vengono visualizzati nella casella di gruppo con etichetta **Applicazioni** nella finestra SndVol. In genere, ogni sessione contiene tutti i flussi di riproduzione da una determinata finestra dell'applicazione. Tramite i dispositivi di scorrimento nella finestra di Sndvol, gli utenti controllano i livelli di volume delle singole applicazioni audio.

Come regola generale, un'applicazione deve assegnare tutti i flussi di riproduzione alla stessa sessione audio. WASAPI non impedisce a un'applicazione di distribuire i flussi di riproduzione tra più sessioni. Tuttavia, la proliferazione risultante dei dispositivi di scorrimento del volume in Sndvol potrebbe confondere gli utenti.

Come opzione, una finestra dell'applicazione può visualizzare un dispositivo di scorrimento del volume. Il dispositivo di scorrimento dell'applicazione deve riflettere sempre lo stato del dispositivo di scorrimento Sndvol corrispondente. Pertanto, se l'utente modifica il livello del volume spostando il dispositivo di scorrimento nella finestra dell'applicazione, il dispositivo di scorrimento corrispondente nella finestra Sndvol si sposterà in unisono con il dispositivo di scorrimento dell'applicazione. Analogamente, se l'utente sposta il dispositivo di scorrimento Sndvol, il dispositivo di scorrimento dell'applicazione deve essere spostato all'unisono con il dispositivo di scorrimento Sndvol.

Per supportare questo comportamento, WASAPI implementa [**l'interfaccia ISimpleAudioVolume.**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) Quando l'utente sposta il dispositivo di scorrimento dell'applicazione, l'applicazione chiama il metodo [**ISimpleAudioVolume::SetMasterVolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) per regolare di conseguenza il livello del volume della sessione. Sndvol monitora le modifiche apportate al volume tramite questo metodo e riflette le modifiche nei dispositivi di scorrimento del volume visualizzati. Inoltre, un'applicazione può ricevere notifiche relative alle modifiche del volume della sessione apportate dall'utente tramite Sndvol. A questo scopo, l'applicazione implementa [**un'interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e registra l'interfaccia con WASAPI. Successivamente, ogni volta che l'utente modifica il livello del volume della sessione tramite Sndvol, l'applicazione riceve una chiamata di notifica tramite il metodo [**IAudioSessionEvents::OnSimpleVolumeChanged.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) Per un esempio di codice che implementa **un'interfaccia IAudioSessionEvents,** vedere [Eventi della sessione audio.](audio-session-events.md) Per un esempio di codice che registra **un'interfaccia IAudioSessionEvents,** vedere [Eventi audio per applicazioni audio legacy.](audio-events-for-legacy-audio-applications.md)

**L'interfaccia ISimpleAudioVolume** applica lo stesso livello di volume in modo uniforme a tutti i canali in una sessione audio. Sebbene questa interfaccia soddisfi i requisiti di controllo del volume della maggior parte delle applicazioni, alcune applicazioni potrebbero richiedere funzionalità di controllo del volume più specializzate. [**L'interfaccia IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) controlla il volume di un singolo flusso in una sessione rispetto agli altri flussi nella sessione. **IAudioStreamVolume** consente inoltre a un client di controllare singolarmente i livelli di volume di tutti i canali nel flusso. Ad esempio, un'applicazione potrebbe usare questa funzionalità per ottenere effetti audio, ad esempio la simulazione del movimento spaziale di un'origine audio tramite panoramica da sinistra a destra. Un'altra interfaccia specializzata, [**IChannelAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)controlla i livelli di volume dei singoli canali in una sessione. Ad esempio, un'applicazione potrebbe usare **IChannelAudioVolume** per implementare i controlli di bilanciamento per un sistema audio stereofonico.

I dispositivi di  scorrimento del volume nella casella Applicazioni in Sndvol riflettono solo le modifiche apportate al volume tramite **l'interfaccia ISimpleAudioVolume.** Non riflettono le modifiche al volume apportate tramite le interfacce **IAudioStreamVolume** e **IChannelAudioVolume.** Sebbene alcune applicazioni possano consentire agli utenti di controllare direttamente o indirettamente le impostazioni del volume tramite **IAudioStreamVolume** e **IChannelAudioVolume,** gli sviluppatori devono evitare di presentare dispositivi di scorrimento dell'applicazione per queste impostazioni del volume che gli utenti probabilmente confondono con i dispositivi di scorrimento del volume in Sndvol. In caso contrario, un utente potrebbe spostare un dispositivo di scorrimento dell'applicazione in attesa di vedere la modifica riflessa in un dispositivo di scorrimento Sndvol e confondersi quando non si verifica alcuna modifica di questo tipo. Gli sviluppatori possono evitare questo problema tramite un'attenta progettazione dell'interfaccia utente.

Il livello di volume effettivo di qualsiasi canale nel sottomix della sessione, come detto dagli altoparlanti, è il prodotto dei quattro fattori a livello di volume seguenti:

-   Livelli di volume per canale dei flussi nella sessione, che i client possono controllare tramite i metodi **nell'interfaccia IAudioStreamVolume.**
-   Livello di volume per canale della sessione, che i client possono controllare tramite i metodi **nell'interfaccia IChannelAudioVolume.**
-   Livello del volume master della sessione, che i client possono controllare tramite i metodi **nell'interfaccia ISimpleAudioVolume.**
-   Livello di volume basato su criteri della sessione, che il sistema modifica in modo dinamico quando cambia la combinazione globale.

Ognuno dei quattro fattori a livello di volume nell'elenco precedente è un valore compreso nell'intervallo da 0,0 a 1,0, dove 0,0 indica silenzio e 1,0 indica il volume completo (nessuna attenuazione). Il livello di volume effettivo è anche un valore compreso nell'intervallo da 0,0 a 1,0.

Il motore audio applica il livello di volume effettivo per ogni canale ai canali in un flusso prima di combinare il flusso con gli altri flussi nella sessione audio. Se i valori di esempio in un canale superano 0 decibel dopo che il motore audio li ha moltiplicati per il livello di volume effettivo, il motore ritaglia i campioni prima di aggiungerli al sottomix della sessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> </dl>

 

 



