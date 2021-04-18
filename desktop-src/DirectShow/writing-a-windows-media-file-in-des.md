---
description: Scrittura di un file di Windows Media in DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Scrittura di un file di Windows Media in DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320759"
---
# <a name="writing-a-windows-media-file-in-des"></a><span data-ttu-id="18a16-103">Scrittura di un file di Windows Media in DES</span><span class="sxs-lookup"><span data-stu-id="18a16-103">Writing a Windows Media File in DES</span></span>

<span data-ttu-id="18a16-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="18a16-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="18a16-105">In questa sezione viene descritto come scrivere un file Windows Media usando i [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="18a16-105">This section describes how to write a Windows Media file using [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18a16-106">Non usare il motore di rendering intelligente per scrivere file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="18a16-106">Do not use the Smart Render Engine to write Windows Media files.</span></span> <span data-ttu-id="18a16-107">Usare sempre il motore di rendering di base (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="18a16-107">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

 

<span data-ttu-id="18a16-108">Per scrivere un file di Windows Media, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="18a16-108">To write a Windows Media file, do the following:</span></span>

1.  <span data-ttu-id="18a16-109">Chiamare il **sito Web** sul motore di rendering, con un puntatore al provider di chiavi.</span><span class="sxs-lookup"><span data-stu-id="18a16-109">Call **SetSite** on the render engine, with a pointer to your key provider.</span></span>
2.  <span data-ttu-id="18a16-110">Compilare il front-end del grafo.</span><span class="sxs-lookup"><span data-stu-id="18a16-110">Build the front end of the graph.</span></span> <span data-ttu-id="18a16-111">Vedere [rendering di un progetto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="18a16-111">(See [Rendering a Project](rendering-a-project.md).)</span></span>
3.  <span data-ttu-id="18a16-112">Creare il filtro [WM ASF Writer](wm-asf-writer-filter.md) e aggiungerlo al grafico.</span><span class="sxs-lookup"><span data-stu-id="18a16-112">Create the [WM ASF Writer](wm-asf-writer-filter.md) filter and add it to the graph.</span></span>
4.  <span data-ttu-id="18a16-113">Per impostare il nome del file, utilizzare l'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) sul filtro WM ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="18a16-113">Use the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface on the WM ASF Writer filter to set the file name.</span></span>
5.  <span data-ttu-id="18a16-114">Configurare il writer ASF WM per l'utilizzo di un profilo Windows Media.</span><span class="sxs-lookup"><span data-stu-id="18a16-114">Configure the WM ASF Writer to use a Windows Media profile.</span></span> <span data-ttu-id="18a16-115">Ogni profilo ha un numero predefinito di flussi.</span><span class="sxs-lookup"><span data-stu-id="18a16-115">Each profile has a predefined number of streams.</span></span> <span data-ttu-id="18a16-116">È necessario scegliere un profilo che corrisponda ai gruppi nel progetto.</span><span class="sxs-lookup"><span data-stu-id="18a16-116">You must choose a profile that matches the groups in your project.</span></span>

    <span data-ttu-id="18a16-117">L'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contiene alcuni metodi diversi per l'impostazione del profilo.</span><span class="sxs-lookup"><span data-stu-id="18a16-117">The [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface contains a few different methods for setting the profile.</span></span> <span data-ttu-id="18a16-118">Ad esempio, il metodo **ConfigureFilterUsingProfileGuid** specifica un profilo di sistema come GUID.</span><span class="sxs-lookup"><span data-stu-id="18a16-118">For example, the **ConfigureFilterUsingProfileGuid** method specifies a system profile as a GUID.</span></span> <span data-ttu-id="18a16-119">In alternativa, è possibile utilizzare i metodi Windows Media Format per ottenere un puntatore **IWMProfile** , quindi chiamare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span><span class="sxs-lookup"><span data-stu-id="18a16-119">Or, you can use Windows Media Format methods to get an **IWMProfile** pointer and then call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span></span> <span data-ttu-id="18a16-120">Per ulteriori informazioni, vedere [Configuring the ASF Writer](configuring-the-asf-writer.md).</span><span class="sxs-lookup"><span data-stu-id="18a16-120">For more information, see [Configuring the ASF Writer](configuring-the-asf-writer.md).</span></span>

6.  <span data-ttu-id="18a16-121">Connettere il front-end al writer ASF.</span><span class="sxs-lookup"><span data-stu-id="18a16-121">Connect the front end to the ASF Writer.</span></span> <span data-ttu-id="18a16-122">Il front-end del grafico contiene un pin di output per ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="18a16-122">The front end of the graph contains one output pin for each group.</span></span> <span data-ttu-id="18a16-123">Supponendo che sia stato specificato un profilo compatibile, il writer ASF deve avere un set di pin di input corrispondente.</span><span class="sxs-lookup"><span data-stu-id="18a16-123">Assuming that you specified a compatible profile, the ASF Writer should have a matching set of input pins.</span></span> <span data-ttu-id="18a16-124">Connettere ogni pin di output al pin di input corrispondente.</span><span class="sxs-lookup"><span data-stu-id="18a16-124">Connect each output pin to the corresponding input pin.</span></span> <span data-ttu-id="18a16-125">Il modo più semplice per eseguire questa operazione è usare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="18a16-125">The easiest way to do this is using the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="18a16-126">Per prima cosa, creare una nuova istanza del [Generatore di grafici di acquisizione](capture-graph-builder.md) e inizializzarla con un puntatore a gestione grafico dei filtri:</span><span class="sxs-lookup"><span data-stu-id="18a16-126">First, create a new instance of the [Capture Graph Builder](capture-graph-builder.md) and initialize it with a pointer to the Filter Graph Manager:</span></span>

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    <span data-ttu-id="18a16-127">Recuperare quindi il pin di output per ogni gruppo chiamando il metodo [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="18a16-127">Next, retrieve the output pin for each group by calling the [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) method.</span></span> <span data-ttu-id="18a16-128">Chiamare **RenderStream** per connettere il PIN al writer ASF:</span><span class="sxs-lookup"><span data-stu-id="18a16-128">Call **RenderStream** to connect the pin to the ASF Writer:</span></span>

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a><span data-ttu-id="18a16-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18a16-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18a16-130">Uso di Windows Media con i servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="18a16-130">Using Windows Media With DirectShow Editing Services</span></span>](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



