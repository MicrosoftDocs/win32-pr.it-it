---
description: Consente al renderer video avanzato (EVR) di limitare l'output in modo che corrisponda alla larghezza di banda della GPU.
ms.assetid: d591af2e-d47d-4220-a4f6-968f2ac45284
title: Attributo EVRConfig_AllowDropToThrottle (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97cbab6fae6644b3c0187d09edb59ab2538012e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049304"
---
# <a name="evrconfig_allowdroptothrottle-attribute"></a><span data-ttu-id="662b6-103">\_Attributo AllowDropToThrottle di EVRConfig</span><span class="sxs-lookup"><span data-stu-id="662b6-103">EVRConfig\_AllowDropToThrottle attribute</span></span>

<span data-ttu-id="662b6-104">Consente al renderer video avanzato (EVR) di limitare l'output in modo che corrisponda alla larghezza di banda della GPU.</span><span class="sxs-lookup"><span data-stu-id="662b6-104">Allows the Enhanced Video Renderer (EVR) to limit its output to match GPU bandwidth.</span></span>

## <a name="data-type"></a><span data-ttu-id="662b6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="662b6-105">Data type</span></span>

<span data-ttu-id="662b6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="662b6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="662b6-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="662b6-107">Get/set</span></span>

<span data-ttu-id="662b6-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="662b6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="662b6-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="662b6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="662b6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="662b6-110">Remarks</span></span>

<span data-ttu-id="662b6-111">Questo attributo può essere impostato sul sink di supporto EVR.</span><span class="sxs-lookup"><span data-stu-id="662b6-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="662b6-112">Per impostare l'attributo, utilizzare **QueryInterface** per eseguire una query sul sink multimediale EVR per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="662b6-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="662b6-113">L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoRenderPrefs \_ ALLOWOUTPUTTHROTTLING** in EVR.</span><span class="sxs-lookup"><span data-stu-id="662b6-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowOutputThrottling** flag on the EVR.</span></span> <span data-ttu-id="662b6-114">Per una descrizione di questo flag, vedere [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="662b6-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="662b6-115">La costante GUID per questo attributo viene esportata da strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="662b6-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="662b6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="662b6-116">Requirements</span></span>



| <span data-ttu-id="662b6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="662b6-117">Requirement</span></span> | <span data-ttu-id="662b6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="662b6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="662b6-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="662b6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="662b6-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="662b6-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="662b6-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="662b6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="662b6-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="662b6-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="662b6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="662b6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="662b6-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="662b6-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="662b6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="662b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="662b6-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="662b6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="662b6-127">Attributi EVR</span><span class="sxs-lookup"><span data-stu-id="662b6-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="662b6-128">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="662b6-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




