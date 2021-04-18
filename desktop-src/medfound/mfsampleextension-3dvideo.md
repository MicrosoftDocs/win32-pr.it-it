---
description: Specifica se un esempio multimediale contiene un frame video 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Attributo MFSampleExtension_3DVideo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309100"
---
# <a name="mfsampleextension_3dvideo-attribute"></a><span data-ttu-id="25b5d-103">\_Attributo 3DVideo di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="25b5d-103">MFSampleExtension\_3DVideo attribute</span></span>

<span data-ttu-id="25b5d-104">Specifica se un esempio multimediale contiene un frame video 3D.</span><span class="sxs-lookup"><span data-stu-id="25b5d-104">Specifies whether a media sample contains a 3D video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="25b5d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="25b5d-105">Data type</span></span>

<span data-ttu-id="25b5d-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25b5d-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="25b5d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="25b5d-107">Remarks</span></span>

<span data-ttu-id="25b5d-108">Se questo attributo è **true**, l'esempio multimediale contiene un frame video con due o più visualizzazioni stereoscopiche.</span><span class="sxs-lookup"><span data-stu-id="25b5d-108">If this attribute is **TRUE**, the media sample contains a video frame that has two or more stereoscopic views.</span></span> <span data-ttu-id="25b5d-109">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="25b5d-109">The default value is **FALSE**.</span></span>

<span data-ttu-id="25b5d-110">Un componente che genera fotogrammi video 3D deve impostare questo attributo su **true** in ogni esempio multimediale che contiene un frame 3D.</span><span class="sxs-lookup"><span data-stu-id="25b5d-110">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b5d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25b5d-111">Requirements</span></span>



| <span data-ttu-id="25b5d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b5d-112">Requirement</span></span> | <span data-ttu-id="25b5d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="25b5d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25b5d-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b5d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="25b5d-115">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="25b5d-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="25b5d-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b5d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="25b5d-117">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="25b5d-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="25b5d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25b5d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b5d-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b5d-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b5d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25b5d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b5d-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25b5d-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="25b5d-122">MFSampleExtension \_ 3DVideo \_ SampleFormat</span><span class="sxs-lookup"><span data-stu-id="25b5d-122">MFSampleExtension\_3DVideo\_SampleFormat</span></span>](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




