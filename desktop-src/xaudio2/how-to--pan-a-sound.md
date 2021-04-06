---
description: In questo argomento viene illustrato come è possibile impostare la matrice di output di una voce di origine mono che restituisce una voce master stereo per ottenere una panoramica tra gli altoparlanti sinistro e destro.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Procedura: eseguire il panning di un suono'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883126"
---
# <a name="how-to-pan-a-sound"></a>Procedura: eseguire il panning di un suono

In questo argomento viene illustrato come è possibile impostare la matrice di output di una voce di origine mono che restituisce una voce master stereo per ottenere una panoramica tra gli altoparlanti sinistro e destro.

## <a name="to-setup-panning"></a>Per configurare la panoramica

1.  Recuperare la configurazione dell'altoparlante utilizzando [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  Creare una matrice che contenga la matrice di output. La dimensione minima della matrice di output corrisponde al numero di canali nella voce di origine per il numero di canali nella voce di output. In questo caso, un array di otto elementi gestirà un output mono Voice in qualsiasi formato di output fino a 7,1 audio surround.

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  Calcolare i livelli di trasmissione in base alla panoramica desiderata tra gli altoparlanti sinistro e destro. In questo esempio, i valori di Pan variano da-1 a 1 con-1 che indica tutto il suono a sinistra e 1 indica tutti i suoni nell'altoparlante destro.

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  Impostare gli indici della matrice di output corrispondenti agli altoparlanti sinistro e destro con i valori calcolati nel passaggio precedente. Gli altoparlanti sinistro e destro vengono determinati osservando la maschera di canale restituita da [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask). Poiché i canali devono sempre essere codificati nell'ordine specificato nella pagina di riferimento [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , è possibile determinare l'indice della matrice corrispondente a un singolo altoparlante.

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  Applicare la matrice di output alla voce di origine usando [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix). La voce di origine sarà una voce di origine o un submix Voice invio a una voce submix o a una voce Master. È possibile ottenere informazioni sulle voci di origine e di destinazione, ad esempio il numero di canali, usando [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Controllo volume e pitch XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
