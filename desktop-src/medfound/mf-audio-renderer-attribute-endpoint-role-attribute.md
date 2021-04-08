---
description: Specifica il ruolo endpoint audio per il renderer audio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967846"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a><span data-ttu-id="1d60d-103">\_Attributo del \_ \_ \_ ruolo endpoint dell'attributo RENDERER audio MF \_</span><span class="sxs-lookup"><span data-stu-id="1d60d-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="1d60d-104">Specifica il ruolo endpoint audio per il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="1d60d-104">Specifies the audio endpoint role for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="1d60d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1d60d-105">Data type</span></span>

<span data-ttu-id="1d60d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1d60d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d60d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d60d-107">Remarks</span></span>

<span data-ttu-id="1d60d-108">È possibile usare questo attributo per configurare il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="1d60d-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="1d60d-109">L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:</span><span class="sxs-lookup"><span data-stu-id="1d60d-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="1d60d-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): impostare questo attributo usando il puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="1d60d-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="1d60d-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): impostare questo attributo usando il puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel parametro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="1d60d-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="1d60d-112">Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="1d60d-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="1d60d-113">Un dispositivo endpoint audio è un dispositivo hardware che si trova in un'estremità di un percorso dati audio, ad esempio una cuffia o un altoparlante.</span><span class="sxs-lookup"><span data-stu-id="1d60d-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span>

<span data-ttu-id="1d60d-114">Se questo attributo è impostato, il renderer audio utilizza il dispositivo audio predefinito per il ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="1d60d-114">If this attribute is set, the audio renderer uses the default audio device for the specified role.</span></span> <span data-ttu-id="1d60d-115">Il valore di questo attributo è un membro dell'enumerazione **ERole** , che è definito nel file di intestazione mmdeviceapi. h.</span><span class="sxs-lookup"><span data-stu-id="1d60d-115">The value of this attribute is a member of the **ERole** enumeration, which is defined in the header file mmdeviceapi.h.</span></span> <span data-ttu-id="1d60d-116">Per ulteriori informazioni, vedere la documentazione principale sull'API audio.</span><span class="sxs-lookup"><span data-stu-id="1d60d-116">For more information, see the Core Audio API documentation.</span></span> <span data-ttu-id="1d60d-117">Se questo attributo non è impostato, il renderer audio utilizza il dispositivo endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="1d60d-117">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="1d60d-118">Se questo attributo è impostato, non impostare l'attributo [**\_ \_ \_ \_ \_ ID endpoint dell'attributo MF audio RENDERER**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1d60d-118">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span> <span data-ttu-id="1d60d-119">Se entrambi gli attributi sono impostati, si verificherà un errore quando viene creato il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="1d60d-119">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="1d60d-120">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1d60d-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d60d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d60d-121">Requirements</span></span>



| <span data-ttu-id="1d60d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d60d-122">Requirement</span></span> | <span data-ttu-id="1d60d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1d60d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d60d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d60d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d60d-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d60d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1d60d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d60d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d60d-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d60d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1d60d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d60d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d60d-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d60d-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d60d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d60d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d60d-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d60d-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d60d-132">Attributi renderer audio</span><span class="sxs-lookup"><span data-stu-id="1d60d-132">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d60d-133">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="1d60d-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1d60d-134">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="1d60d-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1d60d-135">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="1d60d-135">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




