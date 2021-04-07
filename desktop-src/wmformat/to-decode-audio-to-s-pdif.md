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
# <a name="to-decode-audio-to-spdif"></a><span data-ttu-id="4881d-112">Per decodificare l'audio in S/PDIF</span><span class="sxs-lookup"><span data-stu-id="4881d-112">To Decode Audio to S/PDIF</span></span>

<span data-ttu-id="4881d-113">L'audio codificato con il codec Windows Media Audio 9 Professional può essere decodificato in formato di interconnessione digitale Sony/Philips (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="4881d-113">Audio encoded with the Windows Media Audio 9 Professional codec can be decoded to Sony/Philips Digital Interconnect Format (S/PDIF).</span></span> <span data-ttu-id="4881d-114">Per generare l'output S/PDIF, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="4881d-114">To generate S/PDIF output, perform the following steps:</span></span>

1.  <span data-ttu-id="4881d-115">Aprire un file contenente un flusso Windows Media Audio 9 Professional chiamando il metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="4881d-115">Open a file that contains a Windows Media Audio 9 Professional stream by calling the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span>
2.  <span data-ttu-id="4881d-116">Identificare il numero di output del flusso desiderato.</span><span class="sxs-lookup"><span data-stu-id="4881d-116">Identify the output number of the stream that you want.</span></span> <span data-ttu-id="4881d-117">Per ulteriori informazioni, vedere [per identificare i numeri di output](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="4881d-117">For more information, see [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="4881d-118">Chiamare il metodo [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) per configurare l'output S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="4881d-118">Call the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method to configure S/PDIF output.</span></span> <span data-ttu-id="4881d-119">Usare g \_ wszEnableWMAProSPDIFOutput per il nome dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="4881d-119">Use g\_wszEnableWMAProSPDIFOutput for the setting name.</span></span> <span data-ttu-id="4881d-120">Il tipo di dati è **WMT di \_ tipo \_ bool**; impostare il valore su **true** per abilitare l'output S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="4881d-120">The data type is **WMT\_TYPE\_BOOL**; set the value to **TRUE** to enable S/PDIF output.</span></span>
4.  <span data-ttu-id="4881d-121">Ottenere l'interfaccia delle proprietà di output ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) del formato di output desiderato chiamando il metodo [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) .</span><span class="sxs-lookup"><span data-stu-id="4881d-121">Get the output properties interface ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) of the desired output format by calling the [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) method.</span></span> <span data-ttu-id="4881d-122">Per ulteriori informazioni sull'enumerazione dei formati di output, vedere [assegnazione di formati di output](assigning-output-formats.md).</span><span class="sxs-lookup"><span data-stu-id="4881d-122">For more information about enumerating output formats, see [Assigning Output Formats](assigning-output-formats.md).</span></span>
5.  <span data-ttu-id="4881d-123">Impostare il formato di output chiamando il metodo [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) .</span><span class="sxs-lookup"><span data-stu-id="4881d-123">Set the output format by calling the [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) method.</span></span> <span data-ttu-id="4881d-124">Passare un puntatore all'interfaccia **IWMOutputMediaProps** ottenuta nel passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="4881d-124">Pass in a pointer to the **IWMOutputMediaProps** interface obtained in step 4.</span></span>
6.  <span data-ttu-id="4881d-125">Apportare qualsiasi altra modifica alla configurazione e iniziare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="4881d-125">Make any other configuration changes and begin playback.</span></span>

> [!Note]  
> <span data-ttu-id="4881d-126">È possibile eseguire i passaggi precedenti sul lettore sincrono usando i metodi corrispondenti dell'interfaccia [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="4881d-126">You can perform the preceding steps on the synchronous reader by using the corresponding methods of the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

 

<span data-ttu-id="4881d-127">Il codice di esempio seguente illustra come impostare un flusso audio per l'output di audio come dati S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="4881d-127">The following example code demonstrates how to set an audio stream to output audio as S/PDIF data.</span></span> <span data-ttu-id="4881d-128">Questa funzione presuppone che un file sia già stato caricato nel lettore e che sia stato identificato il numero di output.</span><span class="sxs-lookup"><span data-stu-id="4881d-128">This function assumes that a file has already been loaded in the reader and that the output number has been identified.</span></span> <span data-ttu-id="4881d-129">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="4881d-129">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4881d-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4881d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4881d-131">**Argomenti avanzati**</span><span class="sxs-lookup"><span data-stu-id="4881d-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="4881d-132">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="4881d-132">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="4881d-133">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="4881d-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="4881d-134">**Interfaccia IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="4881d-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="4881d-135">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="4881d-135">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




