---
title: Elaborazione dei dati audio
description: Elaborazione dei dati audio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, dati audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298555"
---
# <a name="processing-the-audio-data"></a>Elaborazione dei dati audio

L'implementazione predefinita di **DoProcessOutput** inizia con il recupero di un puntatore a una struttura **WAVEFORMATEX** valida, esattamente come è stato fatto in **AllocateStreamingResources**. USA quindi le informazioni contenute in tale struttura per calcolare il numero di campioni nel buffer di input in attesa di essere elaborati. Il codice seguente viene dall'implementazione predefinita:


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



Il codice esamina quindi il membro **wBitsPerSample** per determinare la profondità del bit dell'audio. Questo valore viene utilizzato in un'istruzione switch per fornire un'elaborazione separata per audio a 8 bit e a 16 bit.

## <a name="differences-between-8-bit-and-16-bit-audio"></a>Differenze tra audio a 8 e 16 bit

Esistono differenze importanti tra audio a 8 e 16 bit. Pertanto, le routine di elaborazione per creare l'effetto Echo sono diverse. I due formati sono diversi nei modi seguenti:

-   Ogni formato ha dimensioni di campionamento diverse: gli esempi a 8 bit occupano un byte di memoria, mentre gli esempi a 16 bit occupano due byte.
-   Ogni formato rappresenta l'ampiezza audio in modo diverso. l'audio a 8 bit è rappresentato da un Unsigned Integer con un intervallo compreso tra 0 e 255; il valore 128 rappresenta il silenzio. l'audio a 16 bit è rappresentato da un Signed Integer con un intervallo compreso tra-32768 e 32767; il valore zero rappresenta il silenzio.

Mentre il processo di creazione dell'effetto Echo è sostanzialmente identico per ogni formato, i dettagli devono essere leggermente diversi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




