---
description: Specifica la modalità di controllo della frequenza per un flusso video H. 264.
ms.assetid: EA8EFEFA-9292-4D7B-BF5D-DE5239BB1D2C
title: Attributo MF_MT_H264_RATE_CONTROL_MODES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3fc19070cd3b45aa25a1307a216f611dce1fd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307514"
---
# <a name="mf_mt_h264_rate_control_modes-attribute"></a><span data-ttu-id="cd28b-103">\_ \_ \_ \_ Attributo modalità di controllo della velocità MF mt H264 \_</span><span class="sxs-lookup"><span data-stu-id="cd28b-103">MF\_MT\_H264\_RATE\_CONTROL\_MODES attribute</span></span>

<span data-ttu-id="cd28b-104">Specifica la modalità di controllo della frequenza per un flusso video H. 264.</span><span class="sxs-lookup"><span data-stu-id="cd28b-104">Specifies the rate-control mode for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="cd28b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cd28b-105">Data type</span></span>

<span data-ttu-id="cd28b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cd28b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="cd28b-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="cd28b-107">Get/set</span></span>

<span data-ttu-id="cd28b-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="cd28b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="cd28b-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="cd28b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="cd28b-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="cd28b-110">Applies to</span></span>

[<span data-ttu-id="cd28b-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="cd28b-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="cd28b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd28b-112">Remarks</span></span>

<span data-ttu-id="cd28b-113">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="cd28b-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="cd28b-114">Il valore corrisponde al campo **bmRateControlModes** nel controllo probe/commit 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="cd28b-114">The value corresponds to the **bmRateControlModes** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd28b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd28b-115">Requirements</span></span>



| <span data-ttu-id="cd28b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd28b-116">Requirement</span></span> | <span data-ttu-id="cd28b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cd28b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd28b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd28b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd28b-119">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cd28b-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="cd28b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd28b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd28b-121">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="cd28b-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="cd28b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd28b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd28b-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd28b-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd28b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd28b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd28b-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cd28b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cd28b-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="cd28b-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




