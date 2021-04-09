---
description: Specifica la modalità di utilizzo per un codificatore H. 264 UVC.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: Attributo MF_MT_H264_USAGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad5239c81e490f5069b8a6f95d4a91c1f150f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129551"
---
# <a name="mf_mt_h264_usage-attribute"></a><span data-ttu-id="860e6-103">\_ \_ Attributo Usage MF mt H264 \_</span><span class="sxs-lookup"><span data-stu-id="860e6-103">MF\_MT\_H264\_USAGE attribute</span></span>

<span data-ttu-id="860e6-104">Specifica la modalità di utilizzo per un codificatore H. 264 UVC.</span><span class="sxs-lookup"><span data-stu-id="860e6-104">Specifies the usage mode for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="860e6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="860e6-105">Data type</span></span>

<span data-ttu-id="860e6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="860e6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="860e6-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="860e6-107">Get/set</span></span>

<span data-ttu-id="860e6-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="860e6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="860e6-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="860e6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="860e6-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="860e6-110">Applies to</span></span>

[<span data-ttu-id="860e6-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="860e6-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="860e6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="860e6-112">Remarks</span></span>

<span data-ttu-id="860e6-113">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="860e6-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="860e6-114">Il valore corrisponde al campo **bUsage** nel controllo probe/commit 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="860e6-114">The value corresponds to the **bUsage** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="860e6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="860e6-115">Requirements</span></span>



| <span data-ttu-id="860e6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="860e6-116">Requirement</span></span> | <span data-ttu-id="860e6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="860e6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="860e6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="860e6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="860e6-119">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="860e6-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="860e6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="860e6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="860e6-121">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="860e6-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="860e6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="860e6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="860e6-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="860e6-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="860e6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="860e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="860e6-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="860e6-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="860e6-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="860e6-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




