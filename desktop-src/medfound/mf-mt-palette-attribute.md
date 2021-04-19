---
description: Contiene le voci della tavolozza per un tipo di supporto video. Utilizzare questo attributo per i formati video pallettizzati, ad esempio RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: Attributo MF_MT_PALETTE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310825"
---
# <a name="mf_mt_palette-attribute"></a><span data-ttu-id="83c83-104">\_Attributo della \_ tavolozza MF mt</span><span class="sxs-lookup"><span data-stu-id="83c83-104">MF\_MT\_PALETTE attribute</span></span>

<span data-ttu-id="83c83-105">Contiene le voci della tavolozza per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="83c83-105">Contains the palette entries for a video media type.</span></span> <span data-ttu-id="83c83-106">Utilizzare questo attributo per i formati video pallettizzati, ad esempio RGB 8.</span><span class="sxs-lookup"><span data-stu-id="83c83-106">Use this attribute for palettized video formats, such as RGB 8.</span></span>

## <a name="data-type"></a><span data-ttu-id="83c83-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="83c83-107">Data type</span></span>

<span data-ttu-id="83c83-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="83c83-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="83c83-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="83c83-109">Remarks</span></span>

<span data-ttu-id="83c83-110">I dati dell'attributo sono una matrice di unioni [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) .</span><span class="sxs-lookup"><span data-stu-id="83c83-110">The attribute data is an array of [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) unions.</span></span>

<span data-ttu-id="83c83-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="83c83-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="83c83-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83c83-112">Requirements</span></span>



| <span data-ttu-id="83c83-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="83c83-113">Requirement</span></span> | <span data-ttu-id="83c83-114">Valore</span><span class="sxs-lookup"><span data-stu-id="83c83-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83c83-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83c83-115">Minimum supported client</span></span><br/> | <span data-ttu-id="83c83-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83c83-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="83c83-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83c83-117">Minimum supported server</span></span><br/> | <span data-ttu-id="83c83-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="83c83-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="83c83-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83c83-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c83-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c83-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c83-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83c83-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c83-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="83c83-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="83c83-123">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="83c83-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="83c83-124">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="83c83-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="83c83-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="83c83-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="83c83-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="83c83-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




