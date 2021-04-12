---
description: CLSID di un mixer video personalizzato per il sink multimediale Enhanced video renderer (EVR).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: Attributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343946"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a><span data-ttu-id="0744e-103">\_Attributo CLSID per l'attivazione del \_ \_ mixer video personalizzato \_ \_</span><span class="sxs-lookup"><span data-stu-id="0744e-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID attribute</span></span>

<span data-ttu-id="0744e-104">CLSID di un mixer video personalizzato per il sink multimediale Enhanced video renderer (EVR).</span><span class="sxs-lookup"><span data-stu-id="0744e-104">CLSID of a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="0744e-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0744e-105">Data type</span></span>

<span data-ttu-id="0744e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="0744e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="0744e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="0744e-107">Remarks</span></span>

<span data-ttu-id="0744e-108">Se si sta creando EVR tramite un oggetto Activation, è possibile usare questo attributo per impostare un mixer video personalizzato in EVR.</span><span class="sxs-lookup"><span data-stu-id="0744e-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="0744e-109">Usare questo attributo come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0744e-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="0744e-110">Chiamare la funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare un oggetto Activation per il EVR.</span><span class="sxs-lookup"><span data-stu-id="0744e-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="0744e-111">La funzione restituisce un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="0744e-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="0744e-112">Impostare questo attribue sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chiamando [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="0744e-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="0744e-113">Il valore dell'attributo è il CLSID del mixer video personalizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0744e-113">The value of the attribute is the CLSID of the application's custom video mixer.</span></span>

<span data-ttu-id="0744e-114">Se questo attributo è impostato, EVR chiama **CoCreateInstance** con il CLSID specificato per creare il mixer video personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0744e-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video mixer.</span></span> <span data-ttu-id="0744e-115">Il mixer video deve esporre l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="0744e-115">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="0744e-116">Il mixer viene creato come server COM in-process.</span><span class="sxs-lookup"><span data-stu-id="0744e-116">The mixer is created as an in-process COM server.</span></span>

<span data-ttu-id="0744e-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0744e-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0744e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0744e-118">Requirements</span></span>



| <span data-ttu-id="0744e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0744e-119">Requirement</span></span> | <span data-ttu-id="0744e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0744e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0744e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0744e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0744e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0744e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0744e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0744e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0744e-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0744e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0744e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0744e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0744e-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0744e-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0744e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0744e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0744e-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0744e-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0744e-129">Attributi renderer video avanzati</span><span class="sxs-lookup"><span data-stu-id="0744e-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="0744e-130">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="0744e-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="0744e-131">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="0744e-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="0744e-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="0744e-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="0744e-133">Oggetti attivazione</span><span class="sxs-lookup"><span data-stu-id="0744e-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




