---
description: Specifica un oggetto attivazione che consente di creare un mixer video personalizzato per il sink multimediale EVR (Enhanced video renderer).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: Attributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130727"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a><span data-ttu-id="cddd2-103">Attiva \_ l' \_ \_ \_ attributo Activate del mixer video personalizzato \_ MF</span><span class="sxs-lookup"><span data-stu-id="cddd2-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_ACTIVATE attribute</span></span>

<span data-ttu-id="cddd2-104">Specifica un oggetto attivazione che consente di creare un mixer video personalizzato per il sink multimediale EVR (Enhanced video renderer).</span><span class="sxs-lookup"><span data-stu-id="cddd2-104">Specifies an activation object that creates a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="cddd2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cddd2-105">Data type</span></span>

<span data-ttu-id="cddd2-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="cddd2-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="cddd2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="cddd2-107">Remarks</span></span>

<span data-ttu-id="cddd2-108">Se si sta creando EVR tramite un oggetto Activation, è possibile usare questo attributo per impostare un mixer video personalizzato in EVR.</span><span class="sxs-lookup"><span data-stu-id="cddd2-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="cddd2-109">Usare questo attributo come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="cddd2-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="cddd2-110">Chiamare la funzione [_ *MFCreateVideoRendererActivate* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare un oggetto Activation per il EVR.</span><span class="sxs-lookup"><span data-stu-id="cddd2-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="cddd2-111">La funzione restituisce un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="cddd2-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="cddd2-112">Impostare questo attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chiamando [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="cddd2-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="cddd2-113">Il valore dell'attributo è un puntatore a un oggetto di attivazione implementato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="cddd2-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="cddd2-114">L'oggetto attivazione del chiamante deve esporre l'interfaccia **IMFActivate** .</span><span class="sxs-lookup"><span data-stu-id="cddd2-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="cddd2-115">Se si imposta questo attributo, EVR chiama [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare il mixer video personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cddd2-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video mixer.</span></span> <span data-ttu-id="cddd2-116">Il mixer video deve esporre l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="cddd2-116">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span>

<span data-ttu-id="cddd2-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cddd2-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cddd2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cddd2-118">Requirements</span></span>



| <span data-ttu-id="cddd2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cddd2-119">Requirement</span></span> | <span data-ttu-id="cddd2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cddd2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cddd2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cddd2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cddd2-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cddd2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cddd2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cddd2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cddd2-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cddd2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cddd2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cddd2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cddd2-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cddd2-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cddd2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cddd2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cddd2-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cddd2-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cddd2-129">Attributi renderer video avanzati</span><span class="sxs-lookup"><span data-stu-id="cddd2-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="cddd2-130">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="cddd2-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="cddd2-131">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="cddd2-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="cddd2-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="cddd2-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="cddd2-133">Oggetti attivazione</span><span class="sxs-lookup"><span data-stu-id="cddd2-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




