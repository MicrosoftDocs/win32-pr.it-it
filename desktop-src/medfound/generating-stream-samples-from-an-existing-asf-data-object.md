---
description: Generazione di esempi di flusso da un oggetto dati ASF esistente
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Generazione di esempi di flusso da un oggetto dati ASF esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127883"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>Generazione di esempi di flusso da un oggetto dati ASF esistente

L'oggetto *splitter* ASF è un componente di livello WMContainer che analizza l'oggetto dati ASF di un file di formato Advanced Systems (ASF).

Prima di passare i pacchetti di dati alla barra di divisione, l'applicazione deve inizializzare, configurare e selezionare i flussi nella barra di divisione per prepararla per il processo di analisi. Per informazioni, vedere [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) e [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).

I metodi necessari per l'analisi dell'oggetto dati ASF sono i seguenti:

-   [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) che avvia il processo di analisi effettuando il push del buffer contenente i pacchetti di dati nella barra di divisione.
-   [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) che raccoglie gli esempi di flusso generati dal buffer passato alla barra di divisione.

## <a name="finding-the-data-offset"></a>Ricerca dell'offset dei dati

Prima di avviare il processo di analisi, l'applicazione deve individuare l'oggetto dati all'interno del file ASF. Esistono due modi per ottenere l'offset dell'oggetto dati dall'inizio del file:

-   Prima di avere inizializzato l'oggetto ContentInfo, è possibile chiamare il metodo [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Questo metodo richiede un buffer che contiene i primi 30 byte dell'intestazione ASF. Restituisce la dimensione dell'intera intestazione che indica l'offset al primo pacchetto di dati. Questo valore include anche le dimensioni dell'intestazione dell'oggetto dati di 50 byte.
-   Dopo avere inizializzato l'oggetto ContentInfo, è possibile ottenere il descrittore di presentazione chiamando [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)e quindi eseguendo una query sul descrittore di presentazione per l'attributo di [**\_ \_ \_ \_ \_ offset iniziale dei dati MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md) . Il valore di questo attributo è la dimensione dell'intestazione.
    > [!Note]  
    > L'attributo di [**\_ lunghezza dei dati MF PD \_ ASF \_ \_**](mf-pd-asf-data-length-attribute.md) nel descrittore di presentazione specifica la lunghezza dell'oggetto dati ASF.

     

In entrambi i casi, il valore restituito è la dimensione dell'oggetto intestazione più le dimensioni della sezione dell'intestazione dell'oggetto dati. Pertanto, il valore risultante è l'offset all'inizio dei pacchetti di dati nell'oggetto dati ASF. Quando si inizia a inviare dati alla barra di divisione, i dati devono iniziare in corrispondenza di questo offset dall'inizio del file ASF.

Il valore di offset viene passato come parametro a **ParseData** che avvia il processo di analisi.

L'oggetto dati è suddiviso in pacchetti di dati. Ogni pacchetto di dati contiene un'intestazione del pacchetto di dati che fornisce informazioni sull'analisi dei pacchetti e i dati di payload, ovvero i dati multimediali digitali effettivi. In uno scenario di ricerca, l'applicazione potrebbe volere che la barra di divisione avvii l'analisi in un particolare pacchetto di dati. A tale scopo, è possibile usare l'indicizzatore ASF per recuperare l'offset. L'indicizzatore restituisce un valore di offset che inizia in corrispondenza del limite del pacchetto. Se non si utilizza l'indicizzatore, verificare che l'offset venga avviato all'inizio dell'intestazione del pacchetto di dati. Se un offset non valido viene passato alla barra di divisione, ad esempio se il valore non punta al limite del pacchetto, le chiamate a **ParseHeader** e **GetNextSample** hanno esito positivo, ma **GetNextSample** non recupera alcun campione e il valore **null** viene ricevuto nel parametro *pSample* .

Se la barra di divisione è configurata in modo da essere analizzata nella direzione inversa, la barra di divisione inizia sempre l'analisi alla fine del buffer multimediale passato a **ParseData**. Pertanto, per l'analisi inversa nella chiamata a **ParseData**, passare l'offset nel parametro *cbLength* , che specifica la lunghezza dei dati e impostare *cbBufferOffset* su zero.

## <a name="generating-samples-for-asf-data-packets"></a>Generazione di esempi per i pacchetti di dati ASF

Un'applicazione avvia il processo di analisi passando i pacchetti di dati alla barra di divisione. L'input per la barra di divisione è costituito da una serie di buffer multimediali che contengono l'intero oggetto o frammenti dell'oggetto dati. L'output della barra di divisione è costituito da una serie di esempi di supporti che contengono i dati dei pacchetti.

Per passare i dati di input alla barra di divisione, creare un buffer multimediale e riempirlo con i dati della sezione oggetto dati del file ASF. Per ulteriori informazioni sui buffer multimediali, vedere [buffer multimediali](media-buffers.md). Passare quindi il buffer multimediale al metodo [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . È inoltre possibile specificare:

-   Offset nel buffer in cui deve iniziare l'analisi della barra di divisione. Se l'offset è zero, l'analisi inizia all'inizio del buffer. Per informazioni sull'impostazione dell'offset dei dati, vedere la sezione "ricerca dell'offset dei dati" in questo argomento.
-   Quantità di dati da analizzare. Se questo valore è zero, la barra di divisione viene analizzata fino a quando non raggiunge la fine del buffer, come specificato dal metodo [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .

La barra di divisione genera esempi di supporti facendo riferimento ai dati nei buffer multimediali. Il client può recuperare gli esempi di output chiamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in un ciclo fino a quando non sono presenti altri dati da analizzare. Se **GetNextSample** restituisce il \_ flag ASF STATUSFLAGS \_ incompleto nel parametro *pdwStatusFlags* , significa che sono disponibili altri esempi da recuperare e che l'applicazione può chiamare nuovamente **GetNextSample** . In caso contrario, chiamare **ParseData** per passare più dati alla barra di divisione. Per gli esempi generati, la barra di divisione imposta le informazioni seguenti:

-   La barra di divisione imposta un timestamp per tutti gli esempi generati. L'ora di esempio rappresenta l'ora di presentazione e non include il tempo di preiscrizione. L'applicazione può chiamare [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) per ottenere l'ora di presentazione, in unità di 100 nanosecondi.
-   Se si verifica un'interruzione durante la generazione del campione, la barra di divisione imposta l'attributo di [**\_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sul primo campione dopo la discontinuità. Le discontinuità sono in genere dovute a pacchetti eliminati in una connessione di rete, a dati di file danneggiati o al cambio di barra di divisione da un flusso di origine a un altro.
-   Per video, la barra di divisione controlla se l'esempio contiene un fotogramma chiave. In caso contrario, la barra di divisione imposta l'attributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) nell'esempio.

Se la barra di divisione analizza i pacchetti di dati ricevuti da un server multimediale, è possibile che la lunghezza del pacchetto sia variabile. In questo caso, il client deve chiamare **ParseData** per ogni pacchetto e impostare l' [**attributo \_ \_ limite del pacchetto MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) in ogni buffer inviato al separatore. Questo attributo indica alla barra di divisione se il buffer multimediale contiene l'inizio di un pacchetto ASF. Impostare l'attributo su **true** se il buffer contiene l'inizio di un nuovo pacchetto. Se il buffer contiene una continuazione del pacchetto precedente, impostare l'attributo su **false**. I buffer non possono estendersi su più pacchetti.

Prima di passare i nuovi buffer multimediali alla barra di divisione, l'applicazione deve chiamare [**IMFASFSplitter:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush). Questo metodo reimposta la barra di divisione e cancella tutti i frame parziali in attesa di essere completati. Questa operazione è utile in uno scenario di ricerca in cui l'offset si trova in una posizione diversa.

### <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come analizzare i pacchetti di dati. In questo esempio viene analizzato dall'inizio dell'oggetto dati alla fine del flusso e vengono visualizzate informazioni sugli esempi contenenti fotogrammi chiave. Per un esempio completo in cui viene usato questo codice, vedere [esercitazione: lettura di un file ASF](tutorial--reading-an-asf-file.md).


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

 

 



