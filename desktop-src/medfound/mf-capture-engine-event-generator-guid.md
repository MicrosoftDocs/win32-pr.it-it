---
description: Identifica il componente che ha generato un evento di acquisizione.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Attributo MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307980"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a><span data-ttu-id="fcfb5-103">\_ \_ \_ \_ Attributo GUID generatore eventi motore di acquisizione \_ MF</span><span class="sxs-lookup"><span data-stu-id="fcfb5-103">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID attribute</span></span>

<span data-ttu-id="fcfb5-104">Identifica il componente che ha generato un evento di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="fcfb5-104">Identifies the component that generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="fcfb5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fcfb5-105">Data type</span></span>

<span data-ttu-id="fcfb5-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="fcfb5-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="fcfb5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcfb5-107">Remarks</span></span>

<span data-ttu-id="fcfb5-108">Questo attributo viene visualizzato in alcuni eventi del motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="fcfb5-108">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="fcfb5-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) sull'oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="fcfb5-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) on the event object.</span></span> <span data-ttu-id="fcfb5-110">L'oggetto evento viene passato all'applicazione tramite il metodo [**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="fcfb5-110">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

<span data-ttu-id="fcfb5-111">Il valore è un identificatore di interfaccia per il componente che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="fcfb5-111">The value is an interface identifier for the component that generated the event.</span></span> <span data-ttu-id="fcfb5-112">Ad esempio, il valore **IID \_ IMFCapturePreviewSink** indica il sink di anteprima ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span><span class="sxs-lookup"><span data-stu-id="fcfb5-112">For example, the value **IID\_IMFCapturePreviewSink** indicates the preview sink ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span></span> <span data-ttu-id="fcfb5-113">Non tutti gli eventi di acquisizione contengono questo attributo.</span><span class="sxs-lookup"><span data-stu-id="fcfb5-113">Not every capture event contains this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcfb5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcfb5-114">Requirements</span></span>



| <span data-ttu-id="fcfb5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcfb5-115">Requirement</span></span> | <span data-ttu-id="fcfb5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fcfb5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfb5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcfb5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fcfb5-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fcfb5-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="fcfb5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcfb5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fcfb5-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fcfb5-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fcfb5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcfb5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcfb5-122"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcfb5-122"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcfb5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcfb5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcfb5-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fcfb5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fcfb5-125">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="fcfb5-125">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="fcfb5-126">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="fcfb5-126">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




