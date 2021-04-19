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
# <a name="direct3d-video-motion-estimation"></a>Valutazione movimento video Direct3D

Questo articolo contiene informazioni aggiuntive per la stima del vettore di movimento con le API video di Direct3D 12. Questa funzionalità è stata introdotta in Windows 10, versione 2004 (10,0; Compilazione 19041). La stima del movimento è il processo di determinazione dei vettori di movimento che descrivono la trasformazione da un'immagine 2D a un'altra. La stima del movimento è una parte essenziale della codifica video e può essere usata negli algoritmi di conversione della frequenza dei fotogrammi. 

Sebbene la stima del movimento possa essere implementata con gli shader, lo scopo della funzionalità di stima del movimento D3D12 è esporre l'accelerazione della funzione fissa per la ricerca di movimento in modo da eseguire l'offload di questa parte del lavoro da 3D. Spesso si tratta della modalità di esposizione dello strumento di stima del movimento del codificatore video GPU. L'obiettivo della stima del movimento D3D12 è il flusso ottico, ma si noti che gli estimatori del movimento del codificatore possono essere ottimizzati per migliorare la compressione.


## <a name="checking-for-support"></a>Verifica del supporto

Determinare il supporto per tutte le funzionalità video D3D chiamando [ID3D12VideoDevice:: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) e passando un valore dall'enumerazione [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) per specificare la funzionalità per cui viene eseguita una query sul supporto. Per eseguire una query sulle dimensioni e le risoluzioni del blocco supportate per un determinato formato, usare il valore **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** e fornire una struttura [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) per *pFeatureSupportData* , come illustrato nell'esempio riportato di seguito. Nella versione corrente è supportato solo **DXGI_FORMAT_NV12** , quindi il contenuto in altri formati potrebbe dover essere convertito in colori e downsampling per usare la stima di movimento.

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a>Oggetto di contesto dello strumento di stima del movimento

L'oggetto [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) mantiene il contesto per le operazioni di stima del movimento video. Creare una nuova istanza di questa interfaccia chiamando [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).

Le dimensioni del blocco, la precisione e l'intervallo di dimensioni supportato selezionati variano in base ai valori supportati dall'hardware restituito dal controllo della funzionalità **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** . È possibile selezionare un intervallo di dimensioni inferiori rispetto a quello supportato dal driver. L'intervallo di dimensioni informa le dimensioni di allocazione interne.

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



## <a name="storage-of-motion-vectors"></a>Archiviazione di vettori di movimento

[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) archivia i vettori di movimento. Questa interfaccia viene utilizzata dalla struttura [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) restituita da [ID3D12VideoEncodeCommandList:: EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion). La trama 2D di output risolto è una trama [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) dove R include il componente orizzontale e G include il componente verticale del vettore di movimento. Questa trama è dimensionata in modo da mantenere una coppia di componenti per blocco. Chiamare [ID3D12VideoEncodeCommandList:: ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) per traslare l'output del vettore di movimento di **EstimateMotion** da formati dipendenti dall'hardware in un formato coerente definito dalle API per la stima del movimento del video.

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

 **ID3D12VideoMotionVectorHeap** viene usato anche per fornire i vettori di hint nella struttura [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .



## <a name="estimate-motion-in-a-command-list"></a>Stimare il movimento in un elenco di comandi

Chiamare [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) da un [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) per richiamare l'operazione di stima del movimento.

Nell'esempio seguente viene eseguita la ricerca del movimento e vengono risolti i vettori di movimento nella trama 2D con [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).  Le risorse D3D12 usate come input per **EstimateMotion** devono trovarsi nello stato [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) e la risorsa scritta da **ResolveMotionVectorHeap** deve trovarsi nello stato [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

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


## <a name="protected-resources"></a>Risorse protette

Direct3D 12 Motion Vector stima supporta la lettura e la scrittura nelle risorse protette da DRM hardware se supportate dal driver. Se le risorse di input sono protette da DRM hardware, l'output è anche una risorsa hardware protetta da DRM. I metodi usati per creare l'oggetto contesto della stima del movimento e l'heap del vettore di movimento,  [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) e [ID3D12VideoDevice1:: CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), accettano entrambi un [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) usato per gestire l'accesso alle risorse protette. 

Usare [ID3D12VideoMotionEstimator:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) e [ID3D12VideoMotionVectorHeap:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) per recuperare gli oggetti **ID3D12ProtectedResourceSession** forniti al momento della creazione degli oggetti.



## <a name="related-topics"></a>Argomenti correlati

* [API video Direct3D 12](direct3d-12-video-apis.md)
* [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
