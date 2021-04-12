---
description: Specifica il modo in cui un frame video 3D viene archiviato in un esempio di supporto.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Attributo MFSampleExtension_3DVideo_SampleFormat (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131127"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a><span data-ttu-id="f391b-103">MFSampleExtension \_ 3DVideo- \_ attributo SampleFormat</span><span class="sxs-lookup"><span data-stu-id="f391b-103">MFSampleExtension\_3DVideo\_SampleFormat attribute</span></span>

<span data-ttu-id="f391b-104">Specifica il modo in cui un frame video 3D viene archiviato in un esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="f391b-104">Specifies how a 3D video frame is stored in a media sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="f391b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f391b-105">Data type</span></span>

<span data-ttu-id="f391b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f391b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f391b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f391b-107">Remarks</span></span>

<span data-ttu-id="f391b-108">Il valore di questo attributo è un membro dell'enumerazione [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .</span><span class="sxs-lookup"><span data-stu-id="f391b-108">The value of this attribute is a member of the [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) enumeration.</span></span>

<span data-ttu-id="f391b-109">Un componente che genera fotogrammi video 3D deve impostare questo attributo su **true** in ogni esempio multimediale che contiene un frame 3D.</span><span class="sxs-lookup"><span data-stu-id="f391b-109">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span> <span data-ttu-id="f391b-110">L'attributo viene ignorato se l'attributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) è **false** o non impostato.</span><span class="sxs-lookup"><span data-stu-id="f391b-110">The attribute is ignored if the [MFSampleExtension\_3DVideo](mfsampleextension-3dvideo.md) attribute is **FALSE** or not set.</span></span>

## <a name="requirements"></a><span data-ttu-id="f391b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f391b-111">Requirements</span></span>



| <span data-ttu-id="f391b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f391b-112">Requirement</span></span> | <span data-ttu-id="f391b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f391b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f391b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f391b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f391b-115">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f391b-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f391b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f391b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f391b-117">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f391b-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f391b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f391b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f391b-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f391b-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f391b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f391b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f391b-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f391b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f391b-122">\_3DVideo MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="f391b-122">MFSampleExtension\_3DVideo</span></span>](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




