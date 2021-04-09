---
description: Contiene un puntatore agli attributi del flusso del flusso connesso su una trasformazione di Media Foundation basata su hardware.
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Attributo MFT_CONNECTED_STREAM_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880606"
---
# <a name="mft_connected_stream_attribute-attribute"></a><span data-ttu-id="01b52-103">\_ \_ Attributo attributo flusso connesso MFT \_</span><span class="sxs-lookup"><span data-stu-id="01b52-103">MFT\_CONNECTED\_STREAM\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="01b52-104">Contiene un puntatore agli attributi del flusso del flusso connesso su una trasformazione di Media Foundation basata su hardware.</span><span class="sxs-lookup"><span data-stu-id="01b52-104">Contains a pointer to the stream attributes of the connected stream on a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="01b52-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="01b52-105">Data type</span></span>

<span data-ttu-id="01b52-106">**IMFAttributes \** _ archiviato come _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="01b52-106">**IMFAttributes\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="01b52-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="01b52-107">Get/set</span></span>

<span data-ttu-id="01b52-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="01b52-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="01b52-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="01b52-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="01b52-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="01b52-110">Remarks</span></span>

<span data-ttu-id="01b52-111">Le applicazioni in genere non utilizzano questo attributo.</span><span class="sxs-lookup"><span data-stu-id="01b52-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="01b52-112">Questo attributo viene usato per MFTs che fungono da proxy per un dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="01b52-112">This attribute is used for MFTs that act as proxies to a hardware device.</span></span> <span data-ttu-id="01b52-113">Per informazioni dettagliate, vedere [hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="01b52-113">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>

<span data-ttu-id="01b52-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="01b52-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b52-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01b52-115">Requirements</span></span>



| <span data-ttu-id="01b52-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b52-116">Requirement</span></span> | <span data-ttu-id="01b52-117">Valore</span><span class="sxs-lookup"><span data-stu-id="01b52-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b52-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b52-118">Minimum supported client</span></span><br/> | <span data-ttu-id="01b52-119">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="01b52-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="01b52-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b52-120">Minimum supported server</span></span><br/> | <span data-ttu-id="01b52-121">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="01b52-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="01b52-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01b52-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b52-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b52-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b52-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01b52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b52-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01b52-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01b52-126">MFT \_ connesso \_ al \_ \_ flusso HW</span><span class="sxs-lookup"><span data-stu-id="01b52-126">MFT\_CONNECTED\_TO\_HW\_STREAM</span></span>](mft-connected-to-hw-stream.md)
</dt> <dt>

[<span data-ttu-id="01b52-127">MFTs hardware</span><span class="sxs-lookup"><span data-stu-id="01b52-127">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="01b52-128">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="01b52-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




