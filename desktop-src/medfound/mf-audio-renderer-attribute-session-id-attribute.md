---
description: Specifica la classe di criteri audio per il renderer audio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883450"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a><span data-ttu-id="b9d58-103">\_ \_ \_ \_ Attributo ID sessione attributo MF audio RENDERER \_</span><span class="sxs-lookup"><span data-stu-id="b9d58-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID attribute</span></span>

<span data-ttu-id="b9d58-104">Specifica la classe di criteri audio per il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="b9d58-104">Specifies the audio policy class for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9d58-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b9d58-105">Data type</span></span>

<span data-ttu-id="b9d58-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b9d58-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d58-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9d58-107">Remarks</span></span>

<span data-ttu-id="b9d58-108">Questo attributo associa il renderer audio a una classe di criteri audio.</span><span class="sxs-lookup"><span data-stu-id="b9d58-108">This attribute associates the audio renderer with an audio policy class.</span></span> <span data-ttu-id="b9d58-109">Ogni classe Policy dispone di un proprio volume e controllo dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b9d58-109">Each policy class has its own volume and policy control.</span></span> <span data-ttu-id="b9d58-110">Se questo attributo non è impostato, il nuovo SAR viene unito alla sessione audio predefinita dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9d58-110">If this attribute is not set, the new SAR joins the application's default audio session.</span></span> <span data-ttu-id="b9d58-111">Per altre informazioni, vedere [**IAudioClient:: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) nella documentazione principale dell'API audio.</span><span class="sxs-lookup"><span data-stu-id="b9d58-111">For more information, see [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in the core audio API documentation.</span></span>

<span data-ttu-id="b9d58-112">È possibile usare questo attributo per configurare il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="b9d58-112">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="b9d58-113">L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:</span><span class="sxs-lookup"><span data-stu-id="b9d58-113">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="b9d58-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): impostare questo attributo usando il puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="b9d58-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="b9d58-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): impostare questo attributo usando il puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel parametro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="b9d58-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="b9d58-116">Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="b9d58-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="b9d58-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b9d58-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9d58-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9d58-118">Requirements</span></span>



| <span data-ttu-id="b9d58-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9d58-119">Requirement</span></span> | <span data-ttu-id="b9d58-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b9d58-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d58-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d58-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9d58-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9d58-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b9d58-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d58-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9d58-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9d58-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9d58-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9d58-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9d58-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9d58-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d58-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9d58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d58-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9d58-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9d58-129">Attributi renderer audio</span><span class="sxs-lookup"><span data-stu-id="b9d58-129">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9d58-130">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="b9d58-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b9d58-131">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="b9d58-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b9d58-132">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="b9d58-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
