---
description: Acquisizione di video in un file di Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Acquisizione di video in un file di Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234500"
---
# <a name="capturing-video-to-a-windows-media-file"></a><span data-ttu-id="e0e0b-103">Acquisizione di video in un file di Windows Media</span><span class="sxs-lookup"><span data-stu-id="e0e0b-103">Capturing Video to a Windows Media File</span></span>

<span data-ttu-id="e0e0b-104">Per acquisire video e codificarlo in un file Windows Media Video (WMV), connettere il pin di acquisizione al filtro di [writer ASF WM](wm-asf-writer-filter.md) , come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="e0e0b-104">To capture video and encode it to a Windows Media Video (WMV) file, connect the capture pin to the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the following diagram.</span></span>

![grafico di acquisizione Windows Media](images/vidcap03.png)

<span data-ttu-id="e0e0b-106">Il modo più semplice per creare questo grafico è specificando MEDIASUBTYPE \_ ASF nel metodo [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :</span><span class="sxs-lookup"><span data-stu-id="e0e0b-106">The easiest way to build this graph is by specifing MEDIASUBTYPE\_Asf in the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



<span data-ttu-id="e0e0b-107">Il valore MEDIASUBTYPE \_ ASF indica al generatore del grafico di acquisizione di usare il filtro del writer ASF WM come sink di file.</span><span class="sxs-lookup"><span data-stu-id="e0e0b-107">The value MEDIASUBTYPE\_Asf tells the Capture Graph Builder to use the WM ASF Writer filter as the file sink.</span></span> <span data-ttu-id="e0e0b-108">Il generatore del grafico di acquisizione crea il filtro, lo aggiunge al grafo e chiama [**IFileSinkFilter:: myFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) per impostare il nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="e0e0b-108">The Capture Graph Builder creates the filter, adds it to the graph, and calls [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) to set the name of the output file.</span></span> <span data-ttu-id="e0e0b-109">Restituisce un puntatore al filtro come parametro in uscita (</span><span class="sxs-lookup"><span data-stu-id="e0e0b-109">It returns a pointer to the filter as an outgoing parameter (</span></span>


```
pASFWriter
```



<span data-ttu-id="e0e0b-110">Nell'esempio precedente).</span><span class="sxs-lookup"><span data-stu-id="e0e0b-110">in the previous example).</span></span>

<span data-ttu-id="e0e0b-111">Usare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) nel writer ASF WM per impostare il profilo Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e0e0b-111">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface on the WM ASF Writer to set the Windows Media profile.</span></span> <span data-ttu-id="e0e0b-112">È necessario eseguire questa operazione prima di connettere i pin del writer ASF WM.</span><span class="sxs-lookup"><span data-stu-id="e0e0b-112">You must do this before you connect any pins on the WM ASF Writer.</span></span>


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



<span data-ttu-id="e0e0b-113">Per ulteriori informazioni sull'impostazione del profilo, vedere [creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="e0e0b-113">For more information about setting the profile, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="e0e0b-114">Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di acquisizione al writer ASF:</span><span class="sxs-lookup"><span data-stu-id="e0e0b-114">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the capture filter to the ASF Writer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



<span data-ttu-id="e0e0b-115">Ogni pin di input nel filtro WM ASF Writer corrisponde a un flusso nel profilo Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e0e0b-115">Each input pin on the WM ASF Writer filter corresponds to a stream in the Windows Media profile.</span></span> <span data-ttu-id="e0e0b-116">È necessario connettere ogni pin, in modo che il contenuto del file corrisponda a quello del profilo.</span><span class="sxs-lookup"><span data-stu-id="e0e0b-116">You must connect every pin, so that the file content matches the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0e0b-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0e0b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0e0b-118">Acquisizione di video in un file</span><span class="sxs-lookup"><span data-stu-id="e0e0b-118">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



