---
description: In questo argomento viene illustrato come integrare X3DAudio con XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Procedura: Integrare X3DAudio con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757691"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Procedura: Integrare X3DAudio con XAudio2

In questo argomento viene illustrato come integrare X3DAudio con XAudio2. È possibile usare X3DAudio per fornire i valori volume e pitch per le voci XAudio2 e i parametri per l'effetto XAudio2 incorporato. In questo argomento si presuppone che sia stato creato un grafico audio come descritto in [procedura: creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md). Se non è già stato creato un grafico audio, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) avrà esito negativo.

**Per inizializzare X3DAudio**

1.  Inizializzare X3DAudio chiamando [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    La funzione [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) accetta flag che indicano la configurazione del relatore, la velocità del suono nelle unità internazionali definite dall'utente al secondo e un handle per restituire un'istanza del motore X3DAudio. Chiamare [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) per ottenere la maschera di canale del formato di output.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Creare istanze del [**\_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e delle strutture di [**\_ emettitore X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

    La struttura del [**\_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) rappresenta la posizione in cui viene udito il suono. In genere, si tratta della posizione della fotocamera o di una posizione vicina. La struttura dell' [**\_ emettitore X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) rappresenta la posizione dell'elemento che crea il suono. Ci sarà una struttura **di \_ emettitore X3DAUDIO** per ogni suono rilevato.

    I membri delle strutture che non verranno aggiornati in un ciclo di gioco devono essere inizializzati qui. La maggior parte dei membri delle strutture può semplicemente essere inizializzata su zero. Tuttavia, alcuni membri di [**X3DAUDIO \_ emittor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) devono essere impostati in modo da essere inizializzati su valori diversi da zero. Il membro ChannelCount dell' **\_ emettitore X3DAUDIO** deve essere inizializzato sul numero di canali nella voce rappresentata dall'emittente. Inoltre, il membro CurveDistanceScaler di **X3DAUDIO \_ emittor** deve essere compreso nell'intervallo \_ da FLT min a flt \_ max.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Creare un'istanza della struttura [**delle \_ \_ impostazioni di X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .

    La [**struttura \_ \_ delle impostazioni di X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) viene utilizzata per restituire i risultati calcolati da [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate). La funzione **X3DAudioCalculate** non alloca memoria per alcun parametro. Ciò significa che è necessario allocare matrici per i membri pMatrixCoefficients e pDelayTimes della struttura **\_ \_ delle impostazioni DSP X3DAUDIO** se si intende usarli. Inoltre, è necessario impostare i membri SrcChannelCount e DstChannelCount sul numero di canali nelle voci di origine e di destinazione del emettitore.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Usare [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) nella voce mastering per ottenere il numero di InputChannels per **nChannels**. Per le versioni di XAUDIO2 di DirectX SDK precedenti a Windows 8, usare IXAudio2:: GetDeviceDetails.

     

Eseguire questi passaggi una volta ogni due o tre fotogrammi per calcolare le nuove impostazioni e applicarle. In questo esempio, una voce di origine invia direttamente alla voce mastering e a una voce submix con un effetto di riverbero applicato.

**Per usare X3DAudio per calcolare e applicare nuove impostazioni audio 3D**

1.  Aggiornare le [**strutture \_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**\_ emittor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) con la posizione, la velocità e l'orientamento correnti.

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  Chiamare [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) per calcolare le nuove impostazioni per le voci.

    I parametri per [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) saranno il [**\_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) aggiornato e le strutture di [**\_ emissione X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) . I flag indicheranno i valori che **X3DAudioCalculate** deve calcolare e la [**struttura \_ \_ delle impostazioni DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) che conterrà i risultati dei calcoli eseguiti.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Usare [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) per applicare i valori volume e pitch alla voce di origine.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Usare [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) per applicare il livello di riverbero calcolato alla voce submix.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Usare [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) per applicare il coefficiente diretto del filtro di passaggio basso calcolato alla voce di origine.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[Panoramica di X3DAudio](x3daudio-overview.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Controllo volume e pitch XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
