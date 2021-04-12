---
description: La \_ Proprietà pkey AudioEndpoint \_ FormFactor specifica il fattore di forma del dispositivo dell'endpoint audio. Il fattore di forma indica gli attributi fisici del dispositivo dell'endpoint audio modificato dall'utente.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483684"
---
# <a name="pkey_audioendpoint_formfactor"></a><span data-ttu-id="72f44-104">PKEY \_ AudioEndpoint \_ FormFactor</span><span class="sxs-lookup"><span data-stu-id="72f44-104">PKEY\_AudioEndpoint\_FormFactor</span></span>

<span data-ttu-id="72f44-105">La proprietà **pkey \_ AudioEndpoint \_ FormFactor** specifica il fattore di forma del dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="72f44-105">The **PKEY\_AudioEndpoint\_FormFactor** property specifies the form factor of the audio endpoint device.</span></span> <span data-ttu-id="72f44-106">Il fattore di forma indica gli attributi fisici del dispositivo dell'endpoint audio modificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="72f44-106">The form factor indicates the physical attributes of the audio endpoint device that the user manipulates.</span></span>

<span data-ttu-id="72f44-107">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="72f44-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="72f44-108">Il membro **uintVal** della struttura **PROPVARIANT** contiene un valore di enumerazione di cui è stato eseguito il cast al tipo uint.</span><span class="sxs-lookup"><span data-stu-id="72f44-108">The **uintVal** member of the **PROPVARIANT** structure contains an enumeration value that is cast to type UINT.</span></span> <span data-ttu-id="72f44-109">Viene impostato su uno dei seguenti valori di enumerazione [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) :</span><span class="sxs-lookup"><span data-stu-id="72f44-109">It is set to one of the following [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) enumeration values:</span></span>

-   <span data-ttu-id="72f44-110">RemoteNetworkDevice</span><span class="sxs-lookup"><span data-stu-id="72f44-110">RemoteNetworkDevice</span></span>
-   <span data-ttu-id="72f44-111">Altoparlanti</span><span class="sxs-lookup"><span data-stu-id="72f44-111">Speakers</span></span>
-   <span data-ttu-id="72f44-112">LineLevel</span><span class="sxs-lookup"><span data-stu-id="72f44-112">LineLevel</span></span>
-   <span data-ttu-id="72f44-113">Cuffie</span><span class="sxs-lookup"><span data-stu-id="72f44-113">Headphones</span></span>
-   <span data-ttu-id="72f44-114">Microfono</span><span class="sxs-lookup"><span data-stu-id="72f44-114">Microphone</span></span>
-   <span data-ttu-id="72f44-115">Cuffie</span><span class="sxs-lookup"><span data-stu-id="72f44-115">Headset</span></span>
-   <span data-ttu-id="72f44-116">Portatile</span><span class="sxs-lookup"><span data-stu-id="72f44-116">Handset</span></span>
-   <span data-ttu-id="72f44-117">UnknownDigitalPassthrough</span><span class="sxs-lookup"><span data-stu-id="72f44-117">UnknownDigitalPassthrough</span></span>
-   <span data-ttu-id="72f44-118">SPDIF</span><span class="sxs-lookup"><span data-stu-id="72f44-118">SPDIF</span></span>
-   <span data-ttu-id="72f44-119">HDMI</span><span class="sxs-lookup"><span data-stu-id="72f44-119">HDMI</span></span>
-   <span data-ttu-id="72f44-120">UnknownFormFactor</span><span class="sxs-lookup"><span data-stu-id="72f44-120">UnknownFormFactor</span></span>

## <a name="requirements"></a><span data-ttu-id="72f44-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72f44-121">Requirements</span></span>



| <span data-ttu-id="72f44-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f44-122">Requirement</span></span> | <span data-ttu-id="72f44-123">Valore</span><span class="sxs-lookup"><span data-stu-id="72f44-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f44-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72f44-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72f44-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72f44-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="72f44-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72f44-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72f44-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72f44-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="72f44-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72f44-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f44-129"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f44-129"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f44-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72f44-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f44-131">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="72f44-131">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="72f44-132">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="72f44-132">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




