---
description: Contiene un valore definito dal chiamante per un evento METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: Attributo MF_EVENT_MFT_CONTEXT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049714"
---
# <a name="mf_event_mft_context-attribute"></a><span data-ttu-id="b3db0-103">\_Attributo di \_ contesto MFT evento \_ MF</span><span class="sxs-lookup"><span data-stu-id="b3db0-103">MF\_EVENT\_MFT\_CONTEXT attribute</span></span>

<span data-ttu-id="b3db0-104">Contiene un valore definito dal chiamante per un evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="b3db0-104">Contains a caller-defined value for an [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3db0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b3db0-105">Data type</span></span>

<span data-ttu-id="b3db0-106">**ULONG \_ PTR** archiviato come **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b3db0-106">**ULONG\_PTR** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="b3db0-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b3db0-107">Get/set</span></span>

<span data-ttu-id="b3db0-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="b3db0-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="b3db0-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="b3db0-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b3db0-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="b3db0-110">Applies to</span></span>

[<span data-ttu-id="b3db0-111">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="b3db0-111">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="b3db0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3db0-112">Remarks</span></span>

<span data-ttu-id="b3db0-113">Questo attributo viene utilizzato con l'evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="b3db0-113">This attribute is used with the [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="b3db0-114">Il valore dell'attributo viene tratto dal parametro *ulParam* del metodo [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .</span><span class="sxs-lookup"><span data-stu-id="b3db0-114">The value of the attribute is taken from the *ulParam* parameter of the [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) method.</span></span>

<span data-ttu-id="b3db0-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b3db0-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3db0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3db0-116">Requirements</span></span>



| <span data-ttu-id="b3db0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3db0-117">Requirement</span></span> | <span data-ttu-id="b3db0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b3db0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3db0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3db0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3db0-120">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b3db0-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b3db0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3db0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3db0-122">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b3db0-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b3db0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3db0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3db0-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3db0-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3db0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3db0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3db0-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3db0-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3db0-127">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="b3db0-127">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="b3db0-128">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="b3db0-128">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




