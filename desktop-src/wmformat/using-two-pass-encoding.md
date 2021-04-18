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
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a><span data-ttu-id="51a38-111">Uso della codifica Two-Pass (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="51a38-111">Using Two-Pass Encoding (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="51a38-112">Alcuni codec supportano la codifica a due passaggi per determinati formati.</span><span class="sxs-lookup"><span data-stu-id="51a38-112">Some codecs support two-pass encoding for certain formats.</span></span> <span data-ttu-id="51a38-113">In alcuni casi, per un codec è necessario che un formato specificato venga codificato utilizzando due sessioni.</span><span class="sxs-lookup"><span data-stu-id="51a38-113">In some cases, a codec requires that a specified format be encoded using two passes.</span></span> <span data-ttu-id="51a38-114">Quando si usa la codifica a due passaggi, si inviano gli esempi per il flusso al codec prima del passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="51a38-114">When two-pass encoding is used, you send the samples for the stream to the codec before the encoding pass.</span></span> <span data-ttu-id="51a38-115">Il codec analizza gli esempi e configura il passaggio di codifica basato sull'analisi.</span><span class="sxs-lookup"><span data-stu-id="51a38-115">The codec analyzes the samples and configures the encoding pass based on the analysis.</span></span> <span data-ttu-id="51a38-116">Ciò comporta un file codificato in modo più efficiente.</span><span class="sxs-lookup"><span data-stu-id="51a38-116">This results in a more efficiently encoded file.</span></span>

<span data-ttu-id="51a38-117">Per determinare se un codec supporta la codifica One-Pass o due passaggi, o entrambi, per un determinato formato, chiamare [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) con g \_ wszNumPasses e il valore appropriato, quindi enumerare i formati per verificare se viene restituito quello desiderato.</span><span class="sxs-lookup"><span data-stu-id="51a38-117">To determine whether a codec supports one-pass encoding, or two-pass, or both, for a given format, call [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) with g\_wszNumPasses and the appropriate value, and then enumerate the formats to see if the one you want is returned.</span></span> <span data-ttu-id="51a38-118">Per ulteriori informazioni sui codec Windows Media che supportano la codifica a due passaggi, vedere [scelta di un metodo di codifica](choosing-an-encoding-method.md).</span><span class="sxs-lookup"><span data-stu-id="51a38-118">For more information about the Windows Media codecs that support two-pass encoding, see [Choosing an Encoding Method](choosing-an-encoding-method.md).</span></span>

<span data-ttu-id="51a38-119">È possibile usare la codifica a due passaggi con Windows Media Format SDK chiamando i metodi dell'interfaccia [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="51a38-119">You can use two-pass encoding with the Windows Media Format SDK by calling methods of the [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) interface.</span></span>

<span data-ttu-id="51a38-120">Nei casi in cui è richiesta la codifica a due passaggi per un particolare formato, ma l'applicazione non riesce a eseguire un passaggio di pre-elaborazione, la prima chiamata a [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) avrà esito negativo con il numero di \_ \_ passaggi num E non validi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="51a38-120">In cases where two-pass encoding is required for a particular format, but the application fails to perform a preprocessing pass, the first call to [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) will fail with NS\_E\_INVALID\_NUM\_PASSES.</span></span>

<span data-ttu-id="51a38-121">La funzione di esempio seguente illustra come eseguire la codifica a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="51a38-121">The following example function demonstrates how to perform two-pass encoding.</span></span> <span data-ttu-id="51a38-122">Questa funzione viene chiamata dopo che il writer è stato impostato con un profilo e avviato.</span><span class="sxs-lookup"><span data-stu-id="51a38-122">This function is called after the writer has been set with a profile and started.</span></span> <span data-ttu-id="51a38-123">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="51a38-123">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="51a38-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51a38-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a38-125">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="51a38-125">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




