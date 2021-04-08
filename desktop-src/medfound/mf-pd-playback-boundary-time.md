---
description: Archivia l'ora (in unità 100-nanosecondi) in corrispondenza della quale deve iniziare la presentazione, relativa all'inizio dell'origine del supporto.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: Attributo MF_PD_PLAYBACK_BOUNDARY_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058252"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a><span data-ttu-id="a0fb9-103">\_ \_ \_ Attributo tempo limite riproduzione MF PD \_</span><span class="sxs-lookup"><span data-stu-id="a0fb9-103">MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute</span></span>

<span data-ttu-id="a0fb9-104">Archivia l'ora (in unità 100-nanosecondi) in corrispondenza della quale deve iniziare la presentazione, relativa all'inizio dell'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-104">Stores the time (in 100-nanoseconds units) at which the presentation must begin, relative to the start of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="a0fb9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a0fb9-105">Data type</span></span>

<span data-ttu-id="a0fb9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a0fb9-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="a0fb9-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="a0fb9-107">Get/set</span></span>

<span data-ttu-id="a0fb9-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="a0fb9-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="a0fb9-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a0fb9-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="a0fb9-110">Applies to</span></span>

[<span data-ttu-id="a0fb9-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a0fb9-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="a0fb9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0fb9-112">Remarks</span></span>

<span data-ttu-id="a0fb9-113">L' \_ \_ \_ attributo tempo limite riproduzione MF PD \_ è facoltativo per le origini multimediali in una playlist.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-113">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is optional for media sources in a playlist.</span></span> <span data-ttu-id="a0fb9-114">Questo valore indica l'ora di inizio effettiva della presentazione.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-114">This value indicates the actual start time of the presentation.</span></span> <span data-ttu-id="a0fb9-115">Si consideri una playlist che include origini multimediali *Element1*, *element2* e *Element3* in una sequenza.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-115">Consider a playlist that includes media sources *Element1*, *Element2*, and *Element3* in a sequence.</span></span> <span data-ttu-id="a0fb9-116">15 secondi dopo l'avvio della riproduzione di *Element1* , si verifica una modifica dinamica del flusso.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-116">15 seconds after *Element1* starts playing, a dynamic stream change occurs.</span></span> <span data-ttu-id="a0fb9-117">Il nuovo flusso deve iniziare a riprodurre 15 secondi nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-117">The new stream must start playing 15 seconds into the presentation.</span></span> <span data-ttu-id="a0fb9-118">Tuttavia, il fotogramma chiave più vicino al tempo di presentazione di 15 secondi è a 12 secondi per il nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-118">However, the keyframe nearest the presentation time of 15 seconds is at 12 seconds for the new stream.</span></span> <span data-ttu-id="a0fb9-119">Per avviare la nuova presentazione a 15 secondi, è necessario un contrassegno, in modo che gli esempi decodificati vengano eliminati da 12 secondi a 15 secondi.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-119">To start the new presentation at 15 seconds, a markin is required so that the decoded samples are dropped from 12 seconds to 15 seconds.</span></span>

<span data-ttu-id="a0fb9-120">Prima della transizione, l'evento [MENewPresentation](menewpresentation.md) viene generato dall'origine supporto.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-120">Before the transition, the [MENewPresentation](menewpresentation.md) event is raised by the media source.</span></span> <span data-ttu-id="a0fb9-121">Viene restituito il descrittore di presentazione che contiene l'attributo dell' [ID dell'elemento di \_ \_ riproduzione \_ \_ MF PD](mf-pd-playback-element-id.md) per *Element1*.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-121">This returns the presentation descriptor that contains the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute for *Element1*.</span></span> <span data-ttu-id="a0fb9-122">Contiene inoltre l' \_ \_ attributo di tempo limite riproduzione MF PD \_ \_ impostato su 15 secondi per indicare l'ora in cui si è verificata la transizione.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-122">Additionally, it contains the MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute that is set to 15 seconds to indicate the time when the transition occurred.</span></span> <span data-ttu-id="a0fb9-123">L'origine multimediale esegue il contrassegno dopo 15 secondi dopo la decodifica, impedendo la visualizzazione dei frame da 12 a 15 secondi.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-123">The media source performs the markin at 15 seconds after decoding, which prevents the frames from 12 seconds to 15 seconds from being displayed.</span></span>

<span data-ttu-id="a0fb9-124">Questo valore influisce solo su Markin Time e non influisce sul modo in cui la sessione multimediale regola i timestamp.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-124">This value affects only markin time and does not affect how the Media Session adjusts time stamps.</span></span> <span data-ttu-id="a0fb9-125">Questo attributo viene ignorato a meno che l'origine del supporto non indichi tramite l'attributo [ \_ ID dell'elemento di \_ riproduzione \_ \_ MF PD](mf-pd-playback-element-id.md) che questa presentazione è lo stesso elemento di riproduzione del precedente.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-125">This attribute is ignored unless the media source indicates through the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute that this presentation is the same playback element as the previous one.</span></span>

<span data-ttu-id="a0fb9-126">L' \_ attributo del \_ tempo limite per la riproduzione MF PD \_ \_ è simile a quello dell'attributo [MEDIASTART di MF \_ TOPONODE \_ ](mf-toponode-mediastart-attribute.md) impostato nel nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-126">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is similar to the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute that is set on the topology node.</span></span> <span data-ttu-id="a0fb9-127">Per le applicazioni in esecuzione in Windows Vista, le origini multimediali che implementano [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devono usare **MF \_ TOPONODE \_ MEDIASTART** anziché l' \_ \_ ora limite di riproduzione MF PD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a0fb9-127">For applications running on Windows Vista, media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use **MF\_TOPONODE\_MEDIASTART** instead of MF\_PD\_PLAYBACK\_BOUNDARY\_TIME.</span></span>

<span data-ttu-id="a0fb9-128">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a0fb9-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0fb9-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0fb9-129">Requirements</span></span>



| <span data-ttu-id="a0fb9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0fb9-130">Requirement</span></span> | <span data-ttu-id="a0fb9-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a0fb9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fb9-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0fb9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a0fb9-133">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a0fb9-133">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a0fb9-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0fb9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a0fb9-135">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a0fb9-135">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a0fb9-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0fb9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0fb9-137"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0fb9-137"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0fb9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0fb9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fb9-139">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a0fb9-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a0fb9-140">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="a0fb9-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




