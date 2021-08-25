---
title: Creazione dell'effetto Echo
description: Creazione dell'effetto Echo
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Windows Media Player plug-in, metodo DoProcessOutput di esempio Echo
- plug-in, metodo DoProcessOutput di esempio Echo
- plug-in di elaborazione del segnale digitale, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP,metodo DoProcessOutput
- Esempio di plug-in Echo DSP, creazione dell'effetto echo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcb79b5be53f391854f38ce9aeba1c1bbff61ed2c0a982395c7063ff53146760
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902291"
---
# <a name="creating-the-echo-effect"></a>Creazione dell'effetto Echo

È prima necessario rimuovere il codice dall'esempio della procedura guidata che ridimensiona l'audio. Dalla sezione a 8 bit rimuovere il codice seguente:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



Tenere presente che m \_ fScaleFactor è stato sostituito da m \_ dwDelayTime.

Dalla sezione a 16 bit rimuovere il codice seguente:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



L'implementazione di **DoProcessOutput** fornita dal codice di esempio della procedura guidata plug-in crea un ciclo while che esegue l'iterazione una volta per ogni esempio nel buffer di input fornito da Windows Media Player. Questo ciclo funziona allo stesso modo per l'audio a 8 bit e a 16 bit, anche se è necessario un ciclo separato per ognuno. In ogni caso, il ciclo viene avviato con il test seguente:


```C++
while (dwSamplesToProcess--)

```



Una volta all'interno del ciclo, le routine di elaborazione sono molto simili per l'audio a 8 bit e a 16 bit. La differenza principale è che il codice nella sezione a 8 bit modifica l'intervallo di valori di dati da -128 a 127 e quindi riconverte l'intervallo prima di scrivere i dati nel buffer di output. Questo è importante per mantenere la simmetria della forma d'onda audio durante l'elaborazione.

È ora possibile iniziare ad aggiungere e sostituire il codice nel ciclo di elaborazione.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Recuperare un esempio dal buffer di input

Durante ogni iterazione del ciclo, un singolo campione viene recuperato dal buffer di input. Per l'audio a 8 bit, l'esempio viene spostato nel nuovo intervallo e quindi il puntatore al buffer di input viene avanzato all'esempio successivo. Il codice seguente deriva dalla procedura guidata del plug-in:


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



Per l'audio a 16 bit, il processo è lo stesso ad eccezione della normalizzazione:


```C++
// Get the input sample.
int i = *pwInputData++;

```



Tenere presente che i puntatori nel codice a 16 bit sono stati convertiti nel tipo **short**.

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>Recuperare un campione dal buffer di ritardo

Recuperare quindi un singolo campione dal buffer di ritardo. Per il codice a 8 bit, gli esempi di ritardo vengono archiviati nell'intervallo nativo compreso tra 0 e 255. Il codice seguente, che è necessario aggiungere, recupera un esempio di ritardo a 8 bit:


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



Per l'audio a 16 bit, il processo è simile al seguente:


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Scrivere l'esempio di input nel buffer di ritardo

A questo punto, è necessario archiviare l'esempio di input nel buffer di ritardo nella stessa posizione da cui è stato recuperato l'esempio di ritardo. Di seguito è riportato il codice da aggiungere per l'audio a 8 bit:


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Questo è il codice da aggiungere per la sezione a 16 bit:


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Spostare il puntatore del buffer di ritardo

Ora che il lavoro nel buffer di ritardo è stato completato per questa iterazione, è possibile far avanzare il puntatore mobile al buffer di ritardo. Se il puntatore raggiunge la fine del buffer circolare, è necessario modificarne il valore in modo che punti alla parte superiore del buffer. A tale scopo per l'audio a 8 bit, usare il codice seguente:


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



Ecco il codice per la sezione a 16 bit:


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



Poiché il puntatore nella sezione a 16 bit è effettivamente una copia della variabile membro, è necessario ricordarsi di aggiornare il valore nella variabile membro con il nuovo indirizzo. Se non si riesce a eseguire questa operazione, il puntatore del buffer di ritardo punta ripetutamente alla parte superiore del buffer e l'effetto echo non funzionerà come previsto. Aggiungere il codice seguente alla sezione a 16 bit:


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Combinare l'esempio di input con l'esempio delay

È qui che si usano i valori della combinazione umida e della combinazione a secco per creare l'esempio di output finale. È sufficiente moltiplicare ogni campione per il valore a virgola mobile che rappresenta la percentuale del segnale finale per il campione. Moltiplicare il campione di input per il valore archiviato in m fDryMix; moltiplicare il campione di ritardo per \_ il valore archiviato in m \_ fWetMix. Aggiungere quindi i due valori. Il codice da aggiungere è identico per le sezioni a 8 bit e a 16 bit:


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Scrivere i dati nel buffer di output

Infine, copiare l'esempio misto nel buffer di output e quindi far avanzare il puntatore del buffer di output. Per l'audio a 8 bit, la procedura guidata del plug-in usa il codice seguente per ripristinare l'intervallo originale dell'esempio:


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



Per l'audio a 16 bit, la procedura guidata usa il codice seguente come passaggio finale nel ciclo di elaborazione:


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




