---
description: Specifica il numero di buffer creati dall'allocatore di campionamento video per ogni esempio video.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: Attributo MF_SA_BUFFERS_PER_SAMPLE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753175"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a><span data-ttu-id="e7134-103">\_Buffer SA MF \_ \_ per attributo di \_ esempio</span><span class="sxs-lookup"><span data-stu-id="e7134-103">MF\_SA\_BUFFERS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="e7134-104">Specifica il numero di buffer creati dall'allocatore di campionamento video per ogni esempio video.</span><span class="sxs-lookup"><span data-stu-id="e7134-104">Specifies how many buffers the video-sample allocator creates for each video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="e7134-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e7134-105">Data type</span></span>

<span data-ttu-id="e7134-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e7134-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e7134-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7134-107">Remarks</span></span>

<span data-ttu-id="e7134-108">Se si usa l'interfaccia [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) per allocare esempi video, è possibile usare questo attributo per creare esempi video contenenti più buffer.</span><span class="sxs-lookup"><span data-stu-id="e7134-108">If you use the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate video samples, you can use this attribute to create video samples that contain multiple buffers.</span></span> <span data-ttu-id="e7134-109">Se, ad esempio, il valore dell'attributo è 2, l'allocatore crea due buffer video per ogni esempio video.</span><span class="sxs-lookup"><span data-stu-id="e7134-109">For example, if the attribute value is 2, the allocator creates two video buffers for each video sample.</span></span> <span data-ttu-id="e7134-110">Impostare l'attributo nel parametro *pAttributes* del metodo [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="e7134-110">Set the attribute in the *pAttributes* parameter of the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

<span data-ttu-id="e7134-111">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="e7134-111">The default value is 1.</span></span> <span data-ttu-id="e7134-112">Se l'attributo non è impostato, l'allocatore crea esempi video contenenti un singolo buffer per campione.</span><span class="sxs-lookup"><span data-stu-id="e7134-112">If the attribute is not set, the allocator creates video samples that contain a single buffer per sample.</span></span>

<span data-ttu-id="e7134-113">Questo attributo è destinato principalmente alle trasformazioni di Media Foundation (MFTs) che supportano l'output 3D stereo, nella situazione seguente:</span><span class="sxs-lookup"><span data-stu-id="e7134-113">This attribute is primarily intended for Media Foundation transforms (MFTs) that support stereo 3D output, in the following situation:</span></span>

-   <span data-ttu-id="e7134-114">Il MFT supporta Microsoft DirectX Graphics Infrastructure (DXGI).</span><span class="sxs-lookup"><span data-stu-id="e7134-114">The MFT supports Microsoft DirectX Graphics Infrastructure (DXGI).</span></span>
-   <span data-ttu-id="e7134-115">Il MFT alloca gli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="e7134-115">The MFT allocates its own output samples.</span></span>
-   <span data-ttu-id="e7134-116">Il MFT usa l'interfaccia [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) per allocare gli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="e7134-116">The MFT uses the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate the output samples.</span></span>
-   <span data-ttu-id="e7134-117">Il formato video 3D utilizza un buffer separato per ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e7134-117">The 3D video format uses a separate buffer for each view.</span></span>

<span data-ttu-id="e7134-118">Se tutti questi criteri sono true, la MFT deve impostare il valore dell'attributo su 2 (un buffer per ogni visualizzazione).</span><span class="sxs-lookup"><span data-stu-id="e7134-118">If all of these criteria are true, the MFT should set the attribute value to 2 (one buffer per view).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7134-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7134-119">Requirements</span></span>



| <span data-ttu-id="e7134-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7134-120">Requirement</span></span> | <span data-ttu-id="e7134-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e7134-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7134-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7134-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7134-123">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e7134-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e7134-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7134-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7134-125">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="e7134-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e7134-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7134-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7134-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7134-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7134-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7134-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7134-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7134-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




