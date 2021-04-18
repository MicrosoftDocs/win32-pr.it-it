---
description: L' \_ \_ enumerazione modalità loopback multicast descrive la modalità loopback multicast.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Enumerazione MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333967"
---
# <a name="multicast_loopback_mode-enumeration"></a><span data-ttu-id="bdf25-103">\_ \_ Enumerazione modalità loopback multicast</span><span class="sxs-lookup"><span data-stu-id="bdf25-103">MULTICAST\_LOOPBACK\_MODE enumeration</span></span>

<span data-ttu-id="bdf25-104">\[**Multicast \_ La \_ modalità loopback** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bdf25-104">\[**MULTICAST\_LOOPBACK\_MODE** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bdf25-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bdf25-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bdf25-106">L' **enumerazione \_ \_ modalità loopback multicast** descrive la modalità loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="bdf25-106">The **MULTICAST\_LOOPBACK\_MODE** enum describes the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf25-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdf25-107">Syntax</span></span>


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a><span data-ttu-id="bdf25-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="bdf25-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bdf25-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ nessun \_ loopback**</span><span class="sxs-lookup"><span data-stu-id="bdf25-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM\_NO\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="bdf25-110">Il loopback multicast è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bdf25-110">Multicast loopback is disabled.</span></span> <span data-ttu-id="bdf25-111">Ciò significa che due applicazioni nello stesso computer che si uniscono allo stesso gruppo multicast possono ottenere i pacchetti dell'altro.</span><span class="sxs-lookup"><span data-stu-id="bdf25-111">That means two applications on the same machine joining the same multicast group can get each other's packets.</span></span>

</dd> <dt>

<span data-ttu-id="bdf25-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_loopback completo di mm \_**</span><span class="sxs-lookup"><span data-stu-id="bdf25-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM\_FULL\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="bdf25-113">Viene anche eseguito il loop di tutti i pacchetti inviati.</span><span class="sxs-lookup"><span data-stu-id="bdf25-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="bdf25-114">Questa modalità è utile solo per i test.</span><span class="sxs-lookup"><span data-stu-id="bdf25-114">This mode is useful only for testing.</span></span>

</dd> <dt>

<span data-ttu-id="bdf25-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_loopback selettivo mm \_**</span><span class="sxs-lookup"><span data-stu-id="bdf25-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM\_SELECTIVE\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="bdf25-116">Il loopback selettivo è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bdf25-116">Selective loopback is enabled.</span></span> <span data-ttu-id="bdf25-117">Ciò significa che più applicazioni in un computer possono partecipare allo stesso gruppo multicast senza confusione.</span><span class="sxs-lookup"><span data-stu-id="bdf25-117">That means enabled multiple applications on one machine can join the same multicast group without confusion.</span></span> <span data-ttu-id="bdf25-118">I pacchetti vengono riprodotti in ciclo dallo stack e ogni sessione RTP è responsabile del filtraggio dei pacchetti indesiderati.</span><span class="sxs-lookup"><span data-stu-id="bdf25-118">The packets are looped back from the stack and each RTP session is responsible for filtering out unwanted packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdf25-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdf25-119">Requirements</span></span>



| <span data-ttu-id="bdf25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf25-120">Requirement</span></span> | <span data-ttu-id="bdf25-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bdf25-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf25-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="bdf25-122">TAPI version</span></span><br/> | <span data-ttu-id="bdf25-123">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bdf25-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bdf25-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdf25-124">Header</span></span><br/>       | <dl> <span data-ttu-id="bdf25-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf25-125"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdf25-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdf25-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf25-127">**IMulticastControl:: Get \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="bdf25-127">**IMulticastControl::get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[<span data-ttu-id="bdf25-128">**IMulticastControl::p UT \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="bdf25-128">**IMulticastControl::put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




