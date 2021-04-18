---
description: L'interfaccia IMulticastControl viene implementata da IPConf MSP ed è disponibile solo per gli oggetti chiamata multicast.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interfaccia IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331603"
---
# <a name="imulticastcontrol-interface"></a><span data-ttu-id="ae952-103">Interfaccia IMulticastControl</span><span class="sxs-lookup"><span data-stu-id="ae952-103">IMulticastControl interface</span></span>

<span data-ttu-id="ae952-104">\[**IMulticastControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ae952-104">\[**IMulticastControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ae952-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ae952-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ae952-106">L'interfaccia **IMulticastControl** viene implementata da IPConf MSP ed è disponibile solo per gli oggetti chiamata multicast.</span><span class="sxs-lookup"><span data-stu-id="ae952-106">The **IMulticastControl** interface is implemented by the IPConf MSP and available only on multicast call objects.</span></span> <span data-ttu-id="ae952-107">Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP.</span><span class="sxs-lookup"><span data-stu-id="ae952-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="ae952-108">L'interfaccia **IMulticastControl** controlla la modalità loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="ae952-108">The **IMulticastControl** interface controls the multicast loopback mode.</span></span>

<span data-ttu-id="ae952-109">In modalità di \_ \_ loopback senza loopback, il loopback multicast è disabilitato, ovvero due applicazioni nello stesso computer che si uniscono allo stesso gruppo multicast otterranno i pacchetti dell'altro.</span><span class="sxs-lookup"><span data-stu-id="ae952-109">In the MM\_NO\_LOOPBACK mode, multicast loopback is disabled, which means two applications on the same machine who join the same multicast group will get each other's packets.</span></span> <span data-ttu-id="ae952-110">Questa modalità offre le prestazioni migliori se è presente sempre una sola applicazione che partecipa al gruppo multicast nel computer.</span><span class="sxs-lookup"><span data-stu-id="ae952-110">This mode has the best performance if there is always only one application joining the multicast group on the machine.</span></span> <span data-ttu-id="ae952-111">MM \_ \_ la modalità di loopback non è la modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="ae952-111">MM\_NO\_LOOPBACK mode is the default mode.</span></span>

<span data-ttu-id="ae952-112">La \_ \_ modalità loopback completa mm è efficace solo per i test.</span><span class="sxs-lookup"><span data-stu-id="ae952-112">The MM\_FULL\_LOOPBACK mode is good only for testing.</span></span> <span data-ttu-id="ae952-113">Viene anche eseguito il loop di tutti i pacchetti inviati.</span><span class="sxs-lookup"><span data-stu-id="ae952-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="ae952-114">Questa operazione può essere usata per verificare se i dispositivi sono in funzione.</span><span class="sxs-lookup"><span data-stu-id="ae952-114">This can be used to test if the devices are working.</span></span>

<span data-ttu-id="ae952-115">La \_ modalità loopback selettivo mm \_ viene utilizzata per consentire a più applicazioni in un computer di partecipare allo stesso gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="ae952-115">The MM\_SELECTIVE\_LOOPBACK mode is used to enable multiple applications on one machine to join the same multicast group.</span></span> <span data-ttu-id="ae952-116">I pacchetti vengono riprodotti in ciclo dallo stack e ogni sessione RTP è responsabile del filtraggio dei pacchetti indesiderati.</span><span class="sxs-lookup"><span data-stu-id="ae952-116">The packets are looped back from the stack, and each RTP session is responsible for filtering out unwanted packets.</span></span>

## <a name="members"></a><span data-ttu-id="ae952-117">Membri</span><span class="sxs-lookup"><span data-stu-id="ae952-117">Members</span></span>

<span data-ttu-id="ae952-118">L'interfaccia **IMulticastControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ae952-118">The **IMulticastControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ae952-119">**IMulticastControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ae952-119">**IMulticastControl** also has these types of members:</span></span>

-   [<span data-ttu-id="ae952-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="ae952-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ae952-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="ae952-121">Methods</span></span>

<span data-ttu-id="ae952-122">L'interfaccia **IMulticastControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ae952-122">The **IMulticastControl** interface has these methods.</span></span>



| <span data-ttu-id="ae952-123">Metodo</span><span class="sxs-lookup"><span data-stu-id="ae952-123">Method</span></span>                                                          | <span data-ttu-id="ae952-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae952-124">Description</span></span>                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="ae952-125">**ottenere \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="ae952-125">**get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md) | <span data-ttu-id="ae952-126">Ottiene la modalità di loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="ae952-126">Gets the multicast loopback mode.</span></span><br/> |
| [<span data-ttu-id="ae952-127">**Inserisci \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="ae952-127">**put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md) | <span data-ttu-id="ae952-128">Imposta la modalità loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="ae952-128">Sets the multicast loopback mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ae952-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae952-129">Requirements</span></span>



| <span data-ttu-id="ae952-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae952-130">Requirement</span></span> | <span data-ttu-id="ae952-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ae952-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae952-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ae952-132">TAPI version</span></span><br/> | <span data-ttu-id="ae952-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ae952-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ae952-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae952-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ae952-135"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae952-135"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ae952-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae952-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ae952-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae952-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ae952-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ae952-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ae952-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae952-139"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ae952-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae952-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae952-141">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="ae952-141">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

