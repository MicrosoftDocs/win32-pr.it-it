---
title: Elaborazione dei dati audio
description: Elaborazione dei dati audio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Windows Media Player plug-in, metodo DoProcessOutput di esempio Echo
- plug-in, metodo DoProcessOutput di esempio Echo
- plug-in di elaborazione del segnale digitale, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, dati audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678e1debd586017bfbe748d4f2bed6d17607afcbe2719b5e3ecba8cabf667af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334484"
---
# <a name="processing-the-audio-data"></a>Elaborazione dei dati audio

L'implementazione predefinita di **DoProcessOutput** inizia recuperando un puntatore a una struttura **WAVEFORMATEX** valida, esattamente come è stato fatto in **AllocateStreamingResources.** Usa quindi le informazioni in tale struttura per calcolare il numero di campioni nel buffer di input in attesa di elaborazione. Il codice seguente deriva dall'implementazione predefinita:


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



Il codice esamina quindi il membro **wBitsPerSample** per determinare la profondità in bit dell'audio. Questo valore viene usato in un'istruzione switch per fornire un'elaborazione separata per l'audio a 8 bit e a 16 bit.

## <a name="differences-between-8-bit-and-16-bit-audio"></a>Differenze tra audio a 8 bit e audio a 16 bit

Esistono importanti differenze tra l'audio a 8 bit e quello a 16 bit. Di conseguenza, le routine di elaborazione per creare l'effetto echo sono diverse. I due formati differiscono nei modi seguenti:

-   Ogni formato ha dimensioni di campionamento diverse: i campioni a 8 bit occupano ognuno un byte di memoria, mentre i campioni a 16 bit occupano ognuno due byte.
-   Ogni formato rappresenta l'ampiezza audio in modo diverso. L'audio a 8 bit è rappresentato da un intero senza segno con un intervallo compreso tra 0 e 255; Il valore 128 rappresenta il silenzio. L'audio a 16 bit è rappresentato da un intero con segno con un intervallo compreso tra -32768 e 32767; Il valore zero rappresenta il silenzio.

Anche se il processo di creazione dell'effetto echo è fondamentalmente identico per ogni formato, i dettagli devono essere leggermente diversi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




