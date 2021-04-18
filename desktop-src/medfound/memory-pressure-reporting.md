---
description: La funzionalità di creazione di report con utilizzo intensivo della memoria consente a un'applicazione Direct3D di determinare quando il working set di memoria video è troppo grande.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Segnalazione di utilizzo intensivo della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309632"
---
# <a name="memory-pressure-reporting"></a><span data-ttu-id="43582-103">Segnalazione di utilizzo intensivo della memoria</span><span class="sxs-lookup"><span data-stu-id="43582-103">Memory Pressure Reporting</span></span>

<span data-ttu-id="43582-104">La funzionalità di creazione di report con utilizzo intensivo della memoria consente a un'applicazione Direct3D di determinare quando il working set di memoria video è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="43582-104">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span>

<span data-ttu-id="43582-105">Il numero di richieste di *memoria* è la richiesta effettuata nel sottosistema di memoria da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43582-105">*Memory pressure* is the demand placed on the memory subsystem by an application.</span></span> <span data-ttu-id="43582-106">Sebbene qualsiasi applicazione Direct3D possa usare la funzionalità di creazione di report con utilizzo intensivo della memoria, questa funzionalità è particolarmente utile per le applicazioni che eseguono il rendering video usando Direct3D.</span><span class="sxs-lookup"><span data-stu-id="43582-106">While any Direct3D application can use memory pressure reporting, this feature is especially useful for applications that render video by using Direct3D.</span></span> <span data-ttu-id="43582-107">La riproduzione video in genere trae vantaggio da grandi quantità di buffering, in modo che sia possibile decodificare i frame in anticipo.</span><span class="sxs-lookup"><span data-stu-id="43582-107">Video playback typically benefits from large amounts of buffering, so that frames can be decoded in advance.</span></span> <span data-ttu-id="43582-108">Sebbene il buffering generi una riproduzione più uniforme, può influire negativamente sulle prestazioni in caso di dimensioni eccessive del working set, a causa dei seguenti fattori:</span><span class="sxs-lookup"><span data-stu-id="43582-108">While buffering generally results in smoother playback, it can actually degrade performance if the working set grows too large, due to the following factors:</span></span>

-   <span data-ttu-id="43582-109">La memoria potrebbe essere rimossa dalla cache.</span><span class="sxs-lookup"><span data-stu-id="43582-109">Memory might be evicted from the cache.</span></span> <span data-ttu-id="43582-110">Nel peggiore dei casi, questo problema può verificarsi in ogni fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="43582-110">In the worst case, this can occur on every video frame.</span></span>
-   <span data-ttu-id="43582-111">Le allocazioni di memoria possono essere inserite in segmenti di memoria non ottimali.</span><span class="sxs-lookup"><span data-stu-id="43582-111">Memory allocations might be placed in nonoptimal memory segments.</span></span>

<span data-ttu-id="43582-112">A partire da Windows 7, Direct3D può segnalare alcune statistiche relative al numero di richieste di memoria video:</span><span class="sxs-lookup"><span data-stu-id="43582-112">Starting in Windows 7, Direct3D can report some statistics about the video memory pressure:</span></span>

-   <span data-ttu-id="43582-113">Numero di byte rimossi dal processo in un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="43582-113">The number of bytes evicted by the process over an interval of time.</span></span>
-   <span data-ttu-id="43582-114">Quantità di memoria posizionata in segmenti di memoria non ottimali.</span><span class="sxs-lookup"><span data-stu-id="43582-114">The amount of memory placed in nonoptimal memory segments.</span></span>
-   <span data-ttu-id="43582-115">Indicazione approssimativa dell'efficienza complessiva delle allocazioni di memoria posizionate nella memoria non ottimale.</span><span class="sxs-lookup"><span data-stu-id="43582-115">A rough indication of the overall efficiency of the memory allocations placed in nonoptimal memory.</span></span>

<span data-ttu-id="43582-116">Queste informazioni consentono a un'applicazione di mantenere un working set ragionevole.</span><span class="sxs-lookup"><span data-stu-id="43582-116">This information can help an application to maintain a reasonable working set.</span></span>

## <a name="using-memory-pressure-reporting"></a><span data-ttu-id="43582-117">Uso della segnalazione con utilizzo intensivo della memoria</span><span class="sxs-lookup"><span data-stu-id="43582-117">Using Memory Pressure Reporting</span></span>

<span data-ttu-id="43582-118">La creazione di report con utilizzo intensivo della memoria usa l'interfaccia **IDirect3DQuery9** esistente per eseguire query sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43582-118">Memory pressure reporting uses the existing **IDirect3DQuery9** interface to query the device.</span></span> <span data-ttu-id="43582-119">È stato aggiunto un nuovo tipo di query all'enumerazione **D3DQUERYTYPE** .</span><span class="sxs-lookup"><span data-stu-id="43582-119">A new query type has been added to the **D3DQUERYTYPE** enumeration.</span></span>


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



<span data-ttu-id="43582-120">Per usare questa query, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="43582-120">To use this query, perform the following steps:</span></span>

1.  <span data-ttu-id="43582-121">Chiamare **IDirect3DDevice9Ex:: CreateQuery** con il **flag \_ MEMORYPRESSURE di D3DQUERYTYPE** .</span><span class="sxs-lookup"><span data-stu-id="43582-121">Call **IDirect3DDevice9Ex::CreateQuery** with the **D3DQUERYTYPE\_MEMORYPRESSURE** flag.</span></span> <span data-ttu-id="43582-122">Questo metodo restituisce un puntatore all'interfaccia **IDirect3DQuery9** .</span><span class="sxs-lookup"><span data-stu-id="43582-122">This method returns a pointer to the **IDirect3DQuery9** interface.</span></span>
2.  <span data-ttu-id="43582-123">Chiamare **IDirect3DQuery9:: Issue** con il **flag \_ Begin di D3DISSUE** per iniziare l'intervallo di misurazione.</span><span class="sxs-lookup"><span data-stu-id="43582-123">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_BEGIN** flag to begin the measurement interval.</span></span>
3.  <span data-ttu-id="43582-124">Chiamare **IDirect3DQuery9:: Issue** con il **flag \_ finale D3DISSUE** .</span><span class="sxs-lookup"><span data-stu-id="43582-124">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_END** flag.</span></span>
4.  <span data-ttu-id="43582-125">Chiamare **IDirect3DQuery9:: GetData** per ottenere il risultato della query.</span><span class="sxs-lookup"><span data-stu-id="43582-125">Call **IDirect3DQuery9::GetData** to get the query result.</span></span> <span data-ttu-id="43582-126">La query restituisce una struttura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="43582-126">The query returns a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

## <a name="example-code"></a><span data-ttu-id="43582-127">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="43582-127">Example Code</span></span>

<span data-ttu-id="43582-128">Nell'esempio seguente vengono illustrate due funzioni che misurano la pressione della memoria.</span><span class="sxs-lookup"><span data-stu-id="43582-128">The following example shows two functions that measure memory pressure.</span></span> <span data-ttu-id="43582-129">Il primo inizia l'intervallo di misurazione e il secondo recupera i risultati della misurazione.</span><span class="sxs-lookup"><span data-stu-id="43582-129">The first begins the measurement interval, and the second retrieves the results of the measurement.</span></span>


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="43582-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43582-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43582-131">API video Direct3D</span><span class="sxs-lookup"><span data-stu-id="43582-131">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 



