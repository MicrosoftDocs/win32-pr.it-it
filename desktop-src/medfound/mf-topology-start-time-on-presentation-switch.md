---
description: Specifica l'ora di inizio per le presentazioni accodate dopo la prima presentazione.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: Attributo MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308455"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a><span data-ttu-id="f4d96-103">\_Ora di inizio della topologia MF \_ \_ \_ sull' \_ attributo del \_ comcambio di presentazione</span><span class="sxs-lookup"><span data-stu-id="f4d96-103">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute</span></span>

<span data-ttu-id="f4d96-104">Specifica l'ora di inizio per le presentazioni accodate dopo la prima presentazione.</span><span class="sxs-lookup"><span data-stu-id="f4d96-104">Specifies the start time for presentations that are queued after the first presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4d96-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f4d96-105">Data type</span></span>

<span data-ttu-id="f4d96-106">**Int64** archiviato come **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4d96-106">**INT64** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="f4d96-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="f4d96-107">Get/set</span></span>

<span data-ttu-id="f4d96-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="f4d96-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="f4d96-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="f4d96-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f4d96-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="f4d96-110">Applies To</span></span>

[<span data-ttu-id="f4d96-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="f4d96-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="f4d96-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4d96-112">Remarks</span></span>

<span data-ttu-id="f4d96-113">Quando l'applicazione Accoda la prima presentazione nella sessione multimediale, l'applicazione specifica l'ora di inizio nel parametro *pvarStartPosition* del metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) .</span><span class="sxs-lookup"><span data-stu-id="f4d96-113">When the application queues the first presentation on the Media Session, the application specifies the start time in the *pvarStartPosition* parameter of the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method.</span></span> <span data-ttu-id="f4d96-114">Per tutte le presentazioni successive, tuttavia, l'ora di inizio viene assegnata dall' \_ ora di inizio della topologia MF \_ \_ \_ sull'attributo del \_ comcambio di presentazione \_ nella topologia.</span><span class="sxs-lookup"><span data-stu-id="f4d96-114">For any subsequent presentations, however, the start time is given by the MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute on the topology.</span></span> <span data-ttu-id="f4d96-115">L'ora di inizio è specificata in unità 100-nanosecondi rispetto all'inizio della presentazione.</span><span class="sxs-lookup"><span data-stu-id="f4d96-115">The start time is specified in 100-nanosecond units, relative to the beginning of the presentation.</span></span> <span data-ttu-id="f4d96-116">Se, ad esempio, il valore è 50 milioni, la riproduzione inizia 5 secondi nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="f4d96-116">For example, if the value is 50000000, playback starts 5 seconds into the presentation.</span></span> <span data-ttu-id="f4d96-117">Se questo attributo non è impostato, l'ora di inizio predefinita è zero.</span><span class="sxs-lookup"><span data-stu-id="f4d96-117">If this attribute is not set, the default start time is zero.</span></span>

<span data-ttu-id="f4d96-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f4d96-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4d96-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4d96-119">Requirements</span></span>



| <span data-ttu-id="f4d96-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4d96-120">Requirement</span></span> | <span data-ttu-id="f4d96-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f4d96-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d96-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4d96-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4d96-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f4d96-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f4d96-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4d96-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4d96-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4d96-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f4d96-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4d96-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4d96-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4d96-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4d96-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4d96-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4d96-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4d96-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4d96-130">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="f4d96-130">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




