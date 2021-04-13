---
description: Specifica la modalità di allocazione delle superfici Microsoft Direct3D 11 per gli esempi di supporti.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Attributo MF_SA_D3D11_USAGE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226379"
---
# <a name="mf_sa_d3d11_usage-attribute"></a><span data-ttu-id="97385-103">\_Attributo utilizzo di MF SA \_ d3d11 \_</span><span class="sxs-lookup"><span data-stu-id="97385-103">MF\_SA\_D3D11\_USAGE attribute</span></span>

<span data-ttu-id="97385-104">Specifica la modalità di allocazione delle superfici Microsoft Direct3D 11 per gli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="97385-104">Specifies how to allocate Microsoft Direct3D 11 surfaces for media samples.</span></span> <span data-ttu-id="97385-105">L'utilizzo indica direttamente se un campione è accessibile dalla CPU o dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="97385-105">The usage directly reflects whether a sample is accessible by the CPU or GPU.</span></span>

## <a name="data-type"></a><span data-ttu-id="97385-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="97385-106">Data type</span></span>

<span data-ttu-id="97385-107">**D3d11 \_ UTILIZZO** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97385-107">**D3D11\_USAGE** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="97385-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="97385-108">Remarks</span></span>

<span data-ttu-id="97385-109">Il valore di questo attributo è un valore di [**\_ utilizzo di d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .</span><span class="sxs-lookup"><span data-stu-id="97385-109">The value of this attribute is a [**D3D11\_USAGE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) value.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="97385-110">Trasformazioni Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97385-110">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="97385-111">In questo contesto, l'attributo si applica solo quando la trasformazione Microsoft Media Foundation (MFT) restituisce **true** per l'attributo d3d11 in grado di [ \_ \_ \_ riconoscere il valore MF SA](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="97385-111">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="97385-112">Se una MFT supporta Direct3D 11, questo attributo fornisce un suggerimento alla MFT durante l'allocazione delle superfici di Microsoft Direct3D per l'output.</span><span class="sxs-lookup"><span data-stu-id="97385-112">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="97385-113">Impostare l'attributo nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="97385-113">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="97385-114">Chiamare [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) per ottenere l'archivio di attributi MFT.</span><span class="sxs-lookup"><span data-stu-id="97385-114">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="97385-115">Chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="97385-115">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="97385-116">La pipeline Media Foundation imposta l'attributo prima dell'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="97385-116">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="97385-117">Il MFT deve tentare di rispettare l'impostazione quando alloca superfici.</span><span class="sxs-lookup"><span data-stu-id="97385-117">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="97385-118">Se ciò non è possibile, il MFT può ignorare l'attributo, anziché l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="97385-118">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="97385-119">Inoltre, se il MFT richiede l'input di superfici Direct3D, può esporre questo attributo come hint per la modalità di allocazione delle superfici di input.</span><span class="sxs-lookup"><span data-stu-id="97385-119">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="97385-120">Eseguire una query sull'attributo come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="97385-120">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="97385-121">Chiamare [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) per ottenere gli attributi del flusso di input.</span><span class="sxs-lookup"><span data-stu-id="97385-121">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="97385-122">Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="97385-122">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="97385-123">Allocatore di esempio</span><span class="sxs-lookup"><span data-stu-id="97385-123">Sample Allocator</span></span>

<span data-ttu-id="97385-124">Questo attributo può essere impostato nell'allocatore video di esempio, nel metodo [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="97385-124">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="97385-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97385-125">Requirements</span></span>



| <span data-ttu-id="97385-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="97385-126">Requirement</span></span> | <span data-ttu-id="97385-127">Valore</span><span class="sxs-lookup"><span data-stu-id="97385-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97385-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97385-128">Minimum supported client</span></span><br/> | <span data-ttu-id="97385-129">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="97385-129">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="97385-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97385-130">Minimum supported server</span></span><br/> | <span data-ttu-id="97385-131">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="97385-131">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="97385-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97385-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="97385-133"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="97385-133"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97385-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97385-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97385-135">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97385-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
