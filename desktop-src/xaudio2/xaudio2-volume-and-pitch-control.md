---
description: Questo argomento descrive il controllo del volume e del passo di XAudio2.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: Controllo del volume e del passo XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6376ad599b496a640b49d7eb539e1da774e31c71a3bf2a8e0c863fc140e19b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962490"
---
# <a name="xaudio2-volume-and-pitch-control"></a>Controllo del volume e del passo XAudio2

Questo argomento descrive il controllo del volume e del passo di XAudio2.

## <a name="volume-control"></a>Controllo volume

I livelli di volume sono espressi come moltiplicatori di ampiezza a virgola mobile tra -XAUDIO2 MAX VOLUME LEVEL e \_ \_ \_ XAUDIO2 \_ MAX VOLUME LEVEL \_ \_ (da -224 a 224), con un guadagno massimo di 144,5 dB. Un volume di 1,0 indica che non è presente alcuna attenuazione o guadagno; 0 indica il silenzio; e i livelli negativi possono essere usati per invertire la fase dell'audio. In XAudio2.h sono disponibili due funzioni inline per la conversione tra unità di volume: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) e [**XAudio2AmplitudeRatioToDecibels.**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)

È possibile applicare un livello di volume all'audio in diversi punti durante il flusso attraverso il grafo XAudio2:

-   Tutti i tipi di voce applicano un livello di volume complessivo all'input, che controllano usando il [**metodo IXAudio2Voice::SetVolume.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) Nelle voci submix e mastering, il livello di volume complessivo viene applicato subito prima della catena di filtri e effetti predefinita della voce. Nelle voci di origine, il livello di volume complessivo viene applicato dopo la catena di filtri e effetti predefinita della voce.
-   Le voci applicano un livello di volume per canale all'output, che controllano usando il [**metodo IXAudio2Voice::SetChannelVolumes.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) Il livello di volume per canale viene applicato subito dopo la conversione della frequenza di campionamento finale della voce e prima che venga inviato ad altre voci.
-   Ogni connessione tra una voce e un'altra dispone di una tabella di livelli usati per inviare audio da ogni canale di origine a ogni canale di destinazione, controllato tramite il metodo [**IXAudio2Voice::SetOutputMatrix.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)

Per impostazione predefinita, tutti i volumi complessivi e i volumi di canale sono inizialmente 1.0. Per impostazione predefinita, tutte le matrici a livello di trasmissione hanno valori appropriati che mantengono la potenza del segnale e il posizionamento del canale nel modo più accurato possibile. Per informazioni dettagliate, vedere Panoramica del mapping dei canali predefiniti di [XAudio2.](xaudio2-default-channel-mapping.md)

> [!Note]  
> XAudio2 regola automaticamente i livelli di volume in base alle impostazioni del parlante dell'utente per mantenere un livello di volume coerente tra le configurazioni. Se le impostazioni dell'utente non corrispondono alla configurazione fisica, il volume sarà troppo alto o troppo debole rispetto a un sistema con impostazioni accurate. Ad esempio, un sistema configurato per gli altoparlanti audio surround 5.1 che hanno solo due altoparlanti connessi avrà un suono troppo debole. XAudio2 non è in grado di rilevare se le impostazioni del parlante dell'utente corrispondono correttamente alla configurazione fisica.

 

## <a name="pitch-control"></a>Controllo dell'intonazione

I toni sono espressi come rapporti di velocità di input/output tra 1/1.024 e 1.024/1, inclusi. Un rapporto di 1/1.024 abbassa il passo di 10 ottetti, mentre un rapporto di 1.024/1 lo aumenta di 10 ottetti. È possibile usare solo il metodo [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) per applicare regolazioni del passo alle voci di origine e solo se non sono state create con il flag XAUDIO2 \_ VOICE \_ NOPITCH. Il rapporto di frequenza predefinito è 1/1, che indica che non è stata apportata alcuna modifica al passo. In XAudio2.h sono disponibili due funzioni inline per la conversione tra rapporti di frequenza e semitoni: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) e [**XAudio2SemitonesToFrequencyRatio.**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo volume e passo](volume-and-pitch-control.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Modificare il tono della voce](how-to--change-voice-pitch.md)
</dt> <dt>

[Procedura: Modificare il volume vocale](how-to--change-voice-volume.md)
</dt> </dl>

 

 
