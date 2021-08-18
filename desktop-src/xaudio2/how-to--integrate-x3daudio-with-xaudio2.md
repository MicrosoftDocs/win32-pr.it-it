---
description: Questo argomento illustra come integrare X3DAudio con XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Procedura: Integrare X3DAudio con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c940acbe78e8d4ca4247f77500adeeca7c9619057a3008dea50fc8b55a9f364e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962690"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Procedura: Integrare X3DAudio con XAudio2

Questo argomento illustra come integrare X3DAudio con XAudio2. È possibile usare X3DAudio per specificare i valori di volume e passo per le voci XAudio2 e i parametri per l'effetto di riverbero incorporato di XAudio2. Questo argomento presuppone che sia stato creato un grafo audio come descritto in [Procedura: Compilare](how-to--build-a-basic-audio-processing-graph.md)un'elaborazione audio di base Graph . Se non è già stato creato un grafico audio, [**X3DAudioInitialize avrà**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) esito negativo.

**Per inizializzare X3DAudio**

1.  Inizializzare X3DAudio chiamando [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    La funzione [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) accetta flag che indicano la configurazione dell'altoparlante, la velocità del suono in unità del mondo definite dall'utente al secondo e un handle per restituire un'istanza del motore X3DAudio. Chiamare [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) per ottenere la maschera di canale del formato di output.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Creare istanze delle [**strutture LISTENER \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ EMITTER.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

    La [**struttura LISTENER \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) rappresenta la posizione di qualsiasi elemento che ascolta il suono. In genere, si tratta della posizione della fotocamera o di una posizione vicina. La [**struttura X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) rappresenta la posizione dell'elemento che crea il suono. Per ogni suono monitorato sarà presente una struttura **\_ EMITTER X3DAUDIO.**

    I membri delle strutture che non verranno aggiornati in un ciclo di gioco devono essere inizializzati qui. La maggior parte dei membri delle strutture può essere semplicemente inizializzata su zero. Tuttavia, alcuni membri di [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) devono essere impostati per essere inizializzati su valori diversi da zero. Il membro ChannelCount **dell'emettitore X3DAUDIO \_** deve essere inizializzato sul numero di canali nella voce che rappresenta l'emettitore. Inoltre, il membro CurveDistanceScaler di **X3DAUDIO \_ EMITTER** deve essere compreso nell'intervallo da FLT MIN a \_ FLT \_ MAX.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Creare un'istanza della [**struttura X3DAUDIO \_ DSP \_ SETTINGS.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)

    La [**struttura X3DAUDIO \_ DSP \_ SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) viene usata per restituire i risultati calcolati da [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate). La **funzione X3DAudioCalculate** non alloca memoria per nessuno dei parametri. Ciò significa che è necessario allocare matrici per i membri pMatrixCoefficients e pDelayTimes della struttura **\_ DSP \_ SETTINGS X3DAUDIO** se si intende usarle. È inoltre necessario impostare i membri SrcChannelCount e DstChannelCount sul numero di canali nelle voci di origine e di destinazione dell'emettitore.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Usare [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) nella voce mastering per ottenere il numero di InputChannels per **nChannels**. Per le versioni di DirectX SDK di XAUDIO2 precedenti Windows 8, usare IXAudio2::GetDeviceDetails.

     

Eseguire questi passaggi una volta ogni due o tre fotogrammi per calcolare le nuove impostazioni e applicarle. In questo esempio, una voce di origine invia direttamente alla voce mastering e a una voce submix con un effetto riverbero applicato.

**Per usare X3DAudio per calcolare e applicare nuove impostazioni audio 3D**

1.  Aggiornare le [**strutture LISTENER \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) con la posizione, la velocità e l'orientamento correnti.

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

    

2.  Chiamare [**X3DAudioCalculate per calcolare**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) le nuove impostazioni per le voci.

    I parametri [**per X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) saranno le strutture [**X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) aggiornate. I flag indicherà quali valori **X3DAudioCalculate** deve calcolare e quale struttura [**X3DAUDIO \_ DSP \_ SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) consecherà i risultati dei calcoli eseguiti.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Usare [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) per applicare i valori di volume e passo alla voce di origine.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Usare [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) per applicare il livello di riverbero calcolato alla voce submix.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Usare [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) per applicare il coefficiente diretto del filtro di passaggio basso calcolato alla voce di origine.

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

[Controllo del volume e del passo XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
