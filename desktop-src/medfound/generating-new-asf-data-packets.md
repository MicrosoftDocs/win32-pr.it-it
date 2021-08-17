---
description: Generazione di nuovi pacchetti di dati ASF
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Generazione di nuovi pacchetti di dati ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9473037d656bd4fcc01b91a908103fcda3e364a36e8caaf42cfc0558381e5af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742076"
---
# <a name="generating-new-asf-data-packets"></a>Generazione di nuovi pacchetti di dati ASF

Il *multiplexer* ASF è un componente di livello WMContainer che funziona con l'oggetto dati [ASF](asf-file-structure.md) e offre a un'applicazione la possibilità di generare pacchetti di dati ASF per un flusso che soddisfano i requisiti definiti nell'oggetto ContentInfo.

Il multiplexer ha un input e un output. Riceve un esempio di flusso che contiene dati multimediali digitali e produce uno o più pacchetti di dati che possono essere scritti in un contenitore ASF.

L'elenco seguente riepiloga il processo di generazione di pacchetti di dati ASF:

1.  Passare i dati di input al multiplexer in [**IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Raccogliere i pacchetti di dati chiamando [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in un ciclo finché non vengono recuperati tutti i pacchetti completi.
3.  Dopo la conversione dei dati di input in pacchetti completi, potrebbero essere presenti alcuni dati in sospeso nel multiplexer, che non sono stati recuperati da [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Chiamare [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) per creare pacchetti degli esempi in sospeso e raccoglierli dal multiplexer chiamando di nuovo **GetNextPacket.**
4.  Aggiornare gli oggetti intestazione ASF associati chiamando [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) per riflettere le modifiche apportate dal multiplexer durante la generazione di pacchetti di dati.

Il diagramma seguente illustra la generazione di pacchetti di dati per un file ASF tramite il multiplexer.

![Diagramma che mostra la generazione di pacchetti di dati per un file asf](images/packet.gif)

## <a name="asf-data-packet-creation"></a>Creazione di pacchetti di dati ASF

Dopo aver creato e inizializzato il multiplexer come descritto in Creazione dell'oggetto [Multiplexer,](creating-the-multiplexer-object.md)chiamare [**IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) per passare i dati di input al multiplexer per l'elaborazione in pacchetti di dati. L'input specificato deve essere in un campione multimediale [**(interfaccia IMFSample)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) che può avere uno o più buffer multimediali [**(interfaccia IMFMediaBuffer)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) che contengono i dati per un flusso. In caso di transcodificare DA ASF ad ASF, l'esempio di supporti di input può essere generato dalla barra di divisione che crea esempi di flussi in pacchetto. Per altre informazioni, vedere [Suddivisione ASF.](asf-splitter.md)

Prima di [**chiamare ProcessSample,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)assicurarsi che il timestamp dell'esempio di supporti di input sia un'ora di presentazione valida. in caso **contrario, ProcessSample** ha esito negativo e restituisce il codice TIMESTAMP \_ MF E \_ NO \_ \_ SAMPLE.

Il multiplexer può accettare l'input come campioni di supporti compressi o non compressi tramite [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample). Il multiplexer assegna tempi di invio a questi esempi a seconda dell'utilizzo della larghezza di banda del flusso. Durante questo processo, il multiplexer controlla i parametri del bucket di perdita (velocità in bit e utilizzo della finestra del buffer) e può rifiutare campioni che non rispettano tali valori. L'esempio di supporti di input può non riuscire nel controllo della larghezza di banda per uno dei motivi seguenti:

-   Se il campione di supporti di input è arrivato in ritardo perché l'ora dell'ultima trasmissione assegnata è maggiore del timestamp di questo esempio di supporti. [**ProcessSample ha**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) esito negativo e restituisce il **codice di errore MF E LATE \_ \_ \_ SAMPLE.**
-   Se il timestamp nell'esempio di supporti di input è precedente all'ora di invio assegnata (indica l'overflow del buffer). Il multiplexer può ignorare questa situazione se è configurato per regolare la velocità in bit impostando il flag **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE** durante l'inizializzazione del multiplexer. Per altre informazioni, vedere "Inizializzazione di multiplexer e bucket Impostazioni" in [Creazione dell'oggetto Multiplexer](creating-the-multiplexer-object.md). Se questo flag non è impostato e il multiplexer rileva un sovraccarico della larghezza di banda, [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ha esito negativo e restituisce il codice di errore **MF \_ E BANDWIDTH \_ \_ OVERRUN.**

Dopo che il multiplexer ha assegnato l'ora di invio, l'esempio di supporto di input viene aggiunto alla finestra di invio, ovvero un elenco di esempi di supporti di input ordinati in base agli orari di invio e pronti per l'elaborazione in pacchetti di dati. Durante la costruzione del pacchetto di dati, l'esempio di supporti di input viene analizzato e i dati pertinenti vengono scritti in un pacchetto di dati come payload. Un pacchetto di dati completo può contenere dati di uno o più esempi di supporti di input.

Quando nella finestra di invio arrivano nuovi esempi di supporti di input, questi vengono aggiunti a una coda finché non sono disponibili esempi di supporti sufficienti per formare un pacchetto completo. I dati nei buffer multimediali contenuti nell'esempio di supporti di input non vengono copiati nel pacchetto di dati generato. Il pacchetto di dati contiene riferimenti ai buffer dei supporti di input fino a quando l'esempio di supporti di input non è stato completamente in pacchetto e il pacchetto completo non è stato raccolto dal multiplexer.

Quando è disponibile un pacchetto di dati completo, è possibile recuperarlo chiamando [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Se si chiama [**ProcessSample mentre**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) sono disponibili pacchetti completi pronti per il recupero, l'operazione ha esito negativo e restituisce il codice di errore **MF \_ E \_ NOTACCEPTING.** Ciò indica che il multiplexer non può accettare più input ed è necessario chiamare **GetNextPacket** per recuperare i pacchetti in attesa. Idealmente, ogni **chiamata a ProcessSample** deve essere seguita da una o più **chiamate GetNextPacket** per ottenere i pacchetti di dati completi. La creazione di un pacchetto di dati completo può richiedere più di un campione di supporti di input. Al contrario, i dati in un campione di supporti di input possono estendersi su più pacchetti. Pertanto, non tutte le chiamate a **ProcessSample** generano esempi di supporti di output.

Se l'esempio di supporti di input contiene un fotogramma chiave indicato dall'attributo [**\_ CleanPoint MFSampleExtension,**](mfsampleextension-cleanpoint-attribute.md) il multiplexer copia l'attributo nel pacchetto.

## <a name="getting-asf-data-packets"></a>Recupero di pacchetti di dati ASF

Per raccogliere gli esempi di supporti di output per un pacchetto di dati completo generato dal multiplexer, chiamare [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in un ciclo finché non sono rimasti altri esempi di supporti di output per il pacchetto. Di seguito sono elencati i casi di esito positivo:

-   Se è disponibile un pacchetto di dati completo, [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) riceve il flag **\_ ASF STATUS \_ FLAGS \_ INCOMPLETE** nel *parametro pdwStatusFlags.* Il *parametro ppIPacket* riceve un puntatore al primo pacchetto di dati. È necessario chiamare questo metodo finché riceve questo flag. A ogni iterazione, *ppIPacket* punta al pacchetto successivo nella coda.
-   Se è presente un solo pacchetto di dati, *ppIPacket* vi punta e il flag **\_ ASF STATUS \_ FLAGS \_ INCOMPLETE** non viene ricevuto in *pdwStatusFlags*.
-   [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) può avere esito positivo senza produrre pacchetti di dati se il multiplexer è ancora in corso di creazione di pacchetti e aggiunta di pacchetti di dati. In questo caso *ppIPacket* punta a **NULL.** Per continuare, è necessario fornire al multiplexer più esempi di supporti di input chiamando [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).

Il codice di esempio seguente illustra una funzione che genera pacchetti di dati usando il multiplexer. Il contenuto del pacchetto di dati generato verrà scritto nel flusso di byte di dati allocato dal chiamante.


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



La `WriteBufferToByteStream` funzione è illustrata nell'argomento [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

Per visualizzare un'applicazione completa che usa questo esempio di codice, vedere Esercitazione: Copia di file [ASF](tutorial--copying-asf-streams-from-one-file-to-another.md)Flussi da un file a un altro .

## <a name="post-packet-generation-calls"></a>Post Packet-Generation chiamate

Per assicurarsi che non siano presenti pacchetti di dati completi in attesa nel multiplexer, chiamare [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush). In questo modo il multiplexer deve inviare in pacchetto tutti i campioni di supporti in corso. L'applicazione può raccogliere questi pacchetti sotto forma di campioni multimediali tramite **GetNextPacket** in un ciclo fino a quando non sono rimasti altri pacchetti da recuperare.

Dopo aver generato tutti gli esempi di supporti, chiamare [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) per aggiornare l'oggetto intestazione ASF associato a questi pacchetti di dati. L'oggetto Header viene specificato passando l'oggetto ContentInfo usato per inizializzare il multiplexer. Questa chiamata aggiorna vari oggetti Header per riflettere le modifiche apportate dal multiplexer durante la generazione di pacchetti di dati. Queste informazioni includono il numero di pacchetti, la durata dell'invio, la durata di riproduzione e i numeri di flusso di tutti i flussi. Vengono aggiornate anche le dimensioni complessive dell'intestazione.

È necessario assicurarsi che [**End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) sia chiamato dopo il recupero di tutti i pacchetti di dati. Se sono presenti pacchetti in attesa nel multiplexer, **End** avrà esito negativo e restituirà il codice di errore **MF \_ E FLUSH \_ \_ NEEDED.** In questo caso, ottenere il pacchetto in attesa chiamando [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) e [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in un ciclo.

> [!Note]  
> Per la codifica VBR, dopo aver **chiamato End** è necessario impostare le statistiche di codifica nelle proprietà di codifica dell'oggetto ContentInfo. Per informazioni su questo processo, vedere "Configurazione dell'oggetto ContentInfo con codificatore Impostazioni" in Impostazione delle proprietà [nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md). L'elenco seguente mostra le proprietà specifiche da impostare:
>
> -   [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md) è la velocità in bit media del contenuto VBR.
> -   [**MFPKEY \_ BAVG è**](mfpkey-bavgproperty.md) la finestra del buffer per la velocità in bit media.
> -   [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md) è la velocità in bit massima del contenuto VBR.
> -   [**MFPKEY \_ BMAX è**](mfpkey-bmaxproperty.md) la finestra del buffer di picco.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Esercitazione: Copia di file FLUSSI da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Esercitazione: Scrittura di un file WMA tramite la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



