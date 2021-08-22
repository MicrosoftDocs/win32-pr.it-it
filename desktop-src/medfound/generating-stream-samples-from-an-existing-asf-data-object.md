---
description: Generazione di esempi di flusso da un oggetto dati ASF esistente
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Generazione di esempi di flusso da un oggetto dati ASF esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fb99440c3fc4721851f183b3bfc7aefafd3f652d0436b29e9cea1209ba59b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974450"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>Generazione di esempi di flusso da un oggetto dati ASF esistente

L'oggetto *splitter* ASF è un componente del livello WMContainer che analizza l'oggetto dati ASF di un file ASF (Advanced Systems Format).

Prima di passare pacchetti di dati alla barra di divisione, l'applicazione deve inizializzare, configurare e selezionare i flussi nella barra di divisione per prepararlo per il processo di analisi. Per informazioni, vedere [Creazione dell'oggetto separatore ASF](creating-the-asf-splitter-object.md) [e Configurazione dell'oggetto separatore ASF](configuring-the-asf-splitter-object.md).

I metodi necessari per l'analisi dell'oggetto dati ASF sono:

-   [**IMFASFSplitter::P arseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) che avvia il processo di analisi tramite push del buffer contenente pacchetti di dati nella barra di divisione.
-   [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) che raccoglie gli esempi di flusso generati dal buffer passato alla barra di divisione.

## <a name="finding-the-data-offset"></a>Ricerca dell'offset dei dati

Prima di avviare il processo di analisi, l'applicazione deve individuare l'oggetto dati all'interno del file ASF. Esistono due modi per ottenere l'offset dell'oggetto dati dall'inizio del file:

-   Prima di inizializzare l'oggetto ContentInfo, è possibile chiamare il [**metodo IMFASFContentInfo::GetHeaderSize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) Questo metodo richiede un buffer che contiene i primi 30 byte dell'intestazione ASF. Restituisce le dimensioni dell'intera intestazione che indica l'offset al primo pacchetto di dati. Questo valore include anche le dimensioni dell'intestazione dell'oggetto dati di 50 byte.
-   Dopo aver inizializzato l'oggetto ContentInfo, è possibile ottenere il descrittore di presentazione chiamando [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)e quindi eseguire una query sul descrittore di presentazione per l'attributo [**MF \_ PD \_ ASF \_ DATA START \_ \_ OFFSET.**](mf-pd-asf-data-start-offset-attribute.md) Il valore di questo attributo è la dimensione dell'intestazione.
    > [!Note]  
    > [**L'attributo \_ MF PD \_ ASF DATA \_ \_ LENGTH**](mf-pd-asf-data-length-attribute.md) nel descrittore di presentazione specifica la lunghezza dell'oggetto dati ASF.

     

In entrambi i casi, il valore restituito è la dimensione dell'oggetto Intestazione più le dimensioni della sezione di intestazione dell'oggetto dati. Pertanto, il valore risultante è l'offset all'inizio dei pacchetti di dati nell'oggetto dati ASF. Quando si inizia a inviare dati alla barra di divisione, i dati devono iniziare a questo offset dall'inizio del file ASF.

Il valore di offset viene passato come parametro a **ParseData che** avvia il processo di analisi.

L'oggetto dati è suddiviso in pacchetti di dati. Ogni pacchetto di dati contiene un'intestazione di pacchetto di dati che fornisce informazioni sull'analisi dei pacchetti e i dati del payload, ovvero i dati multimediali digitali effettivi. In uno scenario di ricerca, l'applicazione potrebbe richiedere che la barra di divisione inizi l'analisi in corrispondenza di un determinato pacchetto di dati. A tale scopo, è possibile usare l'indicizzatore ASF per recuperare l'offset. L'indicizzatore restituisce un valore di offset che inizia in corrispondenza del limite del pacchetto. Se non si usa l'indicizzatore, assicurarsi che l'offset inizi all'inizio dell'intestazione del pacchetto di dati. Se viene passato un offset non valido alla barra di divisione, ad esempio il valore non punta al limite del pacchetto, le chiamate **ParseHeader** e **GetNextSample** hanno esito positivo, ma **GetNextSample** non recupera alcun campione e viene ricevuto **NULL** nel *parametro pSample.*

Se la barra di divisione è configurata per l'analisi in senso inverso, la barra di divisione inizia sempre l'analisi alla fine del buffer multimediale passato a **ParseData**. Pertanto, per l'analisi inversa nella chiamata a **ParseData,** passare l'offset nel *parametro cbLength,* che specifica la lunghezza dei dati e imposta *cbBufferOffset* su zero.

## <a name="generating-samples-for-asf-data-packets"></a>Generazione di esempi per pacchetti di dati ASF

Un'applicazione avvia il processo di analisi passando i pacchetti di dati alla barra di divisione. L'input per la barra di divisione è una serie di buffer multimediali che contengono l'intero oggetto o frammenti dell'oggetto dati. L'output della barra di divisione è una serie di esempi di supporti che contengono i dati del pacchetto.

Per passare i dati di input alla barra di divisione, creare un buffer multimediale e riempirlo con i dati della sezione Oggetto dati del file ASF. Per altre informazioni sui buffer multimediali, vedere [Buffer multimediali.](media-buffers.md) Passare quindi il buffer multimediale al [**metodo IMFASFSplitter::P arseData.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) È inoltre possibile specificare:

-   Offset nel buffer in cui deve iniziare l'analisi della barra di divisione. Se l'offset è zero, l'analisi inizia all'inizio del buffer. Per informazioni sull'impostazione dell'offset dei dati, vedere la sezione "Ricerca dell'offset dei dati" in questo argomento.
-   Quantità di dati da analizzare. Se questo valore è zero, la barra di divisione viene analizzata fino a raggiungere la fine del buffer, come specificato dal [**metodo IMFMediaBuffer::GetCurrentLength.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength)

La barra di divisione genera esempi di supporti facendo riferimento ai dati nei buffer multimediali. Il client può recuperare gli esempi di output chiamando [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in un ciclo finché non sono presenti altri dati da analizzare. Se **GetNextSample** restituisce il flag ASF \_ STATUSFLAGS INCOMPLETE nel \_ parametro *pdwStatusFlags,* significa che sono presenti più esempi da recuperare e l'applicazione può chiamare **nuovamente GetNextSample.** In caso contrario, **chiamare ParseData** per passare più dati alla barra di divisione. Per gli esempi generati, la barra di divisione imposta le informazioni seguenti:

-   La barra di divisione imposta un timestamp su tutti gli esempi generati. L'ora di esempio rappresenta l'ora di presentazione e non include l'ora di pre-registrazione. L'applicazione può chiamare [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) per ottenere l'ora di presentazione, in unità da 100 nanosecondi.
-   Se si verifica un'interruzione durante la generazione del campione, la barra di divisione imposta l'attributo [**MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) nel primo esempio dopo la discontinuità. Le discontinuità sono in genere causate da pacchetti eliminati in una connessione di rete, da dati di file danneggiati o dalla barra di divisione che passa da un flusso di origine a un altro.
-   Per il video, la barra di divisione controlla se l'esempio contiene un fotogramma chiave. In caso contrario, la barra di divisione imposta [**l'attributo MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) nell'esempio.

Se la barra di divisione analizza pacchetti di dati ricevuti da un server multimediale, è possibile che la lunghezza del pacchetto sia variabile. In questo caso, il client deve chiamare **ParseData** per ogni pacchetto e impostare [**l'attributo MFASFSPLITTER \_ PACKET \_ BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) su ogni buffer inviato alla barra di divisione. Questo attributo indica alla barra di divisione se il buffer multimediale contiene l'inizio di un pacchetto ASF. Impostare l'attributo **su TRUE** se il buffer contiene l'inizio di un nuovo pacchetto. Se il buffer contiene una continuazione del pacchetto precedente, impostare l'attributo su **FALSE**. I buffer non possono estendersi su più pacchetti.

Prima di passare nuovi buffer multimediali alla barra di divisione, l'applicazione deve chiamare [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush). Questo metodo reimposta la barra di divisione e cancella tutti i frame parziali in attesa di essere completati. Ciò è utile in uno scenario di ricerca in cui l'offset si trova in una posizione diversa.

### <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come analizzare i pacchetti di dati. Questo esempio analizza dall'inizio dell'oggetto dati alla fine del flusso e visualizza informazioni sugli esempi che contengono fotogrammi chiave. Per un esempio completo che usa questo codice, vedere [Esercitazione: Lettura di un file ASF.](tutorial--reading-an-asf-file.md)


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra di divisione ASF](asf-splitter.md)
</dt> </dl>

 

 



