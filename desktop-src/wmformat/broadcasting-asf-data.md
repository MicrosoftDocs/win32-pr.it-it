---
title: Trasmissione di dati ASF
description: Trasmissione di dati ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK, trasmissione di dati ASF
- Advanced Systems Format (ASF), trasmissione di dati
- ASF (Advanced Systems Format), trasmissione di dati
- Windows Media Format SDK, invio di dati ASF
- Advanced Systems Format (ASF), invio di dati
- ASF (Advanced Systems Format), invio di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44fc9ea0515822c765b0cb3af457254341a64f08e64d566aa9e226a48758e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434465"
---
# <a name="broadcasting-asf-data"></a>Trasmissione di dati ASF

Questo argomento descrive come inviare dati ASF attraverso una rete usando il protocollo HTTP. L'invio di file in rete richiede l'uso dell'oggetto writer, pertanto è necessario avere una conoscenza generale di questo oggetto prima di leggere questo argomento. Per altre informazioni, vedere [Scrittura di file ASF.](writing-asf-files.md)

Se si inizia con dati non compressi, eseguire le operazioni seguenti:

1.  Creare l'oggetto writer chiamando la [**funzione WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) Questa funzione restituisce un **puntatore IWMWriter.**
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Creare l'oggetto sink di rete chiamando la [**funzione WMCreateWriterNetworkSink,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) che restituisce un **puntatore IWMWriterNetworkSink.**
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Chiamare [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) nel sink di rete e specificare il numero di porta da aprire. ad esempio, 8080. Facoltativamente, chiamare [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) per ottenere l'URL dell'host. I client accederanno al contenuto da questo URL. È anche possibile chiamare [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) per limitare il numero di client.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Collegare il sink di rete al writer chiamando [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) nel writer, con un puntatore all'interfaccia **IWMWriterNetworkSink** del sink di rete.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Impostare il profilo ASF chiamando il metodo [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sull'oggetto writer, con un [**puntatore IWMProfile.**](iwmprofile.md) Per informazioni sulla creazione di un profilo, vedere [Utilizzo dei profili](working-with-profiles.md).
6.  Facoltativamente, specificare i metadati usando [**l'interfaccia IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) nel writer.
7.  Chiamare [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) nel writer.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Per ogni esempio, chiamare il [**metodo IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) Specificare il numero di flusso, l'ora di presentazione, la durata dell'esempio e un puntatore al buffer di esempio. Il **metodo WriteSample** comprime gli esempi.
9.  Al termine, chiamare [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) nel writer.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Chiamare [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) nel writer per scollegare l'oggetto sink di rete.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Chiamare [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) sul sink di rete per rilasciare la porta.
    ```C++
    hr = pNetSink->Close();
    ```

    

Un altro modo per trasmettere il contenuto asf in rete è leggerlo da un file ASF esistente. L'esempio WMVNetWrite fornito nell'SDK illustra questo approccio. Oltre ai passaggi elencati in precedenza, eseguire le operazioni seguenti:

1.  Creare un oggetto lettore e chiamare **il metodo Open** con il nome del file.
2.  Chiamare [**IWMReaderAdvanced::SetManualStreamSelection sull'oggetto**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) lettore, con il valore **TRUE.** In questo modo l'applicazione può leggere ogni flusso nel file, inclusi i flussi con esclusione reciproca.
3.  Eseguire una query sul lettore per [**l'interfaccia IWMProfile.**](iwmprofile.md) Usare questo puntatore quando si chiama [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sull'oggetto writer (passaggio 5 della procedura precedente).
4.  Per ogni flusso definito nel profilo, chiamare [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) per ottenere il numero di flusso. Passare questo numero di flusso al metodo [**IWMReaderAdvanced::SetReceiveStreamSamples del**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) lettore. Questo metodo informa il lettore di fornire esempi compressi, anziché decodificarli. Gli esempi verranno recapitati all'applicazione tramite il metodo di callback [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) dell'applicazione.

    È necessario ottenere informazioni sul codec per ogni flusso letto non compresso e aggiungerlo all'intestazione prima della trasmissione. Per ottenere le informazioni sul codec, chiamare [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) per enumerare i codec associati al file nel lettore. Selezionare le informazioni sul codec che corrispondono alla configurazione del flusso. Impostare quindi le informazioni sul codec nel writer chiamando [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando le informazioni ottenute dal lettore.

5.  Dopo aver impostato il profilo nel writer, chiamare [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) nel writer per ottenere il numero di input. Per ogni input, chiamare [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) con il valore **NULL.** Ciò indica all'oggetto writer che l'applicazione consegnerà esempi compressi, quindi il writer non deve usare codec per comprimere i dati. Assicurarsi di chiamare **SetInputProps** prima di chiamare **BeginWriting.**
6.  Facoltativamente, copiare gli attributi dei metadati dal lettore al writer
7.  Poiché gli esempi del lettore sono già compressi, usare il metodo [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) per scrivere gli esempi, anziché **il metodo WriteSample.** Il **metodo WriteStreamSample** ignora le consuete procedure di compressione dell'oggetto writer.
8.  Quando il lettore raggiunge la fine del file, invia una notifica EOF WMT \_ all'applicazione.

Inoltre, l'applicazione deve guidare l'orologio sull'oggetto lettore, in modo che il lettore estrae i dati dal file il più rapidamente possibile. A tale scopo, chiamare il metodo [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) sul lettore, con il valore **TRUE.** Dopo che il lettore ha inviato la notifica WMT STARTED, chiamare \_ [**IWMReaderAdvanced::D eliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) e specificare l'intervallo di tempo che il lettore deve recapitare. Al termine della lettura di questo intervallo di tempo, il lettore chiama il metodo di callback [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) dell'applicazione. L'applicazione deve chiamare **di nuovo DeliverTime** per leggere l'intervallo di tempo successivo. Ad esempio, per leggere dal file a intervalli di un secondo:


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

[**Invio di dati ASF in rete**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




