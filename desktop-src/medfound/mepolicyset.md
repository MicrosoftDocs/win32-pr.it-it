---
description: "Generato da un'autorità di attendibilità di output (OTA) quando il metodo IMFOutputTrustAuthority:: sepolicy viene completato in modo asincrono."
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Evento MEPolicySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309623"
---
# <a name="mepolicyset-event"></a><span data-ttu-id="362e0-103">Evento MEPolicySet</span><span class="sxs-lookup"><span data-stu-id="362e0-103">MEPolicySet event</span></span>

<span data-ttu-id="362e0-104">Generato da un'autorità di attendibilità di output (OTA) quando il metodo [**IMFOutputTrustAuthority:: Sepolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="362e0-104">Raised by an output trust authority (OTA) when the [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="362e0-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="362e0-105">Event values</span></span>

<span data-ttu-id="362e0-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="362e0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="362e0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="362e0-107">VARTYPE</span></span>              | <span data-ttu-id="362e0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="362e0-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="362e0-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="362e0-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="362e0-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="362e0-110">No event data.</span></span><br/> <br/> |
| <span data-ttu-id="362e0-111">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="362e0-111">VT\_UI4</span></span><br/> | <span data-ttu-id="362e0-112">Identificatore che può essere impostato su un [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) tramite l'attributo [MF_POLICY_ID](mf-policy-id.md) .</span><span class="sxs-lookup"><span data-stu-id="362e0-112">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) through the [MF_POLICY_ID](mf-policy-id.md) attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="362e0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="362e0-113">Requirements</span></span>



| <span data-ttu-id="362e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="362e0-114">Requirement</span></span> | <span data-ttu-id="362e0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="362e0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="362e0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="362e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="362e0-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="362e0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="362e0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="362e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="362e0-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="362e0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="362e0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="362e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="362e0-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="362e0-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="362e0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="362e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="362e0-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="362e0-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




