---
description: Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso video del sink di record.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: Attributo MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f5e297ddb5f06e71fe05a95df73aa205a7889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880238"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a><span data-ttu-id="55537-103">Attributo per i \_ \_ \_ campioni non \_ \_ \_ \_ elaborati \_ del motore di acquisizione MF video Max</span><span class="sxs-lookup"><span data-stu-id="55537-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="55537-104">Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso video del sink di record.</span><span class="sxs-lookup"><span data-stu-id="55537-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="55537-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="55537-105">Data type</span></span>

<span data-ttu-id="55537-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="55537-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="55537-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="55537-107">Remarks</span></span>

<span data-ttu-id="55537-108">Per configurare questo attributo nel motore di acquisizione, aggiungerlo al parametro *pAttributes* quando si chiama [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="55537-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="55537-109">Il valore massimo per questo attributo è 17.</span><span class="sxs-lookup"><span data-stu-id="55537-109">The maximum value for this attribute is 17.</span></span>

<span data-ttu-id="55537-110">Una volta che il record ha memorizzato nel buffer il numero massimo di campioni non elaborati, specificato da MF \_ Capture \_ Engine \_ record \_ sink \_ video \_ Max \_ unprocessed \_ Samples, Elimina la frequenza dei fotogrammi eliminando gli esempi.</span><span class="sxs-lookup"><span data-stu-id="55537-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="55537-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55537-111">Requirements</span></span>



| <span data-ttu-id="55537-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="55537-112">Requirement</span></span> | <span data-ttu-id="55537-113">Valore</span><span class="sxs-lookup"><span data-stu-id="55537-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="55537-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55537-114">Minimum supported client</span></span><br/> | <span data-ttu-id="55537-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="55537-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="55537-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55537-116">Minimum supported server</span></span><br/> | <span data-ttu-id="55537-117">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="55537-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55537-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55537-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="55537-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="55537-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55537-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55537-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55537-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55537-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="55537-122">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="55537-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="55537-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="55537-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




