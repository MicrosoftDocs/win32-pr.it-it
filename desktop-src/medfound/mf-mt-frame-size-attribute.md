---
description: Larghezza e altezza di un frame video, in pixel.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: Attributo MF_MT_FRAME_SIZE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318718"
---
# <a name="mf_mt_frame_size-attribute"></a><span data-ttu-id="0e7d1-103">\_ \_ Attributo dimensione frame MF mt \_</span><span class="sxs-lookup"><span data-stu-id="0e7d1-103">MF\_MT\_FRAME\_SIZE attribute</span></span>

<span data-ttu-id="0e7d1-104">Larghezza e altezza di un frame video, in pixel.</span><span class="sxs-lookup"><span data-stu-id="0e7d1-104">Width and height of a video frame, in pixels.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e7d1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0e7d1-105">Data type</span></span>

<span data-ttu-id="0e7d1-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="0e7d1-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e7d1-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e7d1-107">Remarks</span></span>

<span data-ttu-id="0e7d1-108">I 32 bit superiori contengono la larghezza e i 32 bit inferiori contengono l'altezza.</span><span class="sxs-lookup"><span data-stu-id="0e7d1-108">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="0e7d1-109">Per impostare questo attributo, utilizzare la funzione [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="0e7d1-109">To set this attribute, use the [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) function.</span></span> <span data-ttu-id="0e7d1-110">Per ottenere questo attributo, usare la funzione [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="0e7d1-110">To get this attribute, use the [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) function.</span></span>

<span data-ttu-id="0e7d1-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0e7d1-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="0e7d1-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="0e7d1-112">Examples</span></span>


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a><span data-ttu-id="0e7d1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e7d1-113">Requirements</span></span>



| <span data-ttu-id="0e7d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e7d1-114">Requirement</span></span> | <span data-ttu-id="0e7d1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0e7d1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e7d1-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e7d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e7d1-117">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e7d1-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0e7d1-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e7d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e7d1-119">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0e7d1-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0e7d1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e7d1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e7d1-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e7d1-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e7d1-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e7d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e7d1-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e7d1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e7d1-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0e7d1-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="0e7d1-125">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="0e7d1-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




