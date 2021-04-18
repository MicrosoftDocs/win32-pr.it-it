---
description: Specifica l'ID fornitore per un Microsoft Media Foundation basato su hardware.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: Attributo MFT_ENUM_HARDWARE_VENDOR_ID_Attribute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309078"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a><span data-ttu-id="a3612-103">\_ \_ \_ \_ Attributo attributo ID fornitore hardware MFT enum \_</span><span class="sxs-lookup"><span data-stu-id="a3612-103">MFT\_ENUM\_HARDWARE\_VENDOR\_ID\_Attribute attribute</span></span>

<span data-ttu-id="a3612-104">Specifica l'ID fornitore per una trasformazione di Microsoft Media Foundation basata su hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="a3612-104">Specifies the vendor ID for a hardware-based Microsoft Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="a3612-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a3612-105">Data type</span></span>

<span data-ttu-id="a3612-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="a3612-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="a3612-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="a3612-107">Get/set</span></span>

<span data-ttu-id="a3612-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="a3612-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="a3612-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="a3612-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3612-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3612-110">Remarks</span></span>

<span data-ttu-id="a3612-111">Questo attributo è informativo e facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a3612-111">This attribute is informational and optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3612-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3612-112">Requirements</span></span>



| <span data-ttu-id="a3612-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3612-113">Requirement</span></span> | <span data-ttu-id="a3612-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a3612-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3612-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3612-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a3612-116">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a3612-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="a3612-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3612-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a3612-118">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="a3612-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="a3612-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3612-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3612-120"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3612-120"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3612-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3612-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3612-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3612-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a3612-123">MFTs hardware</span><span class="sxs-lookup"><span data-stu-id="a3612-123">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="a3612-124">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="a3612-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




