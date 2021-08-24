---
title: Aggiunta di sink al writer
description: Aggiunta di sink al writer
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Advanced Systems Format (ASF), aggiunta di sink al writer
- ASF (Advanced Systems Format), aggiunta di sink al writer
- Advanced Systems Format (ASF), sink
- ASF (Advanced Systems Format), sink
- Advanced Systems Format (ASF), sink writer
- ASF (Advanced Systems Format),sink writer
- sink, aggiunta al writer
- sink writer, aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca64b412dd83e9bbba1d8de66b2aef335573c9e50073c2afe898fed0c34761b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810021"
---
# <a name="adding-sinks-to-the-writer"></a>Aggiunta di sink al writer

I sink del writer sono oggetti separati dal writer e devono essere aggiunti al writer per essere usati. Se si scrive in un file, è sufficiente chiamare [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), che configura automaticamente il sink del file. In caso contrario, per aggiungere un sink al writer, chiamare il [**metodo IWMWriterAdvanced::AddSink.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) **AddSink** richiede un puntatore [**all'interfaccia IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) del sink.

Dopo aver terminato di usare un sink, è necessario chiuderlo chiamando il metodo appropriato, a seconda del tipo di sink, e quindi rimuoverlo dal writer chiamando [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).

Nell'esempio di codice seguente viene illustrato come creare un sink di file writer e aggiungerlo al writer. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice.](using-the-code-examples.md)


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero di messaggi di errore da un sink**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




