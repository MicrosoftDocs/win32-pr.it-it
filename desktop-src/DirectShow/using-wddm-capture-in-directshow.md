---
description: Uso di WDDM Capture in DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Uso di WDDM Capture in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314381"
---
# <a name="using-wddm-capture-in-directshow"></a><span data-ttu-id="b9394-103">Uso di WDDM Capture in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b9394-103">Using WDDM Capture in DirectShow</span></span>

<span data-ttu-id="b9394-104">Questo argomento si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b9394-104">This topic applies to Windows Vista and later.</span></span>

<span data-ttu-id="b9394-105">Alcune schede video hanno funzionalità di acquisizione video integrate.</span><span class="sxs-lookup"><span data-stu-id="b9394-105">Some video cards have integrated video capture functionality.</span></span> <span data-ttu-id="b9394-106">In queste schede i frame video acquisiti vengono inseriti in memoria video (VRAM).</span><span class="sxs-lookup"><span data-stu-id="b9394-106">On these cards, captured video frames are placed in video memory (VRAM).</span></span> <span data-ttu-id="b9394-107">Prima di Windows Vista, non era disponibile un meccanismo standard per l'elaborazione dei frame mentre rimanevano in VRAM.</span><span class="sxs-lookup"><span data-stu-id="b9394-107">Prior to Windows Vista, there was no standard mechanism for processing the frames while they remained in VRAM.</span></span> <span data-ttu-id="b9394-108">Al contrario, i dati devono essere copiati nella memoria di sistema, elaborati e quindi copiati di nuovo in VRAM per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b9394-108">Instead, the data had to be copied into system memory, processed, and then copied back to VRAM for display.</span></span> <span data-ttu-id="b9394-109">In Windows Vista, DirectShow supporta ora un meccanismo per mantenere i frame video in VRAM nell'intera pipeline di elaborazione, dall'acquisizione alla visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b9394-109">In Windows Vista, DirectShow now supports a mechanism for keeping the video frames in VRAM throughout the processing pipeline, from capture to display.</span></span>

<span data-ttu-id="b9394-110">Il filtro KsProxy determina se il driver supporta la funzionalità di acquisizione della superficie VRAM eseguendo una query sul driver per la \_ proprietà della superficie di acquisizione preferita di KSPROPERTY \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9394-110">The KsProxy filter determines if the driver supports VRAM surface capture by querying the driver for the KSPROPERTY\_PREFERRED\_CAPTURE\_SURFACE property.</span></span> <span data-ttu-id="b9394-111">Questa proprietà è documentata nella documentazione di Windows Driver Kit. Se il driver supporta la funzionalità di acquisizione della superficie VRAM, KsProxy alloca un tipo speciale di esempio multimediale che include un puntatore a una superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9394-111">(This property is documented in the Windows Driver Kit documentation.) If the driver supports VRAM surface capture, KsProxy allocates a special kind of media sample that holds a pointer to a Direct3D surface.</span></span>

<span data-ttu-id="b9394-112">Successivamente, KsProxy determina se il filtro downstream supporta l'accelerazione video DirectX (DXVA) 2,0, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b9394-112">Next, KsProxy determines whether the downstream filter supports DirectX Video Acceleration (DXVA) 2.0, as follows:</span></span>

1.  <span data-ttu-id="b9394-113">KsProxy esegue una query sul pin di input downstream per l'interfaccia **IMFGetService** .</span><span class="sxs-lookup"><span data-stu-id="b9394-113">KsProxy queries the downstream input pin for the **IMFGetService** interface.</span></span>
2.  <span data-ttu-id="b9394-114">Se il pin espone **IMFGetService**, ksproxy chiama **IMFGetService:: GetService** per l'interfaccia **IDirect3DDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="b9394-114">If the pin exposes **IMFGetService**, KsProxy calls **IMFGetService::GetService** for the **IDirect3DDeviceManager** interface.</span></span> <span data-ttu-id="b9394-115">Il servizio identier è il \_ servizio di accelerazione del video \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9394-115">The service identier is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="b9394-116">Entrambe le interfacce sono documentate nella documentazione di Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="b9394-116">Both of these interfaces are documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="b9394-117">Se il filtro downstream non supporta DXVA 2,0, KsProxy alloca un buffer di memoria di sistema aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="b9394-117">If the downstream filter does not support DXVA 2.0, KsProxy allocates an additional system memory buffer.</span></span> <span data-ttu-id="b9394-118">Usa questo buffer per copiare i fotogrammi video da VRAM a memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9394-118">It uses this buffer to copy the video frames from VRAM to system memory.</span></span> <span data-ttu-id="b9394-119">Il metodo [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) dell'esempio multimediale restituisce un puntatore a questo buffer di memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9394-119">The media sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to this system memory buffer.</span></span>

<span data-ttu-id="b9394-120">Tuttavia, se il filtro downstream supporta DXVA 2,0, KsProxy non alloca un buffer di memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9394-120">However, if the downstream filter does support DXVA 2.0, then KsProxy does not allocate a system memory buffer.</span></span> <span data-ttu-id="b9394-121">In tal caso, il metodo **Getpointer** restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b9394-121">In that case, the **GetPointer** method returns E\_NOTIMPL.</span></span> <span data-ttu-id="b9394-122">Al contrario, si prevede che il filtro downstream acceda direttamente alla superficie Direct3D dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="b9394-122">Instead, the downstream filter is expected to access the sample's Direct3D surface directly.</span></span> <span data-ttu-id="b9394-123">Esistono due modi per il filtro downstream per ottenere un puntatore alla superficie, entrambi equivalenti:</span><span class="sxs-lookup"><span data-stu-id="b9394-123">There are two ways for the downstream filter to get a pointer to the surface, both of them equivalent:</span></span>

-   <span data-ttu-id="b9394-124">Eseguire una query sull'esempio per l'interfaccia **IMFGetService** e chiamare **GetService** per l'interfaccia **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="b9394-124">Query the sample for the **IMFGetService** interface and call **GetService** for the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="b9394-125">L'identificatore del servizio è \_ il \_ servizio buffer di.</span><span class="sxs-lookup"><span data-stu-id="b9394-125">The service identifier is MR\_BUFFER\_SERVICE.</span></span>
-   <span data-ttu-id="b9394-126">Eseguire una query sull'esempio per l'interfaccia [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) e chiamare [**IMediaSample2Config:: GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span><span class="sxs-lookup"><span data-stu-id="b9394-126">Query the sample for the [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) interface and call [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9394-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9394-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9394-128">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="b9394-128">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



