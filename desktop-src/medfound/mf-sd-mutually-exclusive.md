---
description: Specifica se un flusso si escludono a vicenda con altri flussi dello stesso tipo.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Attributo MF_SD_MUTUALLY_EXCLUSIVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315014"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a><span data-ttu-id="81340-103">Attributo che si \_ \_ escludono a vicenda MF SD \_</span><span class="sxs-lookup"><span data-stu-id="81340-103">MF\_SD\_MUTUALLY\_EXCLUSIVE attribute</span></span>

<span data-ttu-id="81340-104">Specifica se un flusso si escludono a vicenda con altri flussi dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="81340-104">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span>

## <a name="data-type"></a><span data-ttu-id="81340-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="81340-105">Data type</span></span>

<span data-ttu-id="81340-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="81340-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="81340-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="81340-107">Get/set</span></span>

<span data-ttu-id="81340-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="81340-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="81340-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="81340-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="81340-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="81340-110">Applies to</span></span>

[<span data-ttu-id="81340-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="81340-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="81340-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="81340-112">Remarks</span></span>

<span data-ttu-id="81340-113">Se questo attributo è **true** (diverso da zero), il flusso si escludono a vicenda con altri flussi dello stesso tipo, ad esempio audio o video, all'interno della stessa presentazione.</span><span class="sxs-lookup"><span data-stu-id="81340-113">If this attribute is **TRUE** (nonzero), the stream is mutually exclusive with other streams of the same type, such as audio or video, within the same presentation.</span></span> <span data-ttu-id="81340-114">Se, ad esempio, un file AVI contiene più flussi audio, viene contrassegnato come si escludono a vicenda, perché deve essere riprodotto un solo flusso audio alla volta.</span><span class="sxs-lookup"><span data-stu-id="81340-114">For example, if an AVI file contains multiple audio streams, they are marked as mutually exclusive, because only one audio stream should be played at one time.</span></span>

<span data-ttu-id="81340-115">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="81340-115">The default value is **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="81340-116">Questo attributo non viene usato per i file di formato Advanced Systems (ASF), che hanno un modo più sofisticato per rappresentare i criteri di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="81340-116">This attribute is not used for Advanced Systems Format (ASF) files, which have a more sophisticated way to represent mutual exclusion criteria.</span></span> <span data-ttu-id="81340-117">Per ulteriori informazioni, vedere [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="81340-117">For more information, see [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span></span>

 

<span data-ttu-id="81340-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="81340-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="81340-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81340-119">Requirements</span></span>



| <span data-ttu-id="81340-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="81340-120">Requirement</span></span> | <span data-ttu-id="81340-121">Valore</span><span class="sxs-lookup"><span data-stu-id="81340-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81340-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81340-122">Minimum supported client</span></span><br/> | <span data-ttu-id="81340-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81340-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="81340-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81340-124">Minimum supported server</span></span><br/> | <span data-ttu-id="81340-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81340-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="81340-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81340-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="81340-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81340-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81340-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81340-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81340-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81340-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="81340-130">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="81340-130">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




