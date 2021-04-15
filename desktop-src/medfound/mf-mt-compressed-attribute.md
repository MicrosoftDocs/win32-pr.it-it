---
description: Specifica se i dati multimediali sono compressi per un tipo di supporto.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Attributo MF_MT_COMPRESSED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528237"
---
# <a name="mf_mt_compressed-attribute"></a><span data-ttu-id="f3e88-103">\_ \_ Attributo compresso MF mt</span><span class="sxs-lookup"><span data-stu-id="f3e88-103">MF\_MT\_COMPRESSED attribute</span></span>

<span data-ttu-id="f3e88-104">Specifica se i dati multimediali sono compressi per un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f3e88-104">Specifies for a media type whether the media data is compressed.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3e88-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f3e88-105">Data type</span></span>

<span data-ttu-id="f3e88-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f3e88-106">**UINT32**</span></span>

<span data-ttu-id="f3e88-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="f3e88-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3e88-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3e88-108">Remarks</span></span>

<span data-ttu-id="f3e88-109">Se questo attributo è **true**, il tipo di supporto è un formato compresso.</span><span class="sxs-lookup"><span data-stu-id="f3e88-109">If this attribute is **TRUE**, the media type is a compressed format.</span></span> <span data-ttu-id="f3e88-110">In caso contrario, il tipo di supporto non è compresso o il tipo di compressione non è noto.</span><span class="sxs-lookup"><span data-stu-id="f3e88-110">Otherwise, either the media type is uncompressed or the compression type is not known.</span></span>

<span data-ttu-id="f3e88-111">Non è garantito che l'attributo sia impostato su **true** per tutti i formati compressi, quindi le applicazioni in genere non si basano su questo attributo.</span><span class="sxs-lookup"><span data-stu-id="f3e88-111">This attribute is not guaranteed to be set to **TRUE** for all compressed formats, so applications should generally not rely this attribute.</span></span> <span data-ttu-id="f3e88-112">Il modo più affidabile per determinare se un formato è compresso consiste nel mantenere un elenco di formati noti.</span><span class="sxs-lookup"><span data-stu-id="f3e88-112">The most reliable way to determine whether a format is compressed is to maintain a list of known formats.</span></span> <span data-ttu-id="f3e88-113">Se un'applicazione non riconosce un formato, come specificato nell'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) , non dovrebbe presupporre nulla sulla compressione del formato.</span><span class="sxs-lookup"><span data-stu-id="f3e88-113">If an application does not recognize a format, as specified in the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute, it should not assume anything about the compression of the format.</span></span>

<span data-ttu-id="f3e88-114">Per determinare se un formato usa la compressione temporale (ad esempio, alcuni esempi vengono calcolati come Delta degli esempi precedenti), controllare l'attributo [**indipendente da tutti i campioni di MF \_ mt \_ All \_ \_**](mf-mt-all-samples-independent-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e88-114">To determine whether a format uses temporal compression (meaning that some samples are computed as deltas from earlier samples), check the [**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) attribute.</span></span>

<span data-ttu-id="f3e88-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f3e88-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e88-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3e88-116">Requirements</span></span>



| <span data-ttu-id="f3e88-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3e88-117">Requirement</span></span> | <span data-ttu-id="f3e88-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f3e88-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e88-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e88-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e88-120">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f3e88-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f3e88-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e88-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e88-122">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f3e88-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f3e88-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3e88-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e88-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e88-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e88-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3e88-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e88-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3e88-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3e88-127">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="f3e88-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f3e88-128">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="f3e88-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f3e88-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="f3e88-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f3e88-130">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="f3e88-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




