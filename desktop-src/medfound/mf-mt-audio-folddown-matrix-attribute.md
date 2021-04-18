---
description: Specifica il modo in cui un decodificatore audio deve trasformare l'audio multicanale nell'output stereo. Questo processo viene anche definito riduzioni.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Attributo MF_MT_AUDIO_FOLDDOWN_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309554"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a><span data-ttu-id="7f801-104">\_ \_ \_ Attributo Matrix FOLDDOWN audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="7f801-104">MF\_MT\_AUDIO\_FOLDDOWN\_MATRIX attribute</span></span>

<span data-ttu-id="7f801-105">Specifica il modo in cui un decodificatore audio deve trasformare l'audio multicanale nell'output stereo.</span><span class="sxs-lookup"><span data-stu-id="7f801-105">Specifies how an audio decoder should transform multichannel audio to stereo output.</span></span> <span data-ttu-id="7f801-106">Questo processo viene anche definito *riduzioni*.</span><span class="sxs-lookup"><span data-stu-id="7f801-106">This process is also called *fold-down*.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f801-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7f801-107">Data type</span></span>

<span data-ttu-id="7f801-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="7f801-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="7f801-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f801-109">Remarks</span></span>

<span data-ttu-id="7f801-110">Questo attributo si applica ai tipi di supporti audio.</span><span class="sxs-lookup"><span data-stu-id="7f801-110">This attribute applies to audio media types.</span></span>

<span data-ttu-id="7f801-111">Il valore di questo attributo è una struttura della [**\_ matrice MFFOLDDOWN**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .</span><span class="sxs-lookup"><span data-stu-id="7f801-111">The value of this attribute is an [**MFFOLDDOWN\_MATRIX**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) structure.</span></span>

<span data-ttu-id="7f801-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7f801-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f801-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f801-113">Requirements</span></span>



| <span data-ttu-id="7f801-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f801-114">Requirement</span></span> | <span data-ttu-id="7f801-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7f801-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f801-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f801-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f801-117">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7f801-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7f801-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f801-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f801-119">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="7f801-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7f801-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f801-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f801-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f801-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f801-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f801-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f801-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f801-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f801-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="7f801-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7f801-125">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="7f801-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7f801-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7f801-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7f801-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="7f801-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




