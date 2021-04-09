---
description: Specifica se il motore di acquisizione acquisisce video ma non audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Attributo MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967048"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a><span data-ttu-id="100e3-103">\_Motore di acquisizione MF usare l' \_ \_ \_ \_ \_ attributo solo dispositivo video</span><span class="sxs-lookup"><span data-stu-id="100e3-103">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="100e3-104">Specifica se il motore di acquisizione acquisisce video ma non audio.</span><span class="sxs-lookup"><span data-stu-id="100e3-104">Specifies whether the capture engine captures video but not audio.</span></span>

## <a name="data-type"></a><span data-ttu-id="100e3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="100e3-105">Data type</span></span>

<span data-ttu-id="100e3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="100e3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="100e3-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="100e3-107">Remarks</span></span>

<span data-ttu-id="100e3-108">Se questo attributo è **true**, il motore di acquisizione non seleziona né usa un dispositivo di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="100e3-108">If this attribute is **TRUE**, the capture engine does not select or use an audio capture device.</span></span> <span data-ttu-id="100e3-109">Impostare questo attributo su **true** se si desidera acquisire video senza audio.</span><span class="sxs-lookup"><span data-stu-id="100e3-109">Set this attribute to **TRUE** if you want to capture video without audio.</span></span> <span data-ttu-id="100e3-110">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="100e3-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="100e3-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="100e3-111">Requirements</span></span>



| <span data-ttu-id="100e3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="100e3-112">Requirement</span></span> | <span data-ttu-id="100e3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="100e3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="100e3-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="100e3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="100e3-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="100e3-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="100e3-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="100e3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="100e3-117">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="100e3-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="100e3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="100e3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="100e3-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="100e3-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="100e3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="100e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="100e3-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="100e3-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="100e3-122">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="100e3-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="100e3-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="100e3-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




