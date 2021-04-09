---
title: Funzioni wrapper plug-in
description: Funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi Adapter collegato alla pipeline senza acquisire manualmente un puntatore all'adapter.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API Windows Biometric Framework API di Windows Biometric Framework, funzioni wrapper per il plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856710"
---
# <a name="plug-in-wrapper-functions"></a><span data-ttu-id="7199d-104">Funzioni wrapper plug-in</span><span class="sxs-lookup"><span data-stu-id="7199d-104">Plug-in Wrapper Functions</span></span>

<span data-ttu-id="7199d-105">L'API Windows Biometric Framework include funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi Adapter collegato alla pipeline senza acquisire manualmente un puntatore alla scheda.</span><span class="sxs-lookup"><span data-stu-id="7199d-105">The Windows Biometric Framework API includes wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span> <span data-ttu-id="7199d-106">Ogni wrapper controlla gli argomenti di input, recupera un puntatore di adapter e chiama la funzione richiesta.</span><span class="sxs-lookup"><span data-stu-id="7199d-106">Each wrapper checks the input arguments, retrieves an adapter pointer, and calls the requested function.</span></span> <span data-ttu-id="7199d-107">Il wrapper **WbioEngineSetHashAlgorithm** , ad esempio, ha la firma seguente:</span><span class="sxs-lookup"><span data-stu-id="7199d-107">For example, the **WbioEngineSetHashAlgorithm** wrapper has the following signature.</span></span>


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



<span data-ttu-id="7199d-108">La funzione verifica che l'argomento della *pipeline* non sia **null**, che esista un adattatore del motore e che la funzione [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) esista.</span><span class="sxs-lookup"><span data-stu-id="7199d-108">The function verifies that the *Pipeline* argument is not **NULL**, that an engine adapter exists, and that the [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) function exists.</span></span> <span data-ttu-id="7199d-109">Tutte le funzioni wrapper sono definite nel \_ file di intestazione WinBio adapter. h.</span><span class="sxs-lookup"><span data-stu-id="7199d-109">All wrapper functions are defined in the Winbio\_adapter.h header file.</span></span> <span data-ttu-id="7199d-110">Negli argomenti seguenti vengono illustrati i wrapper disponibili.</span><span class="sxs-lookup"><span data-stu-id="7199d-110">The following topics discuss the available wrappers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7199d-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7199d-111">In this section</span></span>



| <span data-ttu-id="7199d-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="7199d-112">Topic</span></span>                                                               | <span data-ttu-id="7199d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7199d-113">Description</span></span>                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7199d-114">Wrapper dell'adattatore del motore</span><span class="sxs-lookup"><span data-stu-id="7199d-114">Engine Adapter Wrappers</span></span>](engine-adapter-wrappers.md)<br/>   | <span data-ttu-id="7199d-115">Funzioni che è possibile utilizzare per chiamare funzioni sull'adattatore del motore.</span><span class="sxs-lookup"><span data-stu-id="7199d-115">Functions that you can use to call functions on your engine adapter.</span></span> <span data-ttu-id="7199d-116">Queste funzioni sono definite in WinBio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="7199d-116">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="7199d-117">Wrapper adattatore sensore</span><span class="sxs-lookup"><span data-stu-id="7199d-117">Sensor Adapter Wrappers</span></span>](sensor-adapter-wrappers.md)<br/>   | <span data-ttu-id="7199d-118">Funzioni che è possibile utilizzare per chiamare funzioni sulla scheda del sensore.</span><span class="sxs-lookup"><span data-stu-id="7199d-118">Functions that you can use to call functions on your sensor adapter.</span></span> <span data-ttu-id="7199d-119">Queste funzioni sono definite in WinBio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="7199d-119">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="7199d-120">Wrapper dell'adattatore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7199d-120">Storage Adapter Wrappers</span></span>](storage-adapter-wrappers.md)<br/> | <span data-ttu-id="7199d-121">Funzioni che è possibile utilizzare per chiamare funzioni sull'adattatore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7199d-121">Functions that you can use to call functions on your storage adapter.</span></span> <span data-ttu-id="7199d-122">Queste funzioni sono definite in WinBio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="7199d-122">These functions are defined in Winbio\_adapter.h.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7199d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7199d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7199d-124">Riferimento al plug-in</span><span class="sxs-lookup"><span data-stu-id="7199d-124">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> </dl>

 

 





