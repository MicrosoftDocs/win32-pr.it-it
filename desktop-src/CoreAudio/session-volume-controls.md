---
description: Controlli volume sessione
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Controlli volume sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add29b18b39c942c54926190ef9c0f85e447bb88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877945"
---
# <a name="session-volume-controls"></a>Controlli volume sessione

Come spiegato in precedenza, i client WASAPI possono controllare individualmente il livello del volume di ogni [sessione audio](audio-sessions.md). WASAPI applica l'impostazione del volume per una sessione in modo uniforme a tutti i flussi della sessione. Ogni livello di volume è un valore compreso tra 0,0 e 1,0, dove 0,0 indica il silenzio e 1,0 indica il volume completo (nessuna attenuazione).

Un client crea in modo implicito una sessione assegnando il primo flusso alla sessione. Il livello di volume predefinito della nuova sessione è 1,0. Come illustrato in precedenza, l'utente può regolare il livello del volume della sessione tramite l'interfaccia utente di un programma di controllo (ad esempio, sndvol) che è un client WASAPI. Le impostazioni di controllo sono permanenti.

Oltre alle impostazioni del volume controllate dal client, il sistema applica le proprie impostazioni del volume alle sessioni. Queste impostazioni sono basate sui criteri audio e cambiano in modo dinamico in risposta alle modifiche apportate ai flussi che compongono la combinazione audio globale. Per ulteriori informazioni sui criteri audio, vedere [componenti audio in modalità utente](user-mode-audio-components.md).

Il software di sistema che implementa il controllo del volume per ogni flusso moltiplica gli esempi PCM nel flusso in base al livello di volume effettivo. Il livello di volume effettivo è il risultato della moltiplicazione delle impostazioni del volume del client e del sistema. Quindi, la variazione risultante nell'ampiezza del segnale è una combinazione lineare dei livelli di volume del client e di sistema. Se ad esempio il livello del volume del client è 0,8 e il livello del volume di sistema è 0,5, il livello di volume effettivo è (0,8)<sup>.</sup> (0,5) = 0,4.

Si noti che la sonorità percepita non è lineare rispetto all'ampiezza del segnale. Al contrario, la sonorità varia approssimativamente come il logaritmo del livello di volume v:

sonorità in decibel = 20<sup>.</sup> log ₁ ₀ (v)

Pertanto, l'impostazione v = 0,5 attenua la sonorità del segnale originale (il segnale prima che venga applicato il livello del volume) di 6 decibel, impostando v = 0,25, il segnale viene attenuato di 12 decibel e così via. Un livello di volume v = 1,0, corrispondente a 0 decibel, non modifica il livello del segnale originale.

Le applicazioni audio con interfacce utente per il controllo del livello del volume visualizzano in genere i dispositivi di scorrimento che generano modifiche in sonorità percepite, che sono linearmente proporzionali alle modifiche nella posizione del dispositivo di scorrimento. Per produrre una relazione lineare tra la sonorità percepita e la posizione del dispositivo di scorrimento, l'applicazione deve definire una relazione non lineare tra il livello di volume v e la posizione del dispositivo di scorrimento. Per altre informazioni, vedere [controlli del volume con rastremazione audio](audio-tapered-volume-controls.md).

Come spiegato in precedenza, il programma di controllo del volume di sistema, sndvol, Visualizza i dispositivi di scorrimento del volume per le sessioni audio che giocano in ogni dispositivo di rendering audio. Questi dispositivi di scorrimento vengono visualizzati nella casella di gruppo **applicazioni** con etichetta nella finestra SndVol. In genere, ogni sessione contiene tutti i flussi di riproduzione da una particolare finestra dell'applicazione. Attraverso i dispositivi di scorrimento nella finestra sndvol, gli utenti controllano i livelli di volume delle singole applicazioni audio.

Come regola generale, un'applicazione deve assegnare tutti i relativi flussi di riproduzione alla stessa sessione audio. WASAPI non impedisce a un'applicazione di distribuire i flussi di riproduzione tra più sessioni. Tuttavia, la proliferazione risultante di dispositivi di scorrimento del volume in sndvol potrebbe confondere gli utenti.

In alternativa, una finestra dell'applicazione può visualizzare un dispositivo di scorrimento del volume. Il dispositivo di scorrimento dell'applicazione deve rispecchiare sempre lo stato del dispositivo di scorrimento sndvol corrispondente. Pertanto, se l'utente modifica il livello del volume spostando il dispositivo di scorrimento nella finestra dell'applicazione, il dispositivo di scorrimento corrispondente nella finestra sndvol dovrebbe essere spostato all'uniformità con il dispositivo di scorrimento dell'applicazione. Analogamente, se l'utente sposta il dispositivo di scorrimento sndvol, il dispositivo di scorrimento dell'applicazione verrà spostato all'unisono con il dispositivo di scorrimento sndvol.

Per supportare questo comportamento, WASAPI implementa l'interfaccia [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . Quando l'utente sposta il dispositivo di scorrimento dell'applicazione, l'applicazione chiama il metodo [**ISimpleAudioVolume:: SetMasterVolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) per regolare di conseguenza il livello del volume di sessione. Sndvol monitora le modifiche del volume apportate tramite questo metodo e riflette le modifiche nei dispositivi di scorrimento del volume visualizzati. Inoltre, un'applicazione può ricevere notifiche delle modifiche del volume di sessione effettuate dall'utente tramite sndvol. A questo scopo, l'applicazione implementa un'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e registra l'interfaccia con WASAPI. Successivamente, ogni volta che l'utente modifica il livello di volume della sessione tramite sndvol, l'applicazione riceve una chiamata di notifica tramite il metodo [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) . Per un esempio di codice che implementa un'interfaccia **IAudioSessionEvents** , vedere [eventi di sessione audio](audio-session-events.md). Per un esempio di codice che registra un'interfaccia **IAudioSessionEvents** , vedere [eventi audio per le applicazioni audio legacy](audio-events-for-legacy-audio-applications.md).

L'interfaccia **ISimpleAudioVolume** applica lo stesso livello di volume in modo uniforme a tutti i canali in una sessione audio. Sebbene questa interfaccia soddisfi i requisiti di controllo del volume della maggior parte delle applicazioni, è possibile che alcune applicazioni richiedano funzionalità di controllo del volume più specializzate. L'interfaccia [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) controlla il volume di un singolo flusso in una sessione relativa agli altri flussi nella sessione. **IAudioStreamVolume** consente inoltre a un client di controllare individualmente i livelli del volume di tutti i canali nel flusso. Ad esempio, un'applicazione può usare questa funzionalità per ottenere effetti audio come la simulazione del movimento spaziale di un'origine audio mediante la panoramica da sinistra a destra. Un'altra interfaccia specializzata, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), controlla i livelli di volume dei singoli canali in una sessione. Ad esempio, un'applicazione può usare **IChannelAudioVolume** per implementare i controlli di bilanciamento per un sistema audio stereofonico.

I dispositivi di scorrimento del volume nella casella **applicazioni** in sndvol riflettono solo le modifiche del volume effettuate tramite l'interfaccia **ISimpleAudioVolume** . Non riflettono le modifiche del volume effettuate tramite le interfacce **IAudioStreamVolume** e **IChannelAudioVolume** . Sebbene alcune applicazioni possano consentire agli utenti di controllare direttamente o indirettamente le impostazioni del volume tramite **IAudioStreamVolume** e **IChannelAudioVolume**, gli sviluppatori devono evitare di presentare i dispositivi di scorrimento dell'applicazione per queste impostazioni del volume che gli utenti possono confondere con i dispositivi di scorrimento del volume in sndvol. In caso contrario, è possibile che un utente sposti il dispositivo di scorrimento di un'applicazione per verificare che la modifica venga riflessa in un dispositivo di scorrimento sndvol e venga confusa in caso di modifica Gli sviluppatori possono evitare questo problema mediante un'attenta progettazione dell'interfaccia utente.

Il livello di volume effettivo di qualsiasi canale della sessione submix, come sentito dagli oratori, è il prodotto dei quattro fattori a livello di volume seguenti:

-   I livelli di volume per canale dei flussi nella sessione, che i client possono controllare attraverso i metodi nell'interfaccia **IAudioStreamVolume** .
-   Livello del volume per canale della sessione, che i client possono controllare attraverso i metodi dell'interfaccia **IChannelAudioVolume** .
-   Livello del volume master della sessione, che i client possono controllare attraverso i metodi dell'interfaccia **ISimpleAudioVolume** .
-   Livello del volume basato su criteri della sessione, che viene modificato in modo dinamico dal sistema come cambia la combinazione globale.

Ognuno dei quattro fattori a livello di volume nell'elenco precedente è un valore compreso tra 0,0 e 1,0, dove 0,0 indica il silenzio e 1,0 indica il volume completo (nessuna attenuazione). Il livello di volume effettivo è anche un valore compreso tra 0,0 e 1,0.

Il motore audio applica il livello di volume effettivo per ogni canale ai canali in un flusso prima di combinare il flusso con gli altri flussi nella sessione audio. Se qualsiasi valore di esempio in un canale supera 0 decibel dopo che il motore audio li ha moltiplicato per il livello di volume effettivo, il motore Ritaglia gli esempi prima di aggiungerli alla sessione submix.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> </dl>

 

 



