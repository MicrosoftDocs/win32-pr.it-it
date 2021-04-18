---
description: Specifica se un tipo di supporto video richiede l'applicazione della protezione della copia.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: Attributo MF_MT_DRM_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315034"
---
# <a name="mf_mt_drm_flags-attribute"></a><span data-ttu-id="50268-103">\_ \_ Attributo flag DRM MF mt \_</span><span class="sxs-lookup"><span data-stu-id="50268-103">MF\_MT\_DRM\_FLAGS attribute</span></span>

<span data-ttu-id="50268-104">Specifica se un tipo di supporto video richiede l'applicazione della protezione della copia.</span><span class="sxs-lookup"><span data-stu-id="50268-104">Specifies whether a video media type requires the enforcement of copy protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="50268-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="50268-105">Data type</span></span>

<span data-ttu-id="50268-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="50268-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="50268-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="50268-107">Remarks</span></span>

<span data-ttu-id="50268-108">Il valore di questo attributo è un membro dell'enumerazione [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .</span><span class="sxs-lookup"><span data-stu-id="50268-108">The value of this attribute is a member of the [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) enumeration.</span></span>

<span data-ttu-id="50268-109">Questo attributo fornisce un suggerimento per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="50268-109">This attribute provides a hint to the application.</span></span> <span data-ttu-id="50268-110">Non viene utilizzato per applicare la protezione della copia o per specificare il meccanismo di protezione della copia.</span><span class="sxs-lookup"><span data-stu-id="50268-110">It is not used to enforce copy protection or to specify the copy protection mechanism.</span></span>

<span data-ttu-id="50268-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="50268-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="50268-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50268-112">Requirements</span></span>



| <span data-ttu-id="50268-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="50268-113">Requirement</span></span> | <span data-ttu-id="50268-114">Valore</span><span class="sxs-lookup"><span data-stu-id="50268-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50268-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50268-115">Minimum supported client</span></span><br/> | <span data-ttu-id="50268-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="50268-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="50268-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50268-117">Minimum supported server</span></span><br/> | <span data-ttu-id="50268-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="50268-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="50268-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50268-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="50268-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="50268-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50268-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50268-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50268-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50268-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="50268-123">MF \_ SD \_ protetto</span><span class="sxs-lookup"><span data-stu-id="50268-123">MF\_SD\_PROTECTED</span></span>](mf-sd-protected-attribute.md)
</dt> <dt>

[<span data-ttu-id="50268-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="50268-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="50268-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="50268-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="50268-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="50268-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="50268-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="50268-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




