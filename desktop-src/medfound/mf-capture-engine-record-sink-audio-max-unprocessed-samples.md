---
description: Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di record.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Attributo MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344581"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a><span data-ttu-id="c02b9-103">\_Attributo degli \_ \_ esempi non \_ \_ \_ \_ elaborati dell'audio \_ di acquisizione del motore di acquisizione MF max</span><span class="sxs-lookup"><span data-stu-id="c02b9-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="c02b9-104">Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di record.</span><span class="sxs-lookup"><span data-stu-id="c02b9-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="c02b9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c02b9-105">Data type</span></span>

<span data-ttu-id="c02b9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c02b9-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="c02b9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c02b9-107">Remarks</span></span>

<span data-ttu-id="c02b9-108">Per configurare questo attributo nel motore di acquisizione, aggiungerlo al parametro *pAttributes* quando si chiama [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="c02b9-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="c02b9-109">Il valore massimo per questo attributo è 100.</span><span class="sxs-lookup"><span data-stu-id="c02b9-109">The maximum value for this attribute is 100.</span></span>

<span data-ttu-id="c02b9-110">Una volta che il record ha memorizzato nel buffer il numero massimo di campioni non elaborati, specificato dal motore di acquisizione record del motore di acquisizione di un numero massimo di campioni \_ \_ \_ \_ \_ \_ \_ non elaborati \_ , Elimina la frequenza dei fotogrammi eliminando gli esempi.</span><span class="sxs-lookup"><span data-stu-id="c02b9-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="c02b9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c02b9-111">Requirements</span></span>



| <span data-ttu-id="c02b9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c02b9-112">Requirement</span></span> | <span data-ttu-id="c02b9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c02b9-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c02b9-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c02b9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c02b9-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c02b9-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c02b9-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c02b9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c02b9-117">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c02b9-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c02b9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c02b9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c02b9-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02b9-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c02b9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c02b9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02b9-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c02b9-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c02b9-122">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="c02b9-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="c02b9-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="c02b9-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




