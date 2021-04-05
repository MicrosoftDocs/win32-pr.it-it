---
description: Specifica come creare un Presenter personalizzato per il renderer video avanzato (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: Attributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057851"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a><span data-ttu-id="3d5ad-103">Attributo per l' \_ attivazione di flag del \_ \_ Presenter video personalizzati \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d5ad-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS attribute</span></span>

<span data-ttu-id="3d5ad-104">Specifica come creare un Presenter personalizzato per il renderer video avanzato (EVR).</span><span class="sxs-lookup"><span data-stu-id="3d5ad-104">Specifies how to create a custom presenter for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="3d5ad-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3d5ad-105">Data type</span></span>

<span data-ttu-id="3d5ad-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3d5ad-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3d5ad-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d5ad-107">Remarks</span></span>

<span data-ttu-id="3d5ad-108">È possibile impostare questo attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ottenuto dalla funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="3d5ad-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="3d5ad-109">Il valore di questo attributo è un **or** bit per bit dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d5ad-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="3d5ad-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5ad-110">Value</span></span>                                          | <span data-ttu-id="3d5ad-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d5ad-111">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5ad-112">**MF \_ Activate \_ \_ ALLOWFAIL Presenter \_ personalizzato**</span><span class="sxs-lookup"><span data-stu-id="3d5ad-112">**MF\_ACTIVATE\_CUSTOM\_PRESENTER\_ALLOWFAIL**</span></span> | <span data-ttu-id="3d5ad-113">Se il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) non riesce a creare il relatore personalizzato dell'applicazione, USA invece il relatore EVR predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d5ad-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom presenter, it uses the default EVR presenter instead.</span></span> <span data-ttu-id="3d5ad-114">Per impostazione predefinita, se l'oggetto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ha esito negativo quando tenta di creare il Presenter personalizzato, il metodo **ActivateObject** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3d5ad-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom presenter, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="3d5ad-115">Le applicazioni possono usare l'attributo [**\_ \_ CLSID Activate Custom \_ video \_ Presenter \_ CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) per specificare un Presenter personalizzato per la EVR.</span><span class="sxs-lookup"><span data-stu-id="3d5ad-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) attribute to specify a custom presenter for the EVR.</span></span>

<span data-ttu-id="3d5ad-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3d5ad-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d5ad-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d5ad-117">Requirements</span></span>



| <span data-ttu-id="3d5ad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d5ad-118">Requirement</span></span> | <span data-ttu-id="3d5ad-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5ad-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5ad-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d5ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5ad-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d5ad-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d5ad-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d5ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5ad-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3d5ad-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d5ad-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d5ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d5ad-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5ad-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d5ad-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d5ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5ad-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d5ad-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d5ad-128">Attributi renderer video avanzati</span><span class="sxs-lookup"><span data-stu-id="3d5ad-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d5ad-129">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="3d5ad-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3d5ad-130">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="3d5ad-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3d5ad-131">Oggetti attivazione</span><span class="sxs-lookup"><span data-stu-id="3d5ad-131">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="3d5ad-132">Come scrivere un presentatore EVR</span><span class="sxs-lookup"><span data-stu-id="3d5ad-132">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




