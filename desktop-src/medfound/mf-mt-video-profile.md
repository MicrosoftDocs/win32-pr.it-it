---
description: Specifica il profilo della codifica video nel tipo di supporto di output. Si tratta di un alias di MF \_ mt \_ MPEG2 \_ profile Attribute.
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Attributo MF_MT_VIDEO_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318063"
---
# <a name="mf_mt_video_profile-attribute"></a><span data-ttu-id="2a3d5-104">\_ \_ Attributo profilo video MF mt \_</span><span class="sxs-lookup"><span data-stu-id="2a3d5-104">MF\_MT\_VIDEO\_PROFILE attribute</span></span>

<span data-ttu-id="2a3d5-105">Specifica il profilo della codifica video nel tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="2a3d5-105">Specifies the profile of video encoding on the output media type.</span></span> <span data-ttu-id="2a3d5-106">Si tratta di un alias di [MF \_ mt \_ MPEG2 \_ profile](mf-mt-mpeg2-profile-attribute.md) Attribute.</span><span class="sxs-lookup"><span data-stu-id="2a3d5-106">This is an alias of [MF\_MT\_MPEG2\_PROFILE](mf-mt-mpeg2-profile-attribute.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a3d5-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2a3d5-107">Data type</span></span>

<span data-ttu-id="2a3d5-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2a3d5-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2a3d5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a3d5-109">Remarks</span></span>

<span data-ttu-id="2a3d5-110">**Codificatori H. 264:**</span><span class="sxs-lookup"><span data-stu-id="2a3d5-110">**H.264 encoders:**</span></span>

<span data-ttu-id="2a3d5-111">Sono stati superati i profili supportati per includere [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) e **eAVEncH264VProfile \_ ConstrainedHigh**.</span><span class="sxs-lookup"><span data-stu-id="2a3d5-111">Supported profiles are exceeded to include [**eAVEncH264VProfile\_ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) and **eAVEncH264VProfile\_ConstrainedHigh**.</span></span>

<span data-ttu-id="2a3d5-112">I codificatori devono supportare sia [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) che [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="2a3d5-112">Encoders shall support both [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) and [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) for this attribute.</span></span>

<span data-ttu-id="2a3d5-113">Questo è statico, quindi i codificatori video devono essere configurati prima dell'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="2a3d5-113">This is static, so video encoders must be configured before the streaming starts.</span></span> <span data-ttu-id="2a3d5-114">Se l'applicazione imposta un profilo che non è supportato dal codificatore, il codificatore rifiuterà il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="2a3d5-114">If the application sets a profile which the encoder does not support, the encoder shall reject the media type.</span></span>

<span data-ttu-id="2a3d5-115">Impostazione predefinita consigliata: profilo [**\_ principale eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="2a3d5-115">Recommended default: [**eAVEncH264VProfile\_Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3d5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a3d5-116">Requirements</span></span>



| <span data-ttu-id="2a3d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a3d5-117">Requirement</span></span> | <span data-ttu-id="2a3d5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2a3d5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3d5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a3d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3d5-120">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a3d5-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2a3d5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a3d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3d5-122">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a3d5-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2a3d5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a3d5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3d5-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a3d5-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a3d5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a3d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3d5-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a3d5-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
