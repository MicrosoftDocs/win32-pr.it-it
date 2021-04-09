---
description: Specifica la rotazione di un frame video in senso antiorario.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: Attributo MF_MT_VIDEO_ROTATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885581"
---
# <a name="mf_mt_video_rotation-attribute"></a><span data-ttu-id="fdc7b-103">\_ \_ Attributo rotazione video MF mt \_</span><span class="sxs-lookup"><span data-stu-id="fdc7b-103">MF\_MT\_VIDEO\_ROTATION attribute</span></span>

<span data-ttu-id="fdc7b-104">Specifica la rotazione di un frame video in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="fdc7b-104">Specifies the rotation of a video frame in the counter-clockwise direction.</span></span>

## <a name="data-type"></a><span data-ttu-id="fdc7b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fdc7b-105">Data type</span></span>

<span data-ttu-id="fdc7b-106">**MFVideoRotationFormat** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdc7b-106">**MFVideoRotationFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc7b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdc7b-107">Remarks</span></span>

<span data-ttu-id="fdc7b-108">Il video da un dispositivo palmare, ad esempio un telefono cellulare, viene spesso ruotato di 90, 180 o 270 gradi.</span><span class="sxs-lookup"><span data-stu-id="fdc7b-108">Video from a handheld device, such as a mobile phone, is often rotated by 90, 180, or 270 degrees.</span></span> <span data-ttu-id="fdc7b-109">Se la fotocamera archivia l'orientamento come metadati nel file video, l'immagine può essere regolata al momento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="fdc7b-109">If the camera stores the orientation as metadata in the video file, the image can be adjusted at the time of playback.</span></span>

<span data-ttu-id="fdc7b-110">Se questo attributo è impostato su **MFVideoRotationFormat \_ 90**, significa che il contenuto è stato ruotato di 90 gradi in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="fdc7b-110">If this attribute set to **MFVideoRotationFormat\_90**, it means that the content has been rotated 90 degrees in the counter-clockwise direction.</span></span> <span data-ttu-id="fdc7b-111">Se il contenuto è stato ruotato di 90 gradi in senso orario, il valore dell'attributo sarà **MFVideoRotationFormat \_ 270**.</span><span class="sxs-lookup"><span data-stu-id="fdc7b-111">If the content was rotated 90 degrees in the clockwise direction, the attribute value would be **MFVideoRotationFormat\_270**.</span></span>

<span data-ttu-id="fdc7b-112">I valori supportati per questo attributo sono enumerati in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span><span class="sxs-lookup"><span data-stu-id="fdc7b-112">The supported values for this attribute are enumerated in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span></span>

<span data-ttu-id="fdc7b-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fdc7b-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc7b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdc7b-114">Requirements</span></span>



| <span data-ttu-id="fdc7b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc7b-115">Requirement</span></span> | <span data-ttu-id="fdc7b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fdc7b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc7b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc7b-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdc7b-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="fdc7b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc7b-120">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="fdc7b-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fdc7b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdc7b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc7b-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdc7b-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc7b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdc7b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc7b-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fdc7b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fdc7b-125">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="fdc7b-125">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




