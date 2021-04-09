---
title: Creazione dell'effetto Echo
description: Creazione dell'effetto Echo
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, creazione dell'effetto Echo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044152"
---
# <a name="creating-the-echo-effect"></a>Creazione dell'effetto Echo

È necessario innanzitutto rimuovere il codice dall'esempio della procedura guidata che consente di ridimensionare l'audio. Dalla sezione a 8 bit rimuovere il codice seguente:


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



L'implementazione di **DoProcessOutput** fornita dal codice di esempio della procedura guidata plug-in crea un ciclo while che esegue l'iterazione una volta per ogni campione nel buffer di input fornito da Windows Media Player. Questo ciclo funziona allo stesso modo per l'audio a 8 bit e a 16 bit, anche se per ciascuna è necessario un ciclo separato. In ogni caso, il ciclo inizia con il test seguente:


```C++
while (dwSamplesToProcess--)

```



Una volta all'interno del ciclo, le routine di elaborazione sono molto simili per l'audio a 8 bit e a 16 bit. La differenza principale consiste nel fatto che il codice nella sezione a 8 bit modifica l'intervallo di valori dei dati da-128 a 127, quindi converte di nuovo l'intervallo prima di scrivere i dati nel buffer di output. Questo è importante per mantenere la simmetria della forma d'onda audio durante l'elaborazione.

A questo punto è possibile iniziare ad aggiungere e sostituire il codice nel ciclo di elaborazione.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Recuperare un campione dal buffer di input

Durante ogni iterazione del ciclo, viene recuperato un singolo campione dal buffer di input. Per l'audio a 8 bit, l'esempio viene spostato nel nuovo intervallo, quindi il puntatore al buffer di input è avanzato per l'esempio successivo. Il codice seguente viene dalla procedura guidata plug-in:


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



Per l'audio a 16 bit, il processo è simile:


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Scrivere l'esempio di input nel buffer di ritardo

A questo punto, è necessario archiviare l'esempio di input nel buffer di ritardo nello stesso percorso da cui è stato recuperato l'esempio di ritardo. Di seguito è riportato il codice che è necessario aggiungere per audio a 8 bit:


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Si tratta del codice da aggiungere per la sezione a 16 bit:


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Spostare il puntatore del buffer di ritardo

Ora che il lavoro nel buffer di ritardo è terminato per questa iterazione, è possibile far avanzare il puntatore mobile al buffer di ritardo. Se il puntatore raggiunge la fine del buffer circolare, è necessario modificarne il valore in modo che punti all'inizio del buffer. Per eseguire questa operazione per audio a 8 bit, usare il codice seguente:


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



Poiché il puntatore nella sezione a 16 bit è effettivamente una copia della variabile membro, è necessario ricordarsi di aggiornare il valore nella variabile membro con il nuovo indirizzo. Se non si riesce a eseguire questa operazione, il puntatore del buffer di ritardo punterà ripetutamente all'inizio del buffer e l'effetto Echo non funzionerà come previsto. Aggiungere il codice seguente alla sezione a 16 bit:


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Combinare l'esempio di input con l'esempio delay

Questa è la posizione in cui si usano i valori Wet Mix e dry mix per creare l'esempio di output finale. È sufficiente moltiplicare ogni campione in base al valore a virgola mobile che rappresenta la percentuale del segnale finale per l'esempio. Moltiplicare l'esempio di input in base al valore archiviato in m \_ fDryMix; moltiplicare l'esempio di ritardo in base al valore archiviato in m \_ fWetMix. Quindi, aggiungere i due valori. Il codice che è necessario aggiungere è identico per le sezioni a 8 bit e a 16 bit:


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Scrivere i dati nel buffer di output

Infine, copiare l'esempio misto nel buffer di output, quindi spostare il puntatore del buffer di output. Per l'audio a 8 bit, la procedura guidata plug-in USA il codice seguente per restituire l'esempio nell'intervallo originale:


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



Per audio a 16 bit, la procedura guidata usa il codice seguente come passaggio finale del ciclo di elaborazione:


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




