---
title: Uso della codifica Two-Pass (Windows Media Format 11 SDK)
description: Uso della codifica Two-Pass
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- ASF (Advanced Systems Format), codifica a due passaggi
- ASF (Advanced Systems Format), codifica a due passaggi
- codifica a due passaggi, informazioni
- codifica a 2 passaggi, informazioni
- codec, codifica a due passaggi
- codifica a due passaggi, interfaccia IWMWriterPreprocess
- codifica a 2 passaggi, interfaccia IWMWriterPreprocess
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3794856f47c1656cc53006268c41a063cdde96
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517337"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Uso della codifica Two-Pass (Windows Media Format 11 SDK)

Alcuni codec supportano la codifica a due passaggi per determinati formati. In alcuni casi, per un codec è necessario che un formato specificato venga codificato utilizzando due sessioni. Quando si usa la codifica a due passaggi, si inviano gli esempi per il flusso al codec prima del passaggio di codifica. Il codec analizza gli esempi e configura il passaggio di codifica basato sull'analisi. Ciò comporta un file codificato in modo più efficiente.

Per determinare se un codec supporta la codifica One-Pass o due passaggi, o entrambi, per un determinato formato, chiamare [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) con g \_ wszNumPasses e il valore appropriato, quindi enumerare i formati per verificare se viene restituito quello desiderato. Per ulteriori informazioni sui codec Windows Media che supportano la codifica a due passaggi, vedere [scelta di un metodo di codifica](choosing-an-encoding-method.md).

È possibile usare la codifica a due passaggi con Windows Media Format SDK chiamando i metodi dell'interfaccia [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .

Nei casi in cui è richiesta la codifica a due passaggi per un particolare formato, ma l'applicazione non riesce a eseguire un passaggio di pre-elaborazione, la prima chiamata a [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) avrà esito negativo con il numero di \_ \_ passaggi num E non validi \_ \_ .

La funzione di esempio seguente illustra come eseguire la codifica a due passaggi. Questa funzione viene chiamata dopo che il writer è stato impostato con un profilo e avviato. Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


```C++
HRESULT PreProcess(IWMWriter* pWriter, DWORD dwInputNum)
{
    HRESULT hr        = S_OK;
    DWORD   dwMaxPass = 0;

    IWMWriterPreprocess* pPreProc = NULL;

    // Get the writer preprocessor interface.
    hr = pWriter->QueryInterface(IID_IWMWriterPreprocess, 
                                 (void**) &pPreProc);
    GOTO_EXIT_IF_FAILED(hr);

    // Check that the input can be preprocessed.
    hr = pPreProc->GetMaxPreprocessingPasses(dwInputNum,0, &dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    if(dwMaxPass == 0)
    {
        hr = NS_E_INVALID_REQUEST;
        goto Exit;
    }

    // Set the number of preprocessing passes to the maximum.
    hr = pPreProc->SetNumPreprocessingPasses(dwInputNum, 0, dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    // Call BeginWriting before calling BeginPreprocessingPass
    hr = pWriter->BeginWriting();

    // Start preprocessing the first pass.
    hr = pPreProc->BeginPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: Make repeated calls to pPreProc->PreprocessSample to
    // preprocess all the samples in the stream.

    // End preprocessing.
    hr = pPreProc->EndPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: If the maximum number of preprocessing passes is greater
    // than one, repeat the preprocessing steps for each pass.

Exit:
    SAFE_RELEASE(pPreProc);
    Return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




