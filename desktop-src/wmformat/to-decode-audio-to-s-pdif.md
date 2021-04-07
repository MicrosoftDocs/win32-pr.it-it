---
title: Per decodificare l'audio in S/PDIF
description: Per decodificare l'audio in S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media Format SDK, decodifica audio in S/PDIF
- Windows Media Format SDK, formato di interconnessione digitale Sony/Philips (S/PDIF)
- ASF (Advanced Systems Format), decodifica audio in S/PDIF
- ASF (Advanced Systems Format), decodifica audio in S/PDIF
- Formato Advanced Systems Format (ASF), Sony/Philips Digital Interconnect (S/PDIF)
- ASF (Advanced Systems Format), formato di interconnessione digitale Sony/Philips (S/PDIF)
- Formato di interconnessione digitale Sony/Philips (S/PDIF), decodifica audio
- S/PDIF (formato di interconnessione digitale Sony/Philips), decodifica audio
- decodifica audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724101"
---
# <a name="to-decode-audio-to-spdif"></a>Per decodificare l'audio in S/PDIF

L'audio codificato con il codec Windows Media Audio 9 Professional può essere decodificato in formato di interconnessione digitale Sony/Philips (S/PDIF). Per generare l'output S/PDIF, seguire questa procedura:

1.  Aprire un file contenente un flusso Windows Media Audio 9 Professional chiamando il metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .
2.  Identificare il numero di output del flusso desiderato. Per ulteriori informazioni, vedere [per identificare i numeri di output](to-identify-output-numbers.md).
3.  Chiamare il metodo [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) per configurare l'output S/PDIF. Usare g \_ wszEnableWMAProSPDIFOutput per il nome dell'impostazione. Il tipo di dati è **WMT di \_ tipo \_ bool**; impostare il valore su **true** per abilitare l'output S/PDIF.
4.  Ottenere l'interfaccia delle proprietà di output ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) del formato di output desiderato chiamando il metodo [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) . Per ulteriori informazioni sull'enumerazione dei formati di output, vedere [assegnazione di formati di output](assigning-output-formats.md).
5.  Impostare il formato di output chiamando il metodo [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) . Passare un puntatore all'interfaccia **IWMOutputMediaProps** ottenuta nel passaggio 4.
6.  Apportare qualsiasi altra modifica alla configurazione e iniziare la riproduzione.

> [!Note]  
> È possibile eseguire i passaggi precedenti sul lettore sincrono usando i metodi corrispondenti dell'interfaccia [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

 

Il codice di esempio seguente illustra come impostare un flusso audio per l'output di audio come dati S/PDIF. Questa funzione presuppone che un file sia già stato caricato nel lettore e che sia stato identificato il numero di output. Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaccia IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




