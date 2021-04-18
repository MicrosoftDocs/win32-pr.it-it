---
description: Per un tipo di supporto video, specifica il modo in cui vengono archiviati i frame video 3D in memoria.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: Attributo MF_MT_VIDEO_3D_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316443"
---
# <a name="mf_mt_video_3d_format-attribute"></a><span data-ttu-id="c333d-103">\_ \_ \_ Attributo formato 3D video MF mt \_</span><span class="sxs-lookup"><span data-stu-id="c333d-103">MF\_MT\_VIDEO\_3D\_FORMAT attribute</span></span>

<span data-ttu-id="c333d-104">Per un tipo di supporto video, specifica il modo in cui vengono archiviati i frame video 3D in memoria.</span><span class="sxs-lookup"><span data-stu-id="c333d-104">For a video media type, specifies how 3D video frames are stored in memory.</span></span>

## <a name="data-type"></a><span data-ttu-id="c333d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c333d-105">Data type</span></span>

<span data-ttu-id="c333d-106">**MFVideo3DFormat** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c333d-106">**MFVideo3DFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c333d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c333d-107">Remarks</span></span>

<span data-ttu-id="c333d-108">Il valore di questo attributo è un membro dell'enumerazione [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) .</span><span class="sxs-lookup"><span data-stu-id="c333d-108">The value of this attribute is a member of the [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) enumeration.</span></span> <span data-ttu-id="c333d-109">L'attributo si applica solo se l'attributo del [ \_ \_ video \_ 3D MF mt](mf-mt-video-3d.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="c333d-109">The attribute applies only if the [MF\_MT\_VIDEO\_3D](mf-mt-video-3d.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="c333d-110">Questo attributo è necessario per i formati video 3D non compressi.</span><span class="sxs-lookup"><span data-stu-id="c333d-110">This attribute is required for uncompressed 3D video formats.</span></span> <span data-ttu-id="c333d-111">È facoltativo per i video compressi 3D.</span><span class="sxs-lookup"><span data-stu-id="c333d-111">It is optional for compressed 3D video.</span></span> <span data-ttu-id="c333d-112">Un'origine multimediale che fornisce frame codificati potrebbe essere in grado di impostare l'attributo, in base alle informazioni contenute nel contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="c333d-112">A media source that delivers encoded frames might be able to set the attribute, based on information in the file container.</span></span> <span data-ttu-id="c333d-113">In caso contrario, l'attributo deve essere impostato dal decodificatore nel tipo di supporto di output del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c333d-113">Otherwise, the attribute should be set by the decoder in the decoder's output media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c333d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c333d-114">Requirements</span></span>



| <span data-ttu-id="c333d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c333d-115">Requirement</span></span> | <span data-ttu-id="c333d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c333d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c333d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c333d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c333d-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c333d-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c333d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c333d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c333d-120">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c333d-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c333d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c333d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c333d-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c333d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c333d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c333d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c333d-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c333d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




