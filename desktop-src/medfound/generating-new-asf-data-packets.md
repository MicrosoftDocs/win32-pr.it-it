---
description: Generazione di nuovi pacchetti di dati ASF
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Generazione di nuovi pacchetti di dati ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f3432ecf34c58247a1533adb202b75f59d770c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484069"
---
# <a name="generating-new-asf-data-packets"></a>Generazione di nuovi pacchetti di dati ASF

Il *multiplexing* ASF è un componente di livello WMContainer che funziona con l' [oggetto dati ASF](asf-file-structure.md) e fornisce a un'applicazione la possibilità di generare pacchetti di dati ASF per un flusso che soddisfano i requisiti definiti nell'oggetto ContentInfo.

Multiplexer include un input e un output. Riceve un esempio di flusso contenente dati multimediali digitali e produce uno o più pacchetti di dati che possono essere scritti in un contenitore ASF.

Nell'elenco seguente viene riepilogato il processo di generazione dei pacchetti di dati ASF:

1.  Passare i dati di input al multiplexer in [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Raccogliere i pacchetti di dati chiamando [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in un ciclo fino a quando non vengono recuperati tutti i pacchetti completi.
3.  Dopo che i dati di input sono stati convertiti in pacchetti completi potrebbero essere presenti alcuni dati in sospeso nel multiplexer, che non è stato recuperato da [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Chiamare [**IMFASFMultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) per packetize gli esempi in sospeso e raccoglierli dal multiplexer chiamando di nuovo **GetNextPacket** .
4.  Aggiornare gli oggetti intestazione ASF associati chiamando [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) per riflettere le modifiche apportate dal multiplexer durante la generazione del pacchetto di dati.

Il diagramma seguente illustra la generazione di pacchetti di dati per un file ASF tramite multiplexer.

![diagramma che mostra la generazione di pacchetti di dati per un file ASF](images/packet.gif)

## <a name="asf-data-packet-creation"></a>Creazione di pacchetti di dati ASF

Dopo la creazione e l'inizializzazione del multiplexer come descritto in [creazione dell'oggetto multiplexer](creating-the-multiplexer-object.md), chiamare [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) per passare i dati di input al multiplexer per l'elaborazione nei pacchetti di dati. L'input specificato deve trovarsi in un esempio di supporto (interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) che può avere uno o più buffer multimediali (interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) ) che contengono i dati per un flusso. Nel caso di una transcodifica da ASF ad ASF, l'esempio di supporti di input può essere generato dalla barra di divisione che crea esempi di flussi in pacchetti. Per ulteriori informazioni, vedere la [barra di divisione ASF](asf-splitter.md).

Prima di chiamare [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), verificare che il timestamp dell'esempio di supporti di input sia un tempo di presentazione valido. in caso contrario **ProcessSample** ha esito negativo e restituisce il \_ codice di timestamp MF e \_ nessun \_ esempio \_ .

Il multiplexer può accettare l'input come esempio di supporti compressi o non compressi tramite [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample). Il multiplexer assegna i tempi di invio a questi esempi a seconda dell'utilizzo della larghezza di banda del flusso. Durante questo processo, il multiplexer controlla i parametri di bucket persi (velocità in bit e utilizzo della finestra del buffer) e può rifiutare campioni che non rispettano tali valori. L'esempio di supporti di input può non riuscire a controllare la larghezza di banda per uno dei seguenti motivi:

-   Se l'esempio di supporti di input è arrivato in ritardo perché il tempo di invio assegnato per ultimo è maggiore del timestamp di questo esempio multimediale. [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ha esito negativo e restituisce il codice di errore di **\_ esempio MF e \_ tardivo \_** .
-   Se il timestamp dell'esempio di supporti di input è precedente all'ora di invio assegnata (indica l'overflow del buffer). Il multiplexer può ignorare questa situazione se è configurata per regolare la velocità in bit impostando il flag **MFASF \_ multiplexer \_ AutoAdjust \_ bitrate** durante l'inizializzazione del multiplexer. Per ulteriori informazioni, vedere l'argomento relativo all'inizializzazione del multiplexer e alle impostazioni dei bucket persi nella [creazione dell'oggetto multiplexer](creating-the-multiplexer-object.md). Se questo flag non è impostato e il multiplexer rileva un sovraccarico della larghezza di banda, [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ha esito negativo e restituisce il codice di errore di **sovraccarico della larghezza di \_ \_ banda \_ MF** e.

Quando il multiplexer assegna l'ora di invio, l'esempio di supporto di input viene aggiunto alla *finestra di trasmissione*, ovvero un elenco di esempi di supporti di input ordinati in base ai tempi di invio e pronti per essere elaborati nei pacchetti di dati. Durante la creazione di pacchetti di dati, l'esempio di supporti di input viene analizzato e i dati rilevanti vengono scritti in un pacchetto di dati come payload. Un pacchetto di dati completo può contenere dati di uno o più esempi di supporti di input.

Quando arrivano nuovi esempi di supporti di input nella finestra di trasmissione, vengono aggiunti a una coda finché non sono disponibili sufficienti esempi di supporti per formare un pacchetto completo. I dati nei buffer multimediali contenuti nell'esempio di supporto di input non vengono copiati nel pacchetto di dati generato. Il pacchetto di dati contiene riferimenti ai buffer del supporto di input fino a quando l'esempio di file multimediale di input non è stato completamente sottoposto a pacchetti e il pacchetto completo è stato raccolto dal multiplexer.

Quando è disponibile un pacchetto di dati completo, può essere recuperato chiamando [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Se si chiama [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) mentre sono presenti pacchetti completi pronti per il recupero, l'operazione ha esito negativo e restituisce il codice di errore **MF \_ e \_ NOTACCEPTING** . Ciò indica che il multiplexer non può accettare più input ed è necessario chiamare **GetNextPacket** per recuperare i pacchetti in attesa. Idealmente, ogni chiamata a **ProcessSample** deve essere seguita da una o più chiamate **GetNextPacket** per ottenere i pacchetti di dati completi. Per creare un pacchetto di dati completo, potrebbe essere necessario più di un esempio di file multimediale di input. Viceversa, i dati in un esempio di supporti di input possono estendersi su più pacchetti. Di conseguenza, non tutte le chiamate a **ProcessSample** produrranno esempi di supporti di output.

Se l'esempio multimediale di input contiene un fotogramma chiave indicato dall'attributo [**\_ CleanPoint di MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) , il multiplexer copia l'attributo nel pacchetto.

## <a name="getting-asf-data-packets"></a>Recupero di pacchetti di dati ASF

Per raccogliere gli esempi di supporti di output per un pacchetto di dati completo generato dal multiplexer, chiamare [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in un ciclo fino a quando non sono presenti altri esempi di supporti di output rimasti per il pacchetto. Di seguito sono elencati i casi di esito positivo:

-   Se è disponibile un pacchetto di dati completo, [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) riceve il flag di **\_ stato ASF \_ \_ incompleto** nel parametro *pdwStatusFlags* , mentre il parametro *ppIPacket* riceve un puntatore al primo pacchetto di dati. È necessario chiamare questo metodo finché riceve questo flag. Con ogni iterazione, *ppIPacket* punta al pacchetto successivo nella coda.
-   Se è presente un solo pacchetto di dati, *ppIPacket* fa riferimento a tale pacchetto e il flag di **\_ stato ASF \_ \_ incompleto** non è stato ricevuto in *pdwStatusFlags*.
-   [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) può avere esito positivo senza produrre pacchetti di dati se il multiplexer è ancora in fase di packetizing e aggiunge pacchetti di dati. In questo caso, *ppIPacket* punta a **null**. Per continuare, è necessario fornire al multiplexer più esempi di supporti di input chiamando [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).

Nell'esempio di codice seguente viene illustrata una funzione che genera pacchetti di dati tramite multiplexer. Il contenuto del pacchetto di dati generato verrà scritto nel flusso di byte dei dati allocato dal chiamante.


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



La `WriteBufferToByteStream` funzione è illustrata nell'argomento [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

Per visualizzare un'applicazione completa che usa questo esempio di codice, vedere [esercitazione: copia di flussi ASF da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="post-packet-generation-calls"></a>Chiamate di post Packet-Generation

Per assicurarsi che non siano presenti pacchetti di dati completi in attesa nel multiplexer, chiamare [**IMFASFMultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush). In questo modo, il multiplexer packetize tutti gli esempi di supporti in corso. L'applicazione può raccogliere questi pacchetti sotto forma di esempi di supporti tramite **GetNextPacket** in un ciclo fino a quando non sono presenti altri pacchetti da recuperare.

Una volta generati tutti gli esempi di supporti, chiamare [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) per aggiornare l'oggetto intestazione ASF associato a questi pacchetti di dati. L'oggetto Header viene specificato passando l'oggetto ContentInfo utilizzato per inizializzare il multiplexer. Questa chiamata Aggiorna vari oggetti intestazione in modo da riflettere le modifiche apportate dal multiplexer durante la generazione del pacchetto di dati. Queste informazioni includono il numero di pacchetti, la durata di invio, la durata della riproduzione e i numeri di flusso di tutti i flussi. Viene aggiornata anche la dimensione complessiva dell'intestazione.

È necessario assicurarsi che [**end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) venga chiamato dopo che tutti i pacchetti di dati sono stati recuperati. Se sono presenti pacchetti in attesa nel multiplexer, **end** avrà esito negativo e restituirà il codice di errore **MF \_ e \_ Flush \_ necessario** . In questo caso, recuperare il pacchetto in attesa chiamando [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) e [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in un ciclo.

> [!Note]  
> Per la codifica VBR, dopo aver chiamato **end** è necessario impostare le statistiche di codifica nelle proprietà di codifica dell'oggetto ContentInfo. Per informazioni su questo processo, vedere "configurazione dell'oggetto ContentInfo con le impostazioni del codificatore" in [impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md). Nell'elenco seguente vengono illustrate le proprietà specifiche da impostare:
>
> -   [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md) è la velocità in bit media del contenuto VBR.
> -   [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md) è la finestra del buffer per la velocità in bit media.
> -   [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md) è la velocità in bit massima del contenuto VBR.
> -   [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) è la finestra del buffer di picco.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Multiplexer ASF](asf-multiplexer.md)
</dt> <dt>

[Esercitazione: copia di flussi ASF da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Esercitazione: scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



