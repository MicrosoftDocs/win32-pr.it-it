---
description: Impone al renderer video avanzato (EVR) di ignorare il secondo campo di ogni frame interlacciato.
ms.assetid: b79d9230-b127-4e9b-b73b-685ce27aefa9
title: Attributo EVRConfig_ForceHalfInterlace (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfeab4bcb3d05e615962fb8acc5f304ba3ea7e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305382"
---
# <a name="evrconfig_forcehalfinterlace-attribute"></a><span data-ttu-id="d4f9b-103">\_Attributo ForceHalfInterlace di EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d4f9b-103">EVRConfig\_ForceHalfInterlace attribute</span></span>

<span data-ttu-id="d4f9b-104">Impone al renderer video avanzato (EVR) di ignorare il secondo campo di ogni frame interlacciato.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-104">Forces the Enhanced Video Renderer (EVR) to skip the second field of every interlaced frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4f9b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d4f9b-105">Data type</span></span>

<span data-ttu-id="d4f9b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d4f9b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d4f9b-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="d4f9b-107">Get/set</span></span>

<span data-ttu-id="d4f9b-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d4f9b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d4f9b-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4f9b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4f9b-110">Remarks</span></span>

<span data-ttu-id="d4f9b-111">Questo attributo può essere impostato sul sink di supporto EVR.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="d4f9b-112">Per impostare l'attributo, utilizzare **QueryInterface** per eseguire una query sul sink multimediale EVR per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="d4f9b-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="d4f9b-113">L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoMixPrefs \_ FORCEHALFINTERLACE** in EVR.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_ForceHalfInterlace** flag on the EVR.</span></span> <span data-ttu-id="d4f9b-114">Per una descrizione di questo flag, vedere [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="d4f9b-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="d4f9b-115">La costante GUID per questo attributo viene esportata da strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f9b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4f9b-116">Requirements</span></span>



| <span data-ttu-id="d4f9b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f9b-117">Requirement</span></span> | <span data-ttu-id="d4f9b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f9b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f9b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f9b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f9b-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d4f9b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d4f9b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f9b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f9b-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4f9b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d4f9b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4f9b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f9b-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f9b-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f9b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4f9b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f9b-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4f9b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4f9b-127">Attributi EVR</span><span class="sxs-lookup"><span data-stu-id="d4f9b-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4f9b-128">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="d4f9b-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




