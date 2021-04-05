---
description: Specifica come creare un mixer personalizzato per il renderer video avanzato (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Attributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757868"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a><span data-ttu-id="e11a5-103">Attributo per l' \_ attivazione di \_ \_ \_ flag mixer video personalizzati \_</span><span class="sxs-lookup"><span data-stu-id="e11a5-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_FLAGS attribute</span></span>

<span data-ttu-id="e11a5-104">Specifica come creare un mixer personalizzato per il renderer video avanzato (EVR).</span><span class="sxs-lookup"><span data-stu-id="e11a5-104">Specifies how to create a custom mixer for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="e11a5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e11a5-105">Data type</span></span>

<span data-ttu-id="e11a5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e11a5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e11a5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e11a5-107">Remarks</span></span>

<span data-ttu-id="e11a5-108">È possibile impostare questo attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ottenuto dalla funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="e11a5-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="e11a5-109">Il valore di questo attributo è un **or** bit per bit dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e11a5-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="e11a5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e11a5-110">Value</span></span>                                      | <span data-ttu-id="e11a5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11a5-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11a5-112">**\_ \_ \_ ALLOWFAIL mixer personalizzato MF \_ Activate**</span><span class="sxs-lookup"><span data-stu-id="e11a5-112">**MF\_ACTIVATE\_CUSTOM\_MIXER\_ALLOWFAIL**</span></span> | <span data-ttu-id="e11a5-113">Se il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) non riesce a creare il mixer personalizzato dell'applicazione, USA invece il mixer EVR predefinito.</span><span class="sxs-lookup"><span data-stu-id="e11a5-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom mixer, it uses the default EVR mixer instead.</span></span> <span data-ttu-id="e11a5-114">Per impostazione predefinita, se l'oggetto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ha esito negativo quando tenta di creare il mixer personalizzato, il metodo **ActivateObject** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e11a5-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom mixer, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="e11a5-115">Le applicazioni possono usare l'attributo [**MF \_ Activate \_ Custom \_ video \_ mixer \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) per specificare un mixer personalizzato per la EVR.</span><span class="sxs-lookup"><span data-stu-id="e11a5-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) attribute to specify a custom mixer for the EVR.</span></span>

<span data-ttu-id="e11a5-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e11a5-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e11a5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e11a5-117">Requirements</span></span>



| <span data-ttu-id="e11a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e11a5-118">Requirement</span></span> | <span data-ttu-id="e11a5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e11a5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e11a5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e11a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e11a5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e11a5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e11a5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e11a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e11a5-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e11a5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e11a5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e11a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e11a5-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e11a5-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e11a5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e11a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11a5-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e11a5-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e11a5-128">Attributi renderer video avanzati</span><span class="sxs-lookup"><span data-stu-id="e11a5-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="e11a5-129">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="e11a5-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e11a5-130">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="e11a5-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e11a5-131">Oggetti attivazione</span><span class="sxs-lookup"><span data-stu-id="e11a5-131">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




