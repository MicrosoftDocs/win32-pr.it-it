---
description: Impone al renderer video avanzato (EVR) di combinare il video in un rettangolo di dimensioni minori rispetto al rettangolo di output, quindi ridimensionare il risultato.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: Attributo EVRConfig_ForceScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82b7e017d414e86b8b4332fe5646e4808d4009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049303"
---
# <a name="evrconfig_forcescaling-attribute"></a><span data-ttu-id="6fcea-103">\_Attributo ForceScaling di EVRConfig</span><span class="sxs-lookup"><span data-stu-id="6fcea-103">EVRConfig\_ForceScaling attribute</span></span>

<span data-ttu-id="6fcea-104">Impone al renderer video avanzato (EVR) di combinare il video in un rettangolo di dimensioni minori rispetto al rettangolo di output, quindi ridimensionare il risultato.</span><span class="sxs-lookup"><span data-stu-id="6fcea-104">Forces the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span>

## <a name="data-type"></a><span data-ttu-id="6fcea-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6fcea-105">Data type</span></span>

<span data-ttu-id="6fcea-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6fcea-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6fcea-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="6fcea-107">Get/set</span></span>

<span data-ttu-id="6fcea-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6fcea-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6fcea-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="6fcea-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="6fcea-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fcea-110">Remarks</span></span>

<span data-ttu-id="6fcea-111">Questo attributo può essere impostato sul sink di supporto EVR.</span><span class="sxs-lookup"><span data-stu-id="6fcea-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="6fcea-112">Per impostare l'attributo, utilizzare **QueryInterface** per eseguire una query sul sink multimediale EVR per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="6fcea-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="6fcea-113">L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoRenderPrefs \_ FORCESCALING** in EVR.</span><span class="sxs-lookup"><span data-stu-id="6fcea-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceScaling** flag on the EVR.</span></span> <span data-ttu-id="6fcea-114">Per una descrizione di questo flag, vedere [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="6fcea-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="6fcea-115">La costante GUID per questo attributo viene esportata da strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="6fcea-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcea-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fcea-116">Requirements</span></span>



| <span data-ttu-id="6fcea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fcea-117">Requirement</span></span> | <span data-ttu-id="6fcea-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcea-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcea-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcea-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6fcea-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6fcea-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcea-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6fcea-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6fcea-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fcea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fcea-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fcea-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fcea-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fcea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fcea-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6fcea-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6fcea-127">Attributi EVR</span><span class="sxs-lookup"><span data-stu-id="6fcea-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="6fcea-128">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="6fcea-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




