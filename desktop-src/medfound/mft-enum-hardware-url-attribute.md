---
description: Contiene il collegamento simbolico per una trasformazione di Media Foundation basata su hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Attributo MFT_ENUM_HARDWARE_URL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226911"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a><span data-ttu-id="b41bb-103">\_ \_ \_ Attributo attributo URL dell' \_ enumerazione MFT</span><span class="sxs-lookup"><span data-stu-id="b41bb-103">MFT\_ENUM\_HARDWARE\_URL\_Attribute attribute</span></span>

<span data-ttu-id="b41bb-104">Contiene il collegamento simbolico per una trasformazione di Media Foundation basata su hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="b41bb-104">Contains the symbolic link for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="b41bb-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b41bb-105">Data type</span></span>

<span data-ttu-id="b41bb-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b41bb-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="b41bb-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b41bb-107">Get/set</span></span>

<span data-ttu-id="b41bb-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="b41bb-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b41bb-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="b41bb-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="b41bb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b41bb-110">Remarks</span></span>

<span data-ttu-id="b41bb-111">Questo attributo è supportato da MFTs basato su hardware.</span><span class="sxs-lookup"><span data-stu-id="b41bb-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="b41bb-112">Il valore dell'attributo è il collegamento simbolico per il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b41bb-112">The value of the attribute is the symbolic link for the device driver.</span></span> <span data-ttu-id="b41bb-113">Questo attributo viene inoltre impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) allocati dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando tali puntatori rappresentano MFTS basati su hardware.</span><span class="sxs-lookup"><span data-stu-id="b41bb-113">This attribute is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="b41bb-114">Il collegamento simbolico deve essere considerato una stringa opaca.</span><span class="sxs-lookup"><span data-stu-id="b41bb-114">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="b41bb-115">Per ottenere il nome visualizzato per un dispositivo, eseguire una query sull'attributo [ \_ \_ nome descrittivo di MFT](mft-friendly-name-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b41bb-115">To get the display name for a device, query the [MFT\_FRIENDLY\_NAME](mft-friendly-name-attribute.md) attribute.</span></span>

<span data-ttu-id="b41bb-116">Per il software MFTs non deve essere impostato questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b41bb-116">Software MFTs should not have this attribute set.</span></span>

<span data-ttu-id="b41bb-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b41bb-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b41bb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b41bb-118">Requirements</span></span>



| <span data-ttu-id="b41bb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b41bb-119">Requirement</span></span> | <span data-ttu-id="b41bb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b41bb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41bb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b41bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b41bb-122">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b41bb-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b41bb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b41bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b41bb-124">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b41bb-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b41bb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b41bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b41bb-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b41bb-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b41bb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b41bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41bb-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b41bb-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b41bb-129">MFTs hardware</span><span class="sxs-lookup"><span data-stu-id="b41bb-129">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="b41bb-130">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="b41bb-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




