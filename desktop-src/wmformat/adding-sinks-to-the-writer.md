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
# <a name="adding-sinks-to-the-writer"></a><span data-ttu-id="37b6f-111">Aggiunta di sink al writer</span><span class="sxs-lookup"><span data-stu-id="37b6f-111">Adding Sinks to the Writer</span></span>

<span data-ttu-id="37b6f-112">I sink del writer sono oggetti separati dal writer e devono essere aggiunti al writer da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="37b6f-112">Writer sinks are separate objects from the writer and must be added to the writer to be used.</span></span> <span data-ttu-id="37b6f-113">Se si scrive in un file, è possibile semplicemente chiamare [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), che configurerà automaticamente il sink di file.</span><span class="sxs-lookup"><span data-stu-id="37b6f-113">If you are writing to a file, you can simply call [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), which will set up the file sink automatically.</span></span> <span data-ttu-id="37b6f-114">In caso contrario, per aggiungere un sink al writer, chiamare il metodo [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) .</span><span class="sxs-lookup"><span data-stu-id="37b6f-114">Otherwise, to add a sink to the writer, call the [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) method.</span></span> <span data-ttu-id="37b6f-115">**AddSink** richiede un puntatore all'interfaccia [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) del sink.</span><span class="sxs-lookup"><span data-stu-id="37b6f-115">**AddSink** requires a pointer to the [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) interface of the sink.</span></span>

<span data-ttu-id="37b6f-116">Al termine dell'utilizzo di un sink, è necessario chiuderlo chiamando il metodo appropriato, a seconda del tipo di sink, quindi rimuoverlo dal writer chiamando [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span><span class="sxs-lookup"><span data-stu-id="37b6f-116">When you are finished using a sink, you should close it by calling the appropriate method, depending on the type of sink, and then remove it from the writer by calling [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span></span>

<span data-ttu-id="37b6f-117">Nell'esempio di codice seguente viene illustrato come creare un sink di file del writer e aggiungerlo al writer.</span><span class="sxs-lookup"><span data-stu-id="37b6f-117">The following example code shows how to create a writer file sink and add it to the writer.</span></span> <span data-ttu-id="37b6f-118">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="37b6f-118">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="37b6f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37b6f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37b6f-120">**Recupero di messaggi di errore da un sink**</span><span class="sxs-lookup"><span data-stu-id="37b6f-120">**Getting Error Messages from a Sink**</span></span>](getting-error-messages-from-a-sink.md)
</dt> <dt>

[<span data-ttu-id="37b6f-121">**Interfaccia IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="37b6f-121">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="37b6f-122">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="37b6f-122">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




