---
description: Specifica le dimensioni della finestra di destinazione per la riproduzione video.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: Attributo MF_TOPOLOGY_PLAYBACK_MAX_DIMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226630"
---
# <a name="mf_topology_playback_max_dims-attribute"></a><span data-ttu-id="8e313-103">\_ \_ \_ Attributo max Dim playback per la riproduzione della topologia \_</span><span class="sxs-lookup"><span data-stu-id="8e313-103">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS attribute</span></span>

<span data-ttu-id="8e313-104">Specifica le dimensioni della finestra di destinazione per la riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="8e313-104">Specifies the size of the destination window for video playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e313-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8e313-105">Data type</span></span>

<span data-ttu-id="8e313-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="8e313-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="8e313-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="8e313-107">Get/set</span></span>

<span data-ttu-id="8e313-108">Per ottenere questo attributo, chiamare [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span><span class="sxs-lookup"><span data-stu-id="8e313-108">To get this attribute, call [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span></span>

<span data-ttu-id="8e313-109">Per impostare questo attributo, chiamare [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span><span class="sxs-lookup"><span data-stu-id="8e313-109">To set this attribute, call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8e313-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="8e313-110">Applies to</span></span>

[<span data-ttu-id="8e313-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="8e313-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="8e313-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e313-112">Remarks</span></span>

<span data-ttu-id="8e313-113">Il caricatore della topologia usa questo attributo per ottimizzare la pipeline prima che venga avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="8e313-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="8e313-114">Se si imposta questo attributo, impostare anche l'attributo di ottimizzazione per la [ \_ \_ \_ \_ riproduzione statica della topologia MF](mf-topology-static-playback-optimizations.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="8e313-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="8e313-115">I 32 bit superiori del valore dell'attributo contengono la larghezza e i 32 bit inferiori contengono l'altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8e313-115">The upper 32 bits of the attribute value contain the width and the lower 32 bits contain the height, both in pixels.</span></span>

<span data-ttu-id="8e313-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8e313-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e313-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e313-117">Requirements</span></span>



| <span data-ttu-id="8e313-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e313-118">Requirement</span></span> | <span data-ttu-id="8e313-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8e313-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e313-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e313-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e313-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e313-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8e313-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e313-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e313-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e313-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8e313-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e313-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e313-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e313-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e313-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e313-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e313-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8e313-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e313-128">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="8e313-128">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e313-129">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="8e313-129">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




