---
description: Specifica i flag di associazione da utilizzare per l'allocazione di superfici Microsoft Direct3D 11 per gli esempi di supporti.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Attributo MF_SA_D3D11_BINDFLAGS (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345836"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a><span data-ttu-id="5bea8-103">\_Attributo BINDFLAGS di MF SA \_ d3d11 \_</span><span class="sxs-lookup"><span data-stu-id="5bea8-103">MF\_SA\_D3D11\_BINDFLAGS attribute</span></span>

<span data-ttu-id="5bea8-104">Specifica i flag di associazione da utilizzare per l'allocazione di superfici Microsoft Direct3D 11 per gli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="5bea8-104">Specifies the binding flags to use when allocating Microsoft Direct3D 11 surfaces for media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="5bea8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5bea8-105">Data type</span></span>

<span data-ttu-id="5bea8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5bea8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5bea8-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bea8-107">Remarks</span></span>

<span data-ttu-id="5bea8-108">Il **valore di questo** attributo è un operatore OR bit per bit di flag di [**\_ binding \_ d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="5bea8-108">The value of this attribute is a bitwise **OR** of [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) flags.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="5bea8-109">Trasformazioni Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bea8-109">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="5bea8-110">In questo contesto, l'attributo si applica solo quando la trasformazione Microsoft Media Foundation (MFT) restituisce **true** per l'attributo d3d11 in grado di [ \_ \_ \_ riconoscere il valore MF SA](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="5bea8-110">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="5bea8-111">Se una MFT supporta Direct3D 11, questo attributo fornisce un suggerimento alla MFT durante l'allocazione delle superfici di Microsoft Direct3D per l'output.</span><span class="sxs-lookup"><span data-stu-id="5bea8-111">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="5bea8-112">Impostare l'attributo nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="5bea8-112">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="5bea8-113">Chiamare [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) per ottenere l'archivio di attributi MFT.</span><span class="sxs-lookup"><span data-stu-id="5bea8-113">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="5bea8-114">Chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5bea8-114">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="5bea8-115">La pipeline Media Foundation imposta l'attributo prima dell'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="5bea8-115">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="5bea8-116">Il MFT deve tentare di rispettare l'impostazione quando alloca superfici.</span><span class="sxs-lookup"><span data-stu-id="5bea8-116">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="5bea8-117">Se ciò non è possibile, il MFT può ignorare l'attributo, anziché l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="5bea8-117">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="5bea8-118">Inoltre, se il MFT richiede l'input di superfici Direct3D, può esporre questo attributo come hint per la modalità di allocazione delle superfici di input.</span><span class="sxs-lookup"><span data-stu-id="5bea8-118">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="5bea8-119">Eseguire una query sull'attributo come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5bea8-119">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="5bea8-120">Chiamare [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) per ottenere gli attributi del flusso di input.</span><span class="sxs-lookup"><span data-stu-id="5bea8-120">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="5bea8-121">Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5bea8-121">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="5bea8-122">Allocatore di esempio</span><span class="sxs-lookup"><span data-stu-id="5bea8-122">Sample Allocator</span></span>

<span data-ttu-id="5bea8-123">Questo attributo può essere impostato nell'allocatore video di esempio, nel metodo [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="5bea8-123">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bea8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bea8-124">Requirements</span></span>



| <span data-ttu-id="5bea8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bea8-125">Requirement</span></span> | <span data-ttu-id="5bea8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5bea8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bea8-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bea8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5bea8-128">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5bea8-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5bea8-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bea8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5bea8-130">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5bea8-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5bea8-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bea8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bea8-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bea8-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bea8-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bea8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bea8-134">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bea8-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
