---
description: Il sink di file ASF è un'implementazione di IMFMediaSink fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai sink di supporto ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Aggiunta di informazioni sul flusso al sink di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306759"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Aggiunta di informazioni sul flusso al sink di file ASF

Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai [sink di supporto ASF](asf-media-sinks.md).

Dopo aver creato un'istanza del sink di file, è necessario configurarlo prima di compilare la topologia. Il sink di file deve conoscere i flussi nel file di output, le informazioni sulla modalità di codifica e i metadati. In questo argomento viene descritto il processo di aggiunta di un flusso nel sink di file.

-   [Aggiunta di flussi nel sink di file ASF](#adding-streams-in-the-asf-file-sink)
-   [Enumerazione dei sink di flusso](#enumerating-stream-sinks)
-   [Argomenti correlati](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Aggiunta di flussi nel sink di file ASF

Il sink di file deve essere a conoscenza dei flussi di output e delle relative proprietà in modo che sia in grado di generare gli esempi di output di conseguenza e di aggiungerli al file ASF di output. Queste impostazioni vengono scritte nell'oggetto intestazione ASF finale.

Per impostare le informazioni sul flusso, è necessario avere un riferimento all'oggetto ASF di sink di file. Per informazioni, vedere [creazione del sink di file ASF](creating-the-asf-file-sink.md).

Nella procedura riportata di seguito vengono riepilogati i passaggi generali per la configurazione di Stream utilizzando l'oggetto profilo ASF.

**Per configurare le informazioni sul flusso nel sink di file ASF**

1.  Creare un oggetto profilo ASF chiamando [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).
2.  Per ogni flusso nel file di output, creare un tipo di supporto per il flusso di destinazione da aggiungere nel sink di file. Il tipo di supporto deve essere compatibile con i tipi di output supportati dai codificatori Windows Media.

    Per informazioni sull'aggiunta di flussi audio al profilo, vedere Creazione di flussi audio per la codifica ASF.

    Per informazioni sull'aggiunta di flussi video al profilo, vedere Creazione di flussi video per la codifica ASF.

3.  Creare flussi in base ai tipi di supporti creati nel passaggio 2 chiamando [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).
4.  Assegnare un numero di flusso per il flusso appena creato chiamando il puntatore all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) ricevuto nel passaggio 3.
5.  Facoltativamente, configurare il flusso con le seguenti informazioni:
    -   Parametri bucket a perdita di parametri impostando gli attributi: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) o [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Estensione del payload, esclusione reciproca chiamando i metodi [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .
6.  Facoltativamente, impostare le dimensioni del pacchetto di dati per il profilo impostando gli attributi [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) e [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) . Il profilo ASF espone l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , a cui un'applicazione può fare riferimento chiamando **IMFASFProfile:: QueryInterface**.
7.  Impostare le informazioni di codifica per il flusso nel sink di file. Descritto in [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).
8.  Aggiungere il flusso al profilo chiamando [**IMFASFProfile:: sestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).
9.  Associare il profilo all'oggetto ContentInfo chiamando [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).

Per modificare un flusso esistente, l'applicazione può ottenere un riferimento all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) del flusso e riconfigurarla in base ai requisiti. Per aggiungere o rimuovere flussi, l'applicazione deve chiamare [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream). Per applicare queste modifiche, modificare o rimuovere i flussi, è necessario impostare di nuovo il profilo nell'oggetto ContentInfo. Viene sovrascritto il profilo esistente già associato all'oggetto ContentInfo.


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a>Enumerazione dei sink di flusso

Per ogni flusso del profilo che l'oggetto ContentInfo è in grado di riconoscere, il sink di file ASF crea e aggiunge un sink del flusso che contiene tutte le proprietà del flusso codificato. Il sink di file ASF è progettato per contenere flussi fissi. Ciò significa che non è possibile aggiungere o rimuovere flussi chiamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) o [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Queste chiamate al sink di file hanno esito negativo con il \_ \_ codice di errore fisso MF E STREAMSINKS \_ . L'aggiunta o la rimozione di flussi nel profilo non comporta l'aggiunta o la rimozione automatica dei sink di flusso nel sink di file. È necessario eliminare l'istanza esistente del file e ricrearla con le nuove informazioni sul flusso se i flussi nel profilo sono stati modificati.

Nella procedura riportata di seguito vengono riepilogati i passaggi generali per l'enumerazione dei sink di flusso nel sink di file ASF.

**Per enumerare i sink di flusso**

1.  Chiamare [**IMFMediaSink:: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) per ottenere il numero totale di sink di flusso nel sink di file ASF.
2.  Loop through the Stream sinks ang ottenere un riferimento all'interfaccia [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) del sink di flusso.

    -oppure-

    Chiamare [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) per ottenere il sink del flusso specificando il numero del flusso. Ogni sink di flusso viene identificato con il numero di flusso impostato durante la creazione del flusso nel profilo.

Se si compila una topologia parziale per la codifica di un file multimediale, è necessario aggiungere il sink di file alla topologia come nodo della topologia di output. Questa operazione può essere eseguita specificando ogni sink di vapore nel sink di file o impostando l'oggetto di attivazione del sink di file e gli identificatori di sink del flusso. Per ulteriori informazioni ed esempi di codice, vedere [creazione di nodi di output](creating-output-nodes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sink di supporti ASF](asf-media-sinks.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



