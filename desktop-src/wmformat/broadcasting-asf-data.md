---
title: Trasmissione di dati ASF
description: Trasmissione di dati ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK, trasmissione di dati ASF
- Formato di sistemi avanzati (ASF), trasmissione di dati
- ASF (Advanced Systems Format), trasmissione di dati
- Windows Media Format SDK, invio di dati ASF
- Formato di sistemi avanzati (ASF), invio di dati
- ASF (Advanced Systems Format), invio di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104046419"
---
# <a name="broadcasting-asf-data"></a>Trasmissione di dati ASF

In questo argomento viene descritto come inviare dati ASF in una rete utilizzando il protocollo HTTP. Per l'invio di file in una rete è necessario utilizzare l'oggetto writer, pertanto è necessario avere una conoscenza generale di questo oggetto prima di leggere questo argomento. Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).

Se si inizia con dati non compressi, procedere come segue:

1.  Creare l'oggetto writer chiamando la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Questa funzione restituisce un puntatore **IWMWriter** .
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Creare l'oggetto sink di rete chiamando la funzione [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , che restituisce un puntatore **IWMWriterNetworkSink** .
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Chiamare [**IWMWriterNetworkSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) nel sink di rete e specificare il numero di porta da aprire. ad esempio, 8080. Facoltativamente, chiamare [**IWMWriterNetworkSink:: GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) per ottenere l'URL dell'host. I client accedono al contenuto da questo URL. È anche possibile chiamare [**IWMWriterNetworkSink:: SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) per limitare il numero di client.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Collegare il sink di rete al writer chiamando [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) sul writer, con un puntatore all'interfaccia **IWMWriterNetworkSink** del sink di rete.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Impostare il profilo ASF chiamando il metodo [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sull'oggetto writer con un puntatore [**IWMProfile**](iwmprofile.md) . Per informazioni sulla creazione di un profilo, vedere [utilizzo dei profili](working-with-profiles.md).
6.  Facoltativamente, specificare i metadati usando l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) nel writer.
7.  Chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) sul writer.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Per ogni esempio, chiamare il metodo [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Specificare il numero di flusso, l'ora di presentazione, la durata dell'esempio e un puntatore al buffer di esempio. Il metodo **WriteSample** comprime gli esempi.
9.  Al termine, chiamare [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) sul writer.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Chiamare [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) sul writer per scollegare l'oggetto sink di rete.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Chiamare [**IWMWriterNetworkSink:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) sul sink di rete per rilasciare la porta.
    ```C++
    hr = pNetSink->Close();
    ```

    

Un altro modo per eseguire lo streaming di contenuto ASF in una rete consiste nel leggerlo da un file ASF esistente. Questo approccio è illustrato nell'esempio WMVNetWrite fornito nell'SDK. Oltre ai passaggi elencati in precedenza, eseguire le operazioni seguenti:

1.  Creare un oggetto Reader e chiamare il metodo **Open** con il nome del file.
2.  Chiamare [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) sull'oggetto Reader, con il valore **true**. Ciò consente all'applicazione di leggere tutti i flussi nel file, inclusi i flussi con esclusione reciproca.
3.  Eseguire una query sul Reader per l'interfaccia [**IWMProfile**](iwmprofile.md) . Utilizzare questo puntatore quando si chiama [**IWMWriter:: Seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) nell'oggetto writer (passaggio 5 nella procedura precedente).
4.  Per ogni flusso definito nel profilo, chiamare [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) per ottenere il numero di flusso. Passare questo numero di flusso al metodo [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) del Reader. Questo metodo comunica al lettore di fornire esempi compressi, anziché decodificarli. Gli esempi verranno recapitati all'applicazione tramite il metodo di callback [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) dell'applicazione.

    È necessario ottenere informazioni sui codec per ogni flusso letto non compresso e aggiungerlo all'intestazione prima della trasmissione. Per ottenere le informazioni sul codec, chiamare [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) per enumerare i codec associati al file nel lettore. Selezionare le informazioni sul codec che corrispondono alla configurazione del flusso. Impostare quindi le informazioni sul codec nel writer chiamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando le informazioni ottenute dal reader.

5.  Dopo aver impostato il profilo nel writer, chiamare [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) sul writer per ottenere il numero di input. Per ogni input, chiamare [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) con il valore **null**. Ciò indica all'oggetto writer che l'applicazione fornirà esempi compressi, quindi il writer non deve usare alcun codec per comprimere i dati. Assicurarsi di chiamare **SetInputProps** prima di chiamare **BeginWriting**.
6.  Facoltativamente, copiare gli attributi di metadati dal reader al writer
7.  Poiché gli esempi dal reader sono già compressi, usare il metodo [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) per scrivere gli esempi, anziché il metodo **WriteSample** . Il metodo **WriteStreamSample** ignora le normali procedure di compressione dell'oggetto writer.
8.  Quando il lettore raggiunge la fine del file, invia una \_ notifica WMT EOF all'applicazione.

Inoltre, l'applicazione deve guidare l'orologio sull'oggetto Reader, in modo che il lettore estragga i dati dal file nel minor tempo possibile. A tale scopo, chiamare il metodo [**IWMReaderAdvanced:: SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) sul Reader, con il valore **true**. Quando il lettore Invia la \_ notifica avviata da WMT, chiamare [**IWMReaderAdvanced::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) e specificare l'intervallo di tempo che il lettore deve recapitare. Al termine della lettura di questo intervallo di tempo, il lettore chiama il metodo [**IWMReaderCallbackAdvanced:: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback dell'applicazione. L'applicazione deve chiamare nuovamente **DeliverTime** per leggere l'intervallo di tempo successivo. Ad esempio, per leggere da un file a intervalli di un secondo:


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Invio di dati ASF in una rete**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




