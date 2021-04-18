---
description: Specifica la categoria del flusso audio per il renderer di streaming audio (SAR).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309591"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a><span data-ttu-id="64132-103">\_Attributo della \_ \_ categoria del \_ flusso di attributi \_ MF audio RENDERER</span><span class="sxs-lookup"><span data-stu-id="64132-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_STREAM\_CATEGORY attribute</span></span>

<span data-ttu-id="64132-104">Specifica la categoria del flusso audio per il [renderer di streaming audio](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="64132-104">Specifies the audio stream category for the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

## <a name="data-type"></a><span data-ttu-id="64132-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="64132-105">Data type</span></span>

<span data-ttu-id="64132-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="64132-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="64132-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="64132-107">Remarks</span></span>

<span data-ttu-id="64132-108">È possibile usare questo attributo per configurare il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="64132-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="64132-109">L'utilizzo dipende dalla funzione chiamata per creare il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="64132-109">The usage depends on which function you call to create the audio renderer.</span></span>



| <span data-ttu-id="64132-110">Funzione</span><span class="sxs-lookup"><span data-stu-id="64132-110">Function</span></span>                                                               | <span data-ttu-id="64132-111">Come impostare l'attributo</span><span class="sxs-lookup"><span data-stu-id="64132-111">How to Set the attribute</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64132-112">**MFCreateAudioRenderer**</span><span class="sxs-lookup"><span data-stu-id="64132-112">**MFCreateAudioRenderer**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | <span data-ttu-id="64132-113">Usare il puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="64132-113">Use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer specified in the *pAudioAttributes* parameter.</span></span>                                                                                          |
| [<span data-ttu-id="64132-114">**MFCreateAudioRendererActivate**</span><span class="sxs-lookup"><span data-stu-id="64132-114">**MFCreateAudioRendererActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | <span data-ttu-id="64132-115">Usare il puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito nel parametro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="64132-115">Use the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned in the *ppActivate* parameter.</span></span> <span data-ttu-id="64132-116">Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="64132-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> |



 

<span data-ttu-id="64132-117">Il valore dell'attributo è un membro dell'enumerazione di [**\_ \_ categoria del flusso audio**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) .</span><span class="sxs-lookup"><span data-stu-id="64132-117">The value of the attribute is a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration.</span></span> <span data-ttu-id="64132-118">Il servizio audio usa la categoria Stream per determinare i criteri audio quando più applicazioni riproducono audio contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="64132-118">The audio service uses the stream category to determine audio policies when multiple applications play audio at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="64132-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64132-119">Requirements</span></span>



| <span data-ttu-id="64132-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="64132-120">Requirement</span></span> | <span data-ttu-id="64132-121">Valore</span><span class="sxs-lookup"><span data-stu-id="64132-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64132-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64132-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64132-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="64132-123">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64132-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64132-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64132-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="64132-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="64132-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64132-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="64132-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64132-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64132-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64132-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64132-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64132-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
