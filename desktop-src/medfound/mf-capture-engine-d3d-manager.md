---
description: Imposta un puntatore al Gestione dispositivi DXGI nel motore di acquisizione.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Attributo MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129799"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a><span data-ttu-id="b881d-103">\_ \_ \_ Attributo gestione D3D del motore di acquisizione MF \_</span><span class="sxs-lookup"><span data-stu-id="b881d-103">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="b881d-104">Imposta un puntatore al Gestione dispositivi DXGI nel motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b881d-104">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="b881d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b881d-105">Data type</span></span>

<span data-ttu-id="b881d-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="b881d-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="b881d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b881d-107">Remarks</span></span>

<span data-ttu-id="b881d-108">Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="b881d-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span> <span data-ttu-id="b881d-109">Questo attributo consente al motore di acquisizione di allocare i fotogrammi video usando le superfici DXGI e di usare l'accelerazione hardware per la decodifica e l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="b881d-109">This attribute enables the capture engine to allocate video frames using DXGI surfaces, and to use hardware acceleration for decoding and video processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b881d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b881d-110">Requirements</span></span>



| <span data-ttu-id="b881d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b881d-111">Requirement</span></span> | <span data-ttu-id="b881d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b881d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b881d-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b881d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b881d-114">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b881d-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b881d-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b881d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b881d-116">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b881d-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b881d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b881d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b881d-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="b881d-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b881d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b881d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b881d-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b881d-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b881d-121">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="b881d-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="b881d-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="b881d-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




