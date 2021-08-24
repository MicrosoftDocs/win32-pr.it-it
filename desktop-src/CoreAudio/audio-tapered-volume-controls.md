---
description: Audio-Tapered di volume
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Audio-Tapered di volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb4856b4f25ad33ae61e9cb250a6b84f0e8799bb9d11d33c1770593bcf3714a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750792"
---
# <a name="audio-tapered-volume-controls"></a>Audio-Tapered di volume

[**L'interfaccia IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) gestisce i controlli del volume con tapering audio. Questi controlli sono particolarmente adatti per le applicazioni Windows che visualizzano i dispositivi di scorrimento del volume. Per un dispositivo di scorrimento del volume associato a un controllo del volume con tocco audio, ogni modifica nella posizione del dispositivo di scorrimento produce una modifica della sonorità percepita proporzionale alla distanza percorsa dal dispositivo di scorrimento. Per una distanza di viaggio specifica, la quantità di volume percepito aumenta o diminuisce è approssimativamente uguale indipendentemente dal fatto che il movimento del dispositivo di scorrimento si verifichi nella parte inferiore, superiore o centrale dell'intervallo di movimento del dispositivo di scorrimento. La sonorità percepita varia approssimativamente in modo lineare con il logaritmo della potenza del segnale audio.

Il termine *conica audio* in origine si riferisce alla forma conica dell'elemento riflessivo in un potentiometro usato come controllo del volume in un dispositivo audio-elettronico. Un elemento riflessivo con tapering audio è più largo in corrispondenza della posizione del volume zero e più ristretto in corrispondenza della posizione massima del volume. Il potentiometro controlla il livello di tensione del segnale audio che il dispositivo riproduce attraverso i suoi altoparlanti. Il nastro è progettato per produrre una relazione approssimativamente lineare tra la posizione del wiper del potentiometro e la sonorità percepita agli altoparlanti. La relazione tra la posizione del wiper e la tensione degli altoparlanti non è lineare.

Al contrario, un elemento regressione con un taper lineare ha una larghezza uniforme sull'intervallo di movimento del tegliatore del potentiometro. Di conseguenza, la tensione degli altoparlanti varia in modo lineare con la posizione del wiper. La relazione tra la posizione del wiper e la voce è non lineare.

Analogamente, un'Windows che visualizza un dispositivo di scorrimento del volume definisce una relazione tra la posizione del dispositivo di scorrimento e il livello del segnale di output agli altoparlanti. La relazione può, in effetti, essere lineare con taper o audio con taper.

Il diagramma seguente illustra il mapping della posizione del dispositivo di scorrimento alla tensione di output e alla sonorità percepita per un controllo del volume con tapering lineare.

![Diagramma di output per un controllo del volume con taper lineare](images/taper1.jpg)

Sul lato sinistro del diagramma precedente, il livello di tensione di output del convertitore audio da digitale ad analogico (DAC) aumenta in modo lineare man mano che il dispositivo di scorrimento del volume passa dalla posizione minima (con etichetta Min) alla posizione massima (con etichetta Max). L'etichetta V<sub>FS</sub> sull'asse verticale rappresenta la tensione di output dell'applicazione livello dati su larga scala.

Tuttavia, la sonorità percepita varia approssimativamente come logaritmo della potenza del segnale audio, come illustrato sul lato destro del diagramma precedente. Di conseguenza, il movimento del dispositivo di scorrimento su un intervallo vicino all'impostazione minima comporta una modifica relativamente grande della sonorità percepita, ma il movimento del dispositivo di scorrimento su un intervallo della stessa larghezza vicino all'impostazione massima causa una modifica relativamente piccola della sonorità percepita.

Sul lato destro del diagramma precedente, la sonorità sull'asse verticale viene misurata in decibel (dB) rispetto all'impostazione di risparmio energia su scala completa (a 0 decibel). La curva di sonorità interseca l'asse verticale in corrispondenza di meno infinito, ma nel diagramma viene visualizzata solo la parte della curva da 0 decibel a -96 decibel. La decisione di mostrare solo questa parte della curva è un po' arbitraria, ma -96 decibel rappresenta comodamente la potenza al livello di output successivo al più basso di un'applicazione livello dati a 16 bit rispetto alla potenza su larga scala. Questo valore viene calcolato come 20<sup>.</sup> log₁₀(1/65535).

Poiché piccole modifiche nella posizione del dispositivo di scorrimento in prossimità dell'impostazione minima nel diagramma precedente comportano modifiche di grande volume, l'utente potrebbe trovare difficile controllare il volume su quest'area. I movimenti del dispositivo di scorrimento relativamente piccoli possono spostare il volume ben al di sopra o al di sotto del livello desiderato. Un controllo del volume migliorato offre una relazione più lineare tra la posizione del dispositivo di scorrimento e la sonorità.

Il diagramma seguente illustra il mapping della posizione del dispositivo di scorrimento alla tensione di output e alla sonorità percepita per un controllo del volume con taper audio.

![Diagramma di output per il controllo del volume con con taper audio](images/taper2.jpg)

Come illustrato sul lato destro del diagramma precedente, la sonorità percepita varia approssimativamente in modo lineare con i cambiamenti nella posizione del dispositivo di scorrimento. A tale scopo, la tensione dell'applicazione livello dati deve variare in modo non lineare con la posizione, come illustrato sul lato sinistro del diagramma. La curva si avvicina asimmetria a 0 batterie quando il dispositivo di scorrimento si sposta verso sinistra rispetto all'impostazione massima. La tensione alla posizione minima del dispositivo di scorrimento è molto piccola, ma potrebbe non essere esattamente zero.

I metodi seguenti **nell'interfaccia IAudioEndpointVolume** usano impostazioni del volume misurate in decibel:

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Questi metodi producono una relazione approssimativamente lineare tra l'impostazione del volume e la sonorità percepita. L'intervallo di volume in decibel dei controlli del volume gestiti da questi metodi dipende dal dispositivo endpoint audio. Per determinare l'intervallo di volumi per un particolare dispositivo, chiamare il [**metodo IAudioEndpointVolume::GetVolumeRange.**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange)

Al contrario, le impostazioni del volume per i metodi seguenti **nell'interfaccia IAudioEndpointVolume** seguono una curva più concisa più concisa sull'intervallo di volumi:

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

In Windows Vista questi metodi usano una curva intermedia tra la curva con tapering audio illustrata nel diagramma precedente e una curva con tapering lineare. Si noti che la forma della curva potrebbe cambiare nelle versioni future Windows. I primi quattro metodi nell'elenco precedente esprimono i livelli di volume come valori normalizzati nell'intervallo compreso tra 0,0 (volume minimo) e 1,0 (volume massimo). Per gli ultimi due metodi nell'elenco, chiamare il metodo [**IAudioEndpointVolume::GetVolumeStepInfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) per ottenere il numero di passaggi nell'intervallo di volumi.

Le interfacce seguenti usano curve lineari con tapering per le impostazioni del volume:

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Per altre informazioni su queste interfacce, vedere Session [Volume Controls](session-volume-controls.md). Per informazioni sugli intervalli di volumi e sui livelli di volume predefiniti nelle varie versioni di Windows, vedere [Default Audio Volume Impostazioni](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> </dl>

 

 
