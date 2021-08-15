---
title: Uso Two-Pass codifica (Windows Media Format 11 SDK)
description: Uso Two-Pass codifica
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- Advanced Systems Format (ASF), codifica a due passi
- ASF (Advanced Systems Format), codifica a due passi
- codifica a due passi, informazioni
- codifica a 2 passi, informazioni
- codec, codifica a due passi
- codifica a due passi, interfaccia IWMWriterPreprocess
- Codifica a 2 passi, interfaccia IWMWriterPreprocess
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0683af636197b3f8116fca4dea85ce15609d2c99b0d9e0c11dfe0a2662a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653836"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Uso Two-Pass codifica (Windows Media Format 11 SDK)

Alcuni codec supportano la codifica a due passi per determinati formati. In alcuni casi, un codec richiede che un formato specificato sia codificato usando due passaggi. Quando si usa la codifica a due passi, si inviano gli esempi per il flusso al codec prima del passaggio di codifica. Il codec analizza gli esempi e configura il passaggio di codifica in base all'analisi. Ciò comporta un file codificato in modo più efficiente.

Per determinare se un codec supporta la codifica a un passaggio, a due passi o entrambi, per un determinato formato, chiamare [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) con g wszNumPasses e il valore appropriato, quindi enumerare i formati per verificare se viene restituito quello \_ desiderato. Per altre informazioni sull'Windows codec multimediali che supportano la codifica a due passi, vedere [Scelta di un metodo di codifica.](choosing-an-encoding-method.md)

È possibile usare la codifica a due passi con Windows Media Format SDK chiamando i metodi [**dell'interfaccia IWMWriterPreprocess.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess)

Nei casi in cui la codifica a due passaggi è necessaria per un formato specifico, ma l'applicazione non riesce a eseguire un passaggio di pre-elaborazione, la prima chiamata a [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) avrà esito negativo con NS \_ E INVALID NUM \_ \_ \_ PASSES.

La funzione di esempio seguente illustra come eseguire la codifica a due passaggi. Questa funzione viene chiamata dopo che il writer è stato impostato con un profilo e avviato. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice.](using-the-code-examples.md)


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

 

 




