---
description: Identifica il flusso che ha generato un evento di acquisizione.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: Attributo MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880241"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a><span data-ttu-id="9dfa7-103">\_Attributo di \_ \_ indice del flusso di eventi del motore di \_ acquisizione MF \_</span><span class="sxs-lookup"><span data-stu-id="9dfa7-103">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX attribute</span></span>

<span data-ttu-id="9dfa7-104">Identifica il flusso che ha generato un evento di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9dfa7-104">Identifies which stream generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="9dfa7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9dfa7-105">Data type</span></span>

<span data-ttu-id="9dfa7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9dfa7-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9dfa7-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="9dfa7-107">Get/set</span></span>

<span data-ttu-id="9dfa7-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9dfa7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="9dfa7-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dfa7-109">Remarks</span></span>

<span data-ttu-id="9dfa7-110">Questo attributo viene visualizzato in alcuni eventi del motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9dfa7-110">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="9dfa7-111">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) sull'oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="9dfa7-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) on the event object.</span></span> <span data-ttu-id="9dfa7-112">L'oggetto evento viene passato all'applicazione tramite il metodo [**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="9dfa7-112">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dfa7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dfa7-113">Requirements</span></span>



| <span data-ttu-id="9dfa7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dfa7-114">Requirement</span></span> | <span data-ttu-id="9dfa7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9dfa7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfa7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dfa7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9dfa7-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9dfa7-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="9dfa7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dfa7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9dfa7-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9dfa7-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9dfa7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dfa7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dfa7-121"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dfa7-121"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dfa7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dfa7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfa7-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9dfa7-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9dfa7-124">**IMFCaptureEngineOnEventCallback:: OnEvent**</span><span class="sxs-lookup"><span data-stu-id="9dfa7-124">**IMFCaptureEngineOnEventCallback::OnEvent**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




