---
description: Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Attributo MF_EVENT_SESSIONCAPS_DELTA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401665"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a><span data-ttu-id="6f1b2-103">\_ \_ Attributo Delta SESSIONCAPS dell'evento MF \_</span><span class="sxs-lookup"><span data-stu-id="6f1b2-103">MF\_EVENT\_SESSIONCAPS\_DELTA attribute</span></span>

<span data-ttu-id="6f1b2-104">Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-104">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f1b2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6f1b2-105">Data type</span></span>

<span data-ttu-id="6f1b2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6f1b2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f1b2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f1b2-107">Remarks</span></span>

<span data-ttu-id="6f1b2-108">Questo attributo contiene una maschera di maschera che indica i flag delle funzionalità che sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-108">This attribute contains a bitmask indicating which capabilities flags have changed.</span></span> <span data-ttu-id="6f1b2-109">Per un elenco dei flag possibili, vedere [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="6f1b2-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span> <span data-ttu-id="6f1b2-110">BITS viene impostato su 1 nella maschera di bit per uno dei motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f1b2-110">Bits are set to 1 in the bitmask for any of the following reasons:</span></span>

-   <span data-ttu-id="6f1b2-111">Il bit di funzionalità corrispondente è stato modificato da 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-111">The corresponding capabilities bit changed from 0 to 1.</span></span>
-   <span data-ttu-id="6f1b2-112">Il bit di funzionalità corrispondente è stato modificato da 1 a 0.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-112">The corresponding capabilities bit changed from 1 to 0.</span></span>
-   <span data-ttu-id="6f1b2-113">Il bit delle funzionalità corrispondente è rimasto 1, ma i dettagli della funzionalità sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-113">The corresponding capabilities bit remained 1, but the details of the capability changed.</span></span> <span data-ttu-id="6f1b2-114">Ad esempio, è stata modificata la velocità massima di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-114">For example, the maximum playback rate changed.</span></span>

<span data-ttu-id="6f1b2-115">Questo attributo viene utilizzato con l'evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1b2-115">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="6f1b2-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1b2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f1b2-117">Requirements</span></span>



| <span data-ttu-id="6f1b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f1b2-118">Requirement</span></span> | <span data-ttu-id="6f1b2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6f1b2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1b2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f1b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1b2-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f1b2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6f1b2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f1b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1b2-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f1b2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6f1b2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f1b2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f1b2-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f1b2-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f1b2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f1b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1b2-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f1b2-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f1b2-128">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="6f1b2-128">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f1b2-129">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="6f1b2-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6f1b2-130">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="6f1b2-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




