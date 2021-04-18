---
description: Specifica se il caricatore della topologia Abilita il processore del video transcodificato (XVP). per le conversioni, abilitazione della conversione di colori con accelerazione hardware.
title: Attributo MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321590"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a><span data-ttu-id="8ac1b-104">\_ \_ Abilita \_ XVP per la topologia MF \_ per l' \_ attributo playback</span><span class="sxs-lookup"><span data-stu-id="8ac1b-104">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK attribute</span></span>

<span data-ttu-id="8ac1b-105">Specifica se il caricatore della topologia Abilita il processore del video transcodificato (XVP).</span><span class="sxs-lookup"><span data-stu-id="8ac1b-105">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="8ac1b-106">per le conversioni, abilitazione della conversione di colori con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="8ac1b-106">for conversions, enabling hardware accelerated color conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="8ac1b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8ac1b-107">Data type</span></span>

<span data-ttu-id="8ac1b-108">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ac1b-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8ac1b-109">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="8ac1b-109">Get/set</span></span>

<span data-ttu-id="8ac1b-110">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8ac1b-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8ac1b-111">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="8ac1b-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8ac1b-112">Si applica a</span><span class="sxs-lookup"><span data-stu-id="8ac1b-112">Applies to</span></span>

[<span data-ttu-id="8ac1b-113">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="8ac1b-113">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="8ac1b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ac1b-114">Remarks</span></span>

<span data-ttu-id="8ac1b-115">Se questo attributo è impostato, il caricatore della topologia effettuerà il pull del processore video, se necessario, durante la risoluzione della topologia non transcodifica.</span><span class="sxs-lookup"><span data-stu-id="8ac1b-115">If this attribute is set, the topology loader will pull in the video processor, if necessary, during non-transcode topology resolution.</span></span> <span data-ttu-id="8ac1b-116">Quando si utilizza la topologia per creare un [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) personalizzato, questo attributo indica al caricatore di usare XVP per le conversioni anziché il convertitore di colori legacy, abilitando così la conversione dei colori accelerata hardware; il convertitore di colori legacy è solo software.</span><span class="sxs-lookup"><span data-stu-id="8ac1b-116">When you are using the topology to build your own [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) this attribute tells the loader to use XVP for conversions instead of the legacy color converter, thus enabling hardware accelerated color conversion; the legacy color converter is software-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac1b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ac1b-117">Requirements</span></span>



| <span data-ttu-id="8ac1b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ac1b-118">Requirement</span></span> | <span data-ttu-id="8ac1b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8ac1b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac1b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ac1b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ac1b-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8ac1b-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ac1b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ac1b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ac1b-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ac1b-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8ac1b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ac1b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ac1b-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac1b-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac1b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ac1b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac1b-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ac1b-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ac1b-128">Gestione dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="8ac1b-128">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="8ac1b-129">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="8ac1b-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




