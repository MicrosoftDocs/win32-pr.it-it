---
description: 'Indica che il tipo di output è stato impostato sul motore di acquisizione in risposta a IMFCaptureSink2:: SetOutputType.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: Attributo MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351646"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a><span data-ttu-id="3b9a7-103">\_ \_ \_ \_ \_ Attributo set del tipo di supporto di output del motore \_ di acquisizione MF</span><span class="sxs-lookup"><span data-stu-id="3b9a7-103">MF\_CAPTURE\_ENGINE\_OUTPUT\_MEDIA\_TYPE\_SET attribute</span></span>

<span data-ttu-id="3b9a7-104">Indica che il tipo di output è stato impostato sul motore di acquisizione in risposta a [**IMFCaptureSink2:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="3b9a7-104">Indicates that the output type has been set on the capture engine in response to [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="data-type"></a><span data-ttu-id="3b9a7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3b9a7-105">Data type</span></span>

<span data-ttu-id="3b9a7-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="3b9a7-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b9a7-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b9a7-107">Remarks</span></span>

<span data-ttu-id="3b9a7-108">È possibile chiamare [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) per verificare se l'operazione ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="3b9a7-108">You can call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) to find out if the operation was successful or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b9a7-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b9a7-109">Requirements</span></span>



| <span data-ttu-id="3b9a7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b9a7-110">Requirement</span></span> | <span data-ttu-id="3b9a7-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3b9a7-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9a7-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b9a7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3b9a7-113">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3b9a7-113">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3b9a7-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b9a7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3b9a7-115">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b9a7-115">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b9a7-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b9a7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b9a7-117"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9a7-117"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b9a7-118">IDL</span><span class="sxs-lookup"><span data-stu-id="3b9a7-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b9a7-119"><dt>Mfcaptureengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b9a7-119"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9a7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b9a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9a7-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3b9a7-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3b9a7-122">**IMFCaptureSink2::SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="3b9a7-122">**IMFCaptureSink2::SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




