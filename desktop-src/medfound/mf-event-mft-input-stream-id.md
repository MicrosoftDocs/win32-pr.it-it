---
description: Specifica un flusso di input in una trasformazione Media Foundation (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: Attributo MF_EVENT_MFT_INPUT_STREAM_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d3966c33dc563fc9e38ad367cc675ba6616c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226266"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a><span data-ttu-id="d9ced-103">\_Attributo dell' \_ \_ ID del \_ flusso di input \_ dell'evento di gestione MFT</span><span class="sxs-lookup"><span data-stu-id="d9ced-103">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID attribute</span></span>

<span data-ttu-id="d9ced-104">Specifica un flusso di input in una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d9ced-104">Specifies an input stream on a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="d9ced-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d9ced-105">Data type</span></span>

<span data-ttu-id="d9ced-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d9ced-106">**UINT32**</span></span>

<span data-ttu-id="d9ced-107">Il valore è un identificatore del flusso di input.</span><span class="sxs-lookup"><span data-stu-id="d9ced-107">The value is an input stream identifier.</span></span>

## <a name="getset"></a><span data-ttu-id="d9ced-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="d9ced-108">Get/set</span></span>

<span data-ttu-id="d9ced-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d9ced-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d9ced-110">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="d9ced-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d9ced-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="d9ced-111">Applies to</span></span>

[<span data-ttu-id="d9ced-112">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="d9ced-112">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="d9ced-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9ced-113">Remarks</span></span>

<span data-ttu-id="d9ced-114">Questo attributo viene usato con gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9ced-114">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="d9ced-115">METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="d9ced-115">METransformDrainComplete</span></span>](metransformdraincomplete.md)
-   [<span data-ttu-id="d9ced-116">METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="d9ced-116">METransformNeedInput</span></span>](metransformneedinput.md)

<span data-ttu-id="d9ced-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d9ced-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9ced-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9ced-118">Requirements</span></span>



| <span data-ttu-id="d9ced-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9ced-119">Requirement</span></span> | <span data-ttu-id="d9ced-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d9ced-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ced-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9ced-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9ced-122">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d9ced-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d9ced-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9ced-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9ced-124">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d9ced-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d9ced-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9ced-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9ced-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9ced-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9ced-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9ced-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ced-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9ced-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9ced-129">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="d9ced-129">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="d9ced-130">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="d9ced-130">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




