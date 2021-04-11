---
description: Specifica la frequenza di aggiornamento del monitoraggio.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: Attributo MF_TOPOLOGY_PLAYBACK_FRAMERATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226631"
---
# <a name="mf_topology_playback_framerate-attribute"></a><span data-ttu-id="140ae-103">\_ \_ Attributo framerate riproduzione MF topologia \_</span><span class="sxs-lookup"><span data-stu-id="140ae-103">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE attribute</span></span>

<span data-ttu-id="140ae-104">Specifica la frequenza di aggiornamento del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="140ae-104">Specifies the monitor refresh rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="140ae-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="140ae-105">Data type</span></span>

<span data-ttu-id="140ae-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="140ae-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="140ae-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="140ae-107">Get/set</span></span>

<span data-ttu-id="140ae-108">Per ottenere questo attributo, chiamare [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="140ae-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="140ae-109">Per impostare questo attributo, chiamare [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="140ae-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="applies-to"></a><span data-ttu-id="140ae-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="140ae-110">Applies to</span></span>

[<span data-ttu-id="140ae-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="140ae-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="140ae-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="140ae-112">Remarks</span></span>

<span data-ttu-id="140ae-113">Il caricatore della topologia usa questo attributo per ottimizzare la pipeline prima che venga avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="140ae-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="140ae-114">Se si imposta questo attributo, impostare anche l'attributo di ottimizzazione per la [ \_ \_ \_ \_ riproduzione statica della topologia MF](mf-topology-static-playback-optimizations.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="140ae-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="140ae-115">La frequenza dei fotogrammi è espressa come rapporto.</span><span class="sxs-lookup"><span data-stu-id="140ae-115">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="140ae-116">I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore.</span><span class="sxs-lookup"><span data-stu-id="140ae-116">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span>

<span data-ttu-id="140ae-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="140ae-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="140ae-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="140ae-118">Requirements</span></span>



| <span data-ttu-id="140ae-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="140ae-119">Requirement</span></span> | <span data-ttu-id="140ae-120">Valore</span><span class="sxs-lookup"><span data-stu-id="140ae-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="140ae-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="140ae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="140ae-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="140ae-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="140ae-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="140ae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="140ae-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="140ae-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="140ae-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="140ae-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="140ae-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="140ae-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140ae-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="140ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140ae-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="140ae-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="140ae-129">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="140ae-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="140ae-130">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="140ae-130">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




