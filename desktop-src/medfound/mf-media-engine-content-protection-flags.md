---
description: Specifica se il motore multimediale giocherà contenuto protetto.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: Attributo MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351351"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a><span data-ttu-id="589e6-103">\_Attributo di \_ \_ flag di protezione del contenuto del motore multimediale \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="589e6-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_FLAGS attribute</span></span>

<span data-ttu-id="589e6-104">Specifica se il motore multimediale giocherà contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="589e6-104">Specifies whether the Media Engine will play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="589e6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="589e6-105">Data type</span></span>

<span data-ttu-id="589e6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="589e6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="589e6-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="589e6-107">Remarks</span></span>

<span data-ttu-id="589e6-108">Il valore di questo attributo è un operatore OR bit per bit di **flag dell'enumerazione** dei flag di [**\_ protezione MF media \_ Engine \_ \_**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) .</span><span class="sxs-lookup"><span data-stu-id="589e6-108">The value of this attribute is a bitwise **OR** of flags from the [**MF\_MEDIA\_ENGINE\_PROTECTION\_FLAGS**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) enumeration.</span></span> <span data-ttu-id="589e6-109">Per abilitare la riproduzione del contenuto protetto, impostare il flag **MF \_ media \_ Engine \_ enable \_ protected \_ Content** .</span><span class="sxs-lookup"><span data-stu-id="589e6-109">To enable playback of protected content, set the **MF\_MEDIA\_ENGINE\_ENABLE\_PROTECTED\_CONTENT** flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="589e6-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="589e6-110">Requirements</span></span>



| <span data-ttu-id="589e6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="589e6-111">Requirement</span></span> | <span data-ttu-id="589e6-112">Valore</span><span class="sxs-lookup"><span data-stu-id="589e6-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="589e6-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="589e6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="589e6-114">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="589e6-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="589e6-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="589e6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="589e6-116">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="589e6-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="589e6-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="589e6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="589e6-118"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="589e6-118"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="589e6-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="589e6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589e6-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="589e6-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="589e6-121">Attributi del motore multimediale</span><span class="sxs-lookup"><span data-stu-id="589e6-121">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="589e6-122">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="589e6-122">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




