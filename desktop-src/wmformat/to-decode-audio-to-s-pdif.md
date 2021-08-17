---
title: Per decodificare l'audio in S/PDIF
description: Per decodificare l'audio in S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media Format SDK, decodifica audio in S/PDIF
- Windows Media Format SDK, Rtf/Philips Digital Interconnect Format (S/PDIF)
- Advanced Systems Format (ASF), decodifica audio in S/PDIF
- ASF (Advanced Systems Format), decodifica audio in S/PDIF
- Advanced Systems Format (ASF), Interconnect Format (S/PDIF)
- ASF (Advanced Systems Format), Interconnect Format (S/PDIF)
- Formato S/PDIF (Digital Interconnect Format), decodifica audio
- S/PDIF (Formato di interconnessione digitale Disambiezione digitale Disarticolata/Philips),decodifica dell'audio
- decodifica di audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bd4fdbafd5685882f34b698c0745b998b6cee2e63514041db17fed2195346c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845589"
---
# <a name="to-decode-audio-to-spdif"></a>Per decodificare l'audio in S/PDIF

L'audio codificato con il codec Windows Media Audio 9 Professional può essere decodificato in formato S/PDIF (Digital Interconnect Format) Di Utf/Philips. Per generare l'output S/PDIF, seguire questa procedura:

1.  Aprire un file che contiene un flusso Windows Media Audio 9 Professional chiamando il [**metodo IWMReader::Open.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
2.  Identificare il numero di output del flusso desiderato. Per altre informazioni, vedere [Per identificare i numeri di output.](to-identify-output-numbers.md)
3.  Chiamare il [**metodo IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) per configurare l'output S/PDIF. Usare g \_ wszEnableWMAProSPDIFOutput come nome dell'impostazione. Il tipo di dati **è WMT \_ TYPE \_ BOOL.** Impostare il valore su **TRUE** per abilitare l'output S/PDIF.
4.  Ottenere l'interfaccia delle proprietà di output ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) del formato di output desiderato chiamando il [**metodo IWMReader::GetOutputFormat.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) Per altre informazioni sull'enumerazione dei formati di output, vedere [Assegnazione di formati di output.](assigning-output-formats.md)
5.  Impostare il formato di output chiamando il [**metodo IWMReader::SetOutputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) Passare un puntatore **all'interfaccia IWMOutputMediaProps** ottenuta nel passaggio 4.
6.  Apportare altre modifiche alla configurazione e avviare la riproduzione.

> [!Note]  
> È possibile eseguire i passaggi precedenti sul lettore sincrono usando i metodi corrispondenti [**dell'interfaccia IWMSyncReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)

 

Il codice di esempio seguente illustra come impostare un flusso audio per l'output audio come dati S/PDIF. Questa funzione presuppone che un file sia già stato caricato nel lettore e che il numero di output sia stato identificato. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice.](using-the-code-examples.md)


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

 

 




