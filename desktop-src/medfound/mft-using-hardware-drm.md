---
description: Specifica se IMFTransform utilizza DRM hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485348"
---
# <a name="mft_using_hardware_drm-attribute"></a><span data-ttu-id="7b720-103">MFT \_ con \_ \_ attributo DRM hardware</span><span class="sxs-lookup"><span data-stu-id="7b720-103">MFT\_USING\_HARDWARE\_DRM attribute</span></span>

<span data-ttu-id="7b720-104">Specifica se IMFTransform utilizza DRM hardware.</span><span class="sxs-lookup"><span data-stu-id="7b720-104">Specifies whether the IMFTransform is using hardware DRM.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b720-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7b720-105">Data type</span></span>

<span data-ttu-id="7b720-106">**UInt32** (considerato **bool**)</span><span class="sxs-lookup"><span data-stu-id="7b720-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="7b720-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="7b720-107">Get/set</span></span>

<span data-ttu-id="7b720-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7b720-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7b720-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="7b720-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7b720-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="7b720-110">Applies to</span></span>

[<span data-ttu-id="7b720-111">**IMTransfrom**</span><span class="sxs-lookup"><span data-stu-id="7b720-111">**IMTransfrom**</span></span>](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a><span data-ttu-id="7b720-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b720-112">Remarks</span></span>

<span data-ttu-id="7b720-113">Se un MFT Decrypter specifica che questo attributo è impostato su 1, utilizza DRM hardware.</span><span class="sxs-lookup"><span data-stu-id="7b720-113">If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM.</span></span> <span data-ttu-id="7b720-114">Se un MFT Decrypter specifica che questo attributo è impostato su 0, non sta utilizzando DRM hardware.</span><span class="sxs-lookup"><span data-stu-id="7b720-114">If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM.</span></span> <span data-ttu-id="7b720-115">Se un MFT Decrypter non specifica questo attributo o lo specifica con un valore diverso, non lo è o non è in grado di indicare se sta utilizzando DRM hardware.</span><span class="sxs-lookup"><span data-stu-id="7b720-115">If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM.</span></span>


<span data-ttu-id="7b720-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7b720-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b720-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b720-117">Requirements</span></span>



| <span data-ttu-id="7b720-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b720-118">Requirement</span></span> | <span data-ttu-id="7b720-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7b720-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b720-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b720-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b720-121">Aggiornamento di Windows 10 aprile 2020</span><span class="sxs-lookup"><span data-stu-id="7b720-121">Windows 10 April 2020 Update</span></span>   <br/>                                       |
| <span data-ttu-id="7b720-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b720-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b720-123">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7b720-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7b720-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b720-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b720-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b720-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b720-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b720-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b720-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b720-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="7b720-128">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="7b720-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




