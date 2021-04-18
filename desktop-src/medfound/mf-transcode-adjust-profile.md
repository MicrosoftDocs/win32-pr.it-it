---
description: Flag del profilo che definiscono le impostazioni del flusso per la topologia transcodifica. I flag sono definiti nell'enumerazione dei \_ flag del profilo MF transcode \_ Adjust \_ \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: Attributo MF_TRANSCODE_ADJUST_PROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308430"
---
# <a name="mf_transcode_adjust_profile-attribute"></a><span data-ttu-id="3e7ee-104">\_Attributo MF transcode \_ Adjust \_ profile</span><span class="sxs-lookup"><span data-stu-id="3e7ee-104">MF\_TRANSCODE\_ADJUST\_PROFILE attribute</span></span>

<span data-ttu-id="3e7ee-105">Flag del profilo che definiscono le impostazioni del flusso per la topologia transcodifica.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-105">Profile flags that define the stream settings for the transcode topology.</span></span> <span data-ttu-id="3e7ee-106">I flag sono definiti nell'enumerazione [**dei \_ \_ \_ \_ flag del profilo MF transcode Adjust**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .</span><span class="sxs-lookup"><span data-stu-id="3e7ee-106">The flags are defined in the [**MF\_TRANSCODE\_ADJUST\_PROFILE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e7ee-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3e7ee-107">Data type</span></span>

<span data-ttu-id="3e7ee-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3e7ee-108">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3e7ee-109">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="3e7ee-109">Get/set</span></span>

<span data-ttu-id="3e7ee-110">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3e7ee-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3e7ee-111">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e7ee-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e7ee-112">Remarks</span></span>

<span data-ttu-id="3e7ee-113">Un'applicazione può impostare questo attributo a livello di contenitore sul profilo transcodifica.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-113">An application can set this attribute at the container level on the transcode profile.</span></span> <span data-ttu-id="3e7ee-114">Se questo attributo è impostato, la funzione [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) modifica gli attributi del flusso durante la compilazione della topologia, a seconda del flag specificato.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-114">If this attribute is set, the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function changes the stream attributes during topology building, depending on the specified flag.</span></span> <span data-ttu-id="3e7ee-115">Se, ad esempio, l'applicazione specifica il flag **\_ predefinito MF transcode \_ Adjust \_ profile \_** , per creare il profilo vengono usate le impostazioni di flusso specificate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-115">For example, if the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_DEFAULT** flag, the application-specified stream settings are used to create the profile.</span></span>

<span data-ttu-id="3e7ee-116">Per il flusso video, la frequenza dei fotogrammi viene aggiornata in base all'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-116">For the video stream, the frame rate is updated based on the media source.</span></span> <span data-ttu-id="3e7ee-117">Se l'applicazione non specifica la modalità interlacciata, il profilo viene aggiornato in modo da usare i frame progressivi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-117">If the application does not specify the interlaced mode, the profile is updated to use progressive frames by default.</span></span>

<span data-ttu-id="3e7ee-118">Se l'applicazione specifica il flag **MF \_ transcode \_ Adjust \_ \_ use \_ source \_ Attributes** , gli attributi di flusso mancanti vengono copiati dall'origine del supporto di input nelle impostazioni del flusso nel profilo transcodifica.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-118">If the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_USE\_SOURCE\_ATTRIBUTES** flag, then missing stream attributes are copied from the input media source to the stream settings in the transcode profile.</span></span>

<span data-ttu-id="3e7ee-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3e7ee-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e7ee-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e7ee-120">Requirements</span></span>



| <span data-ttu-id="3e7ee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e7ee-121">Requirement</span></span> | <span data-ttu-id="3e7ee-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3e7ee-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7ee-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e7ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3e7ee-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e7ee-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3e7ee-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e7ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3e7ee-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e7ee-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3e7ee-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e7ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e7ee-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e7ee-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e7ee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e7ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e7ee-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e7ee-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e7ee-131">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="3e7ee-131">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="3e7ee-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="3e7ee-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




