---
title: Aggiunta di sink al writer
description: Aggiunta di sink al writer
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- ASF (Advanced Systems Format), aggiunta di sink al writer
- ASF (Advanced Systems Format), aggiunta di sink al writer
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- ASF (Advanced Systems Format), sink writer
- ASF (formato avanzato dei sistemi), sink writer
- sink, aggiunta al writer
- sink writer, aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398586"
---
# <a name="adding-sinks-to-the-writer"></a>Aggiunta di sink al writer

I sink del writer sono oggetti separati dal writer e devono essere aggiunti al writer da utilizzare. Se si scrive in un file, è possibile semplicemente chiamare [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), che configurerà automaticamente il sink di file. In caso contrario, per aggiungere un sink al writer, chiamare il metodo [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) . **AddSink** richiede un puntatore all'interfaccia [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) del sink.

Al termine dell'utilizzo di un sink, è necessario chiuderlo chiamando il metodo appropriato, a seconda del tipo di sink, quindi rimuoverlo dal writer chiamando [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).

Nell'esempio di codice seguente viene illustrato come creare un sink di file del writer e aggiungerlo al writer. Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


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

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




