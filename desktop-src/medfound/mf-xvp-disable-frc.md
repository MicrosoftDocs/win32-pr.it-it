---
description: Disabilita la conversione della frequenza dei frame nella MFT del processore video.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Attributo MF_XVP_DISABLE_FRC (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966894"
---
# <a name="mf_xvp_disable_frc-attribute"></a><span data-ttu-id="3b9f8-103">MF \_ XVP \_ Disabilita l' \_ attributo FRC</span><span class="sxs-lookup"><span data-stu-id="3b9f8-103">MF\_XVP\_DISABLE\_FRC attribute</span></span>

<span data-ttu-id="3b9f8-104">Disabilita la conversione della frequenza dei frame nella [**MFT del processore video**](video-processor-mft.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-104">Disables frame-rate conversion in the [**Video Processor MFT**](video-processor-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="3b9f8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3b9f8-105">Data type</span></span>

<span data-ttu-id="3b9f8-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b9f8-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b9f8-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b9f8-107">Remarks</span></span>

<span data-ttu-id="3b9f8-108">Se questo attributo è impostato su **true**, il processore video non eseguirà la conversione della frequenza dei frame.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-108">If this attribute is **TRUE**, the video processor will not perform frame-rate conversion.</span></span> <span data-ttu-id="3b9f8-109">Per impostazione predefinita, il processore video convertirà la frequenza dei fotogrammi in modo che corrisponda al tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-109">By default, the video processor will convert the frame rate to match the output media type.</span></span>

<span data-ttu-id="3b9f8-110">Per impostare l'attributo:</span><span class="sxs-lookup"><span data-stu-id="3b9f8-110">To set this attribute:</span></span>

1.  <span data-ttu-id="3b9f8-111">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sul processore video.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="3b9f8-112">Chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="3b9f8-113">Impostare l'attributo prima dell'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b9f8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b9f8-114">Requirements</span></span>



| <span data-ttu-id="3b9f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b9f8-115">Requirement</span></span> | <span data-ttu-id="3b9f8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3b9f8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9f8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b9f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3b9f8-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3b9f8-118">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3b9f8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b9f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3b9f8-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3b9f8-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3b9f8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b9f8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b9f8-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9f8-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9f8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b9f8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9f8-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3b9f8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




