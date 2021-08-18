---
title: Implementazione di DoProcessOutput
description: Implementazione di DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Windows Media Player plug-in, DSP audio
- plug-in, DSP audio
- plug-in di elaborazione del segnale digitale,DoProcessOutput
- plug-in DSP,DoProcessOutput
- plug-in DSP audio,DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f5aa1a952f16de196bed72ed7ac93dfac95d8333496824e3f0740f506a6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135584"
---
# <a name="implementing-doprocessoutput"></a>Implementazione di DoProcessOutput

Per elaborare i dati audio, è necessario eseguire diversi passaggi in **DoProcessOutput**. La procedura seguente usa il codice di esempio della procedura guidata plug-in come esempi. Se si vuole creare un plug-in DSP audio che elabora contenuto multimediale dello stesso tipo del codice di esempio della procedura guidata plug-in, sarà necessario modificare solo il codice di elaborazione effettivo a cui si fa riferimento nel passaggio 6. Di seguito sono riportati tutti i passaggi implementati in **DoProcessOutput:**

-   Se il plug-in non è attualmente abilitato, è sufficiente copiare i dati invariati nel buffer di output. Se il plug-in converte i dati in un formato diverso, è necessario eseguire anche l'elaborazione della conversione qui.

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   Recuperare un puntatore alla struttura del formato di input. È necessario recuperare i dati dei membri da questa struttura, quindi copiare il puntatore da *m \_ mtInput*.**pbformat a** una variabile puntatore locale di un tipo che corrisponde al tipo di struttura del formato. L'esempio seguente archivia un puntatore a una struttura di formato di input **WAVEFORMATEX:**

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   Calcolare il numero di campioni da elaborare. Il codice di esempio generato dalla procedura guidata plug-in esegue questo passaggio dividendo il numero di byte da elaborare per il membro **nBlockAlign** della struttura del formato di input WAVEFORMATEX e quindi moltiplicando il risultato per il numero di canali, archiviato nel membro **nChannels.** L'esempio seguente deriva dal codice di esempio della procedura guidata plug-in:

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  Determinare la profondità in bit dell'audio. Il codice di esempio della procedura guidata plug-in determina l'audio a 8 o 16 bit controllando il membro **wBitsPerSample** della **struttura WAVEFORMATEX.** Usa quindi tale valore in un'istruzione switch per fornire routine di elaborazione separate per ogni profondità di bit. Potrebbe essere necessario usare una tecnica diversa quando si gestiscono altri tipi di formato e profondità di bit.
    2.  Creare un ciclo per scorrere gli esempi audio nel buffer di input.
    3.  Recuperare un esempio dal buffer di input. A tale scopo, dereferenziare il puntatore ai dati di input e archiviare il risultato in una variabile di tipo int. Per l'audio a 16 bit, è necessario eseguire nuovamente il cast del puntatore BYTE a un puntatore short per gestire la maggiore precisione del campione audio. Dopo aver impostato il valore, è possibile incrementare immediatamente il puntatore *pbInputData* in modo che punti all'esempio successivo. Di seguito sono illustrati gli esempi seguenti:

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

    

    1.  Eseguire l'elaborazione. Qui vengono applicati gli algoritmi che modificano in qualche modo l'esempio. Ciò che si fa è a suo a che fare.
    2.  Scrivere i dati elaborati nel buffer di output. Incrementare immediatamente il puntatore al buffer di output, come nell'esempio seguente:

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  Ripetere il ciclo fino a quando non sono stati elaborati tutti i campioni.
    2.  Restituisce un **HRESULT appropriato.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




