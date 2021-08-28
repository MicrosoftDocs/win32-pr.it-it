---
title: Implementazione di IMediaObject AllocateStreamingResources
description: Implementazione di IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Windows Media Player plug-in, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione del segnale digitale, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
- Esempio di plug-in Echo DSP, buffer di ritardo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291b1f9627d9dfb78ae2aff9d34b6fadd47cbf28a5c2f0830f5833d9e83cde21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508961"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implementazione di IMediaObject::AllocateStreamingResources

Nell'esempio Echo il **metodo AllocateStreamingResources** crea il buffer di ritardo. A tale scopo, eseguire le operazioni seguenti:

1.  Calcolo di una dimensione per il buffer corrispondente al tempo di ritardo specificato per il tipo di supporto specificato.
2.  Allocare nuova memoria o riallocare le dimensioni del buffer, se esiste già.
3.  Chiamata di un metodo che riempie il buffer con valori che rappresentano il silenzio.

Il valore di silence è diverso a seconda della profondità in bit. Per l'audio a 8 bit, il silenzio è rappresentato dal valore esadecimale 80; per l'audio a 16 bit, il silenzio è rappresentato da zero.

## <a name="calculating-the-delay-buffer-size"></a>Calcolo delle dimensioni del buffer di ritardo

Per calcolare le dimensioni necessarie per il buffer di ritardo, è prima necessario recuperare una **struttura WAVEFORMATEX** contenente informazioni sui dati audio. L'esempio seguente recupera un puntatore a questa struttura dall'input **DMO \_ MEDIA \_ TYPE:**


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Dopo aver archiviato un puntatore alla struttura **WAVEFORMATEX** appropriata, è possibile esaminarne i membri e usarli per calcolare le dimensioni del buffer necessarie. L'esempio di codice seguente illustra questa operazione:


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Questo algoritmo calcola le dimensioni del buffer moltiplicando il tempo di ritardo, in millisecondi, per il numero di campioni al millisecondo, quindi moltiplicando il risultato per il numero di canali e quindi moltiplicando il risultato per il numero di byte per campione. Il numero di canali e il numero di byte per campione non sono ovvi; vengono codificati nel membro nBlockAlign. La divisione per 1000 riduce il valore nSamplesPerSec a campioni al millisecondo. il millisecondo è l'unità desiderata perché il tempo di ritardo è espresso in millisecondi.

## <a name="allocating-the-delay-buffer-memory"></a>Allocazione della memoria buffer ritardata

Dopo aver calcolato i requisiti di memoria, è possibile allocare il buffer. Potrebbe essere necessario eliminare il buffer se esiste, ad esempio quando l'utente richiama la pagina delle proprietà per modificare il valore del tempo di ritardo. Il codice seguente illustra l'allocazione del buffer di ritardo:


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



Se il buffer viene allocato correttamente, è necessario spostare il puntatore mobile nella parte superiore del buffer, come illustrato nell'esempio seguente:


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>Riempimento del buffer di ritardo con silenzio

È utile scrivere un metodo per riempire il buffer di ritardo con valori che rappresentano il silenzio. Il metodo deve ricevere il puntatore alla struttura WAVEFORMATEX valida e quindi controllare il membro wBitsPerSample per determinare se l'audio è a 8 bit o superiore. Nell'esempio seguente il buffer di ritardo viene riempito con il valore corretto per silence:


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



Ricordarsi di aggiungere la dichiarazione con inoltro per la funzione al file di intestazione Echo.h nella sezione privata:


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



È necessario aggiungere codice alla fine di AllocateStreamingResources per chiamare questo metodo ogni volta che il buffer di ritardo viene creato o ridimensionato. Il codice di esempio seguente passa il puntatore WAVEFORMATEX denominato pWave al nuovo metodo:


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Riallocazione della memoria buffer ritardata

Quando l'utente modifica il tempo di ritardo usando la pagina delle proprietà, anche le dimensioni del buffer di ritardo devono cambiare. Il codice è già stato aggiunto a AllocateStreamingResources per ridimensionare il buffer, ma è necessario aggiungere una riga di codice a CEcho::p ut delay per chiamare il metodo di allocazione delle risorse ogni volta che il valore della proprietà \_ cambia. Il codice è il seguente:


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso delle risorse di streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




