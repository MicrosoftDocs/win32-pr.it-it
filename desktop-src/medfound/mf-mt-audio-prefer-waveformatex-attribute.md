---
description: Specifica la struttura di formato legacy preferita da usare per la conversione di un tipo di supporto audio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Attributo MF_MT_AUDIO_PREFER_WAVEFORMATEX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528243"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a><span data-ttu-id="dc371-103">MF \_ mt \_ audio \_ preferisce l' \_ attributo WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="dc371-103">MF\_MT\_AUDIO\_PREFER\_WAVEFORMATEX attribute</span></span>

<span data-ttu-id="dc371-104">Specifica la struttura di formato legacy preferita da usare per la conversione di un tipo di supporto audio.</span><span class="sxs-lookup"><span data-stu-id="dc371-104">Specifies the preferred legacy format structure to use when converting an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="dc371-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="dc371-105">Data type</span></span>

<span data-ttu-id="dc371-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dc371-106">**UINT32**</span></span>

<span data-ttu-id="dc371-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="dc371-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc371-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc371-108">Remarks</span></span>

<span data-ttu-id="dc371-109">Questo attributo fornisce un hint per la funzione [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="dc371-109">This attribute provides a hint to the [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) function.</span></span> <span data-ttu-id="dc371-110">Se l'attributo è **true**, la funzione converte il tipo di supporto audio in una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , laddove possibile, anziché convertirlo in una struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dc371-110">If the attribute is **TRUE**, the function converts the audio media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure whenever possible, instead of converting it to a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="dc371-111">La funzione [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) imposta questo attributo.</span><span class="sxs-lookup"><span data-stu-id="dc371-111">The [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) function sets this attribute.</span></span> <span data-ttu-id="dc371-112">È possibile eseguire l'override del valore di questo attributo, ma l'impostazione di questo attributo su **true** non garantisce che un tipo di supporto audio possa essere convertito nel formato [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dc371-112">You can override the value of this attribute, but setting this attribute to **TRUE** does not guarantee that an audio media type can be converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) form.</span></span>

<span data-ttu-id="dc371-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dc371-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc371-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc371-114">Requirements</span></span>



| <span data-ttu-id="dc371-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc371-115">Requirement</span></span> | <span data-ttu-id="dc371-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dc371-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc371-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc371-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc371-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dc371-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dc371-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc371-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc371-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="dc371-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dc371-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc371-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc371-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc371-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc371-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc371-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc371-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc371-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dc371-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="dc371-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dc371-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="dc371-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dc371-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dc371-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dc371-128">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="dc371-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
