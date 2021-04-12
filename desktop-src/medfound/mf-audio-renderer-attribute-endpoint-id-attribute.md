---
description: Specifica l'identificatore per il dispositivo dell'endpoint audio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344596"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a><span data-ttu-id="fce8b-103">\_ \_ \_ \_ Attributo ID endpoint dell'attributo di RENDERER audio MF \_</span><span class="sxs-lookup"><span data-stu-id="fce8b-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="fce8b-104">Specifica l'identificatore per il dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="fce8b-104">Specifies the identifier for the audio endpoint device.</span></span>

## <a name="data-type"></a><span data-ttu-id="fce8b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fce8b-105">Data type</span></span>

<span data-ttu-id="fce8b-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="fce8b-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="fce8b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="fce8b-107">Remarks</span></span>

<span data-ttu-id="fce8b-108">È possibile usare questo attributo per configurare il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="fce8b-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="fce8b-109">L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:</span><span class="sxs-lookup"><span data-stu-id="fce8b-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="fce8b-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): impostare questo attributo usando il puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="fce8b-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="fce8b-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): impostare questo attributo usando il puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel parametro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="fce8b-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="fce8b-112">Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="fce8b-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="fce8b-113">Un dispositivo endpoint audio è un dispositivo hardware che si trova in un'estremità di un percorso dati audio, ad esempio una cuffia o un altoparlante.</span><span class="sxs-lookup"><span data-stu-id="fce8b-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span> <span data-ttu-id="fce8b-114">Per ottenere l'identificatore dell'endpoint audio, usare le API principali audio seguenti:</span><span class="sxs-lookup"><span data-stu-id="fce8b-114">To obtain the audio endpoint identifier, use the following core audio APIs:</span></span>

-   <span data-ttu-id="fce8b-115">Usare l'interfaccia [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) per enumerare i dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fce8b-115">Use the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface to enumerate the devices on the system.</span></span>
-   <span data-ttu-id="fce8b-116">Chiamare [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere l'identificatore per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fce8b-116">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the identifier for the device.</span></span>

<span data-ttu-id="fce8b-117">Per ulteriori informazioni, vedere la documentazione principale sull'API [audio](../coreaudio/core-audio-apis-in-windows-vista.md) .</span><span class="sxs-lookup"><span data-stu-id="fce8b-117">For more information, see the [Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API documentation.</span></span> <span data-ttu-id="fce8b-118">Se questo attributo non è impostato, il renderer audio utilizza il dispositivo endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="fce8b-118">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="fce8b-119">Se questo attributo è impostato, non impostare l'attributo [**del \_ \_ \_ \_ \_ ruolo endpoint dell'attributo del RENDERER MF audio**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="fce8b-119">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span> <span data-ttu-id="fce8b-120">Se entrambi gli attributi sono impostati, si verificherà un errore quando viene creato il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="fce8b-120">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="fce8b-121">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fce8b-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce8b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fce8b-122">Requirements</span></span>



| <span data-ttu-id="fce8b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce8b-123">Requirement</span></span> | <span data-ttu-id="fce8b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fce8b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fce8b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fce8b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fce8b-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fce8b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fce8b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fce8b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fce8b-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fce8b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fce8b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fce8b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce8b-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce8b-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce8b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fce8b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce8b-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fce8b-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fce8b-133">Attributi renderer audio</span><span class="sxs-lookup"><span data-stu-id="fce8b-133">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="fce8b-134">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="fce8b-134">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="fce8b-135">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="fce8b-135">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="fce8b-136">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="fce8b-136">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
