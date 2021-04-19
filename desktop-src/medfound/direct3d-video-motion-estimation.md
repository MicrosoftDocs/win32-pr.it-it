---
description: Questo articolo contiene informazioni aggiuntive per la stima del vettore di movimento con le API video di Direct3D 12.
ms.assetid: ''
title: Valutazione movimento video Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320221"
---
# <a name="direct3d-video-motion-estimation"></a><span data-ttu-id="209cc-103">Valutazione movimento video Direct3D</span><span class="sxs-lookup"><span data-stu-id="209cc-103">Direct3D video motion estimation</span></span>

<span data-ttu-id="209cc-104">Questo articolo contiene informazioni aggiuntive per la stima del vettore di movimento con le API video di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="209cc-104">This article contains guidance for motion vector estimation with Direct3D 12 video APIs.</span></span> <span data-ttu-id="209cc-105">Questa funzionalità è stata introdotta in Windows 10, versione 2004 (10,0; Compilazione 19041).</span><span class="sxs-lookup"><span data-stu-id="209cc-105">This feature was introduced in Windows 10, version 2004 (10.0; Build 19041).</span></span> <span data-ttu-id="209cc-106">La stima del movimento è il processo di determinazione dei vettori di movimento che descrivono la trasformazione da un'immagine 2D a un'altra.</span><span class="sxs-lookup"><span data-stu-id="209cc-106">Motion estimation is the process of determining motion vectors that describe the transformation from one 2D image to another.</span></span> <span data-ttu-id="209cc-107">La stima del movimento è una parte essenziale della codifica video e può essere usata negli algoritmi di conversione della frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="209cc-107">Motion estimation is an essential part of video encoding and can be used in frame rate conversion algorithms.</span></span> 

<span data-ttu-id="209cc-108">Sebbene la stima del movimento possa essere implementata con gli shader, lo scopo della funzionalità di stima del movimento D3D12 è esporre l'accelerazione della funzione fissa per la ricerca di movimento in modo da eseguire l'offload di questa parte del lavoro da 3D.</span><span class="sxs-lookup"><span data-stu-id="209cc-108">While motion estimation can be implemented with shaders, the purpose of the D3D12 Motion Estimation feature is to expose fixed function acceleration for motion searching to offload this part of the work from 3D.</span></span> <span data-ttu-id="209cc-109">Spesso si tratta della modalità di esposizione dello strumento di stima del movimento del codificatore video GPU.</span><span class="sxs-lookup"><span data-stu-id="209cc-109">Often this comes in the form of exposing the GPU video encoder motion estimator.</span></span> <span data-ttu-id="209cc-110">L'obiettivo della stima del movimento D3D12 è il flusso ottico, ma si noti che gli estimatori del movimento del codificatore possono essere ottimizzati per migliorare la compressione.</span><span class="sxs-lookup"><span data-stu-id="209cc-110">The goal of D3D12 Motion estimation is optical flow, but it should be noted that encoder motion estimators may be optimized for improving compression.</span></span>


## <a name="checking-for-support"></a><span data-ttu-id="209cc-111">Verifica del supporto</span><span class="sxs-lookup"><span data-stu-id="209cc-111">Checking for Support</span></span>

<span data-ttu-id="209cc-112">Determinare il supporto per tutte le funzionalità video D3D chiamando [ID3D12VideoDevice:: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) e passando un valore dall'enumerazione [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) per specificare la funzionalità per cui viene eseguita una query sul supporto.</span><span class="sxs-lookup"><span data-stu-id="209cc-112">Determine support for all D3D video features by calling [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) and passing in a value from the [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify the feature for which support is being queried.</span></span> <span data-ttu-id="209cc-113">Per eseguire una query sulle dimensioni e le risoluzioni del blocco supportate per un determinato formato, usare il valore **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** e fornire una struttura [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) per *pFeatureSupportData* , come illustrato nell'esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="209cc-113">To query the supported block size and resolutions for a given format, use the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** value and supply a [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) structure for the *pFeatureSupportData* as shown in the example below.</span></span> <span data-ttu-id="209cc-114">Nella versione corrente è supportato solo **DXGI_FORMAT_NV12** , quindi il contenuto in altri formati potrebbe dover essere convertito in colori e downsampling per usare la stima di movimento.</span><span class="sxs-lookup"><span data-stu-id="209cc-114">In the current release, only **DXGI_FORMAT_NV12** is supported, so content in other formats may need to be color converted and downsampled to use motion estimation.</span></span>

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a><span data-ttu-id="209cc-115">Oggetto di contesto dello strumento di stima del movimento</span><span class="sxs-lookup"><span data-stu-id="209cc-115">The motion estimator context object</span></span>

<span data-ttu-id="209cc-116">L'oggetto [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) mantiene il contesto per le operazioni di stima del movimento video.</span><span class="sxs-lookup"><span data-stu-id="209cc-116">The [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) object maintains context for video motion estimation operations.</span></span> <span data-ttu-id="209cc-117">Creare una nuova istanza di questa interfaccia chiamando [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span><span class="sxs-lookup"><span data-stu-id="209cc-117">Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span></span>

<span data-ttu-id="209cc-118">Le dimensioni del blocco, la precisione e l'intervallo di dimensioni supportato selezionati variano in base ai valori supportati dall'hardware restituito dal controllo della funzionalità **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** .</span><span class="sxs-lookup"><span data-stu-id="209cc-118">The selected block size, precision, and supported size range would depend on values supported by hardware returned from the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** feature check.</span></span> <span data-ttu-id="209cc-119">È possibile selezionare un intervallo di dimensioni inferiori rispetto a quello supportato dal driver.</span><span class="sxs-lookup"><span data-stu-id="209cc-119">You can select a smaller size range than the driver supports.</span></span> <span data-ttu-id="209cc-120">L'intervallo di dimensioni informa le dimensioni di allocazione interne.</span><span class="sxs-lookup"><span data-stu-id="209cc-120">Size range informs internal allocation sizes.</span></span>

```c++
D3D12_VIDEO_MOTION_ESTIMATOR_DESC motionEstimatorDesc = { 
    0, //NodeIndex
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionEstimator> spVideoMotionEstimator;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionEstimator(
    &motionEstimatorDesc, 
    nullptr,
    IID_PPV_ARGS(&spVideoMotionEstimator)));
```



## <a name="storage-of-motion-vectors"></a><span data-ttu-id="209cc-121">Archiviazione di vettori di movimento</span><span class="sxs-lookup"><span data-stu-id="209cc-121">Storage of motion vectors</span></span>

<span data-ttu-id="209cc-122">[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) archivia i vettori di movimento.</span><span class="sxs-lookup"><span data-stu-id="209cc-122">The [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stores motion vectors.</span></span> <span data-ttu-id="209cc-123">Questa interfaccia viene utilizzata dalla struttura [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) restituita da [ID3D12VideoEncodeCommandList:: EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span><span class="sxs-lookup"><span data-stu-id="209cc-123">This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span></span> <span data-ttu-id="209cc-124">La trama 2D di output risolto è una trama [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) dove R include il componente orizzontale e G include il componente verticale del vettore di movimento.</span><span class="sxs-lookup"><span data-stu-id="209cc-124">The resolved output 2D texture is a [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) texture where R holds the horizontal component and G holds the vertical component of the motion vector.</span></span> <span data-ttu-id="209cc-125">Questa trama è dimensionata in modo da mantenere una coppia di componenti per blocco.</span><span class="sxs-lookup"><span data-stu-id="209cc-125">This texture is sized to hold one pair of components per block.</span></span> <span data-ttu-id="209cc-126">Chiamare [ID3D12VideoEncodeCommandList:: ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) per traslare l'output del vettore di movimento di **EstimateMotion** da formati dipendenti dall'hardware in un formato coerente definito dalle API per la stima del movimento del video.</span><span class="sxs-lookup"><span data-stu-id="209cc-126">Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) to translates the motion vector output of **EstimateMotion** from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.</span></span>

```c++
D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC MotionVectorHeapDesc = { 
    0, // NodeIndex 
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionVectorHeap> spVideoMotionVectorHeap;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionVectorHeap(
    &MotionVectorHeapDesc, 
    nullptr, 
    IID_PPV_ARGS(&spVideoMotionVectorHeap)));
```

```cpp
    CD3DX12_RESOURCE_DESC::Tex2D(
        DXGI_FORMAT_R16G16_SINT, 
        Align(1920, 16) / 16, // This example uses a 16x16 block size. Pixel width and height
        Align(1080, 16) / 16, // are adjusted to store the vectors for those blocks.
        1, // ArraySize
        1  // MipLevels
        );

    ATL::CComPtr< ID3D12Resource > spResolvedMotionVectors;
    VERIFY_SUCCEEDED(pDevice->CreateCommittedResource(
        &Properties,
        D3D12_HEAP_FLAG_NONE,
        &resolvedMotionVectorDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        IID_PPV_ARGS(&spResolvedMotionVectors)));
```

 <span data-ttu-id="209cc-127">**ID3D12VideoMotionVectorHeap** viene usato anche per fornire i vettori di hint nella struttura [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .</span><span class="sxs-lookup"><span data-stu-id="209cc-127">**ID3D12VideoMotionVectorHeap** is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) structure.</span></span>



## <a name="estimate-motion-in-a-command-list"></a><span data-ttu-id="209cc-128">Stimare il movimento in un elenco di comandi</span><span class="sxs-lookup"><span data-stu-id="209cc-128">Estimate motion in a command list</span></span>

<span data-ttu-id="209cc-129">Chiamare [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) da un [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) per richiamare l'operazione di stima del movimento.</span><span class="sxs-lookup"><span data-stu-id="209cc-129">Call the [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) from a [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) to invoke the motion estimation operation.</span></span>

<span data-ttu-id="209cc-130">Nell'esempio seguente viene eseguita la ricerca del movimento e vengono risolti i vettori di movimento nella trama 2D con [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="209cc-130">The example below executes the motion search and resolves the motion vectors to the 2D texture with [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>  <span data-ttu-id="209cc-131">Le risorse D3D12 usate come input per **EstimateMotion** devono trovarsi nello stato [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) e la risorsa scritta da **ResolveMotionVectorHeap** deve trovarsi nello stato [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="209cc-131">D3D12 Resources used as input to **EstimateMotion** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state and the resource written to by **ResolveMotionVectorHeap** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span>

```cpp
const D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT outputArgs = {spVideoMotionVectorHeap};

const D3D12_VIDEO_MOTION_ESTIMATOR_INPUT inputArgs = {
    spCurrentResource,
    0,
    spReferenceResource,
    0,
    nullptr // pHintMotionVectorHeap
    };

spCommandList->EstimateMotion(spVideoMotionEstimator, &outputArgs, &inputArgs);

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT outputArgs = { 
    spResolvedMotionVectors,
    {}};

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT inputArgs = {
    spVideoMotionVectorHeap,
    1920,
    1080
    };

spCommandList->ResolveMotionVectorHeap(&outputArgs, &inputArgs);
        
VERIFY(spCommandList->Close());

// Execute Commandlist.
ID3D12CommandList *ppCommandLists[1] = { spCommandList.p };
spCommandQueue->ExecuteCommandLists(1, ppCommandLists);
```


## <a name="protected-resources"></a><span data-ttu-id="209cc-132">Risorse protette</span><span class="sxs-lookup"><span data-stu-id="209cc-132">Protected resources</span></span>

<span data-ttu-id="209cc-133">Direct3D 12 Motion Vector stima supporta la lettura e la scrittura nelle risorse protette da DRM hardware se supportate dal driver.</span><span class="sxs-lookup"><span data-stu-id="209cc-133">Direct3D 12 motion vector estimation supports reading from and writing to hardware DRM protected resources when supported by the driver.</span></span> <span data-ttu-id="209cc-134">Se le risorse di input sono protette da DRM hardware, l'output è anche una risorsa hardware protetta da DRM. I metodi usati per creare l'oggetto contesto della stima del movimento e l'heap del vettore di movimento,  [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) e [ID3D12VideoDevice1:: CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), accettano entrambi un [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) usato per gestire l'accesso alle risorse protette.</span><span class="sxs-lookup"><span data-stu-id="209cc-134">If the input resources are hardware DRM protected, the output is also a hardware DRM protected resource.The methods used to create the motion estimation context object and the motion vector heap,  [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) and [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), both accept a [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) that is used to manage access to protected resources.</span></span> 

<span data-ttu-id="209cc-135">Usare [ID3D12VideoMotionEstimator:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) e [ID3D12VideoMotionVectorHeap:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) per recuperare gli oggetti **ID3D12ProtectedResourceSession** forniti al momento della creazione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="209cc-135">Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) and [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) to retrieve the **ID3D12ProtectedResourceSession** objects provided when the objects were created.</span></span>



## <a name="related-topics"></a><span data-ttu-id="209cc-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="209cc-136">Related topics</span></span>

* [<span data-ttu-id="209cc-137">API video Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="209cc-137">Direct3D 12 Video APIs</span></span>](direct3d-12-video-apis.md)
* [<span data-ttu-id="209cc-138">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="209cc-138">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
