---
description: Specifica se il motore di acquisizione usa l'accelerazione video DirectX (DXVA) per la decodifica dei video.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Attributo MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343936"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a><span data-ttu-id="649c5-103">\_Motore di acquisizione MF disabilitare l' \_ \_ \_ attributo DXVA</span><span class="sxs-lookup"><span data-stu-id="649c5-103">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="649c5-104">Specifica se il motore di acquisizione usa l'accelerazione video DirectX (DXVA) per la decodifica dei video.</span><span class="sxs-lookup"><span data-stu-id="649c5-104">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="649c5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="649c5-105">Data type</span></span>

<span data-ttu-id="649c5-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="649c5-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="649c5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="649c5-107">Remarks</span></span>

<span data-ttu-id="649c5-108">Questo attributo si applica se vengono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="649c5-108">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="649c5-109">Il motore di acquisizione decodifica un flusso video compresso dal dispositivo di acquisizione, ad esempio se il dispositivo di acquisizione genera il video H. 264.</span><span class="sxs-lookup"><span data-stu-id="649c5-109">The capture engine decodes a compressed video stream from the capture device (for example, if the capture device outputs H.264 video).</span></span>
-   <span data-ttu-id="649c5-110">Il decodificatore video supporta la decodifica con accelerazione hardware con DXVA.</span><span class="sxs-lookup"><span data-stu-id="649c5-110">The video decoder supports hardware-accelerated decoding using DXVA.</span></span>
-   <span data-ttu-id="649c5-111">L'applicazione usa l'attributo di [ \_ \_ \_ \_ gestione D3D del motore di acquisizione MF](mf-capture-engine-d3d-manager.md) per impostare il gestione dispositivi DXGI nel motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="649c5-111">The application uses the [MF\_CAPTURE\_ENGINE\_D3D\_MANAGER](mf-capture-engine-d3d-manager.md) attribute to set the DXGI Device Manager on the capture engine.</span></span>

<span data-ttu-id="649c5-112">In caso contrario, questo attributo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="649c5-112">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="649c5-113">Questo attributo consente all'applicazione di disabilitare DXVA, pur continuando a eseguire la decodifica nelle superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="649c5-113">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="649c5-114">Il valore predefinito di questo attributo è **false**, vale a dire che la decodifica DXVA è abilitata quando disponibile.</span><span class="sxs-lookup"><span data-stu-id="649c5-114">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="649c5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="649c5-115">Requirements</span></span>



| <span data-ttu-id="649c5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="649c5-116">Requirement</span></span> | <span data-ttu-id="649c5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="649c5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="649c5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="649c5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="649c5-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="649c5-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="649c5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="649c5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="649c5-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="649c5-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="649c5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="649c5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="649c5-123"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="649c5-123"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649c5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="649c5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649c5-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="649c5-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="649c5-126">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="649c5-126">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="649c5-127">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="649c5-127">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




