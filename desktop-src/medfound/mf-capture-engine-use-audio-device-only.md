---
description: Specifica se il motore di acquisizione acquisisce audio ma non video.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Attributo MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966802"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a><span data-ttu-id="f81cb-103">\_Motore di acquisizione MF usare l' \_ \_ \_ \_ \_ attributo solo dispositivo audio</span><span class="sxs-lookup"><span data-stu-id="f81cb-103">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="f81cb-104">Specifica se il motore di acquisizione acquisisce audio ma non video.</span><span class="sxs-lookup"><span data-stu-id="f81cb-104">Specifies whether the capture engine captures audio but not video.</span></span>

## <a name="data-type"></a><span data-ttu-id="f81cb-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f81cb-105">Data type</span></span>

<span data-ttu-id="f81cb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f81cb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f81cb-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f81cb-107">Remarks</span></span>

<span data-ttu-id="f81cb-108">Se questo attributo è **true**, il motore di acquisizione non seleziona né usa un dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="f81cb-108">If this attribute is **TRUE**, the capture engine does not select or use a video capture device.</span></span> <span data-ttu-id="f81cb-109">Impostare questo attributo su **true** se si desidera acquisire audio senza video.</span><span class="sxs-lookup"><span data-stu-id="f81cb-109">Set this attribute to **TRUE** if you want to capture audio without video.</span></span> <span data-ttu-id="f81cb-110">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="f81cb-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81cb-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f81cb-111">Requirements</span></span>



| <span data-ttu-id="f81cb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f81cb-112">Requirement</span></span> | <span data-ttu-id="f81cb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f81cb-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f81cb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f81cb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f81cb-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f81cb-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f81cb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f81cb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f81cb-117">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f81cb-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f81cb-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f81cb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f81cb-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f81cb-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f81cb-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f81cb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81cb-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f81cb-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f81cb-122">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="f81cb-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="f81cb-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f81cb-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




