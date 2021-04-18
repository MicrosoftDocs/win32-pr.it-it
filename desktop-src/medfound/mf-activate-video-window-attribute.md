---
description: Handle per la finestra di ritaglio video.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Attributo MF_ACTIVATE_VIDEO_WINDOW (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314552"
---
# <a name="mf_activate_video_window-attribute"></a><span data-ttu-id="ad9e8-103">\_Attributo attivazione \_ \_ finestra video MF</span><span class="sxs-lookup"><span data-stu-id="ad9e8-103">MF\_ACTIVATE\_VIDEO\_WINDOW attribute</span></span>

<span data-ttu-id="ad9e8-104">Handle per la finestra di ritaglio video.</span><span class="sxs-lookup"><span data-stu-id="ad9e8-104">Handle to the video clipping window.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad9e8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ad9e8-105">Data type</span></span>

<span data-ttu-id="ad9e8-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ad9e8-106">**UINT64**</span></span>

<span data-ttu-id="ad9e8-107">Considera come **DWORD \_ ptr** (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="ad9e8-107">Treat as **DWORD\_PTR** (**HWND**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9e8-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad9e8-108">Remarks</span></span>

<span data-ttu-id="ad9e8-109">Questo attributo si applica all'oggetto attivazione per il renderer video avanzato (EVR).</span><span class="sxs-lookup"><span data-stu-id="ad9e8-109">This attribute applies to the activation object for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="ad9e8-110">Il valore viene impostato automaticamente quando si chiama [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare l'oggetto attivazione di EVR.</span><span class="sxs-lookup"><span data-stu-id="ad9e8-110">The value is set automatically when you call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the EVR activation object.</span></span>

<span data-ttu-id="ad9e8-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ad9e8-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9e8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad9e8-112">Requirements</span></span>



| <span data-ttu-id="ad9e8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad9e8-113">Requirement</span></span> | <span data-ttu-id="ad9e8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ad9e8-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9e8-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad9e8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ad9e8-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad9e8-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ad9e8-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad9e8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ad9e8-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ad9e8-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad9e8-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad9e8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad9e8-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad9e8-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad9e8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad9e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9e8-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad9e8-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad9e8-123">Attributi renderer video avanzati</span><span class="sxs-lookup"><span data-stu-id="ad9e8-123">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad9e8-124">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="ad9e8-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="ad9e8-125">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="ad9e8-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="ad9e8-126">Oggetti attivazione</span><span class="sxs-lookup"><span data-stu-id="ad9e8-126">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




