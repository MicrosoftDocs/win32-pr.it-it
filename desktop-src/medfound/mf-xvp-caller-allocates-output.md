---
description: Specifica se il chiamante allocherà le trame usate per l'output.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Attributo MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527396"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a><span data-ttu-id="cdb54-103">Il \_ chiamante MF XVP \_ \_ alloca l' \_ attributo output</span><span class="sxs-lookup"><span data-stu-id="cdb54-103">MF\_XVP\_CALLER\_ALLOCATES\_OUTPUT attribute</span></span>

<span data-ttu-id="cdb54-104">Specifica se il chiamante allocherà le trame usate per l'output.</span><span class="sxs-lookup"><span data-stu-id="cdb54-104">Specifies whether that the caller will allocate the textures used for output.</span></span>

## <a name="data-type"></a><span data-ttu-id="cdb54-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cdb54-105">Data type</span></span>

<span data-ttu-id="cdb54-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdb54-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cdb54-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdb54-107">Remarks</span></span>

<span data-ttu-id="cdb54-108">Se questo attributo è **true**, il processore video prevede che le trame di output siano allocate dal chiamante, anche quando si opera in modalità DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="cdb54-108">If this attribute is **TRUE**, the video processor expect output textures to be allocated by the caller, even when operating in DirectX Video Acceleration (DXVA) mode.</span></span> <span data-ttu-id="cdb54-109">Se questo attributo è **false**, il processore video alloca le trame di output quando opera in modalità DXVA e avrà esito negativo se vengono fornite le trame di output fornite dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="cdb54-109">If this attribute is **FALSE**, the video processor will allocate the output textures when operating in DXVA mode, and will fail if caller provided output textures are provided.</span></span>

<span data-ttu-id="cdb54-110">Per impostare l'attributo:</span><span class="sxs-lookup"><span data-stu-id="cdb54-110">To set this attribute:</span></span>

1.  <span data-ttu-id="cdb54-111">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sul processore video.</span><span class="sxs-lookup"><span data-stu-id="cdb54-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="cdb54-112">Chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="cdb54-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="cdb54-113">Impostare l'attributo prima dell'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="cdb54-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb54-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdb54-114">Requirements</span></span>



| <span data-ttu-id="cdb54-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdb54-115">Requirement</span></span> | <span data-ttu-id="cdb54-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cdb54-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb54-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdb54-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb54-118">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cdb54-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cdb54-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdb54-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb54-120">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="cdb54-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cdb54-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdb54-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdb54-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdb54-122"><dt>Mfidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdb54-123">IDL</span><span class="sxs-lookup"><span data-stu-id="cdb54-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdb54-124"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdb54-124"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdb54-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdb54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb54-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cdb54-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




