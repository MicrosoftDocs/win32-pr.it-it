---
description: Specifica la categoria per una trasformazione Media Foundation (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: Attributo MF_TRANSFORM_CATEGORY_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226371"
---
# <a name="mf_transform_category_attribute-attribute"></a><span data-ttu-id="b34e8-103">\_Attributo dell' \_ \_ attributo Category di MF Transform</span><span class="sxs-lookup"><span data-stu-id="b34e8-103">MF\_TRANSFORM\_CATEGORY\_Attribute attribute</span></span>

<span data-ttu-id="b34e8-104">Specifica la categoria per una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="b34e8-104">Specifies the category for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="b34e8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b34e8-105">Data type</span></span>

<span data-ttu-id="b34e8-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b34e8-106">**GUID**</span></span>

<span data-ttu-id="b34e8-107">Per un elenco di valori possibili, vedere [**la \_ categoria MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="b34e8-107">For a list of possible values, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

## <a name="getset"></a><span data-ttu-id="b34e8-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b34e8-108">Get/set</span></span>

<span data-ttu-id="b34e8-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="b34e8-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="b34e8-110">Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="b34e8-110">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="b34e8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b34e8-111">Remarks</span></span>

<span data-ttu-id="b34e8-112">Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="b34e8-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34e8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b34e8-113">Requirements</span></span>



| <span data-ttu-id="b34e8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b34e8-114">Requirement</span></span> | <span data-ttu-id="b34e8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b34e8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34e8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b34e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b34e8-117">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b34e8-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b34e8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b34e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b34e8-119">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b34e8-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b34e8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b34e8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b34e8-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b34e8-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b34e8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b34e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34e8-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b34e8-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b34e8-124">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="b34e8-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




