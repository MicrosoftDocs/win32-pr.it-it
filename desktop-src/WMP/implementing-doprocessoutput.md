---
title: Implementazione di DoProcessOutput
description: Implementazione di DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in per l'elaborazione di segnali digitali, DoProcessOutput
- Plug-in DSP, DoProcessOutput
- plug-in DSP audio, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396202"
---
# <a name="implementing-doprocessoutput"></a>Implementazione di DoProcessOutput

Per elaborare i dati audio, è necessario eseguire diversi passaggi in **DoProcessOutput**. Nei passaggi seguenti viene utilizzato il codice di esempio della procedura guidata plug-in come esempi. Se si desidera creare un plug-in DSP audio che elabora il contenuto multimediale dello stesso tipo utilizzato dal codice di esempio della procedura guidata per il plug-in, sarà necessario solo modificare il codice di elaborazione effettivo a cui fa riferimento il passaggio 6. Di seguito sono riportati tutti i passaggi implementati in **DoProcessOutput**:

-   Se il plug-in non è attualmente abilitato, copiare semplicemente i dati invariati nel buffer di output. Se il plug-in converte i dati in un formato diverso, è necessario eseguire anche l'elaborazione della conversione.

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   Recuperare un puntatore alla struttura del formato di input. È necessario recuperare i dati dei membri da questa struttura, quindi copiare il puntatore da *m \_ mtInput*.**pbFormat** a una variabile puntatore locale di un tipo che corrisponde al tipo di struttura del formato. Nell'esempio seguente viene archiviato un puntatore a una struttura del formato di input **WAVEFORMATEX** :

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   Calcolare il numero di campioni da elaborare. Il codice di esempio generato dalla procedura guidata plug-in esegue questo passaggio dividendo il numero di byte da elaborare per il membro **nBlockAlign** della struttura del formato di input WAVEFORMATEX e quindi moltiplicando il risultato per il numero di canali, che è stato archiviato nel membro **nChannels** . Nell'esempio seguente viene riportato il codice di esempio della procedura guidata plug-in:

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  Determinare la profondità del bit dell'audio. Il codice di esempio della procedura guidata plug-in determina l'audio a 8 bit o a 16 bit esaminando il membro **wBitsPerSample** della struttura **WAVEFORMATEX** . USA quindi tale valore in un'istruzione switch per fornire routine di elaborazione separate per ogni profondità di bit. Potrebbe essere necessario usare una tecnica diversa quando si gestiscono altri tipi di formato e profondità dei bit.
    2.  Creare un ciclo per esaminare gli esempi audio nel buffer di input.
    3.  Recuperare un campione dal buffer di input. A tale scopo, dereferenziare il puntatore ai dati di input e archiviare il risultato in una variabile di tipo int. Per l'audio a 16 bit, è necessario eseguire il cast del puntatore di BYTE a un puntatore breve per gestire la precisione del campione audio maggiore. Una volta ottenuto il valore, è possibile incrementare immediatamente il puntatore *pbInputData* in modo che punti all'esempio successivo. Negli esempi seguenti viene illustrato quanto segue:

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    -oppure-

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  Eseguire l'elaborazione. Questo è il punto in cui si applicano in qualche modo gli algoritmi che modificano l'esempio. Questa operazione è stata eseguita dall'utente.
    2.  Scrivere i dati elaborati nel buffer di output. Incrementare immediatamente il puntatore al buffer di output, come nell'esempio seguente:

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  Ripetere il ciclo finché non vengono elaborati tutti gli esempi.
    2.  Restituisce un valore **HRESULT** appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




