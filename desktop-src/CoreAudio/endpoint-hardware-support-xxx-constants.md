---
description: Le \_ costanti xxx del supporto hardware dell'endpoint \_ \_ sono flag di supporto hardware per un dispositivo endpoint audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Costanti ENDPOINT_HARDWARE_SUPPORT_XXX (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127666"
---
# <a name="endpoint_hardware_support_xxx-constants"></a><span data-ttu-id="e2a39-103">\_ \_ Costanti xxx supporto hardware endpoint \_</span><span class="sxs-lookup"><span data-stu-id="e2a39-103">ENDPOINT\_HARDWARE\_SUPPORT\_XXX Constants</span></span>

<span data-ttu-id="e2a39-104">Le \_ costanti xxx del supporto hardware dell'endpoint \_ \_ sono flag di supporto hardware per un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="e2a39-104">The ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants are hardware support flags for an audio endpoint device.</span></span>



| <span data-ttu-id="e2a39-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="e2a39-105">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="e2a39-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2a39-106">Description</span></span>                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <span data-ttu-id="e2a39-107"><dt>**Endpoint \_ di \_ \_ Volume di supporto hardware**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e2a39-107"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_VOLUME**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="e2a39-108">Il dispositivo dell'endpoint audio supporta un controllo volume hardware.</span><span class="sxs-lookup"><span data-stu-id="e2a39-108">The audio endpoint device supports a hardware volume control.</span></span><br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <span data-ttu-id="e2a39-109"><dt>**Endpoint \_ di Supporto HARDWARE 0x00000002 \_ \_ mute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e2a39-109"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_MUTE**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="e2a39-110">Il dispositivo dell'endpoint audio supporta un controllo di silenziamento hardware.</span><span class="sxs-lookup"><span data-stu-id="e2a39-110">The audio endpoint device supports a hardware mute control.</span></span><br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <span data-ttu-id="e2a39-111"><dt>**Endpoint \_ di 0x00000004 \_ di \_ misurazione del supporto hardware**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e2a39-111"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_METER**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="e2a39-112">Il dispositivo dell'endpoint audio supporta un contatore hardware di picco.</span><span class="sxs-lookup"><span data-stu-id="e2a39-112">The audio endpoint device supports a hardware peak meter.</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="e2a39-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2a39-113">Remarks</span></span>

<span data-ttu-id="e2a39-114">I metodi [**IAudioEndpointVolume:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) e [**IAudioMeterInformation:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usano le \_ \_ costanti xxx del supporto hardware dell'endpoint \_ .</span><span class="sxs-lookup"><span data-stu-id="e2a39-114">The [**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) and [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) methods use the ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span>

<span data-ttu-id="e2a39-115">Una maschera di supporto hardware indica le funzioni implementate da un dispositivo dell'endpoint audio nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="e2a39-115">A hardware support mask indicates which functions an audio endpoint device implements in hardware.</span></span> <span data-ttu-id="e2a39-116">La maschera può essere 0 o la combinazione bit per bit di uno o più \_ componenti hardware endpoint \_ supporta le \_ costanti xxx.</span><span class="sxs-lookup"><span data-stu-id="e2a39-116">The mask can be either 0 or the bitwise-OR combination of one or more ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span> <span data-ttu-id="e2a39-117">Se nella maschera è impostato un bit che corrisponde a una particolare \_ costante del supporto hardware di un endpoint \_ \_ , significa che la funzione rappresentata da tale costante è implementata nell'hardware dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2a39-117">If a bit that corresponds to a particular ENDPOINT\_HARDWARE\_SUPPORT\_XXX constant is set in the mask, then the meaning is that the function represented by that constant is implemented in hardware by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a39-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2a39-118">Requirements</span></span>



| <span data-ttu-id="e2a39-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2a39-119">Requirement</span></span> | <span data-ttu-id="e2a39-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e2a39-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a39-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2a39-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a39-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2a39-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2a39-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2a39-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a39-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2a39-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2a39-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2a39-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2a39-126"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2a39-126"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a39-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2a39-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a39-128">Costanti audio Core</span><span class="sxs-lookup"><span data-stu-id="e2a39-128">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="e2a39-129">**IAudioEndpointVolume::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="e2a39-129">**IAudioEndpointVolume::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[<span data-ttu-id="e2a39-130">**IAudioMeterInformation::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="e2a39-130">**IAudioMeterInformation::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




