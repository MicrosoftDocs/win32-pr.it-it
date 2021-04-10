---
description: Specifica se il caricatore della topologia modificherà i tipi di supporto in una trasformazione Media Foundation (MFT). Le applicazioni in genere non utilizzano questo attributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Attributo MF_ACTIVATE_MFT_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130726"
---
# <a name="mf_activate_mft_locked-attribute"></a><span data-ttu-id="75178-104">MF \_ Activate \_ - \_ attributo bloccato MFT</span><span class="sxs-lookup"><span data-stu-id="75178-104">MF\_ACTIVATE\_MFT\_LOCKED attribute</span></span>

<span data-ttu-id="75178-105">Specifica se il caricatore della topologia modificherà i tipi di supporto in una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="75178-105">Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT).</span></span> <span data-ttu-id="75178-106">Le applicazioni in genere non utilizzano questo attributo.</span><span class="sxs-lookup"><span data-stu-id="75178-106">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="75178-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="75178-107">Data type</span></span>

<span data-ttu-id="75178-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="75178-108">**UINT32**</span></span>

<span data-ttu-id="75178-109">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="75178-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75178-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="75178-110">Remarks</span></span>

<span data-ttu-id="75178-111">Se il valore di questo attributo è diverso da zero, il caricatore della topologia non modificherà i tipi di supporto in MFT.</span><span class="sxs-lookup"><span data-stu-id="75178-111">If value of this attribute is nonzero, the topology loader will not change the media types on the MFT.</span></span> <span data-ttu-id="75178-112">Il caricatore della topologia imposta questo attributo dopo aver caricato la topologia.</span><span class="sxs-lookup"><span data-stu-id="75178-112">The topology loader sets this attribute after it loads the topology.</span></span>

<span data-ttu-id="75178-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="75178-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="75178-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75178-114">Requirements</span></span>



| <span data-ttu-id="75178-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="75178-115">Requirement</span></span> | <span data-ttu-id="75178-116">Valore</span><span class="sxs-lookup"><span data-stu-id="75178-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75178-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75178-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75178-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75178-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="75178-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75178-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75178-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75178-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="75178-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75178-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="75178-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75178-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75178-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75178-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75178-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75178-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="75178-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="75178-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="75178-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="75178-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="75178-127">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="75178-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




