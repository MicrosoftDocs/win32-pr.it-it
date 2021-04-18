---
description: Contiene l'identificatore dell'elemento playlist nella presentazione.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: Attributo MF_PD_PLAYBACK_ELEMENT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318421"
---
# <a name="mf_pd_playback_element_id-attribute"></a><span data-ttu-id="079cf-103">\_ \_ \_ Attributo ID elemento riproduzione MF PD \_</span><span class="sxs-lookup"><span data-stu-id="079cf-103">MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute</span></span>

<span data-ttu-id="079cf-104">Contiene l'identificatore dell'elemento playlist nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="079cf-104">Contains the identifier of the playlist element in the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="079cf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="079cf-105">Data type</span></span>

<span data-ttu-id="079cf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="079cf-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="079cf-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="079cf-107">Get/set</span></span>

<span data-ttu-id="079cf-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="079cf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="079cf-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="079cf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="079cf-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="079cf-110">Applies to</span></span>

[<span data-ttu-id="079cf-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="079cf-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="079cf-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="079cf-112">Remarks</span></span>

<span data-ttu-id="079cf-113">Le origini multimediali che forniscono playlist possono facoltativamente impostare questo attributo sui rispettivi descrittori di presentazione.</span><span class="sxs-lookup"><span data-stu-id="079cf-113">Media sources that deliver playlists can optionally set this attribute on their presentation descriptors.</span></span>

<span data-ttu-id="079cf-114">Quando un'origine multimediale recapita una playlist, invia un evento [MENewPresentation](menewpresentation.md) per ogni elemento della playlist dopo il primo.</span><span class="sxs-lookup"><span data-stu-id="079cf-114">When a media source delivers a playlist, it sends a [MENewPresentation](menewpresentation.md) event for each playlist element after the first.</span></span> <span data-ttu-id="079cf-115">Questo evento contiene un descrittore di presentazione per il nuovo elemento playlist.</span><span class="sxs-lookup"><span data-stu-id="079cf-115">This event contains a presentation descriptor for the new playlist element.</span></span> <span data-ttu-id="079cf-116">L'origine multimediale può assegnare gli identificatori agli elementi impostando l' \_ \_ attributo ID dell'elemento di riproduzione MF PD \_ \_ su ogni descrittore di presentazione, incluso quello creato da [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="079cf-116">The media source can assign identifiers to the elements by setting the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute on each presentation descriptor, including the one created by [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>

<span data-ttu-id="079cf-117">Un'origine multimediale può anche inviare l'evento [MENewPresentation](menewpresentation.md) a causa di un commutatore di flusso dinamico o di una modifica nel numero di flussi.</span><span class="sxs-lookup"><span data-stu-id="079cf-117">A media source might also send the [MENewPresentation](menewpresentation.md) event because of a dynamic stream switch or a change in the number of streams.</span></span> <span data-ttu-id="079cf-118">In tal caso, il valore dell' \_ ID dell'elemento di riproduzione MF PD \_ \_ \_ deve rimanere invariato in entrambe le presentazioni, per indicare che entrambe le presentazioni rappresentano lo stesso elemento della playlist.</span><span class="sxs-lookup"><span data-stu-id="079cf-118">In that situation, the value of MF\_PD\_PLAYBACK\_ELEMENT\_ID should remain the same across both presentations, to indicate that both presentations represent the same playlist element.</span></span> <span data-ttu-id="079cf-119">Se due presentazioni consecutive hanno lo stesso valore per questo attributo, la pipeline Microsoft Media Foundation prevede che i timestamp rimangano continui attraverso la transizione.</span><span class="sxs-lookup"><span data-stu-id="079cf-119">If two consecutive presentations have the same value for this attribute, the Microsoft Media Foundation pipeline expects the time stamps to remain continuous across the transition.</span></span> <span data-ttu-id="079cf-120">Pertanto, l'origine multimediale non deve usare l'attributo di [ \_ \_ \_ \_ avvio effettivo dell'origine eventi MF](mf-event-source-actual-start-attribute.md) quando passa alla presentazione successiva.</span><span class="sxs-lookup"><span data-stu-id="079cf-120">Therefore, the media source must not use the [MF\_EVENT\_SOURCE\_ACTUAL\_START](mf-event-source-actual-start-attribute.md) attribute when it transitions to the next presentation.</span></span>

<span data-ttu-id="079cf-121">Le origini multimediali che implementano [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devono usare l'attributo [ElementID della \_ \_ sequenza \_ MF TOPONODE](mf-toponode-sequence-elementid-attribute.md) anziché \_ l' \_ attributo ID dell'elemento di riproduzione MF PD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="079cf-121">Media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute rather than the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute.</span></span>

<span data-ttu-id="079cf-122">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="079cf-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="079cf-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="079cf-123">Requirements</span></span>



| <span data-ttu-id="079cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="079cf-124">Requirement</span></span> | <span data-ttu-id="079cf-125">Valore</span><span class="sxs-lookup"><span data-stu-id="079cf-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="079cf-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="079cf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="079cf-127">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="079cf-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="079cf-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="079cf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="079cf-129">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="079cf-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="079cf-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="079cf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="079cf-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="079cf-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="079cf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="079cf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="079cf-133">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="079cf-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="079cf-134">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="079cf-134">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




