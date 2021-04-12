---
title: Implementazione di IMediaObject AllocateStreamingResources
description: Implementazione di IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Plug-in di Windows Media Player, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione dei segnali digitali, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
- Esempio di plug-in Echo DSP, buffer di ritardo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396242"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implementazione di IMediaObject:: AllocateStreamingResources

Nell'esempio Echo il metodo **AllocateStreamingResources** crea il buffer di ritardo. A tale scopo, effettuare le operazioni seguenti:

1.  Calcolo di una dimensione per il buffer che corrisponde al tempo di ritardo specificato per il tipo di supporto specificato.
2.  Allocando una nuova memoria o riallocando la dimensione del buffer, se esiste già.
3.  Chiamata a un metodo che riempie il buffer con i valori che rappresentano il silenzio.

Il valore di Silence è diverso a seconda della profondità del bit. Per audio a 8 bit, il silenzio è rappresentato dal valore esadecimale 80; per audio a 16 bit, il silenzio è rappresentato da zero.

## <a name="calculating-the-delay-buffer-size"></a>Calcolo della dimensione del buffer di ritardo

Per calcolare le dimensioni necessarie per il buffer di ritardo, è necessario innanzitutto recuperare una struttura **WAVEFORMATEX** contenente informazioni sui dati audio. Nell'esempio seguente viene recuperato un puntatore a questa struttura dalla struttura **del \_ \_ tipo di supporto DMO** di input:


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Una volta archiviato un puntatore alla struttura **WAVEFORMATEX** corretta, è possibile esaminarne i membri e usarli per calcolare le dimensioni del buffer richieste. Nell'esempio di codice seguente viene illustrato quanto segue:


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Questo algoritmo calcola la dimensione del buffer moltiplicando il tempo di ritardo, in millisecondi, per il numero di campioni per millisecondo, moltiplicando quindi il risultato per il numero di canali, quindi moltiplicando il risultato per il numero di byte per campione. Il numero di canali e il numero di byte per campione non sono evidenti. sono codificati nel membro nBlockAlign. Dividendo per 1000, il valore nSamplesPerSec viene ridotto a campioni per millisecondo; il millisecondo è l'unità desiderata perché il tempo di ritardo è espresso in millisecondi.

## <a name="allocating-the-delay-buffer-memory"></a>Allocazione della memoria del buffer di ritardo

Una volta calcolati i requisiti di memoria, è possibile allocare il buffer. Potrebbe essere necessario eliminare il buffer, se esistente, ad esempio quando l'utente richiama la pagina delle proprietà per modificare il valore di tempo di ritardo. Il codice seguente illustra l'allocazione del buffer di ritardo:


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



Se il buffer viene allocato correttamente, è necessario spostare il puntatore mobile nell'intestazione del buffer, come illustrato nell'esempio seguente:


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>Riempimento del buffer di ritardo con silenziosità

È opportuno scrivere un metodo per riempire il buffer di ritardo con i valori che rappresentano il silenzio. Il metodo deve ricevere il puntatore alla struttura WAVEFORMATEX valida e quindi ispezionare il membro wBitsPerSample per determinare se l'audio è a 8 bit o superiore. Nell'esempio seguente viene compilato il buffer di ritardo con il valore corretto per il silenzio:


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



Ricordarsi di aggiungere la dichiarazione in diretta per la funzione al file di intestazione Echo. h nella sezione privata:


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



È necessario aggiungere il codice alla fine di AllocateStreamingResources per chiamare questo metodo ogni volta che il buffer di ritardo viene creato o ridimensionato. Il codice di esempio seguente passa il puntatore WAVEFORMATEX denominato pWave al nuovo metodo:


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Riallocazione della memoria del buffer di ritardo

Quando l'utente modifica il tempo di ritardo utilizzando la pagina delle proprietà, è necessario modificare anche la dimensione del buffer di ritardo. Il codice è già stato aggiunto a AllocateStreamingResources per ridimensionare il buffer, ma è necessario aggiungere una riga di codice a CEcho::p \_ intervallo di tempo ut per chiamare il metodo di allocazione delle risorse ogni volta che il valore della proprietà cambia. Il codice è il seguente:


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso delle risorse di streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




