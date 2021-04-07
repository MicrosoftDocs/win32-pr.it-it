---
description: Controlli del volume Audio-Tapered
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Controlli del volume Audio-Tapered
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cca0879d27d0eba3d49ca22b019442f882bf917
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748439"
---
# <a name="audio-tapered-volume-controls"></a>Controlli del volume Audio-Tapered

L'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) gestisce i controlli del volume che sono conici audio. Questi controlli sono particolarmente adatti per le applicazioni Windows che visualizzano i dispositivi di scorrimento del volume. Per un dispositivo di scorrimento del volume associato a un controllo volume con rastremazione audio, ogni modifica nella posizione del dispositivo di scorrimento produce una modifica in sonorità percepita che è proporzionale alla distanza percorsa dal dispositivo di scorrimento. Per una particolare distanza di corsa, la quantità in base alla quale l'intensità percepita aumenta o diminuisce è approssimativamente la stessa, indipendentemente dal fatto che il dispositivo di scorrimento si trovi nella parte inferiore, superiore o intermedia dell'intervallo di spostamento del dispositivo di scorrimento. La sonorità percepita varia approssimativamente in modo lineare con il logaritmo della potenza del segnale audio.

Il termine *audio conico* originariamente indicato alla forma conica dell'elemento resistivo in un potenziometro usato come controllo del volume in un dispositivo di elettronica audio. Un elemento resistivo con rastremazione audio è più ampio in corrispondenza della posizione del volume zero e più piccolo in corrispondenza della posizione del volume massimo. Il potenziometro controlla il livello di tensione del segnale audio che il dispositivo riproduce attraverso le relative relatori. La rastrematura è progettata per produrre una relazione approssimativamente lineare tra la posizione del raschiatore del potenziometro e la sonorità percepita nei relatori. La relazione tra la posizione del tergicristallo e la tensione negli altoparlanti è non lineare.

Al contrario, un elemento resistivo con un cono lineare ha una larghezza uniforme sull'intervallo di spostamento del tergicristallo del potenziometro. Di conseguenza, la tensione negli altoparlanti varia in modo lineare con la posizione del tergicristallo. La relazione tra la posizione del tergicristallo e la sonorità è non lineare.

Analogamente, un'applicazione Windows che visualizza un dispositivo di scorrimento del volume definisce una relazione tra la posizione del dispositivo di scorrimento e il livello del segnale di output nei relatori. La relazione può in effetti essere conica lineare o audio conica.

Il diagramma seguente illustra il mapping tra la posizione del dispositivo di scorrimento e la tensione di output e la sonorità per un controllo del volume con rastremazione lineare.

![diagramma di output per un controllo volume con rastremazione lineare](images/taper1.jpg)

Sul lato sinistro del diagramma precedente, il livello di tensione di output del convertitore da Digital a analogico (DAC) audio aumenta in modo lineare quando il dispositivo di scorrimento del volume si sposta dalla posizione minima (con etichetta min) alla posizione massima (con etichetta max). L'etichetta V<sub>FS</sub> sull'asse verticale rappresenta la tensione di output dell'applicazione livello dati a scalabilità totale.

Tuttavia, la sonorità percepita varia approssimativamente come il logaritmo della potenza del segnale audio, come illustrato sul lato destro del diagramma precedente. Di conseguenza, lo spostamento del dispositivo di scorrimento su un intervallo vicino all'impostazione minima comporta una modifica relativamente grande nel volume percepito, ma lo spostamento del dispositivo di scorrimento su un intervallo con la stessa larghezza accanto all'impostazione massima causa una modifica relativamente ridotta in sonorità percepita.

Sul lato destro del diagramma precedente, la sonorità sull'asse verticale viene misurata in decibel (dB) rispetto all'impostazione di risparmio energia a scalabilità totale (a 0 decibel). La curva di sonorità interseca l'asse verticale a meno infinito, ma nel diagramma viene visualizzata solo la parte della curva da 0 decibel a – 96 decibel. La decisione di mostrare solo questa parte della curva è piuttosto arbitraria, ma – 96 decibel rappresenta facilmente la potenza al livello di output successivo a quello più basso di un'applicazione livello dati a 16 bit rispetto alla potenza a scalabilità totale. Questo valore viene calcolato come 20<sup>.</sup> log ₁ ₀ (1/65535).

Poiché le modifiche minime apportate alla posizione del dispositivo di scorrimento vicino all'impostazione minima nel diagramma precedente comportano modifiche di grande intensità, l'utente potrebbe trovare il volume difficile da controllare in quest'area. Movimenti di dispositivo di scorrimento relativamente piccoli possono eseguire il push del volume al di sopra o al di sotto del livello desiderato. Un controllo del volume migliorato fornirebbe una relazione più lineare tra la posizione del dispositivo di scorrimento e la sonorità.

Il diagramma seguente illustra il mapping tra la posizione del dispositivo di scorrimento e la tensione di output e la sonorità per un controllo del volume conico audio.

![diagramma di output per il controllo del volume con rastremazione audio](images/taper2.jpg)

Come illustrato sul lato destro del diagramma precedente, la sonorità percepita varia approssimativamente in modo lineare con le modifiche apportate alla posizione del dispositivo di scorrimento. Per eseguire questa operazione, la tensione dell'applicazione livello dati deve variare in modo non lineare con la posizione, come mostrato sul lato sinistro del diagramma. La curva asintoticamente si avvicina a 0 volt quando il dispositivo di scorrimento si sposta verso sinistra rispetto all'impostazione massima. La tensione nella posizione minima del dispositivo di scorrimento è molto piccola, ma potrebbe non essere esattamente zero.

I metodi seguenti nell'interfaccia **IAudioEndpointVolume** usano le impostazioni del volume misurate in decibel:

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Questi metodi producono una relazione approssimativamente lineare tra l'impostazione del volume e la sonorità percepita. L'intervallo di volumi in decibel dei controlli volume gestiti da questi metodi dipende dal dispositivo dell'endpoint audio. Per determinare l'intervallo di volumi per un particolare dispositivo, chiamare il metodo [**IAudioEndpointVolume:: GetVolumeRange**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange) .

Al contrario, le impostazioni del volume per i metodi seguenti nell'interfaccia **IAudioEndpointVolume** seguono una curva rastremata più delicatamente sull'intervallo di volumi:

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

In Windows Vista questi metodi usano una curva intermedia tra la curva audio-conica mostrata nel diagramma precedente e una curva rastremata lineare. Si noti che la forma della curva potrebbe cambiare nelle versioni future di Windows. I primi quattro metodi nell'elenco precedente esprimono i livelli di volume come valori normalizzati nell'intervallo compreso tra 0,0 (volume minimo) e 1,0 (volume massimo). Per gli ultimi due metodi nell'elenco, chiamare il metodo [**IAudioEndpointVolume:: GetVolumeStepInfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) per ottenere il numero di passaggi nell'intervallo del volume.

Le interfacce seguenti usano curve con rastremazione lineare per le impostazioni del volume:

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Per ulteriori informazioni su queste interfacce, vedere [controlli del volume di sessione](session-volume-controls.md). Per informazioni sugli intervalli di volumi e sui livelli di volume predefiniti nelle varie versioni di Windows, vedere [impostazioni del volume audio predefinito](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> </dl>

 

 
