---
description: Contiene il timestamp del driver di dispositivo.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: Attributo MFSampleExtension_DeviceTimestamp (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880617"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a><span data-ttu-id="f0615-103">\_Attributo DeviceTimestamp di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="f0615-103">MFSampleExtension\_DeviceTimestamp attribute</span></span>

<span data-ttu-id="f0615-104">Contiene il timestamp del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0615-104">Contains the time stamp from the device driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0615-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f0615-105">Data type</span></span>

<span data-ttu-id="f0615-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f0615-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="f0615-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="f0615-107">Get/set</span></span>

<span data-ttu-id="f0615-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="f0615-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="f0615-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="f0615-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f0615-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="f0615-110">Applies to</span></span>

[<span data-ttu-id="f0615-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="f0615-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="f0615-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0615-112">Remarks</span></span>

<span data-ttu-id="f0615-113">Questo attributo è impostato su esempi di supporti creati da un'origine multimediale per un dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f0615-113">This attribute is set on media samples created by a media source for a capture device.</span></span> <span data-ttu-id="f0615-114">Il valore di questo attributo si trova nel dominio [**MFTIME**](mftime.md) , condividendo un'epoca con il contatore delle prestazioni delle query (QPC) e sempre espressa in unità 100 ns.</span><span class="sxs-lookup"><span data-stu-id="f0615-114">This attribute's value is in the [**MFTIME**](mftime.md) domain, sharing an epoch with query performance counter (QPC) time and always expressed in 100ns units.</span></span> <span data-ttu-id="f0615-115">Questo attributo è disponibile per MFTs inserito nella pipeline di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f0615-115">This attribute is available for MFTs inserted into the capture pipeline.</span></span>

<span data-ttu-id="f0615-116">Per ottenere il timestamp relativo all'inizio del flusso, chiamare il metodo [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .</span><span class="sxs-lookup"><span data-stu-id="f0615-116">To get the time stamp relative to the start of streaming, call the [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) method.</span></span>

<span data-ttu-id="f0615-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f0615-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0615-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0615-118">Requirements</span></span>



| <span data-ttu-id="f0615-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0615-119">Requirement</span></span> | <span data-ttu-id="f0615-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f0615-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0615-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0615-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0615-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f0615-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f0615-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0615-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0615-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0615-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f0615-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0615-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0615-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0615-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0615-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0615-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0615-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0615-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0615-129">Acquisizione audio/video in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0615-129">Audio/Video Capture in Media Foundation</span></span>](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f0615-130">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="f0615-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




