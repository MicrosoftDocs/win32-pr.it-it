---
description: Contiene il nome visualizzato per una trasformazione Media Foundation basata su hardware (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: Attributo MFT_FRIENDLY_NAME_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310221"
---
# <a name="mft_friendly_name_attribute-attribute"></a><span data-ttu-id="dc2d0-103">\_Attributo dell' \_ attributo del nome descrittivo MFT \_</span><span class="sxs-lookup"><span data-stu-id="dc2d0-103">MFT\_FRIENDLY\_NAME\_Attribute attribute</span></span>

<span data-ttu-id="dc2d0-104">Contiene il nome visualizzato per una trasformazione Media Foundation basata su hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="dc2d0-104">Contains the display name for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="dc2d0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="dc2d0-105">Data type</span></span>

<span data-ttu-id="dc2d0-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="dc2d0-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="dc2d0-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="dc2d0-107">Get/set</span></span>

<span data-ttu-id="dc2d0-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="dc2d0-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="dc2d0-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="dc2d0-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc2d0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc2d0-110">Remarks</span></span>

<span data-ttu-id="dc2d0-111">Questo attributo è supportato da MFTs basato su hardware.</span><span class="sxs-lookup"><span data-stu-id="dc2d0-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="dc2d0-112">Viene inoltre impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) allocati dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando tali puntatori rappresentano MFTS basati su hardware.</span><span class="sxs-lookup"><span data-stu-id="dc2d0-112">It is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="dc2d0-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dc2d0-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc2d0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc2d0-114">Requirements</span></span>



| <span data-ttu-id="dc2d0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc2d0-115">Requirement</span></span> | <span data-ttu-id="dc2d0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2d0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2d0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc2d0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc2d0-118">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dc2d0-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="dc2d0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc2d0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc2d0-120">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dc2d0-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="dc2d0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc2d0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc2d0-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc2d0-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc2d0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc2d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2d0-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc2d0-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dc2d0-125">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="dc2d0-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




