---
description: Consente al renderer video avanzato (EVR) di migliorare le prestazioni usando il deinterlacciamento Bob.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: Attributo EVRConfig_AllowDropToBob (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401532"
---
# <a name="evrconfig_allowdroptobob-attribute"></a><span data-ttu-id="9db4c-103">\_Attributo AllowDropToBob di EVRConfig</span><span class="sxs-lookup"><span data-stu-id="9db4c-103">EVRConfig\_AllowDropToBob attribute</span></span>

<span data-ttu-id="9db4c-104">Consente al renderer video avanzato (EVR) di migliorare le prestazioni usando il deinterlacciamento Bob.</span><span class="sxs-lookup"><span data-stu-id="9db4c-104">Allows the Enhanced Video Renderer (EVR) to improve performance by using bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="9db4c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9db4c-105">Data type</span></span>

<span data-ttu-id="9db4c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9db4c-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9db4c-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="9db4c-107">Get/set</span></span>

<span data-ttu-id="9db4c-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9db4c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9db4c-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="9db4c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="9db4c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9db4c-110">Remarks</span></span>

<span data-ttu-id="9db4c-111">Questo attributo può essere impostato sul sink EVRmedia.</span><span class="sxs-lookup"><span data-stu-id="9db4c-111">This attribute can be set on the EVRmedia sink.</span></span> <span data-ttu-id="9db4c-112">Per impostare l'attributo, **QueryInterface** esegue una query sul sink multimediale EVR per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="9db4c-112">To set the attribute, **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="9db4c-113">L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoMixPrefs \_ ALLOWDROPTOBOB** in EVR.</span><span class="sxs-lookup"><span data-stu-id="9db4c-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_AllowDropToBob** flag on the EVR.</span></span> <span data-ttu-id="9db4c-114">Per una descrizione di questo flag, vedere [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="9db4c-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="9db4c-115">La costante GUID per questo attributo viene esportata da strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="9db4c-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db4c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9db4c-116">Requirements</span></span>



| <span data-ttu-id="9db4c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db4c-117">Requirement</span></span> | <span data-ttu-id="9db4c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9db4c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9db4c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9db4c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9db4c-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9db4c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9db4c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9db4c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9db4c-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9db4c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9db4c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9db4c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db4c-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db4c-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db4c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9db4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db4c-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9db4c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9db4c-127">Attributi EVR</span><span class="sxs-lookup"><span data-stu-id="9db4c-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9db4c-128">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="9db4c-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




