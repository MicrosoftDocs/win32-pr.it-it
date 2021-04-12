---
description: Specifica se un esempio di supporto è il primo campione dopo un gap nel flusso.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: Attributo MFSampleExtension_Discontinuity (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e401a26c269a3b77d881bc74ae2c7b30d9d88f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527943"
---
# <a name="mfsampleextension_discontinuity-attribute"></a><span data-ttu-id="996a0-103">\_Attributo discontinuità MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="996a0-103">MFSampleExtension\_Discontinuity attribute</span></span>

<span data-ttu-id="996a0-104">Specifica se un esempio di supporto è il primo campione dopo un gap nel flusso.</span><span class="sxs-lookup"><span data-stu-id="996a0-104">Specifies whether a media sample is the first sample after a gap in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="996a0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="996a0-105">Data type</span></span>

<span data-ttu-id="996a0-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="996a0-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="996a0-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="996a0-107">Get/set</span></span>

<span data-ttu-id="996a0-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="996a0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="996a0-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="996a0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="996a0-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="996a0-110">Applies to</span></span>

[<span data-ttu-id="996a0-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="996a0-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="996a0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="996a0-112">Remarks</span></span>

<span data-ttu-id="996a0-113">Questo attributo si applica agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="996a0-113">This attribute applies to media samples.</span></span> <span data-ttu-id="996a0-114">Se questo attributo è true, significa che si è **verificata** una discontinuità nel flusso e questo esempio è il primo a essere visualizzato dopo il gap.</span><span class="sxs-lookup"><span data-stu-id="996a0-114">If this attribute is **TRUE**, it means there was a discontinuity in the stream and this sample is the first to appear after the gap.</span></span>

<span data-ttu-id="996a0-115">Se questo attributo non è impostato, il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="996a0-115">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="996a0-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="996a0-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="996a0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="996a0-117">Requirements</span></span>



| <span data-ttu-id="996a0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="996a0-118">Requirement</span></span> | <span data-ttu-id="996a0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="996a0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="996a0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="996a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="996a0-121">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="996a0-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="996a0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="996a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="996a0-123">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="996a0-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="996a0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="996a0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="996a0-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="996a0-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996a0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="996a0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996a0-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="996a0-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="996a0-128">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="996a0-128">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="996a0-129">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="996a0-129">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




