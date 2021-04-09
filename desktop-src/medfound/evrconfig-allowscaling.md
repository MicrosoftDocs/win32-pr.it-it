---
description: Alllows il renderer video migliorato (EVR) per combinare il video in un rettangolo di dimensioni minori rispetto al rettangolo di output, quindi ridimensionare il risultato.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: Attributo EVRConfig_AllowScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1d0662c7145d9f5c5484df81c2483305402850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878441"
---
# <a name="evrconfig_allowscaling-attribute"></a><span data-ttu-id="dbb09-103">\_Attributo AllowScaling di EVRConfig</span><span class="sxs-lookup"><span data-stu-id="dbb09-103">EVRConfig\_AllowScaling attribute</span></span>

<span data-ttu-id="dbb09-104">Alllows il renderer video migliorato (EVR) per combinare il video in un rettangolo di dimensioni minori rispetto al rettangolo di output, quindi ridimensionare il risultato.</span><span class="sxs-lookup"><span data-stu-id="dbb09-104">Alllows the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span>

## <a name="data-type"></a><span data-ttu-id="dbb09-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="dbb09-105">Data type</span></span>

<span data-ttu-id="dbb09-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dbb09-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="dbb09-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="dbb09-107">Get/set</span></span>

<span data-ttu-id="dbb09-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="dbb09-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="dbb09-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="dbb09-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbb09-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbb09-110">Remarks</span></span>

<span data-ttu-id="dbb09-111">Questo attributo può essere impostato sul sink di supporto EVR.</span><span class="sxs-lookup"><span data-stu-id="dbb09-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="dbb09-112">Per impostare l'attributo, utilizzare **QueryInterface** per eseguire una query sul sink multimediale EVR per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="dbb09-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="dbb09-113">L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoRenderPrefs \_ ALLOWSCALING** in EVR.</span><span class="sxs-lookup"><span data-stu-id="dbb09-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowScaling** flag on the EVR.</span></span> <span data-ttu-id="dbb09-114">Per una descrizione di questo flag, vedere [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="dbb09-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="dbb09-115">La costante GUID per questo attributo viene esportata da strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="dbb09-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb09-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbb09-116">Requirements</span></span>



| <span data-ttu-id="dbb09-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb09-117">Requirement</span></span> | <span data-ttu-id="dbb09-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dbb09-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb09-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbb09-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb09-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dbb09-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dbb09-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbb09-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb09-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbb09-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="dbb09-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbb09-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb09-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbb09-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb09-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbb09-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb09-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dbb09-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dbb09-127">Attributi EVR</span><span class="sxs-lookup"><span data-stu-id="dbb09-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="dbb09-128">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="dbb09-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




