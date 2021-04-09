---
description: Consente la decodifica con accelerazione hardware da un dispositivo Direct3D 9 usando la versione 1,0 di DirectX Video Acceleration (DXVA).
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interfaccia IDirect3DVideoDevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130339"
---
# <a name="idirect3dvideodevice9-interface"></a><span data-ttu-id="a8de7-103">Interfaccia IDirect3DVideoDevice9</span><span class="sxs-lookup"><span data-stu-id="a8de7-103">IDirect3DVideoDevice9 interface</span></span>

<span data-ttu-id="a8de7-104">Consente la decodifica con accelerazione hardware da un dispositivo Direct3D 9 usando la versione 1,0 di DirectX Video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="a8de7-104">Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a8de7-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a8de7-105">When to use</span></span>

<span data-ttu-id="a8de7-106">Questa interfaccia non è destinata all'utilizzo generale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8de7-106">This interface is not intended for general application use.</span></span> <span data-ttu-id="a8de7-107">I filtri del decodificatore DirectShow devono usare l'interfaccia [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , non **IDirect3DVideoDevice9**.</span><span class="sxs-lookup"><span data-stu-id="a8de7-107">DirectShow decoder filters should use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, not **IDirect3DVideoDevice9**.</span></span> <span data-ttu-id="a8de7-108">I pin di input del filtro VMR (video Mixing Renderer) e del filtro overlay mixer espongono **IAMVideoAccelerator**.</span><span class="sxs-lookup"><span data-stu-id="a8de7-108">The input pins of the Video Mixing Renderer (VMR) filter and the Overlay Mixer filter expose **IAMVideoAccelerator**.</span></span>

## <a name="members"></a><span data-ttu-id="a8de7-109">Membri</span><span class="sxs-lookup"><span data-stu-id="a8de7-109">Members</span></span>

<span data-ttu-id="a8de7-110">L'interfaccia **IDirect3DVideoDevice9** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a8de7-110">The **IDirect3DVideoDevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8de7-111">**IDirect3DVideoDevice9** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a8de7-111">**IDirect3DVideoDevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="a8de7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a8de7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8de7-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a8de7-113">Methods</span></span>

<span data-ttu-id="a8de7-114">L'interfaccia **IDirect3DVideoDevice9** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a8de7-114">The **IDirect3DVideoDevice9** interface has these methods.</span></span>



| <span data-ttu-id="a8de7-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a8de7-115">Method</span></span>                                                                                   | <span data-ttu-id="a8de7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8de7-116">Description</span></span>                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8de7-117">**CreateDXVADevice**</span><span class="sxs-lookup"><span data-stu-id="a8de7-117">**CreateDXVADevice**</span></span>](idirect3dvideodevice9-createdxvadevice.md)                       | <span data-ttu-id="a8de7-118">Crea un dispositivo di decodificatore DXVA.</span><span class="sxs-lookup"><span data-stu-id="a8de7-118">Creates a DXVA decoder device.</span></span><br/>                                                                                         |
| [<span data-ttu-id="a8de7-119">**CreateSurface**</span><span class="sxs-lookup"><span data-stu-id="a8de7-119">**CreateSurface**</span></span>](idirect3dvideodevice9-createsurface.md)                             | <span data-ttu-id="a8de7-120">Crea una superficie compressa per la decodifica DXVA.</span><span class="sxs-lookup"><span data-stu-id="a8de7-120">Creates a compressed surface for DXVA decoding.</span></span><br/>                                                                        |
| [<span data-ttu-id="a8de7-121">**GetDXVACompressedBufferInfo**</span><span class="sxs-lookup"><span data-stu-id="a8de7-121">**GetDXVACompressedBufferInfo**</span></span>](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | <span data-ttu-id="a8de7-122">Ottiene informazioni sui buffer compressi necessari per la decodifica con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="a8de7-122">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span><br/>                                |
| [<span data-ttu-id="a8de7-123">**GetDXVAGuids**</span><span class="sxs-lookup"><span data-stu-id="a8de7-123">**GetDXVAGuids**</span></span>](idirect3dvideodevice9-getdxvaguids.md)                               | <span data-ttu-id="a8de7-124">Ottiene un elenco dei profili DXVA supportati dal driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a8de7-124">Gets a list of the DXVA profiles that are supported by the display driver.</span></span><br/>                                             |
| [<span data-ttu-id="a8de7-125">**GetDXVAInternalInfo**</span><span class="sxs-lookup"><span data-stu-id="a8de7-125">**GetDXVAInternalInfo**</span></span>](idirect3dvideodevice9-getdxvainternalinfo.md)                 | <span data-ttu-id="a8de7-126">Esegue una query per la quantità di memoria Scratch che l'HAL (Hardware Abstraction Layer) alloca per l'uso privato.</span><span class="sxs-lookup"><span data-stu-id="a8de7-126">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span> <br/> |
| [<span data-ttu-id="a8de7-127">**GetUncompressedDXVAFormats**</span><span class="sxs-lookup"><span data-stu-id="a8de7-127">**GetUncompressedDXVAFormats**</span></span>](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | <span data-ttu-id="a8de7-128">Ottiene un elenco di formati di pixel non compressi di cui è possibile eseguire il rendering utilizzando un profilo DXVA specificato.</span><span class="sxs-lookup"><span data-stu-id="a8de7-128">Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="a8de7-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8de7-129">Remarks</span></span>

<span data-ttu-id="a8de7-130">Per ottenere un puntatore a questa interfaccia, chiamare **QueryInterface** su un puntatore [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) o [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .</span><span class="sxs-lookup"><span data-stu-id="a8de7-130">To get a pointer to this interface, call **QueryInterface** on an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) or [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) pointer.</span></span>

<span data-ttu-id="a8de7-131">Questa interfaccia supporta solo DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="a8de7-131">This interface supports DXVA 1.0 only.</span></span> <span data-ttu-id="a8de7-132">Non supporta DXVA 2,0.</span><span class="sxs-lookup"><span data-stu-id="a8de7-132">It does not support DXVA 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8de7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8de7-133">Requirements</span></span>



| <span data-ttu-id="a8de7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8de7-134">Requirement</span></span> | <span data-ttu-id="a8de7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a8de7-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a8de7-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8de7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a8de7-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8de7-137">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8de7-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8de7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a8de7-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8de7-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a8de7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8de7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8de7-141"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8de7-141"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8de7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8de7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8de7-143">Interfacce video Direct3D</span><span class="sxs-lookup"><span data-stu-id="a8de7-143">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a8de7-144">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="a8de7-144">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="a8de7-145">Specifica DXVA 1,0</span><span class="sxs-lookup"><span data-stu-id="a8de7-145">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
