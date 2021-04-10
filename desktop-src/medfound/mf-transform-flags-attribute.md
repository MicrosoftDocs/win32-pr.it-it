---
description: Contiene i flag per un oggetto attivazione di Media Foundation Transform (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: Attributo MF_TRANSFORM_FLAGS_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f3e334b83bbe8ce50f8770eb33e1e7a4c799c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966896"
---
# <a name="mf_transform_flags_attribute-attribute"></a><span data-ttu-id="398b7-103">\_Attributo dell'attributo di trasformazione MF \_ flags \_</span><span class="sxs-lookup"><span data-stu-id="398b7-103">MF\_TRANSFORM\_FLAGS\_Attribute attribute</span></span>

<span data-ttu-id="398b7-104">Contiene i flag per un oggetto attivazione di Media Foundation Transform (MFT).</span><span class="sxs-lookup"><span data-stu-id="398b7-104">Contains flags for a Media Foundation transform (MFT) activation object.</span></span>

## <a name="data-type"></a><span data-ttu-id="398b7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="398b7-105">Data type</span></span>

<span data-ttu-id="398b7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="398b7-106">**UINT32**</span></span>

<span data-ttu-id="398b7-107">Il valore è **un operatore OR** bit per bit di flag dell'enumerazione del [**\_ \_ \_ flag**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) di enumerazione MFT.</span><span class="sxs-lookup"><span data-stu-id="398b7-107">The value is a bitwise **OR** of flags from the [**\_MFT\_ENUM\_FLAG**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) enumeration.</span></span>

## <a name="getset"></a><span data-ttu-id="398b7-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="398b7-108">Get/set</span></span>

<span data-ttu-id="398b7-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="398b7-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="398b7-110">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="398b7-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="398b7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="398b7-111">Remarks</span></span>

<span data-ttu-id="398b7-112">Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="398b7-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="398b7-113">L'attributo contiene i flag che descrivono il MFT.</span><span class="sxs-lookup"><span data-stu-id="398b7-113">The attribute contains flags that describe the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="398b7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="398b7-114">Requirements</span></span>



| <span data-ttu-id="398b7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="398b7-115">Requirement</span></span> | <span data-ttu-id="398b7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="398b7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="398b7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="398b7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="398b7-118">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="398b7-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="398b7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="398b7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="398b7-120">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="398b7-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="398b7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="398b7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="398b7-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="398b7-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="398b7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="398b7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398b7-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="398b7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="398b7-125">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="398b7-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
