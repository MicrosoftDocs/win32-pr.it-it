---
description: Contiene i flag per configurare il renderer audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309593"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a><span data-ttu-id="1ecc5-103">\_ \_ \_ Attributo Flags dell'attributo del RENDERER MF audio \_</span><span class="sxs-lookup"><span data-stu-id="1ecc5-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS attribute</span></span>

<span data-ttu-id="1ecc5-104">Contiene i flag per configurare il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-104">Contains flags to configure the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ecc5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1ecc5-105">Data type</span></span>

<span data-ttu-id="1ecc5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1ecc5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1ecc5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ecc5-107">Remarks</span></span>

<span data-ttu-id="1ecc5-108">Il valore di questo attributo è **un operatore OR** bit per bit dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-108">The value of this attribute is a bitwise **OR** of the following flags.</span></span>



| <span data-ttu-id="1ecc5-109">Valore</span><span class="sxs-lookup"><span data-stu-id="1ecc5-109">Value</span></span>                                                   | <span data-ttu-id="1ecc5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ecc5-110">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecc5-111">**\_flag di \_ attributo del RENDERER MF audio \_ \_ \_ CROSSPROCESS**</span><span class="sxs-lookup"><span data-stu-id="1ecc5-111">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**</span></span> | <span data-ttu-id="1ecc5-112">Il renderer audio usa una sessione audio tra processi.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-112">The audio renderer is uses a cross-process audio session.</span></span> <span data-ttu-id="1ecc5-113">Questo flag consente ai renderer audio in più processi di condividere la stessa sessione audio, insieme ai controlli del volume e dei criteri associati.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-113">This flag enables audio renderers in multiple processes to share the same audio session, along with the associated volume and policy controls.</span></span><br/> <span data-ttu-id="1ecc5-114">Se questo flag non è impostato, la sessione audio non può essere condivisa dai renderer audio in altri processi.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-114">If this flag is not set, the audio session cannot be shared by audio renderers in other processes.</span></span><br/> |
| <span data-ttu-id="1ecc5-115">**\_flag di attributo del RENDERER MF audio \_ \_ \_ \_ nopermanente**</span><span class="sxs-lookup"><span data-stu-id="1ecc5-115">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_NOPERSIST**</span></span>    | <span data-ttu-id="1ecc5-116">L'API di sessione audio (WASAPI) di Windows non rende permanente le proprietà per questa sessione audio, ad esempio il volume della sessione.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-116">The Windows audio session API (WASAPI) will not persist the properties for this audio session, such as the session volume.</span></span><br/> <span data-ttu-id="1ecc5-117">Se questo flag non è impostato, WASAPI manterranno le proprietà della sessione audio.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-117">If this flag is not set, WASAPI will persist the audio session properties.</span></span><br/>                                                                                                       |



 

<span data-ttu-id="1ecc5-118">È possibile usare questo attributo per configurare il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-118">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="1ecc5-119">L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:</span><span class="sxs-lookup"><span data-stu-id="1ecc5-119">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="1ecc5-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): impostare questo attributo usando il puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="1ecc5-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="1ecc5-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): impostare questo attributo usando il puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel parametro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="1ecc5-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="1ecc5-122">Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="1ecc5-122">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="1ecc5-123">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1ecc5-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ecc5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ecc5-124">Requirements</span></span>



| <span data-ttu-id="1ecc5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ecc5-125">Requirement</span></span> | <span data-ttu-id="1ecc5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1ecc5-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecc5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ecc5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ecc5-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ecc5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1ecc5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ecc5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ecc5-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ecc5-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1ecc5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ecc5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ecc5-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc5-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ecc5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ecc5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecc5-134">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ecc5-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ecc5-135">Attributi renderer audio</span><span class="sxs-lookup"><span data-stu-id="1ecc5-135">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ecc5-136">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="1ecc5-136">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1ecc5-137">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="1ecc5-137">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1ecc5-138">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="1ecc5-138">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




