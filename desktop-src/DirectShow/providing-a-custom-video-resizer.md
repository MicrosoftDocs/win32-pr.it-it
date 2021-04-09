---
description: Creazione di una ridisposizione video personalizzata
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Creazione di una ridisposizione video personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124107"
---
# <a name="providing-a-custom-video-resizer"></a><span data-ttu-id="105dd-103">Creazione di una ridisposizione video personalizzata</span><span class="sxs-lookup"><span data-stu-id="105dd-103">Providing a Custom Video Resizer</span></span>

<span data-ttu-id="105dd-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="105dd-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

> [!Note]  
> <span data-ttu-id="105dd-105">Questa funzionalità richiede DirectX 9,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="105dd-105">This feature requires DirectX 9.0 or later.</span></span>

 

<span data-ttu-id="105dd-106">Quando [DirectShow editing Services](directshow-editing-services.md) (des) ridimensiona una clip di origine video, il comportamento predefinito è *StretchBlt*, che è veloce ma non con anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="105dd-106">When [DirectShow Editing Services](directshow-editing-services.md) (DES) resizes a video source clip, the default behavior is a *StretchBlt*, which is fast but not anti-aliased.</span></span> <span data-ttu-id="105dd-107">È possibile modificare il comportamento di ridimensionamento implementando un oggetto Resizer personalizzato come filtro di trasformazione DirectShow.</span><span class="sxs-lookup"><span data-stu-id="105dd-107">You can change the resizing behavior by implementing a custom resizer as a DirectShow transform filter.</span></span> <span data-ttu-id="105dd-108">Il filtro deve esporre l'interfaccia [**IResize**](iresize.md) , che consente a des di specificare le dimensioni del video di input e di output.</span><span class="sxs-lookup"><span data-stu-id="105dd-108">The filter must expose the [**IResize**](iresize.md) interface, which enables DES to specify the input and output video size.</span></span> <span data-ttu-id="105dd-109">Per informazioni sulla scrittura di un filtro di trasformazione, vedere [scrittura di filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="105dd-109">For information about writing a transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span> <span data-ttu-id="105dd-110">La classe base **CTransformFilter** è consigliata come punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="105dd-110">The **CTransformFilter** base class is recommended as the starting point.</span></span> <span data-ttu-id="105dd-111">Quando si implementa il filtro, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="105dd-111">When you implement the filter, note the following:</span></span>

-   <span data-ttu-id="105dd-112">Supportare l'interfaccia **IResize** sul filtro (non sui pin).</span><span class="sxs-lookup"><span data-stu-id="105dd-112">Support the **IResize** interface on the filter (not the pins).</span></span>
-   <span data-ttu-id="105dd-113">Il filtro deve accettare solo formati [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (Format \_ videoinfo).</span><span class="sxs-lookup"><span data-stu-id="105dd-113">The filter should accept only [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) formats (FORMAT\_VideoInfo).</span></span> <span data-ttu-id="105dd-114">Rifiutare altri tipi di formato.</span><span class="sxs-lookup"><span data-stu-id="105dd-114">Reject other format types.</span></span>
-   <span data-ttu-id="105dd-115">Il formato video di DES può essere qualsiasi tipo RGB non compresso, incluso RGB a 32 bit con Alpha (MEDIASUBTYPE \_ ARGB32).</span><span class="sxs-lookup"><span data-stu-id="105dd-115">The video format from DES may be any uncompressed RGB type, including 32-bit RGB with alpha (MEDIASUBTYPE\_ARGB32).</span></span> <span data-ttu-id="105dd-116">Il filtro può rifiutare in modo sicuro i formati con **biHeight** < 0.</span><span class="sxs-lookup"><span data-stu-id="105dd-116">Your filter can safely reject formats with **biHeight** < 0.</span></span>
-   <span data-ttu-id="105dd-117">Prima di connettere il pin di output del filtro, il motore di rendering chiama [**IResize::p UT \_ mediaType**](iresize-put-mediatype.md) per impostare il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="105dd-117">Before the Render Engine connects the filter's output pin, it calls [**IResize::put\_MediaType**](iresize-put-mediatype.md) to set the output type.</span></span> <span data-ttu-id="105dd-118">Può anche chiamare [**IResize::p \_ dimensioni UT**](iresize-put-size.md) per modificare le dimensioni di output.</span><span class="sxs-lookup"><span data-stu-id="105dd-118">It may also call [**IResize::put\_Size**](iresize-put-size.md) to adjust the output size.</span></span> <span data-ttu-id="105dd-119">Può chiamare questi due metodi in qualsiasi ordine, un numero qualsiasi di volte, prima di connettere il pin di output.</span><span class="sxs-lookup"><span data-stu-id="105dd-119">It can call these two methods in any order, any number of times, before it connects the output pin.</span></span>
-   <span data-ttu-id="105dd-120">Una volta che il motore di rendering si connette al pin di output, potrebbe chiamare nuovamente **put \_ size** .</span><span class="sxs-lookup"><span data-stu-id="105dd-120">After the Render Engine connects the output pin, it might call **put\_Size** again.</span></span> <span data-ttu-id="105dd-121">Il filtro Resizer deve riconnettere il pin di output con le nuove dimensioni.</span><span class="sxs-lookup"><span data-stu-id="105dd-121">The resizer filter should reconnect its output pin with the new size.</span></span>
-   <span data-ttu-id="105dd-122">All'interno del metodo [**CTransformFilter:: Transform**](ctransformfilter-transform.md) del filtro, estendere il video di input alla dimensione di output.</span><span class="sxs-lookup"><span data-stu-id="105dd-122">Inside the filter's [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, stretch the input video to the output size.</span></span>
-   <span data-ttu-id="105dd-123">Il filtro non deve mai impostare il flag di discontinuità nell'esempio di output o alleghi un tipo di supporto all'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="105dd-123">Your filter should never set the discontinuity flag on the output sample, or attach a media type to the output sample.</span></span>
-   <span data-ttu-id="105dd-124">Per salvare lo stato del filtro in un file GraphEdit (con estensione GRF), implementare l'interfaccia **IPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="105dd-124">To save the filter's state in a GraphEdit (.grf) file, implement the **IPersistStream** interface.</span></span> <span data-ttu-id="105dd-125">Questa operazione è facoltativa, ma utile per i test.</span><span class="sxs-lookup"><span data-stu-id="105dd-125">(This is optional, but useful for testing.)</span></span>

<span data-ttu-id="105dd-126">Per usare il filtro di ridimensionamento, è necessario che il filtro sia registrato come oggetto COM nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="105dd-126">To use the resizer filter, the filter must be registered as a COM object on the user's system.</span></span> <span data-ttu-id="105dd-127">Prima che l'applicazione esegua il rendering del progetto video, eseguire una query sul motore di rendering per l'interfaccia [**IRenderEngine2**](irenderengine2.md) e chiamare [**IRenderEngine2:: SETRESIZERGUID**](irenderengine2-setresizerguid.md) con il CLSID del filtro di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="105dd-127">Before the application renders the video project, query the Render Engine for the [**IRenderEngine2**](irenderengine2.md) interface and call [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) with the CLSID of the resizer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="105dd-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="105dd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="105dd-129">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="105dd-129">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



