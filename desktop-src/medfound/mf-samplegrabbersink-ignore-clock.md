---
description: Specifica se il sink Sample-Grabber usa il clock di presentazione per pianificare gli esempi.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Attributo MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314028"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a><span data-ttu-id="e7b2a-103">\_ \_ Attributo Clock MF SAMPLEGRABBERSINK ignore \_</span><span class="sxs-lookup"><span data-stu-id="e7b2a-103">MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute</span></span>

<span data-ttu-id="e7b2a-104">Specifica se il sink Sample-Grabber usa il clock di presentazione per pianificare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-104">Specifies whether the sample-grabber sink uses the presentation clock to schedule samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="e7b2a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e7b2a-105">Data type</span></span>

<span data-ttu-id="e7b2a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e7b2a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e7b2a-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="e7b2a-107">Get/set</span></span>

<span data-ttu-id="e7b2a-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e7b2a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e7b2a-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b2a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7b2a-110">Remarks</span></span>

<span data-ttu-id="e7b2a-111">È possibile impostare questo attributo sull'oggetto attivazione creato dalla funzione [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="e7b2a-111">You can set this attribute on the activation object created by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="e7b2a-112">Impostare l'attributo prima di chiamare il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sull'oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-112">Set the attribute before calling the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method on the activation object.</span></span>

<span data-ttu-id="e7b2a-113">Per impostazione predefinita, quando il sink Sample-Grabber riceve un campione, attende che l'ora di presentazione dell'esempio richiami il callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-113">By default, when the sample-grabber sink receives a sample, it waits until the presentation time of the sample to invoke the application's callback.</span></span> <span data-ttu-id="e7b2a-114">Se l' \_ \_ attributo Clock MF SAMPLEGRABBERSINK ignore \_ è diverso da zero, il sink Sample-Grabber ignora il clock di presentazione e richiama il callback non appena riceve ogni campione.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-114">If the MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute is nonzero, the sample-grabber sink ignores the presentation clock and invokes the callback as soon as it receives each sample.</span></span>

<span data-ttu-id="e7b2a-115">Utilizzo consigliato:</span><span class="sxs-lookup"><span data-stu-id="e7b2a-115">Recommended usage:</span></span>

-   <span data-ttu-id="e7b2a-116">Se si desidera elaborare i campioni il più rapidamente possibile, impostare questo attributo su **true**.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-116">If you want to process samples as quickly as possible, set this attribute to **TRUE**.</span></span>
-   <span data-ttu-id="e7b2a-117">Se si desidera che le chiamate al metodo di callback siano sincronizzate con il clock, non impostare questo attributo o impostarlo su **false**.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-117">If you want the calls to the callback method to be synchronized with the clock, either do not set this attribute or set it to **FALSE**.</span></span> <span data-ttu-id="e7b2a-118">È possibile ottenere campioni leggermente più avanti rispetto al clock, rimanendo comunque sincronizzati, impostando l'attributo di [**\_ offset dell'ora di \_ esempio \_ \_ MF SAMPLEGRABBERSINK**](mf-samplegrabbersink-sample-time-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b2a-118">You can get samples slightly ahead of the clock, while still remaining synchronized, by setting the [**MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) attribute.</span></span>

<span data-ttu-id="e7b2a-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e7b2a-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b2a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b2a-120">Requirements</span></span>



| <span data-ttu-id="e7b2a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b2a-121">Requirement</span></span> | <span data-ttu-id="e7b2a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b2a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b2a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b2a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b2a-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7b2a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e7b2a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b2a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b2a-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b2a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e7b2a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b2a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b2a-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b2a-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b2a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7b2a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b2a-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7b2a-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7b2a-131">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7b2a-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




