---
description: Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso video del sink di record.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: Attributo MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752455"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a><span data-ttu-id="f21bb-103">\_Attributo per \_ il \_ \_ \_ \_ numero massimo di \_ campioni elaborati \_ del motore di acquisizione MF video</span><span class="sxs-lookup"><span data-stu-id="f21bb-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="f21bb-104">Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso video del sink di record.</span><span class="sxs-lookup"><span data-stu-id="f21bb-104">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="f21bb-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f21bb-105">Data type</span></span>

<span data-ttu-id="f21bb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f21bb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f21bb-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f21bb-107">Remarks</span></span>

<span data-ttu-id="f21bb-108">Per configurare questo attributo nel motore di acquisizione, aggiungerlo al parametro *pAttributes* quando si chiama [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="f21bb-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="f21bb-109">Il valore massimo per questo attributo è 17.</span><span class="sxs-lookup"><span data-stu-id="f21bb-109">The maximum value for this attribute is 17.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21bb-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f21bb-110">Requirements</span></span>



| <span data-ttu-id="f21bb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f21bb-111">Requirement</span></span> | <span data-ttu-id="f21bb-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f21bb-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21bb-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f21bb-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f21bb-114">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f21bb-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f21bb-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f21bb-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f21bb-116">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f21bb-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f21bb-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f21bb-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f21bb-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f21bb-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f21bb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f21bb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21bb-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f21bb-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f21bb-121">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="f21bb-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="f21bb-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f21bb-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




