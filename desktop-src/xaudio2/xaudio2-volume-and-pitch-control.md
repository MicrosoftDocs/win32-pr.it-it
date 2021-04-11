---
description: Questo argomento descrive il volume e il controllo pitch di XAudio2.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: Controllo volume e pitch XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2526cfa50c0260e90e1aae9e2bce21d507dc2e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232453"
---
# <a name="xaudio2-volume-and-pitch-control"></a>Controllo volume e pitch XAudio2

Questo argomento descrive il volume e il controllo pitch di XAudio2.

## <a name="volume-control"></a>Controllo volume

I livelli di volume sono espressi come moltiplicatori di ampiezza a virgola mobile compresi tra-XAUDIO2 \_ \_ e il livello di volume massimo \_ XAUDIO2 \_ \_ \_ (da-224 a 224), con un guadagno massimo di 144,5 dB. Un volume di 1,0 significa che non esiste alcuna attenuazione o guadagno; 0 indica il silenzio; i livelli negativi possono essere usati per invertire la fase dell'audio. In XAudio2. h sono disponibili due funzioni inline per la conversione tra unità di volume: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) e [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels).

È possibile applicare un livello di volume all'audio in diversi punti durante l'attraversamento del grafico XAudio2:

-   Tutti i tipi di voce applicano un livello di volume globale al rispettivo input, che controllano usando il metodo [**IXAudio2Voice:: sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) . In submix e nelle voci di mastering, il livello di volume complessivo viene applicato immediatamente prima della catena di effetti e filtri incorporati della voce. Nelle voci di origine, il livello di volume complessivo viene applicato dopo il filtro e la catena di effetti predefiniti della voce.
-   Le voci applicano un livello di volume per canale al rispettivo output, che controllano usando il metodo [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) . Il livello del volume per canale viene applicato subito dopo la conversione della frequenza di campionamento finale della voce e prima che venga inviato ad altre voci.
-   Ogni connessione tra una voce e un'altra ha una tabella di livelli utilizzata per inviare audio da ogni canale di origine a ciascun canale di destinazione, che viene controllato tramite il metodo [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) .

Per impostazione predefinita, tutti i volumi complessivi e i volumi del canale sono inizialmente 1,0. Per impostazione predefinita, tutte le matrici a livello di trasmissione sono valori appropriati che mantengono il posizionamento del canale e della potenza del segnale nel modo più preciso possibile. Per informazioni dettagliate, vedere la panoramica sul [mapping del canale predefinito di XAudio2](xaudio2-default-channel-mapping.md) .

> [!Note]  
> XAudio2 regola automaticamente i livelli di volume in base alle impostazioni dell'altoparlante dell'utente per mantenere un livello di volume coerente nelle configurazioni. Se le impostazioni dell'utente non corrispondono alla configurazione fisica, il volume sarà troppo elevato o troppo debole rispetto a un sistema con impostazioni accurate. Un sistema configurato per 5,1, ad esempio, è dotato di due altoparlanti che sono collegati solo a due altoparlanti. XAudio2 non è in grado di rilevare se le impostazioni dell'altoparlante utente corrispondono correttamente alla configurazione fisica.

 

## <a name="pitch-control"></a>Controllo pitch

I Pitch sono espressi come velocità di input/rapporto di frequenza di output compreso tra 1/1024 e 1024/1, inclusi. Un rapporto di 1/1024 abbassa il passo di 10 ottave, mentre un rapporto di 1024/1 lo eleva di 10 ottavi. È possibile usare il metodo [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) solo per applicare le regolazioni del passo alle voci di origine e solo se non sono state create con \_ il \_ flag nopitch di XAUDIO2 Voice. Il rapporto di frequenza predefinito è 1/1, ovvero nessuna modifica di passo. In XAudio2. h sono disponibili due funzioni inline per la conversione tra i rapporti di frequenza e i semitoni: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) e [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo volume e pitch](volume-and-pitch-control.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: modificare il pitch vocale](how-to--change-voice-pitch.md)
</dt> <dt>

[Procedura: modificare il volume vocale](how-to--change-voice-volume.md)
</dt> </dl>

 

 
